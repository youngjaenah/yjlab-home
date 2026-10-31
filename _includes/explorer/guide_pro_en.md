# Using Explorer Pro

This guide walks through each feature included in Explorer Pro. If you haven't activated Pro yet, follow the [License Guide](/explorer/guide/license/?lang=en) first. Menu and button names below match the labels shown in the app.

## How Pro features appear

- Without a license, Pro items in the menu bar carry a **PRO** badge. Choosing one opens a short notice with **Upgrade to Pro…**, **Import License…**, and **Cancel**. Nothing else happens.
- Right-click (context) menus don't show Pro items at all until you're licensed. After you activate Pro, they appear the next time you open the menu.
- A license takes effect immediately. You don't need to restart the app.
- Free features work the same whether or not you have Pro. For those, see the [FAQ](/explorer/guide/faq/?lang=en) and [Keyboard Shortcuts](/explorer/guide/shortcuts/?lang=en).

## Dual-Pane View

Open two folders side by side in one tab, then copy or move files from one side to the other.

**How to open it**: **View ▸ Dual-Pane View** (⌘\\), or the **Dual-Pane View** button on the right side of the toolbar (the button appears once Pro is active)

1. Go to your starting folder and choose **View ▸ Dual-Pane View**. Your current view stays in the left pane, and a new pane opens on the right.
2. Click the right pane to make it active, then go to the destination folder. The address bar, sidebar, status bar, and preview always follow the active pane.
3. Select files in one pane and choose **Edit ▸ Copy to Other Pane** (⇧⌥⌘C) or **Edit ▸ Move to Other Pane** (⇧⌥⌘M). The same commands are in the right-click menu for files.
4. You can also drag files to the other pane. On the same volume they're moved, and across volumes they're copied. Hold Option while dragging to copy.
5. Choose **View ▸ Dual-Pane View** again to go back to one pane. The active pane's folder and selection are kept.

- Each pane has its own location, sort order, and view mode.
- Copying or moving to the other pane works like any other copy: you get the progress window, the name-conflict prompt, and Undo. One ⌘Z undoes the whole operation.
- Split tabs are saved per tab and come back after you restart the app.
- Going back to a single pane always works, even without a license.

## Batch Rename

Rename many files at once with find & replace, regular expressions, sequence numbers, and case changes.

**How to open it**: select files, then **Edit ▸ Batch Rename…** or right-click ▸ **Batch Rename…** (no keyboard shortcut)

1. Select the files you want to rename and open **Batch Rename…**. A single file works too.
2. Enter text in **Find:** and **Replace:**. If you need them, turn on **Case sensitive**, **Include extension** (also renames the extension), or **Use regular expressions**. With regular expressions, you can use capture groups such as `$1` and `$2`.
3. To add numbers, turn on **Add sequence numbers** and set **Start:**, **Increment:**, **Padding:** (number of digits), and **Separator:**. Then choose whether the number goes before the name (**Prefix**) or after it (**Suffix**). Numbers follow the order the files appear in the list.
4. Under **Case:**, choose **None**, **lowercase**, **UPPERCASE**, or **Title Case**. The extension's case doesn't change.
5. Check the **Current** and **Proposed** columns, then click **Rename**.

- The preview updates as you type. Nothing changes on disk until you click **Rename**.
- If two files would end up with the same name, or a name isn't allowed (for example, it contains `/`), the row is flagged and **Rename** is disabled. An invalid regular expression disables **Rename** in the same way.
- If some files fail, the rest are still renamed, and the results list each failed file and why it failed.
- One **Edit ▸ Undo Batch Rename** (⌘Z) restores every original name. Batch Rename isn't available in the Trash.

## Compare Folders

See what differs between two folders, then sync only the items you choose, in one direction or both.

**How to open it**: **Tools ▸ Compare Folders…**

1. Open **Compare Folders…**. In Dual-Pane View, **Left:** and **Right:** are filled in with the two panes' folders. Otherwise, the active folder is filled in. Use **Choose…** to pick a different folder.
2. Click **Compare**. Files are compared by size and modified date (**Quick compare (size + date)**), and you can **Cancel** at any time.
3. The results are sorted into **Only in Left**, **Only in Right**, **Newer in Left**, **Newer in Right**, **File vs. Folder**, and **Identical**. Up to this point, nothing has been written to either folder.
4. Under **Direction:**, choose **Left → Right**, **Right → Left**, or **Both (newest wins)**. Use the checkboxes next to each item or category to choose what to sync.
5. Check the summary of copies, replacements, deletions to Trash, and the amount of data to transfer, then click **Run**.

- Files that exist only on the destination side are never deleted unless you check them.
- Replaced and deleted files go to the Trash. They're never permanently deleted.
- **Both (newest wins)** copies the newer version of each file to the other side and never deletes anything. **Identical** items are never synced.
- **File vs. Folder** lists names that are a file on one side and a folder on the other. They're never synced, in any direction. Rename or move one of them yourself, then compare again.
- If you cancel partway through, no half-written file is left under its final name. Subfolders that can't be read are marked as excluded from the comparison.

## Analyze Disk Usage

See which folders and files take up the most space in a folder or volume, sorted by size.

**How to open it**: **Tools ▸ Analyze Disk Usage…** (current folder), right-click a folder ▸ **Analyze Disk Usage…**, or right-click a folder or volume in the sidebar ▸ **Analyze Disk Usage…**

1. Open **Analyze Disk Usage…** on the folder you want to check. The **Disk Space Analyzer** window fills in with the largest items first.
2. Each row shows its size and its percentage of the parent folder (**Share**). Double-click a folder to go into it. To go back up, click a folder in the path at the top of the window.
3. Look at the **Largest Files** list at the bottom to find the biggest individual files.
4. Right-click a row to choose **Move to Trash**, **Reveal in Explorer** (opens its location in the main window), or **Get Info**.

- To get a trashed file back, press ⌘Z in the main window. The analyzer's totals update right away.
- In very large folders, small items are grouped into one **Other (N items)** row. Double-click it to show them all.
- If part of a folder can't be read, its size starts with **≥**, meaning "at least this much". Packages such as apps count as one item, and the analyzer doesn't look inside them.
- Stop a scan anytime with **Cancel** or Esc. Results found up to that point stay visible. When you analyze a volume, the window also shows its used, free, and total space.

## Find Duplicates

Find files whose contents are identical, choose which copy to keep, and move the rest to the Trash.

**How to open it**: **Tools ▸ Find Duplicates…** (current folder), right-click a folder ▸ **Find Duplicates…**, or right-click a folder or volume in the sidebar ▸ **Find Duplicates…**

1. Open **Find Duplicates…** on the folder you want to scan. All subfolders are included, and you can **Cancel** at any time.
2. Groups that waste the most space are listed first. To start with, no file is checked for removal.
3. Check the copies you want to remove. To set the copy to keep in every group at once, use **Oldest**, **Newest**, or **In Folder…** next to **Keep in each group:**.
4. Check the summary (groups, checked files, and space to be freed), click **Move Duplicates to Trash**, and confirm.

- Files are compared by both size and content, so files that just happen to be the same size aren't grouped. Zero-byte files, hard links, and symbolic links are left out.
- Hidden files and folders (such as `.git`) and developer folders (`node_modules`, `DerivedData`, `Pods`, `__pycache__`, and the like) aren't scanned, because the apps that own those files expect them to stay where they are. Turn on **Include hidden files** at the bottom of the window to scan hidden items as well; the scan starts over. Developer folders are skipped unless you open Find Duplicates on one of them directly.
- Every group always keeps at least one copy. You can't check the last remaining copy.
- Files go to the Trash. To restore them, press ⌘Z in the main window.
- Just before removing, each checked file is checked again. If it changed or disappeared after the scan, it's skipped and you'll be told. The copy you're keeping is checked too: if it changed or disappeared, nothing in that group is removed.

## Find in All Subfolders

Search file names or file contents in every subfolder of the current folder.

**How to open it**: **Edit ▸ Find in All Subfolders…** (⇧⌘F), or choose **All Subfolders** in the scope menu next to the search field

1. Go to the folder where the search should start and press ⇧⌘F. The search field switches to **All Subfolders**, and its placeholder reads "Search subfolders — press Return".
2. In the menu next to the search field, choose **Name** (file names) or **Contents** (text inside files).
3. Type your search and press Return. Results appear as they're found. The **Location** column shows which subfolder each file is in.
4. Double-click a result to open it. To go to the folder a file is in, with the file selected, right-click it ▸ **Open Containing Folder**.
5. Press Esc, or change the scope back to **This Folder**, to return to the folder listing.

- Name searches follow the same rules as the free search, so wildcards such as `*.pdf` work.
- Search uses the macOS Spotlight index first. Places Spotlight doesn't index, such as network shares, are searched folder by folder automatically. Explorer never builds an index of its own or leaves anything running in the background.
- You can sort the results, preview them, and narrow them with the filter bar.
- The free search that narrows the current folder (**Edit ▸ Find**, ⌘F, scope **This Folder**) works as before.

## Saved Searches

Save a subfolder search you run often under a name in the sidebar, then run it again with one click.

**How to open it**: while subfolder search results are showing, choose **Edit ▸ Save Search…**

1. Run a subfolder search as described above. If you like, narrow it by type, date, or size with the filter bar.
2. Choose **Edit ▸ Save Search…**, enter a name, and click **Save**.
3. The search appears under **Saved Searches** in the sidebar. Click it later to go to the saved folder and run the search again with the same text, the same mode (**Name** or **Contents**), and the same filters.
4. Right-click a saved search to choose **Rename…** or **Delete Saved Search**.

- **Save Search…** is available only while a subfolder search is running or its results are showing.
- Date filters such as "Last 7 days" are counted from the day you run the search, not the day you saved it.
- If the saved folder no longer exists or its volume isn't connected, you'll see a **Folder Not Available** notice and the search won't run.
- Saved searches are stored only on this Mac. Deleting one doesn't affect any files.

## Filter Bar

Filter the current folder by file type, modified date, or size. Filters work together with the name search in the search field.

**How to open it**: once Pro is active, the filter bar always appears just below the address bar, above the file list.

1. Click one or more type buttons: **Folders**, **Images**, **Docs**, **Audio**, **Video**, or **Archives**. If you select more than one, items of any selected type are shown.
2. In the date menu, choose **Any date**, **Today**, **Last 7 days**, **Last 30 days**, or **This year**.
3. In the size menu, choose **Any size**, **Smaller than 1 MB**, **1 MB – 100 MB**, **Larger than 100 MB**, or **Larger than 1 GB**.
4. Check **Showing X of Y** at the right end of the bar to see how many items remain. To clear every filter, including the name search, click **Clear**.

- An item has to match every filter you set. For example: "Invoice" in the name + **Docs** + **This year**.
- Filters only hide items. They never move or change files.
- Filters reset when you go to another folder or switch tabs or panes.
- While a size filter is on, folders whose size hasn't been calculated yet are left out of the results.

## Group by

Split the Details view into groups by date, type, size, or name, as in Windows File Explorer.

**How to open it**: **View ▸ Group by**, right-click an empty area of the file list ▸ **Group by**, or right-click a column header ▸ **Group by**

1. Switch the folder to **Details** view. Grouping works only in Details view.
2. Under **Group by**, choose **Name**, **Date Modified**, **Type**, or **Size**.
3. The list is split under headers that show each group's item count, such as "Today (12)". Dates are grouped as **Today**, **Yesterday**, **Earlier this week**, **Last week**, **Earlier this month**, **Last month**, **Earlier this year**, and **A long time ago**.
4. Click a group header to collapse or expand that group.
5. To turn grouping off, choose **Group by ▸ (None)**.

- Name groups are **0 - 9**, **A - H**, **I - P**, **Q - Z**, **ㄱ - ㅎ** (Korean), and **Other**. Size groups use the same ranges as Windows, from **Empty (0 KB)** to **Gigantic (>4 GB)**. Folders whose size isn't known yet go under **Unknown**.
- Clicking a column header sorts the items inside each group. The order of the groups stays the same.
- The name search and the filter bar apply first, and the header counts reflect the filtered list.
- Each pane has its own grouping. The last one you chose becomes the default for new panes and the next launch. Grouping isn't available in search results or inside an archive.

## Browse Archives (ZIP, 7z, RAR, tar)

Open an archive like a folder, without extracting it. Look through it, preview files, and copy out only the files you need. Works with .zip, .7z, .rar, .tar, .tar.gz (.tgz), .tar.bz2, .tar.xz, and single .gz, .bz2, and .xz files.

**How to open it**: double-click the archive, or right-click it ▸ **Browse Archive**

1. Double-click an archive to open it like a folder. The address bar shows `…/name.zip` (or `…/name.7z`, and so on).
2. Open subfolders, and use Back or Up to leave. Going Up from the top level of the archive returns you to the folder that contains it.
3. Select a file to see it in the preview pane. Double-click a file to open a read-only copy in its default app.
4. To copy files out, select them, press ⌘C, go to a regular folder, and press ⌘V. You can also drag them to the other pane or to Finder.

- Browsing never changes the archive. A ZIP can also be edited, see **Edit a ZIP** below. 7z, RAR, and tar archives are read-only: the status bar says "Only ZIP archives can be edited."
- A .tar.gz, .tar.bz2, or .tar.xz file has no table of contents, so a large one is read from start to end before the list appears. The status bar shows "Reading … %". Press Esc to stop and go back.
- If a file or folder with the same name is already there and you choose **Replace**, it's replaced only after everything was extracted. If an item can't be extracted (for example, it's password-protected) or you cancel, the existing file or folder is kept as it was.
- To open an archive in its default app the old way, right-click it ▸ **Open with Default App**.
- For a password-protected archive, you can see the list of files. If you try to open, preview, or copy one, you'll see "Password-protected files in this archive can't be opened here." A 7z or RAR whose file names are encrypted too, and the parts of a split archive (.7z.001, .part1.rar, …), can't be browsed. Explorer tells you so and offers **Open with Default App**.
- Links inside a tar archive are listed but not copied out, and the skip is reported.
- Other formats, such as .tar.zst, open in their default app as before.
- Without Pro, double-clicking an archive opens it in its default app, as before. Find in All Subfolders doesn't search inside archives.

## Edit a ZIP

Add, delete, and rename files inside a ZIP you're browsing, like a regular folder.

**How to open it**: open a .zip with **Browse Archive**, then drag or paste files into it, or use **New Folder**, **Rename** (⌘R), and **Delete**

1. To add files, drag them into the ZIP's file list (or onto a folder inside it), or copy them (⌘C) and paste (⌘V) inside the ZIP. Choose **New Folder** to create an empty folder. To move files in instead, cut them (⌘X) and paste inside the ZIP: once the ZIP is updated, the originals go to the Trash, and one Undo (⌘Z) puts everything back. Dragging into a ZIP always copies.
2. To rename an item, select it and press ⌘R, or right-click ▸ **Rename**. Renaming a folder renames everything in it.
3. To delete items, select them and press Delete, then confirm.
4. A progress window shows each change. You can cancel it, and canceling leaves the ZIP exactly as it was.

- Every change writes a complete new ZIP and then swaps it in. Your original ZIP is moved to the Trash, so Undo (⌘Z) brings it back.
- On a drive without a Trash (most network shares), you're asked to confirm first, because the previous version can't be kept and the change can't be undone.
- Files you didn't touch are copied exactly as they were, including password-protected ones. When you add files to a ZIP that has password-protected files, you're asked for a password and the new files are protected with it.
- Some ZIPs can only be browsed: ones whose file names use an older, non-Unicode encoding (common in ZIPs made on older Korean or Japanese Windows), damaged or split ZIPs, and self-extracting archives. The status bar says why.
- If the ZIP was changed by another app while you were browsing it, the change is refused and the list reloads.
- Names you add or rename are saved in the form Windows expects, so Korean and other non-English names show correctly in Windows File Explorer and 7-Zip. ZIPs made with Finder's Compress can be edited too.

## Compress to ZIP

Compress the selected files and folders into a new .zip file, with optional AES-256 password protection.

**How to open it**: select files, then **File ▸ Compress to ZIP** or **File ▸ Compress with Password…**, or right-click ▸ the same commands

1. Select the files and folders you want to compress.
2. Choose **Compress to ZIP**. A new ZIP file appears next to your selection and is selected. For one item, the ZIP takes that item's name. For several items, it takes the name of the folder they're in.
3. To add a password, choose **Compress with Password…**, enter the same password twice, and click **Compress**.

- If a ZIP with that name already exists, it's never overwritten. The new file gets a name like "name 2.zip". To add files to an existing ZIP, see **Edit a ZIP**.
- Your original files aren't changed. You can cancel large jobs from the progress window, and a canceled ZIP isn't left behind.
- Undo (⌘Z) moves the new ZIP file to the Trash.
- These commands aren't available in the Trash or inside an archive. If the password is empty or the two entries don't match, the window stays open and tells you what to fix.

## Stash Shelf

Collect files from several folders in one place, then copy or move them all at once into the destination folder.

**How to open it**: **View ▸ Show Stash Shelf** (⇧⌘Y)

1. Choose **View ▸ Show Stash Shelf**. A thin shelf strip appears between the file list and the status bar, and the menu item is checked. Choose it again to hide the shelf.
2. Drag files or folders onto the shelf, or right-click them ▸ **Add to Stash Shelf**. That menu item appears only while the shelf is shown.
3. Go to the destination folder.
4. Right-click an item on the shelf and choose **Copy All to Current Folder** or **Move All to Current Folder**. You can also drag a single shelf item to the file list or to Finder to copy it.
5. When you're done, right-click ▸ **Remove from Shelf** (one item) or **Clear Shelf** (everything).

- The shelf only remembers where your files are. Adding a file to it doesn't copy or move anything. **Remove from Shelf** and **Clear Shelf** don't affect the files themselves.
- Copying and moving work like any other copy or move: you get progress, the name-conflict prompt, and Undo. Items that were moved successfully are removed from the shelf.
- All windows share one shelf, and its contents are kept after you restart the app. Whether the shelf is shown is set separately for each window.
- If a file is deleted or moved elsewhere, its shelf item is dimmed and skipped. You can't add items from inside an archive.

## Tab Sessions

Save the current window's tabs under a name, then reopen them later in a new window.

**How to open it**: **Window ▸ Save Tab Session…** and **Window ▸ Tab Sessions**

1. Open the tabs you need. Dual-pane splits and each pane's sort order and view mode are saved too.
2. Choose **Window ▸ Save Tab Session…**, enter a name, and click **Save**.
3. Later, choose a session from **Window ▸ Tab Sessions** to open its tabs in a new window. Each session in the list shows its number of tabs and when you saved it.
4. To rename or delete sessions, choose **Window ▸ Tab Sessions ▸ Manage Sessions…**. To rename one, select it and press Return. To remove one, click **Delete**.

- A session always opens in a new window, so your open windows and tabs aren't changed.
- Tabs for folders that no longer exist are skipped. If none of the folders exist, the session opens with a single Home tab.
- You can save more than one session with the same name. Deleting asks for confirmation and can't be undone.
- Reopening your last tabs automatically when the app starts is a separate free feature.

## What's Using This?

See which of your apps is holding a file, folder, or drive open, and close it, like PowerToys File Locksmith on Windows.

**How to open it**: when a drive won't eject or a file is "in use", click **What's Using This?** in the message. Or right-click a file, folder, or drive in the sidebar ▸ **What's Using This?**, or choose **Tools ▸ What's Using This?**

1. The window lists each app or process that holds the item: its name, process ID (PID), and the files it has open (or, for a shell, that it's sitting in the folder).
2. Click **Quit** to close an app normally. The app may ask you to save first. If it doesn't quit, the row says "Still running."
3. **Force Quit** closes an app immediately, for example one that doesn't respond. Explorer asks first, because unsaved changes in that app are lost.
4. If you opened the window from a failed eject or operation, click **Try Again** to repeat it. The window closes once it works.

- Only your own apps are shown. System services, other users, or other computers on a network may also be using the item, and the window says so. Explorer never asks for an administrator password.
- If Explorer itself is listed (for example, a PDF shown in the preview pane, or a drive you're browsing), click **Release Explorer's Holds**.
- Command-line processes, such as a Terminal shell sitting in the folder, can only be force-quit.
- Click **Refresh** to look again.
- Without Pro, "in use" messages work as before. **Tools ▸ What's Using This?** shows a **PRO** badge.

## iPhone and iPad Photos

Browse the photos and videos on an iPhone or iPad connected with a cable, then copy them to your Mac or delete them from the phone, like **This PC ▸ Apple iPhone** on Windows. Nothing needs to be installed on the phone.

**How to open it**: connect the phone with a cable, unlock it, and tap **Trust** if the phone asks. The phone appears under **Locations** in the sidebar.

1. Click the phone in the sidebar, then open **Internal Storage ▸ DCIM**. The camera roll is in monthly folders such as `202610_a`, just as Windows shows them. Each folder shows the date of its newest photo and its total size.
2. The list shows each photo and video with its name, the date it was taken, its type, and its size. Thumbnails appear as you scroll. Sorting, the filter bar, and the Details, List, and Icons views work as in any folder.
3. Select a photo to see it in the preview pane, press Space for Quick Look, or double-click to open it in its default app.
4. To copy to your Mac, drag the files to a folder, the Desktop, the sidebar, Finder, or a web page's upload area. You can also press ⌘C and then ⌘V in a regular folder. Files arrive exactly as they're stored on the phone, with the date they were taken.
5. To copy everything you haven't imported yet, right-click the phone in the sidebar ▸ **Import Pictures and Videos…** and choose a folder (Pictures by default). Photos go into a folder named after the phone. Files that are already there with the same name and size are skipped, so you can run it again after taking new photos.
6. To delete photos from the phone, select them and press Delete, then click **Delete** in the confirmation. Pressing Return cancels. Deleting a folder deletes every photo and video in it, and the confirmation says how many; the folder then disappears from the list.

- **Deleting from the phone can't be undone.** Photos deleted over the cable don't go to the phone's "Recently Deleted" album, so the confirmation asks every time. Copy anything you want to keep first.
- Nothing is ever added to or renamed on the phone. New Folder, Rename, Paste, and dropping files onto the phone aren't available. To put photos on your iPhone, use AirDrop, iCloud Photos, or syncing in Finder.
- If the phone is locked, the window says "Unlock your iPhone and tap Trust if asked." and the list appears as soon as you unlock it. After that, you can keep browsing and copying even if the phone locks again, until you unplug it.
- If you unplug the phone, its tab says the phone isn't connected and reloads when you plug it back in. A copy in progress stops and tells you how many items were copied, with no half-copied files left behind.
- Photos kept only in iCloud (with "Optimize iPhone Storage" on) aren't on the phone, so they aren't shown.
- Files are copied in their original format. Photos taken as HEIC stay HEIC, which macOS opens normally. Edited photos appear as a separate file (for example `IMG_E1234.JPG`) next to the original, and a Live Photo appears as a photo plus a short video.
- Without Pro, the phone appears in the sidebar with a **PRO** badge, and clicking it shows a short notice with **Learn More**.

## Properties

See everything about a file, folder, or selection in one window, and change its name and attributes, like **Properties** (Alt+Enter) on Windows.

**How to open it**: select items and press **⌥↩** or **⌘I**, choose **File ▸ Properties**, or right-click ▸ **Properties**

1. For a file, the window shows its type (for example "JPEG image (.jpg)"), the app it opens with, its location, its **Size** and **Size on disk** in exact bytes, and when it was created, modified, and last opened.
2. For a folder, **Contains** counts its files and folders ("1,204 Files, 37 Folders") along with the total size. The numbers climb while Explorer counts in the background, and counting stops when you close the window. An app or other package counts as one file.
3. With several items selected, the window shows the number of items, their shared type (or "Multiple types"), the folder they're in (or "Various"), and their combined size.
4. To make changes, edit the name, check or clear **Read-only**, **Hidden**, or **Hide extension**, or click **Change…** next to **Opens with:** to pick the app for every file of that type.
5. Click **Apply** to apply the changes and keep the window open, **OK** to apply and close, or **Cancel** to close without changes.
6. To check a file's integrity, click **Calculate** next to **SHA-256:**. Explorer reads the file in the background and shows the progress; click **Cancel** to stop. When it's done, click **Copy** to put the checksum on the clipboard and compare it with the one the download page publishes. It's the same value as `shasum -a 256` in Terminal.

- A rename made here works like any other: ⌘Z undoes it. If the name is taken, Explorer says so and keeps what you typed so you can fix it.
- Attribute changes can't be undone with ⌘Z. Open Properties again to change them back.
- **Read-only** is the macOS Locked flag. A name that starts with a dot is always hidden, so its **Hidden** box can't be cleared.
- Items in the Trash, inside an archive, or on a phone can be viewed but not changed. The button reads **Close**.
- You can open several Properties windows at once.
- **SHA-256** is shown for a single file. Folders, apps and other packages, symbolic links, and several selected items don't have it. If the file changes while it's being read, no checksum is shown. Click **Calculate** again. A file that's only in iCloud or other cloud storage is downloaded to compute it.
- Without Pro, **File ▸ Get Info** (⌘I or ⌥↩) shows the free, read-only info panel for one item: kind, the app that opens it, location, size, created, modified, and accessed dates, and whether it's Read-only or Hidden. Changing them, several items at once, size on disk, and a folder's contents count are what Pro adds.

## Cloud File Status

See which files in iCloud Drive, Google Drive, OneDrive, and Dropbox are stored only online and which are on your Mac, and switch between the two, like the status column in OneDrive on Windows.

**How to use it**: open a folder in iCloud Drive or a cloud storage location in the sidebar. A small badge follows each file name (in icon views, it sits at the bottom left of the icon).

1. A cloud outline means the file is online only. A green check means it's on this Mac. A cloud with a down arrow means it's downloading, and a cloud with an up arrow means it hasn't finished uploading.
2. To keep files on your Mac, select them and right-click ▸ **Download**, or choose **File ▸ Download**.
3. To free up space, select files and right-click ▸ **Free Up Space**, or choose **File ▸ Free Up Space**. The files stay in the cloud and in the list, and download again when you open them.
4. Selecting a folder includes every file inside it.

- Free Up Space only removes the copy on your Mac, and only for files that have finished uploading. Anything not uploaded yet is skipped, and Explorer tells you how many were skipped. Nothing is ever deleted from the cloud.
- A file that's open in another app, or shown in the preview pane, may not be freed. Close it and try again.
- The provider's own app does the downloading and uploading. Explorer only asks macOS to do it.
- Folders have no badge, and Google Docs, Sheets, and Slides files always show the cloud badge because they live online.
- Without Pro, cloud folders browse normally without badges. **File ▸ Download** and **File ▸ Free Up Space** show a **PRO** badge.

## Create Shortcut

Make a shortcut to a file or folder, like **Create shortcut** on Windows. Explorer makes a Finder alias, which opens the original wherever it moves.

**How to use it**: select items and press **⌃⌘A**, choose **File ▸ Create Shortcut**, or right-click ▸ **Create Shortcut**

1. A shortcut named "*name* - Shortcut" appears next to each item and is selected. If that name is taken, Explorer adds (2), (3), and so on.
2. To make shortcuts somewhere else, hold **⌥⌘** while you drag items onto a folder or onto the empty area of a list. The pointer shows the alias arrow.
3. ⌘Z moves the new shortcuts to the Trash, and ⇧⌘Z makes them again.

- Shortcuts can't be made in the Trash, inside an archive, or on a phone, or dropped into a folder you can't write to.
- Double-clicking a shortcut to a folder opens the folder in Explorer.

## Item Check Boxes

Show a check box on each item and select files by clicking their boxes, like **View ▸ Item check boxes** on Windows. This is handy on a trackpad, where ⌘-clicking is awkward.

**How to turn it on**: **View ▸ Item Check Boxes**, or the toolbar's **View** menu. The setting applies to every window and tab.

1. A box appears on the item under the pointer and on every selected item. In Details and List it's at the start of the row; in icon views it's at the top-left corner of the icon.
2. Click a box to add that item to the selection, or click it again to remove it. The rest of the selection stays as it is, so there's no need to hold ⌘.
3. Clicking an item's name or icon still selects only that item, as usual.
4. In Details, the box in the **Name** header selects every item, or clears the selection when everything is already selected. It shows a dash when only some items are selected.

- Double-clicking a box never opens the item.
- If some groups are collapsed in **Group by**, the header box selects only the items you can see.
- Choose **View ▸ Item Check Boxes** again to turn the boxes off.

## Copy Text from the Preview

Copy the whole contents of a text file to the clipboard without opening it.

**How to use it**: select a text, Markdown, or RTF file with the preview pane open, then click the copy button at the right end of the file name above the preview

1. The button turns into a check mark for a moment once the text is on the clipboard.
2. The whole file is copied, even when the preview shows only the first part of a large file.
3. Markdown is copied as its source text. RTF is copied with its formatting, so it pastes formatted into Pages, Word, or Mail and as plain text elsewhere. With **Show Source** on, the raw RTF is copied instead.

- The button appears for files the pane shows as text: plain text, Markdown, RTF, source code, JSON, XML, CSV, HTML, and logs.
- Files larger than 32 MB can't be copied this way.
- To copy only part of the text, select it in the preview and press ⌘C.

## If your license is removed

If you remove your license, for example after a refund, your saved searches, tab sessions, and Stash Shelf items stay on this Mac. They come back if you activate a license again. Free features keep working normally. For other questions, see the [FAQ](/explorer/guide/faq/?lang=en) or email support@yjlab.io.
