# S006-sign – iOS Code Signing Tool (Educational)

[![Telegram](https://img.shields.io/badge/Telegram-@boot_loginssl-blue?style=flat&logo=telegram)](https://t.me/boot_loginssl)
[![Open Source](https://img.shields.io/badge/Open%20Source-❤️-green)](https://github.com/nbhnnkmszq-del/S006-sign)
[![Platform](https://img.shields.io/badge/platform-iOS-lightgrey)](https://developer.apple.com/ios/)
[![Status](https://img.shields.io/badge/status-WIP-yellow)](https://github.com/nbhnnkmszq-del/S006-sign)

> 🟢 **Open Source Project** – Contributions welcome!  
> 📢 **Join our Telegram community:** [@boot_loginssl](https://t.me/boot_loginssl)  
> 👤 **Developer:** [@ROOT_DEX](https://t.me/ROOT_DEX)  
> 🔗 **Repository:** [https://github.com/nbhnnkmszq-del/S006-sign](https://github.com/nbhnnkmszq-del/S006-sign)

---

## 📖 Overview

**S006-sign** is an iOS application built with **Objective-C** that provides a graphical interface for **re-signing iOS applications** (.ipa files). This project is developed **for educational purposes** to demonstrate the complete code-signing pipeline on iOS itself.

> ⚠️ **Important Notice:** This project is currently **under active development**. The signing engine works partially, but the installation component (`IPAInstaller`) is still in progress. It is **not yet ready** for production use.

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

## 🧠 Key Features (Implemented So Far)

- ✅ **Graphical Interface** – Simple, intuitive UI for selecting IPA files and signing assets.
- ✅ **Certificate Manager** – Import `.p12` certificates, view expiry dates, and store passwords securely in Keychain.
- ✅ **File Explorer** – Browse local files, import `.ipa`, `.p12`, and `.mobileprovision`.
- ✅ **App Details View** – Display app metadata, icon, and description.
- ⏳ **Profile Parser** – (Partial) Inspect provisioning profiles.
- ⏳ **Re-signing Engine** – (Partial) Uses `codesign` via `NSTask`, needs improvement.
- ⏳ **Installation** – (Missing) Requires `IPAInstaller` component to complete the workflow.

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

## 🔬 How It Works (Educational Flow)

1. **Select IPA** – User picks an iOS app bundle (.ipa)
2. **Extract** – The IPA is unzipped to access the `.app` payload
3. **Select Profile** – User provides a `.mobileprovision` file
4. **Parse Profile** – Extract entitlements, team ID, and app ID
5. **Select Certificate** – Choose a certificate from the device's keychain
6. **Re-sign** – The binary and embedded frameworks are re-signed
7. **Repackage** – The resigned `.app` is zipped back into an IPA
8. **Verify** – Signature is validated using `SecStaticCode`
9. **Export** – Resigned IPA is saved or shared

---

## 🚧 Project Status & Roadmap

> 🚧 **Work in Progress** – This is a **learning project**, not a production tool.

| Component | Status | Notes |
|-----------|--------|-------|
| UI & Navigation | ✅ Complete | All screens built |
| Certificate Import | ✅ Complete | P12 import, Keychain storage |
| File Management | ✅ Complete | Browse, import, share |
| Signing Engine | ⏳ Partial | Uses `NSTask` + `codesign` |
| IPA Installation | ❌ Missing | `IPAInstaller` class needs to be written |
| Profile Parsing | ⏳ Partial | Basic parsing, needs enhancement |
| Error Handling | ⏳ Partial | Needs more edge cases |

**Next Steps:**
1. Complete the `IPAInstaller` class to enable actual installation.
2. Replace `NSTask` with native `Security.framework` signing APIs.
3. Add support for app extensions and nested frameworks.
4. Improve error handling and user feedback.

---

## 🤝 Contributing

**Contributions are highly welcome!** If you're interested in iOS security or code signing, this is a great project to learn and contribute to.

### Areas where help is needed:
- Writing the missing `IPAInstaller` component.
- Implementing native code signing without `NSTask`.
- Improving provisioning profile parsing.
- Adding support for app extensions.
- Testing on different iOS versions and devices.

### How to contribute:
1. Fork the repository.
2. Create a new branch (`feature/your-feature`).
3. Make your changes and test them.
4. Submit a pull request with a clear description.

---

## ⚠️ Important Disclaimer

> **This project is strictly for educational purposes.**  
> It is not intended for piracy, distribution of copyrighted apps, or any commercial use.  
> The author does not condone or support the use of this tool for bypassing Apple's security or licensing mechanisms.  
> Use only with apps you own or have explicit permission to modify.

---

## 📚 Learning Resources & References

| Source | Description |
|--------|-------------|
| **[Apple Code Signing Guide](https://developer.apple.com/library/archive/documentation/Security/Conceptual/CodeSigningGuide/)** | Official Apple documentation |
| **[iOS Security Guide](https://www.apple.com/business/site/docs/iOS_Security_Guide.pdf)** | Apple's whitepaper on iOS security |
| **[The iPhone Wiki – Code Signing](https://www.theiphonewiki.com/wiki/Code_Signing)** | Community-driven reverse engineering knowledge |
| **[ios-app-signer](https://github.com/DanTheMan827/ios-app-signer)** | Inspiration from existing resigning tools |

---

## 📱 Connect with Me

- **Telegram Channel:** [@boot_loginssl](https://t.me/boot_loginssl)
- **Telegram Username:** [@ROOT_DEX](https://t.me/ROOT_DEX)
- **GitHub Repository:** [https://github.com/nbhnnkmszq-del/S006-sign](https://github.com/nbhnnkmszq-del/S006-sign)

---

## 🔧 Requirements

- iOS 14.0+ (development environment)
- Jailbroken device **OR** developer-signed app with appropriate entitlements
- Xcode 14+ for development
- Valid Apple Developer account (for signing the tool itself)

---

## 🚀 Build & Run

```bash
git clone https://github.com/nbhnnkmszq-del/S006-sign.git
cd S006-sign
pod install  # if using CocoaPods
open S006-sign.xcworkspace
# Build and run on your iOS device
