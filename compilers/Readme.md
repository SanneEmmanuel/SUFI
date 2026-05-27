````markdown id="sufi-readme-all"
# Sufi Compiler – Multi-Platform Installation Guide

This guide covers installation and usage for:

- Windows (Installer)
- Linux (Tarball)
- macOS (PKG Installer)
- Android (JNI Library for Android Studio)

---

# 🪟 WINDOWS INSTALLATION

## Install

1. Download:
```text
sufi_setup.exe
````

2. Run the installer.

3. Follow setup wizard.

Sufi will be installed to:

```text
C:\Program Files\Sufi\bin\sufi.exe
```

---

## Verify

Open Command Prompt:

```bash
sufi --version
```

---

## Run a Sufi file

```bash
sufi hello.sufi -run
```

---

# 🐧 LINUX INSTALLATION

## Download

```text
sufi-linux.tar.gz
```

## Install

```bash
tar -xzf sufi-linux.tar.gz
sudo cp -r sufi-linux/bin/sufi /usr/local/bin/
```

---

## Verify

```bash
sufi --version
```

---

## Run a Sufi file

```bash
sufi hello.sufi -run
```

---

# 🍎 MACOS INSTALLATION

## Install

Download:

```text
sufi-macos.pkg
```

Double click and install.

Sufi installs to:

```text
/usr/local/bin/sufi
```

---

## Verify

```bash
sufi --version
```

---

## Run a Sufi file

```bash
sufi hello.sufi -run
```

---

# 🤖 ANDROID (JNI / ANDROID STUDIO)

## Download

```text
Sufi-Android-JNI.zip
```

---

## Folder Structure

Extract into:

```text
app/src/main/jniLibs/
```

You will see:

```text
jniLibs/
├── arm64-v8a/
├── armeabi-v7a/
├── x86_64/
```

Each folder contains:

```text
libsufi.so
```

---

## Add to Android Studio (CMake)

In `CMakeLists.txt`:

```cmake
add_library(sufi SHARED IMPORTED)

set_target_properties(
    sufi
    PROPERTIES IMPORTED_LOCATION
    ${CMAKE_SOURCE_DIR}/src/main/jniLibs/${ANDROID_ABI}/libsufi.so
)

target_link_libraries(native-lib sufi log)
```

---

## Use in C++

```cpp
#include <jni.h>

extern "C"
JNIEXPORT void JNICALL
Java_com_example_app_Main_runSufi(JNIEnv* env, jobject obj) {
    // Call into Sufi runtime
}
```

---

## Supported Architectures

* arm64-v8a (modern phones)
* armeabi-v7a (older phones)
* x86_64 (emulators)

---

# ⚠️ IMPORTANT NOTES

* Only binaries are shipped (no source code included)
* Sufi is installed as a system binary on desktop platforms
* Android uses JNI shared libraries (.so files)
* All builds are stripped for performance and smaller size

---

# 🚀 BASIC USAGE (ALL PLATFORMS)

Create file:

```text
hello.sufi
```

Example:

```sufi
print("Hello Sufi")
```

Run:

```bash
sufi hello.sufi -run
```

---

# 📦 SUMMARY

| Platform | Output         | Type           |
| -------- | -------------- | -------------- |
| Windows  | sufi_setup.exe | Installer      |
| Linux    | tar.gz         | Binary package |
| macOS    | .pkg           | Installer      |
| Android  | .zip           | JNI libraries  |

---

```
```
