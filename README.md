# 🚀 Continuation of pterodactyl-images

[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Docker Images](https://img.shields.io/badge/Docker-Images-blue)](https://github.com/DonPedroTV/pterodactyl-images/pkgs/container/pterodactyl-images)

This fork is maintained by [**DonPedroTV**](https://github.com/DonPedroTV) as a continuation of the work done in the original repository [**trenutoo/pterodactyl-images**](https://github.com/trenutoo/pterodactyl-images). The original author allowed forks—this README and all image references have been updated to the new namespace.

## 📋 Table of Contents

- [🐳 Pelican/Pterodactyl/WISP Docker Images](#pelicanpterodactylwisp-docker-images)
- [📖 How to Add Image to Your Egg](#how-to-add-image-to-your-egg)
- [👾 Supported Platforms](#supported-platforms)
- [☕ Java Images](#java-images)
  - [☕ Java Amazon Corretto (AMD64/ARM64)](#java-amazon-corretto-amd64arm64)
  - [☕ Java Eclipse Temurin (AMD64/ARM64)](#java-eclipse-temurin-amd64arm64)
  - [☕ Java Azul Zulu (AMD64/ARM64)](#java-azul-zulu-amd64arm64)
  - [☕ Java GraalVM (AMD64/ARM64)](#java-graalvm-amd64arm64)
  - [☕ Java Oracle GraalVM (with Enterprise Edition features) (AMD64/ARM64)](#java-oracle-graalvm-with-enterprise-edition-features-amd64arm64)
  - [☕ Java Dragonwell (AMD64/ARM64)](#java-dragonwell-amd64arm64)
  - [☕ Java Liberica (AMD64/ARM64)](#java-liberica-amd64arm64)
  - [☕ Java OpenJ9 (AMD64)](#java-openj9-amd64)
  - [☕ Java Shenandoah (AMD64/ARM64)](#java-shenandoah-amd64arm64)
- [🟢 Node.js (AMD64/ARM64)](#nodejs-amd64arm64)
- [🐍 Python (AMD64/ARM64)](#python-amd64arm64)
- [🎮 Game Specific](#game-specific)
  - [🔧 Sourcemod (AMD64)](#sourcemod-amd64)

## Pelican/Pterodactyl/WISP Docker Images

Docker images that can be used with the **Pelican/Pterodactyl/WISP Game Panel**. You can request more images by [opening a new issue](https://github.com/DonPedroTV/pterodactyl-images/issues/new). These are mostly created for personal use.

> **Additional Pterodactyl images** can be found at:
> - [Parkervcp](https://github.com/parkervcp/images)
> - [Matthewpi](https://github.com/matthewpi/images)
> - [Yolks](https://github.com/pterodactyl/yolks) repositories.

## How to Add Image to Your Egg

Navigate to `Admin Panel -> Nests -> Select your egg`. Add Docker image URL(s) from the [available list](#supported-platforms) into the **Docker Images** section.

![Admin Panel Screenshot](https://user-images.githubusercontent.com/10975908/120903180-56719d80-c64d-11eb-8666-02de8ea80701.png)

### Supported Platforms

| Image                                                                                                  | Supported Platforms |
| ------------------------------------------------------------------------------------------------------ | ------------------- |
| [☕ Java Amazon Corretto (AMD64/ARM64)](#java-amazon-corretto-amd64arm64) | ![AMD64](https://img.shields.io/badge/AMD64-Supported-green) ![ARM64](https://img.shields.io/badge/ARM64-Supported-green) |
| [☕ Java Azul Zulu (AMD64/ARM64)](#java-azul-zulu-amd64arm64)             | ![AMD64](https://img.shields.io/badge/AMD64-Supported-green) ![ARM64](https://img.shields.io/badge/ARM64-Supported-green) |
| [☕ Java Eclipse Temurin (AMD64/ARM64)](#java-eclipse-temurin-amd64arm64) | ![AMD64](https://img.shields.io/badge/AMD64-Supported-green) ![ARM64](https://img.shields.io/badge/ARM64-Supported-green) |
| [☕ Java GraalVM (AMD64/ARM64)](#java-graalvm-amd64arm64)                 | ![AMD64](https://img.shields.io/badge/AMD64-Supported-green) ![ARM64](https://img.shields.io/badge/ARM64-Supported-green) |
| [☕ Java Oracle GraalVM (with Enterprise Edition features) (AMD64/ARM64)](#java-oracle-graalvm-with-enterprise-edition-features-amd64arm64)                 | ![AMD64](https://img.shields.io/badge/AMD64-Supported-green) ![ARM64](https://img.shields.io/badge/ARM64-Supported-green) |
| [☕ Java Dragonwell (AMD64/ARM64)](#java-dragonwell-amd64arm64)           | ![AMD64](https://img.shields.io/badge/AMD64-Supported-green) ![ARM64](https://img.shields.io/badge/ARM64-Supported-green) |
| [☕ Java Liberica (AMD64/ARM64)](#java-liberica-amd64arm64)               | ![AMD64](https://img.shields.io/badge/AMD64-Supported-green) ![ARM64](https://img.shields.io/badge/ARM64-Supported-green) |
| [☕ Java OpenJ9 (AMD64)](#java-openj9-amd64)                        | ![AMD64](https://img.shields.io/badge/AMD64-Supported-green) |
| [☕ Java Shenandoah (AMD64/ARM64)](#java-shenandoah-amd64arm64)           | ![AMD64](https://img.shields.io/badge/AMD64-Supported-green) ![ARM64](https://img.shields.io/badge/ARM64-Supported-green) |
| [🟢 Node.js (AMD64/ARM64)](#nodejs-amd64arm64)                            | ![AMD64](https://img.shields.io/badge/AMD64-Supported-green) ![ARM64](https://img.shields.io/badge/ARM64-Supported-green) |
| [🐍 Python (AMD64/ARM64)](#python-amd64arm64)                             | ![AMD64](https://img.shields.io/badge/AMD64-Supported-green) ![ARM64](https://img.shields.io/badge/ARM64-Supported-green) |
| [🔧 Sourcemod (AMD64)](#sourcemod-amd64)                            | ![AMD64](https://img.shields.io/badge/AMD64-Supported-green) |

## Java Images

> **Note**: The first four Java distributions (Amazon Corretto, Eclipse Temurin, Azul Zulu, and GraalVM) are my personal preferences for most use cases. Additionally, many users consider Azul Zulu to be one of the most performant Java distributions available.

### Java Amazon Corretto (AMD64/ARM64)

| Version | Image Tag |
|---------|-----------|
| Java 8 | `ghcr.io/donpedrotv/pterodactyl-images:java_8_corretto` |
| Java 11 | `ghcr.io/donpedrotv/pterodactyl-images:java_11_corretto` |
| Java 17 | `ghcr.io/donpedrotv/pterodactyl-images:java_17_corretto` |
| Java 19 | `ghcr.io/donpedrotv/pterodactyl-images:java_19_corretto` |
| Java 20 | `ghcr.io/donpedrotv/pterodactyl-images:java_20_corretto` |
| Java 21 | `ghcr.io/donpedrotv/pterodactyl-images:java_21_corretto` |
| Java 25 | `ghcr.io/donpedrotv/pterodactyl-images:java_25_corretto` |

### Java Eclipse Temurin (AMD64/ARM64)

| Version | Image Tag |
|---------|-----------|
| Java 8 | `ghcr.io/donpedrotv/pterodactyl-images:java_8` |
| Java 11 | `ghcr.io/donpedrotv/pterodactyl-images:java_11` |
| Java 16 | `ghcr.io/donpedrotv/pterodactyl-images:java_16` |
| Java 17 | `ghcr.io/donpedrotv/pterodactyl-images:java_17` |
| Java 18 | `ghcr.io/donpedrotv/pterodactyl-images:java_18` |
| Java 19 | `ghcr.io/donpedrotv/pterodactyl-images:java_19` |
| Java 20 | `ghcr.io/donpedrotv/pterodactyl-images:java_20` |
| Java 21 | `ghcr.io/donpedrotv/pterodactyl-images:java_21` |
| Java 22 | `ghcr.io/donpedrotv/pterodactyl-images:java_22` |

### Java Azul Zulu (AMD64/ARM64)

| Version | Image Tag |
|---------|-----------|
| Java 8 | `ghcr.io/donpedrotv/pterodactyl-images:java_8_zulu` |
| Java 11 | `ghcr.io/donpedrotv/pterodactyl-images:java_11_zulu` |
| Java 16 | `ghcr.io/donpedrotv/pterodactyl-images:java_16_zulu` |
| Java 17 | `ghcr.io/donpedrotv/pterodactyl-images:java_17_zulu` |
| Java 18 | `ghcr.io/donpedrotv/pterodactyl-images:java_18_zulu` |
| Java 19 | `ghcr.io/donpedrotv/pterodactyl-images:java_19_zulu` |
| Java 20 | `ghcr.io/donpedrotv/pterodactyl-images:java_20_zulu` |
| Java 21 (LTS) | `ghcr.io/donpedrotv/pterodactyl-images:java_21_zulu` |
| Java 22 | `ghcr.io/donpedrotv/pterodactyl-images:java_22_zulu` |
| Java 24 | `ghcr.io/donpedrotv/pterodactyl-images:java_24_zulu` |
| Java 25 (LTS) | `ghcr.io/donpedrotv/pterodactyl-images:java_25_zulu` |

### Java GraalVM (AMD64/ARM64)

> **NOTE**: Java 8 is AMD64 only due to lack of support from upstream.

| Version | Image Tag |
|---------|-----------|
| Java 8 GraalVM-CE | `ghcr.io/donpedrotv/pterodactyl-images:java_8_graalvm` |
| Java 11 GraalVM JDK | `ghcr.io/donpedrotv/pterodactyl-images:java_11_graalvm` |
| Java 17 GraalVM JDK | `ghcr.io/donpedrotv/pterodactyl-images:java_17_graalvm` |
| Java 21 GraalVM JDK | `ghcr.io/donpedrotv/pterodactyl-images:java_21_graalvm` |
| Java 22 GraalVM JDK | `ghcr.io/donpedrotv/pterodactyl-images:java_22_graalvm` |
| Java 24 GraalVM JDK | `ghcr.io/donpedrotv/pterodactyl-images:java_24_graalvm` |
| Java 25 GraalVM JDK | `ghcr.io/donpedrotv/pterodactyl-images:java_25_graalvm` |

### Java Oracle GraalVM (with Enterprise Edition features) (AMD64/ARM64)

| Version | Image Tag |
|---------|-----------|
| Java 25 GraalVM-EE JDK | `ghcr.io/donpedrotv/pterodactyl-images:java_25_graalvm_ee` |

### Java Dragonwell (AMD64/ARM64)

| Version | Image Tag |
|---------|-----------|
| Java 8 | `ghcr.io/donpedrotv/pterodactyl-images:java_8_dragonwell` |
| Java 11 | `ghcr.io/donpedrotv/pterodactyl-images:java_11_dragonwell` |
| Java 17 | `ghcr.io/donpedrotv/pterodactyl-images:java_17_dragonwell` |
| Java 21 | `ghcr.io/donpedrotv/pterodactyl-images:java_21_dragonwell` |

### Java Liberica (AMD64/ARM64)

| Version | Image Tag |
|---------|-----------|
| Java 8 | `ghcr.io/donpedrotv/pterodactyl-images:java_8_liberica` |
| Java 11 | `ghcr.io/donpedrotv/pterodactyl-images:java_11_liberica` |
| Java 17 | `ghcr.io/donpedrotv/pterodactyl-images:java_17_liberica` |
| Java 21 | `ghcr.io/donpedrotv/pterodactyl-images:java_21_liberica` |
| Java 22 | `ghcr.io/donpedrotv/pterodactyl-images:java_22_liberica` |

### Java OpenJ9 (AMD64)

| Version | Image Tag |
|---------|-----------|
| Java 8 | `ghcr.io/donpedrotv/pterodactyl-images:java_8_openj9` |
| Java 11 | `ghcr.io/donpedrotv/pterodactyl-images:java_11_openj9` |
| Java 16 | `ghcr.io/donpedrotv/pterodactyl-images:java_16_openj9` |
| Java 17 | `ghcr.io/donpedrotv/pterodactyl-images:java_17_openj9` |
| Java 18 | `ghcr.io/donpedrotv/pterodactyl-images:java_18_openj9` |
| Java 20 | `ghcr.io/donpedrotv/pterodactyl-images:java_20_openj9` |
| Java 21 | `ghcr.io/donpedrotv/pterodactyl-images:java_21_openj9` |

### Java Shenandoah (AMD64/ARM64)

These are [Shipilev experimental builds](https://builds.shipilev.net/). If you're looking for Shenandoah GC, it is also by default shipped with at least Azul, Corretto, and Temurin images starting with Java 11.

| Version | Image Tag |
|---------|-----------|
| Java 8 | `ghcr.io/donpedrotv/pterodactyl-images:java_8_shenandoah` |
| Java 11 | `ghcr.io/donpedrotv/pterodactyl-images:java_11_shenandoah` |
| Java 17 | `ghcr.io/donpedrotv/pterodactyl-images:java_17_shenandoah` |
| Java 21 | `ghcr.io/donpedrotv/pterodactyl-images:java_21_shenandoah` |

## Node.js (AMD64/ARM64)

| Version | Image Tag |
|---------|-----------|
| Node.js 12 | `ghcr.io/donpedrotv/pterodactyl-images:nodejs_12` |
| Node.js 14 | `ghcr.io/donpedrotv/pterodactyl-images:nodejs_14` |
| Node.js 15 | `ghcr.io/donpedrotv/pterodactyl-images:nodejs_15` |
| Node.js 16 | `ghcr.io/donpedrotv/pterodactyl-images:nodejs_16` |
| Node.js 17 | `ghcr.io/donpedrotv/pterodactyl-images:nodejs_17` |
| Node.js 18 | `ghcr.io/donpedrotv/pterodactyl-images:nodejs_18` |
| Node.js 19 | `ghcr.io/donpedrotv/pterodactyl-images:nodejs_19` |
| Node.js 20 | `ghcr.io/donpedrotv/pterodactyl-images:nodejs_20` |
| Node.js 21 | `ghcr.io/donpedrotv/pterodactyl-images:nodejs_21` |
| Node.js 22 | `ghcr.io/donpedrotv/pterodactyl-images:nodejs_22` |

## Python (AMD64/ARM64)

| Version | Image Tag |
|---------|-----------|
| Python 2.7 | `ghcr.io/donpedrotv/pterodactyl-images:python_2.7` |
| Python 3.6 | `ghcr.io/donpedrotv/pterodactyl-images:python_3.6` |
| Python 3.7 | `ghcr.io/donpedrotv/pterodactyl-images:python_3.7` |
| Python 3.8 | `ghcr.io/donpedrotv/pterodactyl-images:python_3.8` |
| Python 3.9 | `ghcr.io/donpedrotv/pterodactyl-images:python_3.9` |
| Python 3.10 | `ghcr.io/donpedrotv/pterodactyl-images:python_3.10` |
| Python 3.11 | `ghcr.io/donpedrotv/pterodactyl-images:python_3.11` |
| Python 3.12 | `ghcr.io/donpedrotv/pterodactyl-images:python_3.12` |
| Python 3.13-rc | `ghcr.io/donpedrotv/pterodactyl-images:python_3.13-rc` |

## Game Specific

### Sourcemod (AMD64)

| Image | Tag |
|-------|-----|
| Source with Sourcemod | `ghcr.io/donpedrotv/pterodactyl-images:games_source-sourcemod` |

> Optionally installs and updates SourceMod/Metamod on each server startup. Requires adding egg environment variable `SOURCEMOD`.

![Sourcemod Screenshot](https://user-images.githubusercontent.com/10975908/159126935-2e3f2883-3b89-4395-b28d-ab23dad0e5f8.png)

> Custom versions can be set with the use of `SM_VERSION` and `MM_VERSION` variables. Invalid versions will default to the latest stable version. Default path is set to csgo and can be overridden with `INSTALL_PATH` egg environment variable.

---

## 🤝 Contributing

Feel free to [open an issue](https://github.com/DonPedroTV/pterodactyl-images/issues) or submit a pull request if you have suggestions or improvements!

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
