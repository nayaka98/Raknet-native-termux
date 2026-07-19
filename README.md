# 🚀 raknet-native Termux ARM64 Prebuilt

![Platform](https://img.shields.io/badge/platform-Termux%20Android-green)
![Architecture](https://img.shields.io/badge/architecture-ARM64%20%2F%20aarch64-blue)
![Type](https://img.shields.io/badge/type-Prebuilt%20Native%20Addon-orange)

A prebuilt **raknet-native** binary for **Android Termux ARM64 (aarch64)**.

This repository provides a ready-to-use native `.node` binary for Termux users who cannot or do not want to compile `raknet-native` manually.

---

# ⚠️ Disclaimer

This is an **unofficial community build**.

- This project is not affiliated with the original `raknet-native` developers.
- This repository only provides a prebuilt binary build for Termux Android ARM64.
- Use this software at your own risk.
- No warranty is provided.
- The maintainer is not responsible for crashes, compatibility problems, data loss, or any issues caused by using this binary.

Always verify the source and understand what you are running.

---

# 📦 About

`raknet-native` is a Node.js native addon that provides RakNet networking functionality.

Original npm package:

https://www.npmjs.com/package/raknet-native

This repository exists because compiling native Node.js addons on Android Termux can be difficult due to:

- CMake compatibility issues
- Compiler differences
- Android/Bionic environment
- Missing official Android prebuilt binaries

---

# ✨ Features

- ✅ Built for Termux Android
- ✅ ARM64 / aarch64 support
- ✅ Ready-to-use `.node` binary
- ✅ No CMake compilation required
- ✅ No manual C++ build required
- ✅ Works with projects requiring `raknet-native`

---

# 📋 Requirements

You need:

- Android ARM64 device
- Termux
- Node.js
- npm

Check your architecture:

```bash
uname -m
```

Expected output:

```
aarch64
```

---

# 📥 Installation

## 1. Clone this repository

Replace `YOUR_REPOSITORY_URL` with the actual GitHub repository URL.

```bash
git clone YOUR_REPOSITORY_URL
```

Enter the repository folder:

```bash
cd YOUR_REPOSITORY_FOLDER
```

---

## 2. Extract raknet.zip

This repository contains:

```
raknet.zip
```

Extract it:

```bash
unzip raknet.zip
```

After extraction you will get:

```
raknet-native/
├── build/
│   └── Release/
│       └── node-raknet.node
├── package.json
└── other files
```

---

## 3. Copy raknet-native folder

Copy the extracted folder into your project `node_modules`.

Example:

```bash
cp -r raknet-native ~/bedrock-client/node_modules/
```

or:

```bash
cp -r raknet-native node_modules/
```

---

# 📂 Final Directory Structure

Your project should look like:

```
node_modules/
└── raknet-native/
    ├── build/
    │   └── Release/
    │       └── node-raknet.node
    ├── package.json
    └── other files
```

---

# ✅ Test Installation

Run:

```bash
node -e "require('raknet-native'); console.log('raknet-native loaded successfully')"
```

Expected result:

```
raknet-native loaded successfully
```

---

# 🧪 Example Usage

Example with `bedrock-protocol`:

```js
import bedrock from "bedrock-protocol";

const client = bedrock.createClient({
    host: "server-address",
    port: 19132,
    username: "Player",
    raknetBackend: "raknet-native"
});
```

---

# 🔧 Build Information

| Information | Value |
|---|---|
| Platform | Android Termux |
| Architecture | ARM64 / aarch64 |
| Binary | node-raknet.node |
| Type | Node.js Native Addon |
| Build | Community Prebuilt |

---

# ❌ Compatibility

This build is intended for:

✅ Android ARM64  
✅ Termux  
✅ Node.js ARM64  

Not guaranteed for:

❌ ARM32 devices  
❌ Windows  
❌ macOS  
❌ Linux x64  
❌ Other architectures

---

# 🛠 Troubleshooting

## Module not found

Check if the binary exists:

```bash
ls node_modules/raknet-native/build/Release/
```

Expected:

```
node-raknet.node
```

---

## Invalid ELF header

Your device architecture does not match.

Check:

```bash
uname -m
```

Required:

```
aarch64
```

---

## Native addon loading error

Native addons depend on:

- Node.js version
- CPU architecture
- Operating system ABI

If you changed Node.js versions and it stops working, use a compatible build or rebuild the addon.

---

# 📜 License

This repository contains a redistributed build of `raknet-native`.

Original package:

https://www.npmjs.com/package/raknet-native

`raknet-native` is licensed under the **ISC License**.

The original license notice is included with this project.

---

# ❤️ Credits

- Original `raknet-native` developers
- Node.js native addon ecosystem
- Termux community
- Android ARM64 users

---

# ⭐ Support

If this project helps you:

- Star the repository
- Report issues
- Share improvements

Thank you!
