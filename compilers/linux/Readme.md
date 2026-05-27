````markdown id="sufi-linux-readme"
# Sufi Compiler – Linux Installation Guide

This package provides the **Sufi compiler as a native Linux binary**.

It is fully self-contained and includes only production-ready binaries.

---

# 📦 DOWNLOAD

Download:

```text
sufi-linux.tar.gz
````

---

# 📁 PACKAGE CONTENTS

After extraction:

```text id="linux-struct"
sufi-linux/
└── bin/
    └── sufi
```

---

# 📥 INSTALLATION

## Step 1: Extract package

```bash id="extract"
tar -xzf sufi-linux.tar.gz
```

---

## Step 2: Move binary to system path

```bash id="install"
sudo cp sufi-linux/bin/sufi /usr/local/bin/
```

---

## Step 3: Give execution permission

```bash id="chmod"
sudo chmod +x /usr/local/bin/sufi
```

---

# ✅ VERIFY INSTALLATION

```bash id="verify"
sufi --version
```

If installed correctly, version information will be displayed.

---

# 🚀 RUN A SUFI FILE

Create a file:

```text id="file"
hello.sufi
```

Example content:

```sufi id="example"
print("Hello Sufi")
```

Run:

```bash id="run"
sufi hello.sufi -run
```

---

# 📍 INSTALL LOCATION

Default installation path:

```text id="path"
/usr/local/bin/sufi
```

---

# 🧹 OPTIONAL CLEAN INSTALL

If you want to reinstall cleanly:

```bash id="clean"
sudo rm -f /usr/local/bin/sufi
```

Then reinstall again using steps above.

---

# ⚠️ IMPORTANT NOTES

* This package contains **only compiled binaries**
* No source code is included
* Compatible with modern Linux distributions (Ubuntu, Debian, Fedora, Arch)
* Must be executed from a terminal
* Requires 64-bit Linux (x86_64)

---

# 📦 SUMMARY

| Item         | Value                 |
| ------------ | --------------------- |
| Binary       | sufi                  |
| Type         | Native ELF executable |
| Install path | /usr/local/bin/sufi   |
| Package      | tar.gz                |

```
```
