# CoreFrame Extensions

**Community extension registry for [CoreFrame](https://github.com/RoftCore/CoreFrame)** — the open-source modular dashboard.

<p align="center">
  <img src="https://img.shields.io/badge/extensions-7-blue" alt="Extensions">
  <img src="https://img.shields.io/badge/license-MIT-green" alt="License">
  <img src="https://img.shields.io/badge/registry-v1-lightgrey" alt="Registry">
</p>

---

## Table of Contents

- [What is this?](#what-is-this)
- [Available extensions](#available-extensions)
- [Installing extensions](#installing-extensions)
  - [From the Marketplace (recommended)](#from-the-marketplace-recommended)
  - [Manual install](#manual-install)
- [Submitting an extension](#submitting-an-extension)
- [Extension format](#extension-format)
- [License](#license)

---

## What is this?

This repository hosts the **official extension registry** for CoreFrame. The file [`registry.json`](registry.json) is the source of truth for the in-app Marketplace — CoreFrame fetches it to display available extensions and their download URLs.

## Available extensions

| Extension | Category | Platforms | Description |
|-----------|----------|-----------|-------------|
| [App Carousel](https://github.com/RoftCore/extensions-coreframe/releases/tag/app_carousel-1.0) | UI | Windows, Linux | Quick-switch between extensions with a circular carousel |
| [Fortune Cookie](https://github.com/RoftCore/extensions-coreframe/releases/tag/fortune_cookie-1.0) | Fun | Windows, Linux | Random fortunes and witty quotes at a click |
| [Network Monitor](https://github.com/RoftCore/extensions-coreframe/releases/tag/network_monitor-1.4) | Cybersecurity | Windows | Public IP, VPN, ports, DNS leaks |
| [Process Manager](https://github.com/RoftCore/extensions-coreframe/releases/tag/process_manager-1.2) | Processes | Windows, Linux | System process management: view, filter, kill and monitor usage |
| [Spotify Downloader](https://github.com/RoftCore/extensions-coreframe/releases/tag/spotify_downloader-1.0) | Media | Windows, Linux | Download Spotify playlists as MP3 via YouTube |
| [System Monitor](https://github.com/RoftCore/extensions-coreframe/releases/tag/system_monitor-1.1) | System | Windows, Linux | CPU, RAM, GPU, disk and system processes |
| [Vault Manager](https://github.com/RoftCore/extensions-coreframe/releases/tag/vault_manager-1.0) | System | Windows, Linux | Encrypted notes and secrets management |

## Installing extensions

### From the Marketplace (recommended)

1. Open CoreFrame
2. Click **Settings (⚙️) → Extensions → Marketplace**
3. Browse or search for an extension
4. Click **Install**

The Marketplace fetches the list from this repository's [`registry.json`](registry.json).

### Manual install

1. Download the `.zip` from the extension's release page
2. Extract to `~/Documents/CoreFrame/extensions/<extension_id>/`
3. Restart CoreFrame (or go to Settings → Extensions → the extension should appear)

## Submitting an extension

To add your extension to the official registry:

1. Create a release on your fork of this repo with the `.zip` asset
2. Edit [`registry.json`](registry.json) with your extension's metadata
3. Open a pull request

Each extension entry must include:

| Field | Type | Description |
|-------|------|-------------|
| `id` | string | Unique identifier (lowercase, no spaces) |
| `name` | string | Display name |
| `version` | string | Semver |
| `author` | string | Your name or alias |
| `description` | string | One-line summary |
| `category` | string | One of: `ui`, `fun`, `cybersecurity`, `processes`, `media`, `system`, `general`, `development` |
| `icon` | string | Icon identifier (Lucide icon set) |
| `platforms` | string[] | Supported platforms: `windows`, `linux`, `macos` |
| `grid_size` | object | Default widget size: `{ "w": N, "h": N }` |
| `download_url` | string | Direct URL to the `.zip` release asset |
| `hidden` | bool | *(optional)* Hide from public listing (default: `false`) |

## Extension format

See the [CoreFrame EXTENSIONS.md](https://github.com/RoftCore/CoreFrame/blob/main/docs/EXTENSIONS.md) for the full guide on creating extensions.

## License

MIT
