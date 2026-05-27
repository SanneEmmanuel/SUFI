````markdown id="sufi-android-readme"
# Sufi Compiler – Android JNI Installation Guide

This package provides Sufi as a **native Android library (JNI)** for use in Android Studio projects.

It supports multiple CPU architectures:
- arm64-v8a
- armeabi-v7a
- x86_64

---

# 📦 DOWNLOAD

Download:
```text
Sufi-Android-JNI.zip
````

---

# 📁 PACKAGE STRUCTURE

After extraction, you will get:

```text id="android-struct"
jniLibs/
├── arm64-v8a/
│   └── libsufi.so
├── armeabi-v7a/
│   └── libsufi.so
├── x86_64/
│   └── libsufi.so
```

These are precompiled native binaries of Sufi.

---

# 📌 INSTALLATION (ANDROID STUDIO)

## Step 1: Copy files

Move the folder into your Android project:

```text id="copy-path"
app/src/main/jniLibs/
```

Final structure:

```text id="final-path"
app/src/main/jniLibs/arm64-v8a/libsufi.so
app/src/main/jniLibs/armeabi-v7a/libsufi.so
app/src/main/jniLibs/x86_64/libsufi.so
```

---

## Step 2: Enable CMake (if not enabled)

In `app/build.gradle`:

```gradle id="gradle"
android {
    defaultConfig {
        externalNativeBuild {
            cmake {}
        }
    }

    externalNativeBuild {
        cmake {
            path "CMakeLists.txt"
        }
    }
}
```

---

## Step 3: Configure CMake

Create or edit:

```text id="cmake-file"
app/CMakeLists.txt
```

Add:

```cmake id="cmake-config"
add_library(sufi SHARED IMPORTED)

set_target_properties(
    sufi
    PROPERTIES IMPORTED_LOCATION
    ${CMAKE_SOURCE_DIR}/src/main/jniLibs/${ANDROID_ABI}/libsufi.so
)

target_link_libraries(
    native-lib
    sufi
    log
)
```

---

# ⚙️ USING SUFI IN NATIVE CODE

## Example C++ JNI call

```cpp id="jni-example"
#include <jni.h>

extern "C"
JNIEXPORT void JNICALL
Java_com_example_app_MainActivity_runSufi(JNIEnv* env, jobject obj) {
    // Sufi native runtime is available here
}
```

---

# 📱 SUPPORTED ARCHITECTURES

| ABI         | Description                         |
| ----------- | ----------------------------------- |
| arm64-v8a   | Modern Android phones (recommended) |
| armeabi-v7a | Older 32-bit Android devices        |
| x86_64      | Android emulators                   |

---

# 🚀 USAGE OVERVIEW

Sufi is used as a native runtime library.

Typical flow:

1. Load JNI library
2. Call native interface
3. Execute compiled Sufi bytecode or runtime logic

---

# ⚠️ IMPORTANT NOTES

* This package contains **precompiled binaries only**
* No source code is included
* Do NOT modify `.so` files
* Android automatically selects correct ABI at runtime
* Requires Android NDK-compatible app setup if extended

---

# 🧪 TEST CHECK

After integration, verify library loads:

```java id="java-test"
System.loadLibrary("sufi");
```

If no crash occurs, installation is successful.

---

# 📦 SUMMARY

* Multi-ABI support included
* Drop-in `jniLibs` integration
* Works with Android Studio + Gradle + CMake
* Fully native performance

```

---
```
