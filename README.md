# Bencode Standalone-HTML-Editor

A modern, standalone web-based editor for Bencode files (.torrent, .bencode) with a sleek dark interface and real-time editing capabilities.

![Bencode Editor](https://img.shields.io/badge/bencode-editor-38bdf8)
![License](https://img.shields.io/badge/license-MIT-green)

<img width="1312" height="729" alt="image" src="https://github.com/user-attachments/assets/5ccbd642-2780-4c0b-a4b9-19a28cf777a5" />

## ✨ Features

- 🎨 **Modern Dark UI** - Beautiful, responsive interface with glassmorphism effects
- 📝 **Live JSON Editing** - Edit bencode data in human-readable JSON format
- 🔄 **Bidirectional Conversion** - Seamless conversion between Bencode and JSON
- 💾 **Smart Save System** - Visual feedback when changes are made
- 📋 **One-Click Copy** - Copy JSON to clipboard with success feedback
- 🖱️ **Drag & Drop** - Simply drag files into the editor
- 🔍 **Syntax Highlighting** - CodeMirror-powered editor with dark theme
- 🎯 **Binary Data Support** - Handles binary data with hex representation
- ⚡ **Zero Dependencies** - Single HTML file, works offline

## 🚀 Usage

### Online
Simply download `bencode_editor.html` and open it in any modern web browser. No installation or server required.

### Features in Action

1. **Open a File**
   - Click the "📂 Open" button
   - Or drag & drop a .torrent or .bencode file anywhere on the page

2. **Edit Content**
   - Modify the JSON in the editor
   - Save button turns blue when changes are detected
   - All bencode data types are supported (integers, strings, lists, dictionaries)

3. **Handle Binary Data**
   - Binary data is displayed as `<hex>XX XX XX...</hex>`
   - Edit hex values directly
   - Legacy `0x` format also supported

4. **Save Changes**
   - Click "💾 Save" to download the modified file
   - Get visual confirmation with ✓ checkmark
   - Original filename is preserved

5. **Copy to Clipboard**
   - Click "📋 Copy" to copy JSON to clipboard
   - Useful for sharing or debugging

## 🛠️ Technical Details

### Bencode Format Support
- **Integers**: `i42e` → `42`
- **Strings**: `5:hello` → `"hello"`
- **Lists**: `li1ei2ee` → `[1, 2]`
- **Dictionaries**: `d3:keyi1ee` → `{"key": 1}`
- **Binary Data**: Represented as hex strings in `<hex>...</hex>` format

### Browser Compatibility
- Any modern browser with ES6 support

### Technologies Used
- **CodeMirror 5.65** - Code editor with syntax highlighting
- **Vanilla JavaScript** - No frameworks, pure ES6+
- **Material Darker Theme** - Eye-friendly dark color scheme

## 📋 Use Cases

- 🌐 **Torrent File Editing** - Modify tracker URLs, file lists, or metadata
- 🔧 **Debugging** - Inspect bencode data in readable format
- 📊 **Data Analysis** - Extract and analyze torrent information
- 🎓 **Learning** - Understand the bencode format interactively
- 🔄 **Format Conversion** - Convert between bencode and JSON

## 💡 Example

**Original Bencode:**
```
d8:announce35:http://tracker.example.com:808013:announce-listll35:http://tracker.example.com:8080eee
```

**Displayed as JSON:**
```json
{
  "announce": "http://tracker.example.com:8080",
  "announce-list": [
    [
      "http://tracker.example.com:8080"
    ]
  ]
}
```

## 🤝 Credits

Vibe-coded by **Piknockyou**

Based on [Bencode Online](https://github.com/Chocobo1/bencode_online) by Chocobo1
- Core bencode encoding/decoding algorithms
- Binary data handling approach

Built with:
- [CodeMirror](https://codemirror.net/) - Versatile text editor
- [Google Fonts](https://fonts.google.com/) - Inter & Fira Code

## 📄 License

MIT License - Feel free to use, modify, and distribute.

## 🐛 Known Limitations

- Maximum file size depends on browser memory (typically ~100MB)
- Very large files may cause slow rendering in the editor
- Binary data editing is limited to hex format

## 🙏 Contributing

Contributions, issues, and feature requests are welcome! Feel free to check the issues page.

## ⭐ Show Your Support

Give a ⭐️ if this project helped you!

---

**Note**: This is a client-side application. All file processing happens in your browser - no data is sent to any server.
