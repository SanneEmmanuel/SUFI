# Sufi macOS Installation Guide

## Download

Download:

- `Sufi-MacOS(V**).zip`

from the GitHub repo above here and unzip to extract the pkg

---

# Install Sufi

1. Double-click:

```text
Sufi-Installer.pkg
```

2. Click:

```text
Continue
```

3. Click:

```text
Install
```

4. Enter your macOS password if prompted.

5. Finish installation.

---

# Verify Installation

Open Terminal and run:

```bash
sufi --version
```

If installed correctly, Sufi will display its version.

---

# Compile and Run a Sufi File

Create a file:

```bash
nano hello.sufi
```

Example:

```sufi
print("Hello World")
```

Save the file.

Compile and run:

```bash
sufi hello.sufi -run
```

---

# Sufi Installation Path

Sufi installs to:

```text
/usr/local/bin/sufi
```

---

# Uninstall Sufi

Open Terminal and run:

```bash
sudo rm -f /usr/local/bin/sufi
```
