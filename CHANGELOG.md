# Changelog — B45 Labs | Library

All notable changes to B45 Labs | Library are documented here.
This project adheres to [Keep a Changelog](https://keepachangelog.com/) and
[Semantic Versioning](https://semver.org/).

## [1.0.0] – 2026-07-08

> **Introducing B45 Labs · Library** — a content and family powerhouse that lives inside Revit.
> Browse and load anything from a single family to a whole sheet, manage families in bulk, and keep
> a shared detail library in sync across every project. This is the first full release of Library as
> its own product — installable and usable on its own, alongside B45 Labs · Coordination.

Library ships as a **fully standalone product** — its own ribbon tab, its own telemetry, and its own
theme — with three tools at its core: **Content Browser**, **Family Manager**, and **Detail Library**.

### Content Browser

A dockable pane to browse, preview, and load content into your model — from two sources (**your open
models** and **your external libraries**), each with the same rich set of tabs:

- **Families** — browse loadable families, search and filter by category, preview thumbnails, and
  insert one or many at a time with chained placement. External `.rfa`/`.rte` libraries are scanned
  from folders you configure and opened in the background — no manual file-opening.
- **System types** — Walls, Floors, Ceilings, Roofs, Pipes, Ducts and more, with a **Smart Insert**
  that either applies the type to your current selection or launches Revit's native draw tool.
- **Materials** — browse by class (Concrete, Wood, Glass, Metal…) and import across documents, with
  automatic rename-on-collision and a texture-path fallback so bitmaps resolve on any machine.
- **Patterns** — drafting and model fill patterns, imported with auto-rename.
- **Drafting Views, Legends, Sheets, and Groups** — cross-document insert of drafting views, legends,
  whole sheets (via the Copy Sheet From Model engine), and model/detail groups with interactive
  placement. Sheets can be filtered by your Project Browser organization.
- **Across every tab:** global search with per-section result counts, universal **Favorites** and
  **Recents**, list or grid layout, four thumbnail sizes (32–128 px), and a layout that adapts down to
  a narrow dock. A **persistent on-disk thumbnail cache** makes the Library open near-instantly instead
  of re-scanning your folders on every launch. Multi-select + batch insert throughout.

### Family Manager

A modeless tool to manage families in bulk, across four tabs (filter by category, search, and
multi-select everywhere):

- **Unlock Family Parameters** — find every locked family parameter (with the reason it's locked), then
  batch-unlock the ones you choose (keep the value, clear the formula, or replace it) and reload the
  families into your project. Pick a family straight from the canvas; per-session undo/redo.
- **Rename** — an accumulating staging buffer: layer Find/Replace (regex), prefix/suffix, and casing
  rules, previewing every proposed name with per-row validation and conflict blocking before you Apply.
  Target families, types, or both.
- **Parameters** — batch-add shared parameters (pick file → group → parameter, choose Instance or Type
  binding and the target group), remove parameters by name, and queue several operations before applying
  them in one pass.
- **Export** — export the selected families to `.rfa`, flat or organized into per-category folders.

### Detail Library

Publish, standardize, and reuse your details across every project:

- **Publish** drafting views and legends to a master library, with automatic or manual version control
  and content-change detection.
- **Check** and **Sync** — audit your project's details against the master and pull the latest, with a
  clear state for each (Up to date, Outdated, Locally modified, Unversioned, Orphan). **Promote** a
  corrected detail back up to the master as a new version.
- Details are tracked by a **stable GUID + content hash**, not by name — so a rename never breaks the
  link, drift is caught automatically, and an unversioned detail adopts into the library when its name
  matches a master. Master libraries are auto-discovered from your configured paths.
- Detail swapping is reliable across **Revit 2023–2027** (a Revit 2026 view-copy edge case that
  previously blocked swaps was resolved for this release).

### A standalone product

- Installed on its own, Library builds its own **`B45 Labs · Library` ribbon tab** — a **Main** panel
  (About Me, User Profile), the **Library** panel (Content Browser, Unlock Family Parameters), and a
  **Help** panel (Plug-in Info, B45 Labs Website, YouTube Tutorials). When B45 Labs · Coordination or
  Production is installed, Library appears as a panel on that product's tab instead.
- **Its own telemetry** (consent-based, opt-out), **its own theme** that follows Revit's light/dark UI in
  real time, and full **Export / Erase my data** support.
- **Full support for Revit 2023, 2024, 2025, 2026, and 2027.**
- Interface languages: **English**, plus **Português (BR), Español, Français, and Русский as BETA**
  (AI-assisted drafts pending native review — tell us where they can be better at support@b45labs.com).

### Notes

- Library installs and updates as its **own product**, side by side with B45 Labs · Coordination.
- Parts of Library appeared earlier in preview inside Coordination; **v1.0.0 is the first full,
  standalone release** of Library as its own product.
