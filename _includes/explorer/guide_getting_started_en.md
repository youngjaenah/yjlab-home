# Getting Started with Explorer for Mac

Explorer for Mac brings the Windows 11 File Explorer layout to macOS: a folder tree on the left, tabs across the top, an editable address bar, and a Details view with sortable columns. This guide walks you through installing the app, finding your way around the window, and the tasks you'll do every day.

Everything described here is free. For the full list of keys, see [Keyboard Shortcuts](/explorer/guide/shortcuts/?lang=en).

## 1. Install and first launch

Explorer for Mac requires macOS 14 Sonoma or later and runs on both Apple Silicon and Intel Macs.

1. Download the DMG from the [Explorer for Mac page](/explorer/?lang=en) and open it.
2. Drag the **Explorer** icon onto the **Applications** folder.
3. Open Explorer from Applications or Launchpad.

If you launch Explorer straight from the disk image, it offers to move itself into Applications. Accept the offer, because in-app updates can't work from a disk image.

### Folder access prompts

Explorer has no setup wizard or permission dialog of its own. Your home folder and drives can be browsed right away. macOS protects some locations, though:

- The first time you open **Desktop**, **Documents**, or **Downloads**, or a network volume, macOS shows its own prompt asking whether Explorer may access it. Click **Allow**. macOS remembers your answer.
- If you clicked **Don't Allow**, the folder shows a short explanation and an **Open Privacy Settings…** button instead of its contents. Turn Explorer back on in **System Settings ▸ Privacy & Security** and the folder lists normally again.
- Some system areas, such as `~/Library` and the Trash, can only be read in full when Explorer has **Full Disk Access** (**System Settings ▸ Privacy & Security ▸ Full Disk Access**). This is optional; without it, sizes for those folders show "—".

### Updates

Choose **Explorer ▸ Check for Updates…** to update at any time. Automatic checks can be turned off in **Settings ▸ Updates**.

## 2. A tour of the window

### Sidebar

The left sidebar works like Windows' navigation pane and is always visible:

- **Home**: a landing page with your **Favorites**, **Recent locations** (the folders you visited most recently), and **Drives**. A new window with nothing to restore opens here.
- **Gallery**: the photos and videos in your chosen folders as a thumbnail grid, newest first. Pictures is the default source. Use **Add Source…** in the Gallery's source menu to include more folders.
- **Favorites**: Desktop, Downloads, Documents, Pictures, Music, and Videos are pinned by default, along with any folders you pin yourself. Drag favorites to reorder them.
- **Locations**: your home folder, Macintosh HD, external drives, and network shares as an expandable folder tree. Removable drives have an eject button.

Two options in **View** control how the tree follows you: **Expand to Open Folder** and **Show All Folders ("Expand Opened Folder")**, matching Windows' navigation pane options.

### Tabs

Each window has a tab bar, even with a single tab. Every tab keeps its own folder, history, selection, sort order, and search.

- Click **+** or press **⌘T** to open a new tab at the current folder.
- Right-click a folder and choose **Open in New Tab** to open it in the background.
- Drag a tab to reorder it, or drag it out of the bar to give it its own window.
- Middle-click a tab, or right-click it and choose **Close Tab**, to close it. The same menu has **Move Tab to New Window**.

Your windows and tabs are restored when you relaunch the app.

### Toolbar

The toolbar sits right above the file list, like Windows 11's command bar: **Back**, **Forward**, **Up**, **New Folder**, **Cut**, **Copy**, **Paste**, **Rename**, **Share**, **Move to Trash**, **Sort**, and **View**. The **Preview** button sits on the right edge.

### Address bar

The address bar shows the current path as clickable segments (a breadcrumb). Click a segment to jump to that folder.

To type a path:

1. Press **⌘L**, choose **Go ▸ Edit Path**, or click the empty space to the right of the path.
2. Type a path such as `/Volumes/Backup` or `~/Projects`. Suggestions from places you've typed before appear below. Press **↓** to move through them.
3. Press **Return** to go there, or **Esc** to cancel.

You can turn off remembering typed addresses, or clear them, in **Settings ▸ Privacy**.

### Search box

The search box to the right of the address bar is named after the current folder (for example, "Search Downloads"). As you type, it filters the current folder by name. Wildcards such as `*.pdf` match the whole name, as in Windows. Press **Esc** to clear the search and show everything again. **⌘F** jumps to the box.

The free search covers the current folder only. Searching all subfolders is a Pro feature.

### File list and views

Switch views with the toolbar's **View** menu. Each folder remembers its own view, like Windows.

- **Details**: a table with sortable columns. This is the default.
- **List**: compact rows of names.
- **Extra Large Icons**, **Large Icons**, **Medium Icons**, **Small Icons**: thumbnail grids for photos and videos.

In Details, folder sizes fill in automatically in the **Size** column. Finder color tags appear as colored dots.

### Preview pane

Press **⇧⌘P**, choose **View ▸ Show Preview Pane**, or click **Preview** in the toolbar. The pane on the right previews the selected item (images, PDFs, text, Markdown, video, and Office documents through Quick Look) and shows its details: size, dates, image dimensions, and camera information. Drag the divider to resize it.

Press **Space** to open a selected file in the full-size Quick Look window.

### Status bar

The status bar at the bottom shows how many items are in the folder. With a selection, it shows the count (for example, "3 of 128 selected") and the total size. A selected folder's size is calculated in the background.

## 3. Everyday tasks

### Navigate and open

- Double-click a folder or press **Return** to open it. Files open in their default app. Explorer uses **Return** for opening, as Windows does; it does not start renaming the way it does in Finder.
- Go up one level with **Backspace (⌫)**, **⌘↑**, or **Up** in the toolbar. The folder you came from stays selected.
- Go back and forward with **⌘[** and **⌘]**.
- Type the first letters of a name to jump to it.
- Aliases and symbolic links to folders open inside Explorer. Apps and other packages open like files. Right-click and choose **Show Package Contents** to browse inside one.

### Create a folder or file

- **New Folder**: press **⇧⌘N** or choose **File ▸ New Folder**. Type a name and press **Return**.
- **New Text Document**: choose **File ▸ New Text Document**, or right-click an empty area of the folder. This creates an empty `.txt` file, ready to be named.

### Copy, cut, and paste

These work the Windows way, with **⌘** in place of **Ctrl**:

1. Select items and press **⌘C** (copy) or **⌘X** (cut). Cut items are dimmed.
2. Open the destination folder and press **⌘V**.
3. The pasted items end up selected, so you can see where they landed.

Press **Esc** to cancel a pending cut. If a name is already taken, you can choose **Replace**, **Keep Both**, or **Skip**, and check **Apply to all remaining items** to use the same choice for the rest. Large copies show a progress window with speed, time remaining, and a cancel button.

### Rename

Select one item and press **⌘R** (or choose **Edit ▸ Rename**). Only the name is selected, not the extension. Press **Return** to confirm or **Esc** to cancel.

### Delete and restore

- Press **⌘⌫** or **⌦** (fn + Delete), or choose **Move to Trash**. Items go to the macOS Trash, the counterpart of the Recycle Bin.
- Backspace alone never deletes anything; it only goes up a folder.
- Some locations, such as certain network volumes, have no Trash. There, Explorer asks for confirmation before deleting permanently.
- To restore items, open the Trash, select them, and choose **Restore** from the right-click menu or the **File** menu. Each item goes back to its original folder. Inside the Trash, **Move to Trash** becomes **Delete Immediately…**.

To open the Trash, press **⌘L**, type `~/.Trash`, and press **Return**. Explorer needs Full Disk Access to list it. <!-- TODO 확인: Trash 진입 경로가 주소창(~/.Trash) 외에 사이드바/메뉴로 있는지 -->

### Undo and redo

**⌘Z** undoes the last file operation: rename, move, copy, Move to Trash, Restore, New Folder, or New Text Document. Redo with **⇧⌘Z** or **⌘Y**. The **Edit** menu shows exactly what will be undone, for example **Undo Rename**.

### Drag and drop

- Dragging to a folder on the same drive moves the items. Dragging to a different drive copies them. Hold **⌥ (Option)** while dropping to copy instead of move.
- You can drop onto folders in the list, the sidebar tree, favorites, or a segment of the address bar.
- To move files to another tab, drag them over its tab and wait for the tab to open, then drop into its list.
- Drags to and from Finder and other apps work as usual.

### Pin favorites

Right-click a folder (in the list or the tree) and choose **Add to Favorites**, or drag the folder into the Favorites section. To unpin it, choose **Remove from Favorites**. **Restore Default Favorites** brings back the standard folders.

### Network drives

Connect to a NAS or SMB share once with Finder's **Go ▸ Connect to Server…** (or by opening it from the network). Explorer then remembers the share under **Locations**, much like a mapped drive on Windows. If macOS later disconnects an idle share, it stays listed as dimmed. Click it to reconnect; your keychain provides the password. Right-click a share and choose **Forget Network Location** to remove it.

### More from the right-click menu

The context menu also offers **Open With**, **Open in New Window**, **Duplicate**, **Copy Path** (**⌥⌘C**), **Open in Terminal**, **Share**, **Get Info**, **Show in Finder**, and **Refresh**. Choose which terminal app **Open in Terminal** uses in **Settings ▸ Terminal**.

## 4. Customizing

- **Sort**: click a column header to sort by that column, and click again to reverse the order. The toolbar's **Sort** button does the same.
- **Folders first**: by default, folders always stay above files. If you turn off **Settings ▸ General ▸ Always show folders first**, Explorer follows the Windows rule: folders stay grouped together but move to the bottom when you sort in descending order.
- **Columns**: in Details, right-click any column header and check the columns you want. You can choose from **Date Modified**, **Date Created**, **Date Accessed**, **Date Added**, **Type**, **Extension**, and **Size**. **Name** is always shown. Drag headers to reorder columns and drag their edges to resize them. Your layout applies to every window.
- **Compact View**: Explorer uses roomier Windows 11-style rows by default. Choose **Compact View** in the toolbar's **View** menu for denser List and Details rows.
- **Hidden files**: press **⇧⌘.** or choose **View ▸ Show Hidden Files**.
- **Settings** (**⌘,**):
  - **General**: date format, **Always show file extensions**, and **Always show folders first**.
  - **Terminal**: the app that **Open in Terminal** uses.
  - **Folder Tree**: the tree-following options.
  - **Privacy**: typed-address history.
  - **Updates**: automatic update checks.

## 5. Differences from Windows Explorer

| In Windows | In Explorer for Mac |
|---|---|
| **Ctrl** shortcuts (Ctrl+C, Ctrl+V…) | **⌘ (Command)** shortcuts (⌘C, ⌘V…) |
| F2 to rename | **⌘R**. Mac laptops use F2 for screen brightness. |
| Backspace goes back | **Backspace (⌫)** goes up to the parent folder. Use **⌘[** to go back. |
| Delete key sends to the Recycle Bin | **⌘⌫** or **⌦** moves items to the **Trash**. **⌫** alone never deletes. |
| Recycle Bin ▸ Restore | Open the Trash and choose **Restore** |
| F5 to refresh | Folders update automatically. **Refresh** is in the right-click menu. |
| Cut a file, paste it in another program, and it moves | Cut and paste moves files inside Explorer. Pasting a cut file into Finder or another app copies it. macOS has no system-wide "cut file" convention. |
| Drives have letters (C:, D:) | Drives appear by name under **Locations**, and paths start with `/`. |

## 6. Going further

Explorer Pro adds Dual-Pane View, Batch Rename, folder compare and sync, a disk usage analyzer, a duplicate finder, a filter bar, grouping, ZIP browsing and compression, subfolder search, the Stash Shelf, and tab sessions. See [Explorer Pro](/explorer/guide/pro/?lang=en). Everything in this guide stays free.

- [Keyboard Shortcuts](/explorer/guide/shortcuts/?lang=en)
- [FAQ](/explorer/guide/faq/?lang=en)
- [License](/explorer/guide/license/?lang=en)
