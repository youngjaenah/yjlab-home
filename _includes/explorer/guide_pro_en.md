# Using Explorer Pro

This guide walks through each feature included in Explorer Pro. If you haven't activated Pro yet, follow the [License Guide](/explorer/guide/license/?lang=en) first. Menu and button names below match the labels shown in the app.

## How Pro features appear

- Without a license, Pro items in the menu bar carry a **PRO** badge. Choosing one opens a short notice with **Upgrade to Pro…**, **Import License…**, and **Cancel**. Nothing else happens.
- Right-click (context) menus don't show Pro items at all until you're licensed. After you activate Pro, they appear the next time you open the menu.
- A license takes effect immediately. You don't need to restart the app.
- Free features work the same whether or not you have Pro. For those, see the [FAQ](/explorer/guide/faq/?lang=en) and [Keyboard Shortcuts](/explorer/guide/shortcuts/?lang=en).

## Dual-Pane View

Open two folders side by side in one tab, then copy or move files from one side to the other.

**How to open it**: **View ▸ Dual-Pane View** (⌘\\), or the **Dual-Pane View** button on the right side of the toolbar

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
3. The results are sorted into **Only in Left**, **Only in Right**, **Newer in Left**, **Newer in Right**, and **Identical**. Up to this point, nothing has been written to either folder.
4. Under **Direction:**, choose **Left → Right**, **Right → Left**, or **Both (newest wins)**. Use the checkboxes next to each item or category to choose what to sync.
5. Check the summary of copies, replacements, deletions to Trash, and the amount of data to transfer, then click **Run**.

- Files that exist only on the destination side are never deleted unless you check them.
- Replaced and deleted files go to the Trash. They're never permanently deleted.
- **Both (newest wins)** copies the newer version of each file to the other side and never deletes anything. **Identical** items are never synced.
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
- Every group always keeps at least one copy. You can't check the last remaining copy.
- Files go to the Trash. To restore them, press ⌘Z in the main window.
- Just before removing, each checked file is checked again. If it changed or disappeared after the scan, it's skipped and you'll be told.

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
- Each pane has its own grouping. The last one you chose becomes the default for new panes and the next launch. Grouping isn't available in search results or inside a ZIP file.

## Browse Archive (ZIP)

Open a .zip file like a folder, without extracting it. Look through it, preview files, and copy out only the files you need.

**How to open it**: double-click a .zip file, or right-click it ▸ **Browse Archive**

1. Double-click a .zip file to open it like a folder. The address bar shows `…/name.zip`.
2. Open subfolders, and use Back or Up to leave. Going Up from the top level of the ZIP returns you to the folder that contains it.
3. Select a file to see it in the preview pane. Double-click a file to open a read-only copy in its default app.
4. To copy files out, select them, press ⌘C, go to a regular folder, and press ⌘V. You can also drag them to the other pane or to Finder.

- The inside of a ZIP is read-only. You can't paste, delete, rename, or create folders there, and the original ZIP file is never changed.
- To open a ZIP in its default app the old way, right-click it ▸ **Open with Default App**.
- For a password-protected ZIP, you can see the list of files. If you try to open, preview, or copy one, you'll see "Encrypted archives are not supported."
- Without Pro, double-clicking a .zip opens it in its default app, as before. Find in All Subfolders doesn't search inside ZIP files.

## Compress to ZIP

Compress the selected files and folders into a new .zip file, with optional AES-256 password protection.

**How to open it**: select files, then **File ▸ Compress to ZIP** or **File ▸ Compress with Password…**, or right-click ▸ the same commands

1. Select the files and folders you want to compress.
2. Choose **Compress to ZIP**. A new ZIP file appears next to your selection and is selected. For one item, the ZIP takes that item's name. For several items, it takes the name of the folder they're in.
3. To add a password, choose **Compress with Password…**, enter the same password twice, and click **Compress**.

- If a ZIP with that name already exists, it's never overwritten. The new file gets a name like "name 2.zip". Adding files to an existing ZIP isn't supported.
- Your original files aren't changed. You can cancel large jobs from the progress window, and a canceled ZIP isn't left behind.
- Undo (⌘Z) moves the new ZIP file to the Trash.
- These commands aren't available in the Trash or inside a ZIP. If the password is empty or the two entries don't match, the window stays open and tells you what to fix.

## Stash Shelf

Collect files from several folders in one place, then copy or move them all at once into the destination folder.

**How to open it**: **View ▸ Show Stash Shelf** (⇧⌘Y), or right-click files ▸ **Add to Stash Shelf**

1. Choose **View ▸ Show Stash Shelf**. A thin shelf strip appears between the file list and the status bar.
2. Drag files or folders onto the shelf, or right-click them ▸ **Add to Stash Shelf**. If the shelf is hidden, it appears automatically.
3. Go to the destination folder.
4. Right-click an item on the shelf and choose **Copy All to Current Folder** or **Move All to Current Folder**. You can also drag a single shelf item to the file list or to Finder to copy it.
5. When you're done, right-click ▸ **Remove from Shelf** (one item) or **Clear Shelf** (everything).

- The shelf only remembers where your files are. Adding a file to it doesn't copy or move anything. **Remove from Shelf** and **Clear Shelf** don't affect the files themselves.
- Copying and moving work like any other copy or move: you get progress, the name-conflict prompt, and Undo. Items that were moved successfully are removed from the shelf.
- All windows share one shelf, and its contents are kept after you restart the app. Whether the shelf is shown is set separately for each window.
- If a file is deleted or moved elsewhere, its shelf item is dimmed and skipped. You can't add items from inside a ZIP file.

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

## If your license is removed

If you remove your license, for example after a refund, your saved searches, tab sessions, and Stash Shelf items stay on this Mac. They come back if you activate a license again. Free features keep working normally. For other questions, see the [FAQ](/explorer/guide/faq/?lang=en) or email support@yjlab.io.
