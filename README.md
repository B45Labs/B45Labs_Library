# B45 Labs · Library — Revit Add-in

![Revit](https://img.shields.io/badge/Revit-2023--2027-0696D7?style=flat-square&logo=autodesk&logoColor=white)
![Platform](https://img.shields.io/badge/Platform-Windows-lightgrey?style=flat-square)
![License](https://img.shields.io/badge/License-Proprietary-red?style=flat-square)
![Version](https://img.shields.io/badge/Version-1.1.1-0696D7?style=flat-square)
![.NET](https://img.shields.io/badge/.NET-net48%20%2F%208.0%20%2F%2010.0-512BD4?style=flat-square)

> B45 Labs · Library is a content and family powerhouse that lives inside Autodesk Revit — browse and load anything from a single family to a whole sheet, manage families in bulk, and keep a shared detail library in sync across every project.

> **Part of the B45 Labs suite.** Library installs and updates **independently**. Installed on its own, it runs standalone with its own ribbon tab; installed alongside **Coordination** or **Production**, it integrates as a panel on that product's tab.

---

## ✨ Key Features

### 📚 Content Browser
A dockable pane to browse, preview, and load content into your model — from two sources (**your open models** and **your external libraries**), each with the same rich set of tabs:

- **Families** — browse loadable families, search and filter by category, preview thumbnails, and insert one or many with chained placement. External `.rfa` / `.rte` libraries are scanned from folders you configure and opened in the background.
- **System types** — Walls, Floors, Ceilings, Roofs, Pipes, Ducts and more, with a **Smart Insert** that applies the type to your selection or launches Revit's native draw tool.
- **Materials** — browse by class (Concrete, Wood, Glass, Metal…) and import across documents, with automatic rename-on-collision and a texture-path fallback.
- **Patterns** — drafting and model fill patterns, imported with auto-rename.
- **Drafting Views, Legends, Sheets, and Groups** — cross-document insert of drafting views, legends, whole sheets, and model/detail groups with interactive placement.
- **Across every tab** — global search with per-section counts, universal **Favorites** and **Recents**, list or grid layout, four thumbnail sizes, a persistent on-disk thumbnail cache, and multi-select + batch insert.

### 🧩 Family Manager
A modeless tool to manage families in bulk, across four tabs (filter, search, and multi-select everywhere):

- **Unlock Family Parameters** — find every locked family parameter (with the reason it's locked), batch-unlock the ones you choose, and reload the families. Pick a family straight from the canvas; per-session undo/redo.
- **Rename** — an accumulating staging buffer: layer Find/Replace (regex), prefix/suffix, and casing rules, with per-row validation and conflict blocking before you Apply.
- **Parameters** — batch-add shared parameters, remove parameters by name, and queue several operations before applying them in one pass.
- **Export** — export selected families to `.rfa`, flat or organized into per-category folders.

### 🗂️ Detail Library
Publish, standardize, and reuse your details across every project:

- **Publish** drafting views and legends to a master library, with version control and content-change detection.
- **Check** and **Sync** — audit your project's details against the master and pull the latest, with a clear state for each (Up to date, Outdated, Locally modified, Unversioned, Orphan). **Promote** a corrected detail back up as a new version.
- Details are tracked by a **stable GUID + content hash**, not by name — so a rename never breaks the link and drift is caught automatically.

---

## 📋 Requirements

| Requirement | Details |
|---|---|
| Autodesk Revit | 2023, 2024, 2025, 2026, 2027 *(full support)* |
| Operating System | Windows 10 / Windows 11 |
| .NET | net48 (R23/R24) · net8.0-windows (R25/R26) · net10.0-windows (R27) |
| Installation | Per-user — no administrator rights required |

---

## 📦 Installation

1. Download the latest installer from [**Releases**](https://github.com/B45Labs/B45Labs_Library/releases).
2. Close Revit before installing.
3. Run the installer, accept the license, and select the Revit versions to install for.
4. Launch Revit — the Library tools appear on the ribbon.

---

## 🌐 Languages

English, plus **Português (BR), Español, Français, and Русский as BETA** — AI-assisted drafts pending native review. If a translation reads wrong, tell us at support@b45labs.com.

---

## 🔄 Updates

B45 Labs · Library checks for newer versions and prompts you when an update is available. Routine updates show a gentle toast; only updates required for compatibility or stability block execution until updated.

---

## 📊 Telemetry

To improve stability and prioritize development, B45 Labs collects limited, consent-based usage signals — **opt-out at any time** from the in-app **My Profile** window:
- Commands executed and usage counts
- Error logs (file paths, model names, and emails redacted before transmission)
- Add-in and Revit version, interface language
- Approximate region (country/region, derived from IP — IP is not stored)
- Anonymous installation and session identifiers

B45 Labs does **not** collect your Revit or Windows username, device/hardware specs, operating-system details, or any project file contents. Your optional user profile is stored **encrypted** on your computer and synced **only if you opt in**. See [PRIVACY.md](PRIVACY.md) for full details.

---

## 📚 Documentation

| Document | Description |
|---|---|
| [TERMS.md](TERMS.md) | Terms of Use / EULA |
| [PRIVACY.md](PRIVACY.md) | Privacy Policy |
| [CHANGELOG.md](CHANGELOG.md) | Version history |
| [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md) | Open-source licenses |
| [SUPPORT.md](SUPPORT.md) | Support information |
| [SECURITY.md](SECURITY.md) | Security policy |

---

## 🆘 Support

Email: **support@b45labs.com**

When reporting issues, include: B45 Labs · Library version, Revit version and build number, steps to reproduce, timestamp and screenshot (redact sensitive details).

---

## ©️ Copyright

Copyright (c) 2026 B45 Labs. All rights reserved.
Use of this Software is governed by [TERMS.md](TERMS.md).
