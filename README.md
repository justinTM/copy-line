# Copy Line for VS Code

[English](README.md) | [中文](README.zh-CN.md)

A practical VS Code extension that helps developers quickly copy file names and line numbers, especially useful for code positioning when collaborating with AI assistants.

![demo](https://img.shields.io/badge/VS%20Code-latest-blue.svg)
![demo](https://img.shields.io/badge/license-MIT-green.svg)
![demo](https://img.shields.io/badge/version-0.0.4-orange.svg)

## ✨ Features

- ⚡ **One-Click Copy** - Quickly copy file names and line numbers after selecting code
- 🎯 **Multiple Formats** - Supports 4 output formats for different scenarios
- 🔧 **Highly Configurable** - Customizable keyboard shortcuts and output formats
- 🤝 **AI-Friendly** - Designed specifically for code positioning when collaborating with AI
- 📋 **Context Menu** - Supports right-click menu and editor title bar buttons

## 🚀 Installation

### Method 1: Install from VS Code Marketplace (Recommended)
1. Open VS Code
2. Press `Cmd+Shift+P` (Mac) or `Ctrl+Shift+P` (Windows/Linux)
3. Type "Extensions: Install Extensions"
4. Search for "Copy Line"
5. Click Install

### Method 2: Install from VSIX Package
1. Download the `.vsix` file
2. Press `Cmd+Shift+P` in VS Code
3. Type "Extensions: Install from VSIX"
4. Select the downloaded file

## 📖 Usage

### Keyboard Shortcuts
- **Mac**: `Cmd + Option + L`
- **Windows/Linux**: `Ctrl + Alt + L`

### Basic Operations
1. **Select** code in the editor (supports multi-line selection and multi-cursor selection)
2. Press the keyboard shortcut or select "Copy Selected File and Line Numbers" from the **context menu**
3. File name and line numbers are copied to the clipboard, ready to paste to AI

### Output Format Examples

#### 1. Labeled Format (Default)
```
File: src/extension.ts (line 24-30)
```

#### 2. Compact Format
```
src/extension.ts:24-30
```

#### 3. Code-Style Format
```
src/extension.ts:24:30
```

#### 4. Natural Language Format
```
在 src/extension.ts 的第 24-30 行
```

## ⚙️ Configuration Options

Search for "Copy Line" in VS Code settings to find all configuration options:

### outputFormat
Output format type, default: `labeled`
- `labeled`: `File: src/file.ts (line 24-30)`
- `compact`: `src/file.ts:24-30`
- `code-style`: `src/file.ts:24:30`
- `natural`: `在 src/file.ts 的第 24 行`

### useAbsolutePath
Whether to use absolute paths, default: `false`
- `false`: Use relative paths (relative to workspace root)
- `true`: Use absolute paths

### showStatusMessage
Whether to show status bar message after copying, default: `true`

### singleLineFormat
Format template for single line selection, default: `line ${line}`
- Available variables: `${line}`, `${start}`, `${end}`

### multiLineFormat
Format template for multi-line selection, default: `line ${start}-${end}`
- Available variables: `${line}`, `${start}`, `${end}`

## 🎯 Use Cases

### Collaborating with AI
Tell AI the code location you want to discuss:

**Input to AI:**
```
Please help me optimize this code:
File: src/extension.ts (line 24-30)
```

**AI Understands:**
Needs to review lines 24-30 of the `src/extension.ts` file

### Code Review
Quickly locate code that needs review:

```
Needs review:
File: src/service/user.ts (line 45-67)
File: src/utils/helper.ts (line 12)
```

### Bug Reporting
Report problematic code to your team:

```
Bug found:
File: src/api/client.ts (line 88-95)
```

## 📝 Custom Configuration Example

```json
{
  "copy-line.outputFormat": "natural",
  "copy-line.useAbsolutePath": true,
  "copy-line.singleLineFormat": "第 ${line} 行",
  "copy-line.multiLineFormat": "第 ${start} 到 ${end} 行",
  "copy-line.showStatusMessage": false
}
```

## ⌨️ Keyboard Shortcut Settings

If the default keyboard shortcut conflicts, you can customize it in VS Code:

1. Open `File > Preferences > Keyboard Shortcuts`
2. Search for "复制选中文件与行号"
3. Click to edit and set a new keyboard shortcut

## 🤝 Contributing

Issues and Pull Requests are welcome!

### Development Setup
1. Clone the repository
2. Run `npm install`
3. Press `F5` to start debugging
4. Test features in the new window

## 📄 License

MIT License - See [LICENSE](LICENSE) file for details

## ⭐ Support

If this extension helps you, please give it a ⭐！

---

**Enjoy collaborating with AI!** 🚀
