# Changelog — B45 Labs | Library

All notable changes to B45 Labs | Library are documented here.
This project adheres to [Keep a Changelog](https://keepachangelog.com/) and
[Semantic Versioning](https://semver.org/).

## [1.1.0] – 2026-08-02

> Showrooms scoped to their Revit version, categories that come from the family instead of the
> folder, a Load button that does not place, contextual F1 help, and a pane that no longer makes
> you wait minutes.

### Added
- **Load** — a new action beside **Load & Place** on both family tabs and on the System tab:
  bring a family or a system type into your project without placing it or starting a draw
  command. The old primary action was renamed from "Insert" to "Load & Place" to tell the two
  apart.
- **Showrooms are scoped to their Revit version** — a library model is listed only in the version
  it was saved in, so Revit 2024 no longer offers the contents of a 2026 showroom it cannot open.
  Folders and family files stay shared across every version. The settings list still shows every
  entry, with a colour-coded badge naming its version (green for the Revit you are running, amber
  otherwise) so an entry saved elsewhere can still be removed, and the status line reports how
  many entries were hidden and why.
- **Contextual F1 help** — press F1 in any Library window (the pane, Family Manager, Unlock
  Family Parameters, Detail Publish, Detail Sync, the settings and cache windows) and the
  matching documentation page opens. It also works **inside the docked pane itself**, which had
  no help at all, and stays Revit's F1 everywhere outside the pane.
- **Type-ahead in every list** — click a list and start typing to jump to the matching row.
- **Completion notifications with counts** — Unlock Family Parameters, all five Family Manager
  actions, Detail Publish and Detail Sync now confirm what they did instead of finishing quietly.
- **Result dialogs** gained a copy-to-clipboard button, plus **Open file** and **Show in folder**
  whenever the operation produced a file. Family Manager's Export report points straight at the
  exported families.
- **User Profile · Export Branding** — set your company name, accent colour and logo once; the
  brand is stored in a shared place, so both B45 products use it on the files they generate.
- **Plug-in Info** — an update-available badge appears when a newer Library release is published.
- **Detail Library** — a tri-state select-all in the header of both the Drafting Views and
  Legends grids, and the Check Details result became a styled Excel export with one worksheet per
  kind, replacing a plain-text dialog dump.
- **Hydrate Tabs** — a button that fills every tab from the local cache on demand, now that tabs
  no longer fill themselves at startup.
- **Navigation rail** — drag it to resize between 40 and 80 pixels; the content adapts.

### Changed
- **"Content Browser" is now "Library"** everywhere in the interface: the pane title, 23 dialog
  captions across 12 screens, the ribbon tooltip and description, the cache settings text, the
  onboarding copy and the installer welcome, in all five languages.
- **The pane carries a brand letterhead**, and the B45 logo lockup was rolled out across every
  Library window and dialog, the progress popups included.
- **Ribbon** — "B45 Labs / Website" is now **Docs** (the command always opened the docs site),
  the "Revit Settings" panel is now **Settings**, and Change Theme, Change Canvas and Change
  Language became one compact icon-only stacked column.
- **Refresh** — the progress bar now advances through the whole scan, reporting every phase and
  every rendered sheet, legend and detail, instead of sitting empty and jumping straight to
  complete. It ends in a notification instead of a blocking dialog that stole focus long after
  you had moved on.
- **Notifications** — progress and completion share one corner of the monitor running Revit, in
  one visual language, and the progress card shows a percent readout. They also appear on the
  monitor running Revit rather than always the primary display.
- **Tabs no longer fill themselves** when Revit starts, when a model opens, or when the pane is
  shown; each tab offers a "Load now" prompt until you ask for it.
- **Modern folder picker on Revit 2023 and 2024** — choosing a library folder or a texture search
  path used to fall back to the old tree-only box with no address bar; all five versions now get
  the picker where a path can be typed or pasted.
- **Small screens** start with the icon-only left rail so the stacked icons no longer overflow;
  the splitter still lets you widen it.
- **Generated files** now use the shared `B45_` name prefix, so exports group together in your
  Downloads folder.
- **Detail Library** — a Refresh that has to open external documents no longer steals your active
  view; it keeps its progress window and leaves you where you were.
- **Library & Texture Settings** — pressing ESC closes and saves, matching Done and the X.
- **Translations** — 227 strings per language were added, covering the Detail Library Sync and
  Publish windows (grid cells and status text included), the notifications and scattered dialog
  titles. The language picker states that the non-English languages are beta.
- **Downloads** — the About window's Releases button and the built-in fallback now point at the
  B45 Labs download page; the two links previously pointed at two different accounts, one wrong.
- **Sign-ups and profiles are attributed to Library** rather than defaulting to Coordination.
- **Uninstall** — now also removes the shared program data folder once no other B45 product
  remains installed.
- **Ribbon** — the Unlock Family Parameters button was removed; the feature itself lives on
  inside Family Manager.
- **About Me** — the biography was rewritten with the real career narrative, in all languages.

### Fixed
- **Categories come from the family, not the folder** — every subfolder of your library used to
  appear in the category dropdown as if it were a Revit category, so the same content showed up
  twice. Folder names already written into the index survived the first fix, because a cached
  item skipped the re-read that would have corrected it; the index is now rebuilt once and
  self-corrects from then on. A library authored across differently-localized Revit installs no
  longer lists the same category twice, and a family whose category was known no longer shows as
  "(Uncategorized)" in the filter while the grid shows the real name.
- **"No families found"** is no longer stamped over a grid that is full of families.
- **Refresh no longer hijacks your session** — a library model surfaced during a scan could stay
  open and focused for the rest of the session; the pane now asks Revit which document is
  actually active before restoring your view, and reports a failed close by name.
- **A wrong download destination** — the update channel could accept a manifest pointing at the
  Coordination download; it is now rejected.
- **F1** — pressing it used to open the B45 page *and* Autodesk's Revit help on top of it.
- **Plug-in Info** — the window no longer clips its content; it is taller and scrolls.
- **Thumbnails** — the preview column was squeezed and clipped when the Family column competed
  for space; thumbnails keep their width, including after switching tabs.
- **Welcome window** — no longer shows a stale, hard-coded version number.
- **Language picker** — the primary button border renders correctly again.
- **Dropdowns** — long lists no longer cut off their last item.

### Performance
- **The Settings dialog took about five minutes to open** on a cold scan, because the whole
  library index was being rewritten every 2.5 seconds on the interface thread. The write now
  happens once, when the scan finishes.
- **It then still took about two minutes**, because the family list was rebuilt and repainted
  once per family as results arrived. The refresh is now coalesced, so the list settles at two to
  three repaints per second.
- **Opening Settings no longer re-probes** the remembered Revit version of every library model,
  and version scoping means models from another Revit version are never opened during Detail Sync
  probing.
- **Revit startup** — Library no longer rehydrates roughly 108 MB of disk cache or rescans the
  freshly opened document at boot, and the usage database no longer initialises on the startup
  path (measured at 65-88% of the add-in's startup cost).
- **Refresh** — progress reporting is throttled to whole-percent changes, so a detail library
  raising thousands of reports does not spend more time reporting than rendering.

### Security
- **User Profile** — your personal profile data is now encrypted at rest on your machine, and
  decrypted only when syncing or exporting it.
- Updated the bundled Microsoft runtime libraries to their latest secure versions, following the
  Autodesk App Store security review.

### Platform
- Full support: Revit 2023, 2024, 2025, 2026, and 2027.

## [1.0.3] – 2026-07-20

> A refined interface, sharper Content Browser thumbnails, and a more reliable Family Manager.

### Changed
- **Interface refresh** — cleaner, more consistent buttons and dialogs across the whole Library,
  tuned for both dark and light themes (shared B45 design system).
- **About Me** — Contact is now the primary action.

### Fixed
- **Content Browser** — thumbnails size correctly on every tab, with no clipping at larger sizes.
- **Family Manager** — reliability fixes, with reworked Unlock Parameters and Remove Host
  (unhost family) logic.
- **Light theme** — button-border and text legibility fixes carried from the shared design system.

## [1.0.2] – 2026-07-12

> Apple-style toasts and a faster, smarter Content Browser scan.

### Added
- **Apple-style notifications** — routine messages now appear as clean, non-blocking toasts in the
  corner of Revit, matching Coordination's new toast system.
- **Faster Content Browser scan** — an in-memory scan cache with document-change invalidation, so
  re-scanning within a session reuses prior results instead of re-reading unchanged models.

### Changed
- **Detail Sync** — fixed the selection count that blocked "Sync Selected," and added a "Needs
  adoption" state that closes a silent-overwrite path, a foreground/background scan mode, and correct
  selection theming.
- **Family Manager · Remove Host** — reliable host removal (including already-unhosted families),
  category-swap support (Generic Model / Casework), pick-from-canvas selection, and grid horizontal
  scroll.
- **Content Browser** — honest Refresh (only prompts when it will open external files; no false "run
  in background"), a wider Type column, and an auto-hidden redundant Category column.
- **Library ribbon** — a Visible Modules dropdown matching Coordination, with a two-line caption.

### Platform
- Full support: Revit 2023, 2024, 2025, 2026, and 2027.

## [1.0.1] – 2026-07-10

> A hotfix release polishing the initial Library launch.

### Changed
- **Content Browser** — a new "used elements only" filter, and faster cache-first startup: loads from
  cache and hydrates when the pane opens, with no network wait.
- **Family Manager** — "Adjust selection" and "Replace" now act on the checked rows, plus Remove Host,
  category scoping, and tri-state fixes.
- **Settings** — embedded Change Theme / Canvas / Language button icons; About wiring fix.

### Fixed
- More reliable theme and language sync; survives a stale co-installed shared component.

### Platform
- Full support: Revit 2023, 2024, 2025, 2026, and 2027.

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
