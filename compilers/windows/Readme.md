```markdown
# Sufi Compiler

Sufi is a lightweight compiler toolchain designed to replace TinyCC with a simplified and unified build system. This installer provides the `sufi` command-line compiler for Windows.

---

## 📦 Installation

### 1. Download Installer
Download the latest `sufi_setup.exe` from the GitHub Actions build artifacts.

### 2. Run Installer
Double-click the installer:

```

sufi_setup.exe

````

Follow the setup wizard and install Sufi to your system.

---

## ⚙️ After Installation

Once installed, open a new **Command Prompt (CMD)** or **PowerShell** window.

Verify installation:

```bash
sufi --version
````

If installed correctly, you should see version information printed.

---

## 🚀 How to Compile and Run

### Compile and run a Sufi program

Use the following command:

```bash
sufi filename.sufi -run
```

### Example

Create a file:

```bash
hello.sufi
```

Example content:

```
print("Hello from Sufi!")
```

Run it:

```bash
sufi hello.sufi -run
```

---

## 🧪 Test Installation

After installing, run:

```bash
sufi --version
```

Then run a sample program:

```bash
echo print("Sufi OK") > test.sufi
sufi test.sufi -run
```

Expected output:

```
Sufi OK
```

---

## 🧰 Usage Summary

| Command               | Description                        |
| --------------------- | ---------------------------------- |
| `sufi --version`      | Show compiler version              |
| `sufi file.sufi -run` | Compile and execute a Sufi program |

---

## 📁 Notes

* Ensure `sufi_compiler.exe` is in your system PATH after installation.
* This tool replaces TinyCC (`tcc`) with a unified Sufi compiler binary.
* Works on Windows (MinGW-based build).

---

## 🧪 Troubleshooting

If `sufi` is not recognized:

1. Restart your terminal
2. Check installation directory:

   ```
   C:\Program Files\SufiCompiler\bin
   ```
3. Add it to PATH manually if needed.

---

## 📜 License

Sufi Compiler is distributed under its project license. See repository for details.

```
```
