# Sufi-Lang™

## *The Language of the Future*

Created by Sanne Karibo
Developed and Licensed by CS-Tech

---

# Welcome to the Future of Native Programming

Sufi-Lang is a next-generation compiled programming language built for one purpose:

> **Maximum speed with minimum complexity.**
> often 8X faster than c++

Sufi combines:

* the simplicity of modern scripting languages,
* the raw execution speed of low-level systems programming,
* and the lightweight efficiency developers have been missing for years.

It was engineered for:

* high-performance servers,
* massive loops,
* mathematical computation,
* native applications,
* networking systems,
* automation,
* and scalable backend infrastructure.

Unlike interpreted languages, Sufi compiles directly into machine code.

No virtual machines.
No runtime engines.
No heavy interpreters.

Just pure native execution.

---

# Why Sufi Exists

Modern programming has become heavy.

Applications take longer to start.
Compilers consume more memory.
Frameworks add unnecessary complexity.
Simple servers now require thousands of lines of code.

Sufi was created to change that.

Sufi focuses on:

* instant startup,
* fast compilation,
* lightweight binaries,
* readable syntax,
* and extremely fast execution.

The result is a language that feels modern while executing with native-level efficiency.

---

# Built for Speed

Sufi was specifically engineered for performance-heavy workloads.

It performs exceptionally well in:

* large loops,
* numerical processing,
* backend systems,
* network services,
* and real-time applications.

Its optimized execution model allows programs to run with extremely low overhead and rapid startup time.

---

# Tiny Compiler. Massive Power.

The Sufi compiler is intentionally lightweight and fast.

Designed to run efficiently even on smaller devices, Sufi minimizes system strain while maximizing performance.

Perfect for:

* VPS deployments,
* cloud systems,
* embedded devices,
* low-resource hardware,
* lightweight containers,
* and scalable infrastructure.

---

# Native Cross-Platform Support

Sufi compilers are available for:

* Microsoft Windows
* Linux
* Apple macOS
* Android (.so JNI support)

Applications compile directly into native machine code on every supported platform.

---

# One-Line Programming Philosophy

Sufi encourages clean, expressive, one-line programming.

Why write ten lines when one line can do the same thing faster and cleaner?

---

# Printing Made Beautiful

No quotation marks required.

No semicolon required.

Just write.

```sufi id="n8xmpa"
write(Hello world)
```

---

# Printing Variables Instantly

```sufi id="53znxv"
int users = 5000

writeVariable(%d, users)
```

Supports familiar C-style formatting with simplified syntax.

---

# One-Line Loops

Fast loops are one of Sufi’s strongest features.

```sufi id="qqb3fu"
loop(100)write(Hello)
```

Need the current loop count?

```sufi id="mv0otj"
loop(5)writeVariable(%d, i)
```

or:

```sufi id="aefh9r"
loop(5)writeVariable(%d, count)
```

Simple. Fast. Native.

---

# Functions Without Boilerplate

Sufi functions are intentionally lightweight.

## Dollar Function Syntax

```sufi id="h3v3f4"
$void start(){

write(Server started)

};$
```

---

# Grouped Function Blocks

```sufi id="jlwmql"
$function

void hello(){

write(Hello world)

}

void boot(){

write(System online)

}
```

Alternative styles are supported:

```sufi id="f5l9ut"
$FUNCTION
```

```sufi id="kkq1vc"
functions:
```

---

# Create Native Servers in Seconds

Sufi was built with servers in mind from the beginning.

Starting a server is a one-line operation.

```sufi id="nyivsq"
server.listen(8080);
```

---

# Beautiful Route Handling

```sufi id="e71kha"
create(home){

return text(Welcome to Sufi)

}

server.get(/, home);
```

---

# Even Simpler Direct Routes

```sufi id="gk9mr3"
SUFI_GET(/hello, {

return text(Hello World)

})
```

---

# Instant Web Responses

Sufi includes built-in response helpers for modern backend development.

## Plain Text

```sufi id="t3m06z"
return text(Hello)
```

---

## JSON

```sufi id="vokwx0"
return json({"success":true})
```

---

## HTML

```sufi id="e0s8dv"
return html(<h1>Sufi Server</h1>)
```

---

## File Responses

```sufi id="61ebcl"
return file(index.html)
```

---

# Read Request Data Easily

```sufi id="r9tkh6"
body(username)

query(page)

param(id)

jsonGet(email)
```

No unnecessary parsing boilerplate.

---

# Macro-Powered Simplicity

Sufi includes a powerful lightweight macro system designed to reduce repetitive code and simplify project structure.

---

# Clean Imports

```sufi id="b6hvhp"
$include network
```

```sufi id="b8y7xq"
$include math
```

```sufi id="4j66s6"
$include graphics
```

---

# Remove Modules Easily

```sufi id="v82z9x"
$remove graphics
```

---

# Expand Projects Naturally

```sufi id="8jqv1m"
$add physics
```

```sufi id="jlwmq7"
$add database
```

---

# Full C Macro Support

Sufi supports traditional C-style macros for advanced systems programming.

## Constants

```sufi id="a3fjlwm"
#define MAX_USERS 1000
```

---

## Function Macros

```sufi id="nfw0e7"
#define square(x) ((x)*(x))
```

---

## Conditional Compilation

```sufi id="ll0t7w"
#ifdef WINDOWS

write(Running on Windows)

#endif
```

---

# Native Multi-Language Power

Sufi can execute other technologies directly from inside your applications.

---

# Run Python Code

```sufi id="32pk0o"
PYTHON_CODE(print("Hello from Python"))
```

---

# Run NodeJS Code

```sufi id="9c76cc"
NODE_CODE(console.log("Hello from Node"))
```

---

# Link Native C Code

```bash id="5b57wz"
sufi app.sufi helper.c
```

---

# Assembly-Level Capability

Sufi also supports low-level native integrations for performance-critical applications.

---

# Extremely Fast Compilation

Compile applications rapidly using the lightweight Sufi compiler.

## Compile

```bash id="vfyjlwm"
sufi app.sufi
```

---

## Compile and Instantly Run

```bash id="8n2x0m"
sufi app.sufi -run
```

---

# Installation

# 🪟 Windows

Download:

```text id="6l9jvc"
sufi_setup.exe
```

Verify:

```bash id="55j5dv"
sufi --version
```

Run:

```bash id="4b9h4g"
sufi hello.sufi -run
```

---

# 🐧 Linux

Install:

```bash id="qfr83u"
tar -xzf sufi-linux.tar.gz

sudo cp -r sufi-linux/bin/sufi /usr/local/bin/
```

---

# 🍎 macOS

Install package:

```text id="uv94ns"
sufi-macos.pkg
```

---

# 🤖 Android JNI Support

Supported architectures:

* arm64-v8a
* armeabi-v7a
* x86_64

CMake integration:

```cmake id="x9zjlwm"
add_library(sufi SHARED IMPORTED)
```

---

# Example Full Application

```sufi id="8stl76"
$include network

server.listen(8080);

create(home){

write(Request received)

return json({"status":"online"})

}

server.get(/, home);
```

---

# The Sufi Vision

Sufi was built to make native programming:

* simpler,
* faster,
* cleaner,
* and more accessible.

It combines:

* modern developer experience,
* lightweight tooling,
* and native execution power.

Sufi is not just another language.

It is a new direction for systems and backend development.

---

# Official Motto

> **Sufi — The Language of the Future**

---

# Credits

Created by:

Sanne Karibo

Developed and Licensed by:

CS-Tech
