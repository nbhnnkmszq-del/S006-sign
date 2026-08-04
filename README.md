# S006-sign – iOS Code Signing Tool

[![Telegram](https://img.shields.io/badge/Telegram-@boot_loginssl-blue?style=flat&logo=telegram)](https://t.me/boot_loginssl)
[![Open Source](https://img.shields.io/badge/Open%20Source-❤️-green)](https://github.com/nbhnnkmszq-del/S006-sign)
[![Platform](https://img.shields.io/badge/platform-iOS-lightgrey)](https://developer.apple.com/ios/)

> 🟢 **Open Source Project** – Contributions welcome!  
> 📢 **Join our Telegram community:** [@boot_loginssl](https://t.me/boot_loginssl)  
> 👤 **Developer:** [@ROOT_DEX](https://t.me/ROOT_DEX)  
> 🔗 **Repository:** [https://github.com/nbhnnkmszq-del/S006-sign](https://github.com/nbhnnkmszq-del/S006-sign)

---

## 📖 Overview

**S006-sign** is an iOS application built with **Objective-C** that provides a graphical interface for ت**re-signing iOS applications** (.ipa files) using user-provided provisioning profiles and certificates. This project is developed **for educational purposes** to demonstrate the complete code-signing pipeline on iOS itself.

Unlike command-line tools, S006-sign runs directly on an iOS device (jailbroken or using developer entitlements), allowing users to understand how signing works from within the mobile environment.

---

## 🎯 Educational Objectives

This project aims to teach:

- How iOS verifies application signatures using **Apple's Security framework**.
- The structure of **.mobileprovision** files (CMS-signed property lists).
- How to extract and manipulate **entitlements** and **application-identifier**.
- The relationship between **certificates**, **private keys**, and **provisioning profiles**.
- How to perform **code signing** programmatically using `SecCode`, `SecStaticCode`, and related APIs.
- The internals of **Mach-O binary signing** and **bundle structure**.
- Working with **Keychain services** (`SecItem`) on iOS to manage certificates.

---

## 🧠 Key Features

- ✅ **Graphical Interface** – Simple, intuitive UI for selecting IPA files and signing assets.
- 🔐 **Profile Parser** – Inspect provisioning profiles (team ID, app ID, devices, expiration).
- 📜 **Entitlements Viewer** – Display and modify entitlements before signing.
- ✍️ **Re-signing Engine** – Replace existing signatures with new ones using a developer certificate.
- 🧪 **Verification** – Validate the signed IPA before installation.
- 📦 **Export** – Save the resigned IPA to Files.app or share via AirDrop.
- 💡 **Code Comments** – Every critical section is documented with explanatory comments.

---

## 🛠 Technologies Used

- **Objective-C** (with ARC)
- **UIKit** – for the user interface
- **Security.framework** – for cryptographic operations and certificate handling
- **CoreFoundation** – for property list and data parsing
- **CommonCrypto** – for hashing (SHA-1, SHA-256)
- **libzip / SSZipArchive** – for IPA extraction and repackaging
- **NSFileManager** – for bundle manipulation

---

## 📂 Project Structure



