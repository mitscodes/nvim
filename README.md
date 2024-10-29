
# Neovim Configuration

This Neovim configuration is designed for a comprehensive and efficient development experience across multiple programming languages. The setup leverages **Lazy** for plugin management and includes support for LSP, formatters, and debuggers for seamless coding, formatting, and debugging.

## Prerequisites

Ensure you have **Neovim v0.9.0+** installed. Follow the OS-specific instructions below to install dependencies and set up the environment.

### Dependencies

- **Git**: Required for cloning repositories and managing plugins.
- **Python**: Needed for Python LSP (`pyright`) and certain plugins.
- **Node.js**: For various language servers like `tsserver`.
- **Go**: For Go language support.
- **Rust**: For Rust language support.
- **Java**: For Java LSP (`jdtls`).

## Installation Steps

### 1. Clone the Repository
```bash
git clone https://github.com/mitscodes/neovim-new ~/.config/nvim
```

### 2. Install Dependencies

#### **MacOS** (Using Homebrew)
```bash
brew install neovim node python go rust openjdk
```

#### **Arch Linux** (Using yay/paru)
```bash
yay -S neovim nodejs npm python go rust jdk-openjdk
```

#### **Ubuntu/Kali Linux** (Using apt)
```bash
sudo apt update
sudo apt install neovim nodejs npm python3 python3-pip golang rustc openjdk-11-jdk
```

### 3. Install Neovim Plugins

Launch Neovim and run:
```bash
:Lazy sync
```

### 4. Install LSP Servers, Formatters, and Debuggers

> **Note:** Mason does **not** automatically install LSP servers, formatters, or debuggers after cloning. You need to manually install these using **Mason**:
>
> ```bash
> :Mason
> ```
>
> Use the list below to know what to install:

## Configured Language Servers, Formatters, and Debuggers

### **LSP Servers**
Configured via **Mason** for the following languages:
- **Python**: `pyright`
- **JavaScript/TypeScript**: `ts_ls`
- **Go**: `gopls`
- **Rust**: `rust_analyzer`
- **HTML/CSS**: `html`, `cssls`, `tailwindcss`
- **Lua**: `ast_grep`
- **Java**: `jdtls`
- **C/C++**: `ccls`
- **C#**: `csharp_ls`
- **PHP**: `phpactor`
- **Ruby**: `solargraph`
- **Ansible**: `ansiblels`
- **Kotlin**: `kotlin_language_server`
- **SQL**: `sqls`
- **Angular**: `angularls`
- **Assembly**: `asm_lsp`

### **Formatters**
Configured using **Conform**:
- **Python**: `black`
- **JavaScript/TypeScript/HTML/CSS**: `prettier`
- **Lua**: `stylua`
- **C/C++**: `clang_format`
- **Java**: `google_java_format`
- **Kotlin**: `ktlint`
- **Go**: `gofmt`
- **PHP**: `phpcsfixer`
- **Rust**: `rustfmt`
- **Ruby**: `rubocop`
- **SQL**: `sqlformat`
- **YAML**: `yamllint`
- **Markdown**: `prettier`

### **Debuggers**
Configured using **nvim-dap**:
- **Python**: `nvim-dap-python`
- **Go**: `nvim-dap-go`
- **JavaScript/TypeScript**: Integrated with **nvim-dap**

### 5. Optional: Install Additional Tools
Some LSP servers or formatters may require extra tools:
- For Java, make sure you have `jdtls` installed and set up.
- For Python, `black` and `flake8` can be installed via `pip`:
  ```bash
  pip install black flake8
  ```

### 6. Running Neovim
Run Neovim using:
```bash
nvim
```
