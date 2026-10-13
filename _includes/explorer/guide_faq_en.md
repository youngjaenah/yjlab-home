# FAQ & Troubleshooting

Answers to the questions we hear most often, plus what to check first when something doesn't work. Menu and button names are written exactly as they appear in the app. Can't find your answer here? Write to support@yjlab.io.

## General

### Does Explorer replace Finder?

No. Explorer is a separate file manager that runs **alongside** Finder. It doesn't turn Finder off, replace it, or change any system settings. Use Explorer for everyday browsing and file management, and leave Finder as it is.

### What's the difference between the free version and Pro?

The free version is a complete file manager: folder tree, tabs, Favorites, Details view, copy/move/rename, undo, Trash restore, network drives, and more. Everything that has been free stays free, with no time limits and no upgrade pop-ups.

Pro is a one-time upgrade that adds advanced tools such as batch rename, folder compare & sync, a disk usage analyzer, dual-pane view, and ZIP browsing and compression. See [Explorer Pro](/explorer/guide/pro/) for details.

### Which Macs does it run on?

Explorer requires **macOS 14 Sonoma or later** and runs on both Apple silicon and Intel Macs.

### How do I install it?

1. Open the DMG file you downloaded.
2. Drag the **Explorer** icon onto the **Applications** folder.
3. Launch Explorer from your Applications folder.

If you launch it straight from the DMG window, updates can't work there, so Explorer offers to move itself. Click **Move to Applications Folder** and it moves itself and relaunches. For a first tour of the app, see [Getting Started](/explorer/guide/getting-started/).

### Some keys behave differently than on Windows.

A few things differ because of the Mac keyboard and macOS conventions:

- The **Delete (⌫)** key goes up to the parent folder, like Backspace on Windows. It never deletes. To delete, press **⌘⌫** or **fn+⌫** (Forward Delete).
- **Rename** is **⌘R**. On most Macs, F2 controls screen brightness.
- **Return (Enter)** opens the selected item.

See [Keyboard Shortcuts](/explorer/guide/shortcuts/) for the full list.

## Permissions

### Why does macOS ask for access to my Desktop, Documents, and Downloads?

To protect your privacy, macOS asks you before any app opens folders such as Desktop, Documents, and Downloads for the first time. The prompt comes from macOS, not from Explorer. Click **Allow** to see the files in that folder. macOS asks only once per folder.

### I clicked "Don't Allow" by mistake. How do I allow access again?

macOS doesn't ask again after you deny access, so you need to turn it on yourself:

1. Click the **Open Privacy Settings…** button that Explorer shows in the blocked folder, or open **System Settings ▸ Privacy & Security ▸ Files & Folders**.
2. Find **Explorer** in the list and turn on the folders you need.
3. Open the folder again in Explorer.

### Do I need to grant Full Disk Access?

Not for everyday use. You only need it to view locations that macOS protects more strictly, such as:

- The Trash (`~/.Trash`)
- Some folders inside `~/Library` (for example, Mail data)
- System-protected areas such as Time Machine internals

When you open one of these, Explorer explains why and shows an **Open Full Disk Access…** button. Turn on **Explorer** in **System Settings ▸ Privacy & Security ▸ Full Disk Access**, then reopen the app if macOS asks you to. Explorer never requests or enables this permission by itself; it only tells you where to find it.

### Why does a folder show "—" for its size?

By default, `~/Library` and the Trash aren't measured, so macOS doesn't keep showing permission prompts; their size reads "—". Grant Explorer Full Disk Access and they're measured like any other folder.

### Does Explorer ask for an administrator password or bypass system protections?

No. Explorer never asks for administrator (root) privileges and never bypasses macOS privacy protections (TCC) or System Integrity Protection. It's distributed directly rather than through the App Store, so it isn't sandboxed, but it can only reach what you've allowed in macOS privacy settings. The app is notarized by Apple.

### macOS says Explorer wants to access files on a network volume.

That's the macOS permission prompt shown the first time you open a NAS or shared folder. Click **Allow**. If you denied it, go to **System Settings ▸ Privacy & Security ▸ Files & Folders**, find **Explorer**, and turn on **Network Volumes**.

## Network drives & NAS (SMB)

### How do I connect to a NAS or a Windows shared folder?

The first connection is made with macOS itself:

1. In Finder, choose **Go ▸ Connect to Server** (⌘K).
2. Enter an address like `smb://server/share` and connect.
3. Once it's connected, the share appears under **Locations** in Explorer's sidebar.

Explorer's address bar doesn't accept `smb://` addresses. After you've connected to a share once, Explorer remembers it, so you can reconnect straight from the sidebar.

### A network share in the sidebar is dimmed.

macOS has disconnected a share that hasn't been used for a while. Like a mapped network drive on Windows, Explorer keeps disconnected shares under **Locations**, dimmed. Click one to reconnect it through macOS and open it. To remove a share you no longer use, right-click it and choose **Forget Network Location**.

### Does Explorer store my NAS password?

No. Explorer never asks for or stores passwords. When reconnecting, macOS uses the credentials saved in your keychain; if none are saved, macOS shows its own sign-in dialog.

### Network folders are slow.

Network folders take longer to list than a local disk; a **Loading…** indicator appears while a folder loads. A few things to check:

- Update to the latest version. Moves within the same share and list refreshes during large operations have been made much faster over several releases.
- A wired connection is far more reliable than Wi‑Fi.
- If the same action is also slow in Finder, the network or server is the likely cause.

### After a cut and paste on a Windows 11 share, a folder won't open.

On recent versions of macOS, a folder on a Windows 11 shared folder can sometimes refuse to open after you move files into or out of it. This is a **caching issue in the macOS SMB client**. It happens in Finder too, and **your files are not damaged.**

1. Eject the share from the sidebar.
2. Connect to the share again. The folder opens normally.

If it keeps happening, advanced users can turn off the macOS SMB directory cache. In Terminal, create the file `/etc/nsmb.conf` with administrator privileges, add the lines below, and reconnect the share:

```
[default]
dir_cache_off=yes
```

This setting applies to every SMB connection on your Mac, not just Explorer. Delete the file to go back to the default behavior.

### Deleting on a network folder asks "Delete Permanently?"

Network shares and some external disks have no Trash. When you delete there, Explorer asks before deleting permanently, just like Windows Explorer. Clicking **Delete Permanently** deletes the items immediately, and this **can't be undone**. The safe choice is the default button.

### Files starting with `.smbdelete` are left on a shared folder.

The SMB server leaves these temporary files when a file is deleted while another program still has it open. Explorer closes its previews before deleting and quietly cleans up leftover files afterward. Files still in use by another app are left alone; they disappear once that app closes them.

## File operations

### Can I undo a move or delete I didn't mean to make?

Yes. **Edit ▸ Undo** (⌘Z) reverses renames, moves, moves to the Trash, and copies. **Edit ▸ Redo** (⌘⇧Z or ⌘Y) does them again.

- Each window remembers its last 10 operations.
- The undo history is cleared when you quit the app.
- Permanent deletes on volumes without a Trash can't be undone.
- If another item has since taken the same name, Explorer skips undoing that item rather than overwrite it.

### How do I put something from the Trash back where it came from?

1. Choose **Go ▸ Edit Path** (⌘L), type `~/.Trash`, and press Return. Viewing the Trash requires Full Disk Access. <!-- TODO 확인: 숨김 파일 표시가 꺼진 상태에서도 주소 입력으로 ~/.Trash 이동이 되는지 -->
2. Select the items you want back.
3. Right-click and choose **Restore**, or choose **File ▸ Restore**.

This works for items trashed by Finder and other apps too. Items whose original location is unknown are skipped, and Explorer tells you which ones. Inside the Trash, **Move to Trash** becomes **Delete Immediately…** for deleting permanently.

### How do I show hidden files?

Choose **View ▸ Show Hidden Files** (⌘⇧.). Choose it again to hide them.

### File extensions aren't showing.

Open **Explorer ▸ Settings…** (⌘,) and, under **General**, turn on **Always show file extensions**. It's on by default; when it's on, Explorer shows extensions even for files macOS has marked to hide them, the way Windows does.

### What happens if a file with the same name already exists where I paste?

A dialog lets you choose one of three options:

- **Keep Both** (default): renames the new item so both are kept (for example, `file 2.txt`).
- **Skip**: leaves this item out.
- **Replace**: moves the existing item to the Trash and puts the new one in its place.

Check **Apply to all remaining items** to use the same choice for the rest of the conflicts.

### How does Explorer handle ZIP files?

In the free version, double-clicking a ZIP file opens it with the macOS default app (such as Archive Utility). With Pro, you can open a ZIP like a folder without extracting it, preview what's inside, and copy files out (read-only). You can also compress a selection with **File ▸ Compress to ZIP**, or add an AES-256 password with **Compress with Password…**. Password-protected ZIPs can be opened with apps that support AES encryption, such as Keka or 7-Zip. <!-- TODO 확인: macOS 아카이브 유틸리티 / Windows 11 기본 탐색기에서 AES-256 ZIP 해제 가능 여부 -->

## Updates

### How do I update to a new version?

Choose **Explorer ▸ Check for Updates…**. If a newer version is available, Explorer downloads it, verifies its signature, replaces itself, and relaunches. No need to download it again from the website.

To turn automatic checking on or off, go to **Explorer ▸ Settings…** and, under **Updates**, use **Check for updates automatically**. Even with automatic checking on, an update is downloaded only after you agree to install it, and it never interrupts a copy or move in progress.

### An update won't install.

Updates can't be installed while the app is running straight from the DMG window. Click **Move to Applications Folder** when prompted, or quit the app, move it into your **Applications** folder, and launch it from there. If that still doesn't work, download the latest DMG from the [website](/explorer/?lang=en) and install over the old copy; your settings are kept.

## License & purchase

### Where do I enter my Pro license?

Open **Explorer ▸ Settings…** and, under **Explorer Pro**, click **Import License…** to choose your license file, or paste your license into the field. Your license is verified offline on your Mac; Explorer never contacts a server. For moving to a new Mac, reinstalling, and more, see [License](/explorer/guide/license/).

### Can I get a refund?

Within 14 days of purchase, we give a full refund, no questions asked. See the [Refund Policy](/explorer/refund/?lang=en) for details.

## Uninstalling & privacy

### How do I uninstall Explorer completely?

1. Quit Explorer.
2. Drag **Explorer** from the **Applications** folder to the Trash.
3. To remove settings and saved data as well, delete these too:
   - `~/Library/Preferences/io.yjlab.Explorer.plist` (view, tab, Favorites, and other settings)
   - `~/Library/Application Support/io.yjlab.Explorer/` (remembered network shares, Trash origin records, and your Pro license)
   - `~/Library/Caches/io.yjlab.Explorer/` (if present)

This also deletes your Pro license file, so keep the license you received at purchase if you plan to reinstall later. You can remove Explorer's permission entries in **System Settings ▸ Privacy & Security**.

### Does Explorer collect my files or usage data?

No. Explorer has no analytics or tracking (no telemetry) and needs no account. File names, paths, and usage data never leave your Mac. The only time the app goes online is to check for updates, and you can turn that off in Settings. To manage the paths you've typed into the address bar, open **Settings…** and, under **Privacy**, turn off **Remember typed addresses** or click **Clear Typed History**. See the [Privacy Policy](/explorer/privacy/?lang=en) for details.

## Contact

### I found a bug. How do I report it?

Choose **Help ▸ Report a Bug…**. A new email opens with your app version and macOS version already filled in. Please describe what you were doing when the problem happened. If you don't use the Mail app, write to support@yjlab.io directly.
