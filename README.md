# Corex-DeepSeek

A lightweight Windows desktop client for [DeepSeek](https://chat.deepseek.com/), built with **Tauri 2 and Rust**.

This project provides direct access to the official DeepSeek web interface through a dedicated desktop application, without implementing a separate frontend or embedding an AI model.

## Technologies

| Technology | Description |
|---|---|
| **Rust** | Native application backend |
| **Tauri 2** | Desktop application framework |
| **WebView2** | Rendering engine for the web interface |
| **Cargo** | Rust dependency and build management |
| **Node.js** | JavaScript tooling |
| **Tauri CLI** | Application development and packaging |
| **NSIS** | Windows installer generation |

## Technical Details

- **Native backend:** Minimal Rust implementation using Tauri.
- **Web interface:** Loads the official DeepSeek website directly.
- **Rendering:** Uses the installed Microsoft Edge WebView2 runtime.
- **Browser configuration:** Custom Chromium arguments to disable selected browser features and unnecessary components.
- **Optimized compilation:** Link-Time Optimization (LTO), optimized release profile, stripped binary and reduced code generation units.
- **Installer:** Windows NSIS installer.

## Project Structure

```text
deepseek/
├── dist/
│   └── index.html
├── src-tauri/
│   ├── icons/
│   │   └── deepseek.ico
│   ├── src/
│   │   ├── lib.rs
│   │   └── main.rs
│   ├── Cargo.toml
│   ├── build.rs
│   └── tauri.conf.json
├── package.json
└── package-lock.json
```

## Build

```bash
npm install
npm run build
```

**Platform:** Windows

**Framework:** Tauri 2

**Language:** Rust
