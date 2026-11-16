# Changelog | B45 Labs | Library

All notable changes to B45 Labs | Library are documented here.
This project adheres to [Keep a Changelog](https://keepachangelog.com/) and
[Semantic Versioning](https://semver.org/).

## [2.0.0] – 2026-11-15

> A new glass look, tags, a search that reads inside your details, export and import of
> families, hatches and types, and a clearer Compare Detail.

### Added

- A new look for the whole Library: the glass interface. The pane, previews, tiles, chips,
  dropdowns, notifications and the settings window share one frosted-glass style, with rounded
  tables and tiles, pill-shaped tabs and toolbars, and one control height and corner radius
  everywhere. In the Plugin Theme the docked pane takes a lighter neutral gray with translucent
  cards. The large preview window follows the new look: the navigation, zoom and footer buttons
  are pill-shaped groups, the zoom box is a field you can type a percentage into, and the footer
  is a glass card with matching margins.
- Tag anything in your own words. Right-click an item or a selection, choose Tags..., type a tag
  and press Enter, then tick or clear existing tags to add or remove them on everything
  selected. Levels like mep/hvac work, and in any tab you search with #mep (which also finds
  mep/hvac) or mix it with words, like "#mep duct"; tags stay on your computer, never inside a
  Revit model.
- Search finds words inside your details, not only in their names. The Library reads what a
  detail says (its text notes, its detail components, the categories it uses and the sheet it
  sits on), so a note that says "gypsum board" is found even when the detail has another name.
  Sheets are found by the views placed on them, schedules by their field names (searching Fire
  Rating finds the schedule that reports it), filters by the categories and parameters they
  test, and view templates by their type, discipline, detail level and filters. Each result says
  why it is there, for example that the word was found in a detail note. Accents are ignored, a
  word typed in English or Portuguese also finds the other through a built-in list (parede finds
  wall) and the row shows which word stood in, and the best matches come first. In the Results
  panel a click selects the row in place, the preview and the jump to its own tab are in the
  right-click menu, and the groups collapse. It all runs on your computer and nothing is sent.
- Send a family or a hatch to a colleague. Right-click a loadable family or a hatch pattern and
  choose Export to file...: a family is saved as a .rfa and a pattern as a standard .pat. System
  families, in-place families and the Solid fill cannot be saved as a file, and the Library says
  so; a .rfa opens only in the same Revit version or a newer one. Send a wall, floor, ceiling or
  roof type as a small recipe file. Right-click the type in the System tab and choose Export to
  file...: the .b45type file carries the layers (function, thickness, material), the core
  settings, and each material's color, transparency and patterns. Importing it recreates the
  type, reuses materials and patterns that already exist by name without changing them, and
  creates the missing ones. Recipes you add to your Library are listed in the System tab with a
  section drawing of their layers, and Load or Insert creates the type in the project. Curtain,
  stacked and profile-based types, textures and rendering appearance are not carried in a
  recipe. Export saves every selected item that can be a file in one go: families as .rfa,
  hatches as .pat, and wall, floor, ceiling and roof types as recipes. You get one summary with
  a button that shows the last file, a name already taken gets (2) so nothing is overwritten,
  and a folder button opens the export folder you choose in Library settings. A new Import
  button at the top of the Library brings in a family (.rfa), a hatch (.pat) or a type recipe
  (.b45type), into the project or into your Library folder. A family already in the project is
  never replaced, and everything you import is named B45_ plus its name, unless it already
  starts with B45_; importing the same file again says Already imported instead of adding a
  copy.
- Compare Detail now tells you what changed, in words. A Changes panel beside the drawing lists
  the old and new text of an edited note or dimension, a swapped line style, what exists on one
  side only, and what moved and how far. Click a row and the drawing zooms to it; Copy as text
  copies the list. Columns keep a minimum width and each description shows on two lines. Step
  through the changes without leaving Compare Detail. The selected change has an Open view
  button that opens the detail in Revit with that element selected, and the What changed panel
  has Previous and Next buttons. A right-click on either drawing swaps it for another library
  that publishes the same detail, or for this project, and Previous and Next detail now come
  first in the toolbar. Compare Detail opens on Revit's own drawing in black and white.
  Highlight and the Changes panel start off, and stay as you set them while you step through the
  details.
- Choose which library a detail comes from. When two library files publish a detail with the
  same name, Sync Details and Check Details show a Library column, and a right-click lets you
  pick the library to compare with and sync from, compare with each library, or compare the
  libraries with each other. The default is the highest version, then the latest publish date. A
  Default library picker at the right end of the tab strip puts every detail on one library with
  a single choice, or back on Automatic (highest version). Use this library in the right-click
  menu now applies to every selected row, and your picks survive a Refresh. Check Details warns
  when a detail name lives in more than one master. A project detail with no stamp is matched to
  the library by name, so if two masters carry the same name the status bar now says how many
  names were ambiguous and the Check report lists them with the masters involved.
- Step through previews without leaving them. The Preview window has Previous and Next buttons
  (and the Left and Right arrow keys) with a counter such as 4 of 9, following the list you
  opened it from with the same search, filter and sort, and the row in the Library follows
  along, so Insert is already on the item you stopped at. The Preview window shows where the
  item lives. The footer shows the complete path of the family file, or of the model a view,
  sheet or schedule came from, shortened in the middle when it is too long, with Copy path and
  Show in folder buttons beside it.
- One right-click menu for every item in every tab. It carries the same actions as the bottom
  buttons (Load, Load & Place, Insert or Import, and Insert as copy for Filters and View
  Templates), favorites, Preview, Show source in Explorer, Copy source path, Copy name and
  Details, and Details has an Open model button that opens the source model only when you click
  it.
- Drafting Views and Groups get a Load action, in the footer and in the right-click menu, like
  Families and System. Load copies the item into the project and stops there: a drafting view is
  not opened and a group is not placed, while Insert still opens the view or starts the
  placement.
- Relocate a library folder or file that moved. Select it in Library settings and press
  Relocate, or right-click the row, and the entry keeps its place in the list. A path another
  entry already uses is refused, Texture Search Paths get the same buttons, and the right-click
  menu also offers Show source, Copy path, Move up, Move down and Remove.
- The update notice can now download and open the installer for you. Click Update, watch the
  percentage, then click Install now; the installer asks you to close Revit and finishes by
  itself. The file is checked before it runs, and if anything goes wrong, or the plug-in came
  from the Autodesk App Store, the notice opens the download page as before.
- Send Feedback is new in About Me: suggest an improvement or report a problem to the B45 Labs
  team without leaving Revit. Name, company and e-mail are optional. It always sends your
  message, the product, plug-in and Revit versions, your language and a random install ID. The
  diagnostics box is off by default and, when ticked, adds your system and the last error. Never
  your project or model files.

### Improved

- Hatch thumbnails look like Revit's own Fill Patterns dialog: black lines on white paper, every
  grid of the pattern, at Revit's scale, in a wide rectangle. Wood, Sand, Concrete and similar
  patterns that came out as gray haze or an empty square are zoomed in until the grain reads,
  and the Models and Library tabs now draw the same hatch the same way. Schedule thumbnails are
  the schedule itself, drawn from its own table: the title band, the column band and the first
  rows with their real text, on white paper. The label under the name is the category the table
  lists (Doors, Rooms, Sheets...), with the kind, such as Sheet List or Material Takeoff, beside
  it. Drafting view, sheet, legend and hatch thumbnails are shown on white paper, as Revit shows
  them, including the ones already saved in the cache. A thumbnail's thin outline is drawn above
  the picture, and solid fills no longer poke out past the rounded corners in the list view.
- The Preview of a schedule draws the table the way it looks on the sheet: white paper, the
  schedule's own font, each cell's fill, bold, italic, alignment and borders, column widths and
  row heights in sheet proportions, and the title band above. Text is still selectable and
  Ctrl+C still copies it. Pictures and merged cells that span rows are not reproduced.
- Cleaner tiles and labels in every tab. Thumbnails have rounded corners, the favorite star
  appears only on hover (a favorite keeps its gold star), names sit on one line with the full
  name in a tooltip, and the category label sits on a small gray chip under the name, in the
  gallery and in the list. Filters, View Templates, Schedules and Groups use the same wide
  thumbnail as Patterns.
- The System tab shows the family under the type name (Basic Wall, Curtain Wall, Stacked
  Wall...) and no longer has a Family column, since the category dropdown above the list already
  filters by category.
- Tabs that have not been loaded yet show a card with the tab's own icon, a title and a Load now
  button, in every tab, and the same card appears when no library folders are configured.
- A search or filter that hides every item now says so. Instead of a blank list, the tab tells
  you that nothing matches and to clear the search or filters to see all items, and Detail Sync,
  Detail Publish, Unlock Family Shared Parameters and the Family Manager explain an empty grid
  in their status bar.
- Clearing the Library cache (Clear all, Clear unused or the per-file picker) now also refreshes
  the open Library. The tabs reload from what is left and stop showing items whose cache you
  just deleted, without restarting Revit, and the reload never opens a library file or starts a
  scan.
- The Library tells you about its own releases, even with Coordination installed. It shows its
  own welcome after an update and its own announcements, its update notice no longer hides
  behind Coordination's, and every notice names its product, such as Library update available.
  Notices from several B45 products now stack in the corner of Revit instead of covering each
  other.
- Plug-in Info shows whether you are up to date for the Library, Coordination and Revit itself,
  reading Up to date or the newer version, as the Coordination window already does. When Revit
  has an update, the link opens Autodesk Access so you update from the official source.
- One language for every B45 plug-in. Change Language sets the language the plug-ins use
  together, live and without a restart, and dates follow it instead of the Windows regional
  setting. When your Revit language has no translation yet, the Library uses English and says so
  in Change Language, where you can still pick any available language. The Library follows a
  live language change. The Content Browser pane, Compare Detail, Sync Details, Check Details,
  Publish, the previews, the ribbon panel titles, the All libraries filter and closed dropdowns
  relabel on the spot, and texts that were still in English, such as rail captions, tooltips,
  scan progress and the refresh dialog, are translated. The Library tab speaks your language and
  follows your theme. Button captions, panel names, tooltips and descriptions follow the plug-in
  language, Change Theme updates the Library icons at once, and F1 works on the Theme, Canvas
  and Language buttons. If you find a mistake or an inconsistency in your own language, tell us
  with Send Feedback in About Me.
- Library settings can be minimized, maximized and left open while you work. It has the same top
  bar as the other B45 windows, keeps a single instance (a second click on the gear brings it
  back), appears in the taskbar and saves your edits when it closes. It opens about 30% wider
  and shorter, and its lower sections scroll.
- In Library settings, a library model that is no longer on disk now reads file not found,
  dimmed and in amber, instead of version unknown. The Cache section also has a checkbox to
  switch off the automatic removal of entries unused for more than N months, while Clear all and
  Clear unused still work when you press them.
- Tips & Tricks no longer blocks Revit. The window is non-modal and stays on top of Revit while
  you keep working, and clicking the button again brings the open window forward instead of
  stacking a second one.
- On Revit's start screen with no model open, the Library tab now enables About Me, My Profile,
  Change Theme, Change Language, Plug-in Settings, Tips & Tricks, Plug-in Info, Docs and
  YouTube. The Library pane and Change Canvas still need a model.
- Your initials follow your preferred name in About Me and My Profile. A preferred name of two
  or more words now gives its first and last initials instead of reading the full name first.
- A version that is too old or known to be broken is now handled by the Library itself. Below
  the minimum supported version, a window offers Exit Revit, I'll do it later or Update now each
  time Revit starts; below the blocked version there is no Later, and the Library ribbon and
  pane stay disabled until you update.

### Fixed

- The large preview no longer brings the library model in front of your project. Opening the
  preview of an item from a library model used to make Revit show that model with a tab of its
  own and send your project behind it; the preview now remembers your active document and puts
  it back as soon as the picture is ready. Refreshing no longer leaves a library model open in
  front of your project. Your project now comes back right after the render that brought the
  model forward, and the library model is closed. With no project open, a refresh skips the
  sheet, legend and drafting view thumbnails so the model cannot surface, and draws them on the
  next refresh made with a project open. Adding a file to the Library no longer opens the model.
  Adding a .rvt in Library settings, or pressing a tab's Refresh, used to scan the new model by
  opening it in front of you; the scan now always opens library models in the background.
- Remove Host no longer freezes Revit when a family cannot be converted. A refusal, such as
  components pinned to the old host plane, now shows as that family's line in the results with
  Revit's wording and what to do (set their Work Plane to a reference plane or a level), and the
  other families still convert, in the model and on disk.
- Compare Detail no longer lists changes on a detail that is up to date. When a detail had been
  inserted into a project that already had a different family with the same name, Revit renamed
  the library's copy and every component showed as a type change; Compare now reads the renamed
  copy as the library family.
- Moved now works on line-based detail components. Moving a strip such as gypsum board used to
  show as orange on one side and red on the other, never as Moved; it now paints blue in Revit's
  own drawing, and the Moved box and Highlight control it.
- Search results no longer say No matches when a tab has them. Typing a search before a tab
  finished loading left the Results panel at zero while the tab itself listed the matches; the
  panel now updates as soon as any tab finishes loading or refreshing.
- Sheets inserted from the Library no longer crop drafting views. When a drafting view had no
  crop, the copy got one invented from its elements and large parts at the edges of a detail
  could be cut off; the copy now keeps the source's crop, or none.
- The Groups tab's kind filter works again. Its second dropdown, which should offer All, Model
  Groups and Detail Groups, showed blank and could not be used.
- Right-click submenus in Check Details and Compare Detail are readable in the dark theme. Use
  this library, Compare with and the left and right drawing submenus used to open as a light
  popup with light text.
- The Library now notices its own updates. Version 1.2.0 showed a long code after its number in
  the Welcome window, which kept it from recognizing a newer version, and a date check that
  always failed stopped the check before it finished. The version now reads cleanly and update
  notices can appear.
- Dropdowns inside table rows no longer flash white on hover. In Publish to Detail Library,
  Unlock Family Shared Parameters and the Family Manager the hover now uses the row's tint and
  stands down on a selected row, and the chevron and text on a selected row are white and
  readable on the blue.
- My Profile now shows its messages. Saved, Draft restored and the export messages were set but
  never displayed; the footer now shows them, and the required-fields note when there is nothing
  else to say.
- Compare Detail opens centered over the Revit window instead of half on a second monitor, the
  same way the Sync window does.

### Notes

- The first Library refresh after updating re-reads each library file once more, because the
  hatch and schedule thumbnails are redrawn. A large library can take a few minutes the first
  time.
- Library 1.2.0 and older cannot recognize a newer version, so the app will not announce this
  update to them. Download v2.0.0 from the website.
- Export saves to Documents\B45 Labs\Library Exports unless you choose another folder in Library
  settings.
- Full support: Revit 2023, 2024, 2025, 2026 and 2027

---

## [1.2.0] – 2026-10-01

> A search that reads the drawing and speaks two languages, Compare Detail, a Schedules tab, a
> real preview for details, sheets and families in 3D, Remove Host and Unlock Parameters on
> family files, and Tips & Tricks.

### Added

- The search reads the drawing, not just its name. Type "CMU" and you get the detail whose note
  says 8" CMU BLOCK. Every detail is indexed by the text written inside it, the detail components
  it places, the sheet it sits on and the categories it contains, and each result says why it
  appeared.
- One search box, all results, grouped. A Results pill lists every match in the section you are
  in, Models or Library, grouped by tab and with thumbnails. Click a row to select it, right-click
  to preview it or jump to its tab, and fold away any group you do not need.
- The search forgives punctuation and typing: "cmu" finds C.M.U., "a501" finds A-501, quotes
  search for a phrase, one wrong letter is forgiven with the results marked as approximate, and
  an "ab" button requires whole words.
- The detail search speaks both languages and puts the best match first. Type "parede" and you
  get the details annotated WALL; type "wall" and you get the ones annotated PAREDE. It knows the
  common drawing vocabulary in English and Portuguese and says when it used it ("Synonym: wall"),
  and quotes search for exactly what you typed. Accents no longer matter, and results are ordered
  by relevance: a detail named for what you typed comes before one that only mentions it in a
  note. No AI and no internet involved.
- Compare Detail: compare the details used in the open project with the approved, published
  details in the Library and see exactly what differs, in Revit's own drawing. Three views (side
  by side, overlaid and a swipe), a Highlight button that colours the differences, a legend whose
  checkboxes work as layers, Previous and Next to step through the list, and a Sync detail
  button that brings the approved version into your project without leaving the comparison.
- Schedules tab: a new tab on both the Models and Library sides lists schedules, key schedules,
  material takeoffs, sheet lists, view lists and note blocks with their category and field count.
  Insert copies the schedule into your project, renames it on a name clash and reports any column
  that could not come across, and Preview shows the whole table as text you can select and copy.
- A real preview for details, legends and sheets. Right-click and choose Preview: it opens in its
  own window, large enough to read the notes, with zoom, pan, Fit and 100%.
- Families get the large preview too, and it turns in 3D. Right-click a family and choose Preview
  to see it far larger than the grid thumbnail, then press 3D to orbit it: middle-drag turns the
  family, left-drag pans and the wheel zooms. Families that never had a thumbnail (profiles,
  detail items, title blocks, annotations) now get a real preview. The preview opens in the
  standard isometric view, and the 3D button appears only where a family can actually be
  orbited.
- Family Manager · Remove Host works on family files on disk. Add .rfa files or a whole folder,
  then save a copy next to each original, copies in a folder you pick, or over the originals.
  Every file is checked after conversion.
- Family Manager · Unlock Parameters works on family files too, with the same three ways to save,
  and can load the unlocked families into the open model.
- Family Manager · Unlock Parameters can delete family parameters. Select them and press Delete:
  the rows turn red, the removal runs in the same Apply as the unlock after a confirmation, and a
  parameter Revit will not let go (built-in, used by a formula or by a dimension label) is
  refused with the reason.
- Tips & Tricks: a new first button in the Help panel with short videos, articles, product news
  and the whole B45 Labs suite, updated from b45labs.com.

### Improved

- My Profile: User Profile has a friendlier name, a new switch decides whether B45 Labs mentions
  its other products, and the export accent colour gains a swatch and a Pick button that opens
  the Windows colour picker.
- The Library settings window opens at once. It used to freeze for up to seventeen seconds when a
  library path sat on a sleeping network or external drive.
- Check Details and Sync Details open immediately and show their progress in three phases,
  instead of appearing only after the whole library had been read. Right-click a row and choose
  Open view to jump to that view in Revit.
- One look for every notification, anchored to the Revit window instead of the corner of the
  screen.
- Refreshing a library that is already read shows its progress and a completion notice, however
  quick it is, so you can tell the click worked.
- The Library follows Revit's theme by default, and its dark tones match the Revit panels it
  docks beside.
- Everything added in this release was reviewed in Portuguese, Spanish, French and Russian, and
  thirteen strings that had stayed in English are translated.

### Fixed

- The Library stopped re-reading itself. Browsing a library re-opened every library file and
  re-drew every preview on each refresh; on a network drive that was around twenty minutes of
  frozen Revit. A library is now read once and served from its saved copy.
- Inserting a detail no longer re-reads the whole library afterwards, and no longer opens the
  library model in front of you.
- Categories are named the way Revit names them. Tag categories no longer disappear into a single
  Annotation row, and the grid column and the dropdown always agree.
- The side rail keeps the tab you had open.
- The first-scan warning no longer appears in every session when a library file sits on a drive
  that is unplugged, and the content of that file stays listed from its last scan.
- The note at the bottom of the Library settings window is readable in the light theme.
- Maximized windows spilled past the work area, and the maximize button went blank in Check
  Details and Unlock Family Parameters.
- The highlighted item in the Family Manager's dropdowns and right-click menu showed dark text on
  the blue selection in the light theme.
- Preview images were left behind in the temp folder after every session.
- The About window's copyright line named a company that does not exist.

### Platform
- The first Library refresh after updating reads each library file once more, because the search
  index changed.
- Full support: Revit 2023, 2024, 2025, 2026 and 2027.

---

## [1.1.1] – 2026-08-08

> Repairs 1.1.0: Excel export could fail on Revit 2023 and 2024 with a missing-assembly error,
> the Light theme showed dark-theme colours on status text, and families outside the curated
> category list showed as "Uncategorized".

### Fixed

- **Excel export could fail on Revit 2023 and 2024.** The App Store security pins moved bundled
  Microsoft libraries to newer versions, and .NET Framework does not roll forward across a
  version change: the first Excel export could ask for an older library identity and be refused.
  The add-in now supplies the matching copy itself, for every library in the payload whose
  requested version differs from the one shipped beside it, the same repair Coordination v2.1.1
  applies to its PDF path. Revit 2025 and newer were never affected.
- **Status and state colours now come from the theme palette**, so Revit's Light theme no longer
  shows dark-theme colours that were unreadable on a light background.
- **Families outside the curated category list no longer show as "Uncategorized".** The Library tab
  now displays the category read from the family file itself and falls back to the curated grouping
  only when the file does not carry one. Sorting follows the name on screen.

### Improved

- When a family file cannot be read for its thumbnail, the message now names the exact file
  instead of a generic error.

### Platform
- Full support: Revit 2023, 2024, 2025, 2026, and 2027.

---

## [1.1.0] – 2026-08-02

> Showrooms scoped to their Revit version, categories that come from the family instead of the
> folder, a Load button that does not place, contextual F1 help, and a pane that no longer makes
> you wait minutes.

### Added
- **Load**: a new action beside **Load & Place** on both family tabs and on the System tab:
  bring a family or a system type into your project without placing it or starting a draw
  command. The old primary action was renamed from "Insert" to "Load & Place" to tell the two
  apart.
- **Showrooms are scoped to their Revit version**: a library model is listed only in the version
  it was saved in, so Revit 2024 no longer offers the contents of a 2026 showroom it cannot open.
  Folders and family files stay shared across every version. The settings list still shows every
  entry, with a colour-coded badge naming its version (green for the Revit you are running, amber
  otherwise) so an entry saved elsewhere can still be removed, and the status line reports how
  many entries were hidden and why.
- **Contextual F1 help**: press F1 in any Library window (the pane, Family Manager, Unlock
  Family Parameters, Detail Publish, Detail Sync, the settings and cache windows) and the
  matching documentation page opens. It also works **inside the docked pane itself**, which had
  no help at all, and stays Revit's F1 everywhere outside the pane.
- **Type-ahead in every list**: click a list and start typing to jump to the matching row.
- **Completion notifications with counts**: Unlock Family Parameters, all five Family Manager
  actions, Detail Publish and Detail Sync now confirm what they did instead of finishing quietly.
- **Result dialogs** gained a copy-to-clipboard button, plus **Open file** and **Show in folder**
  whenever the operation produced a file. Family Manager's Export report points straight at the
  exported families.
- **User Profile · Export Branding**: set your company name, accent colour and logo once; the
  brand is stored in a shared place, so both B45 products use it on the files they generate.
- **Plug-in Info**: an update-available badge appears when a newer Library release is published.
- **Detail Library**: a tri-state select-all in the header of both the Drafting Views and
  Legends grids, and the Check Details result became a styled Excel export with one worksheet per
  kind, replacing a plain-text dialog dump.
- **Hydrate Tabs**: a button that fills every tab from the local cache on demand, now that tabs
  no longer fill themselves at startup.
- **Navigation rail**: drag it to resize between 40 and 80 pixels; the content adapts.

### Changed
- **"Content Browser" is now "Library"** everywhere in the interface: the pane title, 23 dialog
  captions across 12 screens, the ribbon tooltip and description, the cache settings text, the
  onboarding copy and the installer welcome, in all five languages.
- **The pane carries a brand letterhead**, and the B45 logo lockup was rolled out across every
  Library window and dialog, the progress popups included.
- **Ribbon**: "B45 Labs / Website" is now **Docs** (the command always opened the docs site),
  the "Revit Settings" panel is now **Settings**, and Change Theme, Change Canvas and Change
  Language became one compact icon-only stacked column.
- **Refresh**: the progress bar now advances through the whole scan, reporting every phase and
  every rendered sheet, legend and detail, instead of sitting empty and jumping straight to
  complete. It ends in a notification instead of a blocking dialog that stole focus long after
  you had moved on.
- **Notifications**: progress and completion share one corner of the monitor running Revit, in
  one visual language, and the progress card shows a percent readout. They also appear on the
  monitor running Revit rather than always the primary display.
- **Tabs no longer fill themselves** when Revit starts, when a model opens, or when the pane is
  shown; each tab offers a "Load now" prompt until you ask for it.
- **Modern folder picker on Revit 2023 and 2024**: choosing a library folder or a texture search
  path used to fall back to the old tree-only box with no address bar; all five versions now get
  the picker where a path can be typed or pasted.
- **Small screens** start with the icon-only left rail so the stacked icons no longer overflow;
  the splitter still lets you widen it.
- **Generated files** now use the shared `B45_` name prefix, so exports group together in your
  Downloads folder.
- **Detail Library**: a Refresh that has to open external documents no longer steals your active
  view; it keeps its progress window and leaves you where you were.
- **Library & Texture Settings**: pressing ESC closes and saves, matching Done and the X.
- **Translations**: 227 strings per language were added, covering the Detail Library Sync and
  Publish windows (grid cells and status text included), the notifications and scattered dialog
  titles. The language picker states that the non-English languages are beta.
- **Downloads**: the About window's Releases button and the built-in fallback now point at the
  B45 Labs download page; the two links previously pointed at two different accounts, one wrong.
- **Sign-ups and profiles are attributed to Library** rather than defaulting to Coordination.
- **Uninstall**: now also removes the shared program data folder once no other B45 product
  remains installed.
- **Ribbon**: the Unlock Family Parameters button was removed; the feature itself lives on
  inside Family Manager.
- **About Me**: the biography was rewritten with the real career narrative, in all languages.

### Fixed
- **Categories come from the family, not the folder**: every subfolder of your library used to
  appear in the category dropdown as if it were a Revit category, so the same content showed up
  twice. Folder names already written into the index survived the first fix, because a cached
  item skipped the re-read that would have corrected it; the index is now rebuilt once and
  self-corrects from then on. A library authored across differently-localized Revit installs no
  longer lists the same category twice, and a family whose category was known no longer shows as
  "(Uncategorized)" in the filter while the grid shows the real name.
- **"No families found"** is no longer stamped over a grid that is full of families.
- **Refresh no longer hijacks your session**: a library model surfaced during a scan could stay
  open and focused for the rest of the session; the pane now asks Revit which document is
  actually active before restoring your view, and reports a failed close by name.
- **A wrong download destination**: the update channel could accept a manifest pointing at the
  Coordination download; it is now rejected.
- **F1**: pressing it used to open the B45 page *and* Autodesk's Revit help on top of it.
- **Plug-in Info**: the window no longer clips its content; it is taller and scrolls.
- **Thumbnails**: the preview column was squeezed and clipped when the Family column competed
  for space; thumbnails keep their width, including after switching tabs.
- **Welcome window**: no longer shows a stale, hard-coded version number.
- **Language picker**: the primary button border renders correctly again.
- **Dropdowns**: long lists no longer cut off their last item.

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
- **Revit startup**: Library no longer rehydrates roughly 108 MB of disk cache or rescans the
  freshly opened document at boot, and the usage database no longer initialises on the startup
  path (measured at 65-88% of the add-in's startup cost).
- **Refresh**: progress reporting is throttled to whole-percent changes, so a detail library
  raising thousands of reports does not spend more time reporting than rendering.

### Security
- **User Profile**: your personal profile data is now encrypted at rest on your machine, and
  decrypted only when syncing or exporting it.
- Updated the bundled Microsoft runtime libraries to their latest secure versions, following the
  Autodesk App Store security review.

### Platform
- Full support: Revit 2023, 2024, 2025, 2026, and 2027.

## [1.0.3] – 2026-07-20

> A refined interface, sharper Content Browser thumbnails, and a more reliable Family Manager.

### Changed
- **Interface refresh**: cleaner, more consistent buttons and dialogs across the whole Library,
  tuned for both dark and light themes (shared B45 design system).
- **About Me**: Contact is now the primary action.

### Fixed
- **Content Browser**: thumbnails size correctly on every tab, with no clipping at larger sizes.
- **Family Manager**: reliability fixes, with reworked Unlock Parameters and Remove Host
  (unhost family) logic.
- **Light theme**: button-border and text legibility fixes carried from the shared design system.

## [1.0.2] – 2026-07-12

> Apple-style toasts and a faster, smarter Content Browser scan.

### Added
- **Apple-style notifications**: routine messages now appear as clean, non-blocking toasts in the
  corner of Revit, matching Coordination's new toast system.
- **Faster Content Browser scan**: an in-memory scan cache with document-change invalidation, so
  re-scanning within a session reuses prior results instead of re-reading unchanged models.

### Changed
- **Detail Sync**: fixed the selection count that blocked "Sync Selected," and added a "Needs
  adoption" state that closes a silent-overwrite path, a foreground/background scan mode, and correct
  selection theming.
- **Family Manager · Remove Host**: reliable host removal (including already-unhosted families),
  category-swap support (Generic Model / Casework), pick-from-canvas selection, and grid horizontal
  scroll.
- **Content Browser**: honest Refresh (only prompts when it will open external files; no false "run
  in background"), a wider Type column, and an auto-hidden redundant Category column.
- **Library ribbon**: a Visible Modules dropdown matching Coordination, with a two-line caption.

### Platform
- Full support: Revit 2023, 2024, 2025, 2026, and 2027.

## [1.0.1] – 2026-07-10

> A hotfix release polishing the initial Library launch.

### Changed
- **Content Browser**: a new "used elements only" filter, and faster cache-first startup: loads from
  cache and hydrates when the pane opens, with no network wait.
- **Family Manager**: "Adjust selection" and "Replace" now act on the checked rows, plus Remove Host,
  category scoping, and tri-state fixes.
- **Settings**: embedded Change Theme / Canvas / Language button icons; About wiring fix.

### Fixed
- More reliable theme and language sync; survives a stale co-installed shared component.

### Platform
- Full support: Revit 2023, 2024, 2025, 2026, and 2027.

## [1.0.0] – 2026-07-08

> **Introducing B45 Labs · Library**: a content and family powerhouse that lives inside Revit.
> Browse and load anything from a single family to a whole sheet, manage families in bulk, and keep
> a shared detail library in sync across every project. This is the first full release of Library as
> its own product, installable and usable on its own, alongside B45 Labs · Coordination.

Library ships as a **fully standalone product**: its own ribbon tab, its own telemetry, and its own
theme, with three tools at its core: **Content Browser**, **Family Manager**, and **Detail Library**.

### Content Browser

A dockable pane to browse, preview, and load content into your model, from two sources (**your open
models** and **your external libraries**), each with the same rich set of tabs:

- **Families**: browse loadable families, search and filter by category, preview thumbnails, and
  insert one or many at a time with chained placement. External `.rfa`/`.rte` libraries are scanned
  from folders you configure and opened in the background, no manual file-opening.
- **System types**: Walls, Floors, Ceilings, Roofs, Pipes, Ducts and more, with a **Smart Insert**
  that either applies the type to your current selection or launches Revit's native draw tool.
- **Materials**: browse by class (Concrete, Wood, Glass, Metal…) and import across documents, with
  automatic rename-on-collision and a texture-path fallback so bitmaps resolve on any machine.
- **Patterns**: drafting and model fill patterns, imported with auto-rename.
- **Drafting Views, Legends, Sheets, and Groups**: cross-document insert of drafting views, legends,
  whole sheets (via the Copy Sheet From Model engine), and model/detail groups with interactive
  placement. Sheets can be filtered by your Project Browser organization.
- **Across every tab:** global search with per-section result counts, universal **Favorites** and
  **Recents**, list or grid layout, four thumbnail sizes (32–128 px), and a layout that adapts down to
  a narrow dock. A **persistent on-disk thumbnail cache** makes the Library open near-instantly instead
  of re-scanning your folders on every launch. Multi-select + batch insert throughout.

### Family Manager

A modeless tool to manage families in bulk, across four tabs (filter by category, search, and
multi-select everywhere):

- **Unlock Family Parameters**: find every locked family parameter (with the reason it's locked), then
  batch-unlock the ones you choose (keep the value, clear the formula, or replace it) and reload the
  families into your project. Pick a family straight from the canvas; per-session undo/redo.
- **Rename**: an accumulating staging buffer: layer Find/Replace (regex), prefix/suffix, and casing
  rules, previewing every proposed name with per-row validation and conflict blocking before you Apply.
  Target families, types, or both.
- **Parameters**: batch-add shared parameters (pick file → group → parameter, choose Instance or Type
  binding and the target group), remove parameters by name, and queue several operations before applying
  them in one pass.
- **Export**: export the selected families to `.rfa`, flat or organized into per-category folders.

### Detail Library

Publish, standardize, and reuse your details across every project:

- **Publish** drafting views and legends to a master library, with automatic or manual version control
  and content-change detection.
- **Check** and **Sync**: audit your project's details against the master and pull the latest, with a
  clear state for each (Up to date, Outdated, Locally modified, Unversioned, Orphan). **Promote** a
  corrected detail back up to the master as a new version.
- Details are tracked by a **stable GUID + content hash**, not by name, so a rename never breaks the
  link, drift is caught automatically, and an unversioned detail adopts into the library when its name
  matches a master. Master libraries are auto-discovered from your configured paths.
- Detail swapping is reliable across **Revit 2023–2027** (a Revit 2026 view-copy edge case that
  previously blocked swaps was resolved for this release).

### A standalone product

- Installed on its own, Library builds its own **`B45 Labs · Library` ribbon tab**: a **Main** panel
  (About Me, User Profile), the **Library** panel (Content Browser, Unlock Family Parameters), and a
  **Help** panel (Plug-in Info, B45 Labs Website, YouTube Tutorials). When B45 Labs · Coordination or
  Production is installed, Library appears as a panel on that product's tab instead.
- **Its own telemetry** (consent-based, opt-out), **its own theme** that follows Revit's light/dark UI in
  real time, and full **Export / Erase my data** support.
- **Full support for Revit 2023, 2024, 2025, 2026, and 2027.**
- Interface languages: **English**, plus **Português (BR), Español, Français, and Русский as BETA**
  (AI-assisted drafts pending native review, tell us where they can be better at support@b45labs.com).

### Notes

- Library installs and updates as its **own product**, side by side with B45 Labs · Coordination.
- Parts of Library appeared earlier in preview inside Coordination; **v1.0.0 is the first full,
  standalone release** of Library as its own product.
