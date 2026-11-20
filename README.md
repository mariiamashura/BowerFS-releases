# BowerFS

English | [Deutsch](README.de.md) | [Українська](README.uk.md)

A Windows file manager for large libraries of images and video. Fully offline: no internet,
no telemetry, no account. Idea: Mariia Mashura. Technical implementation: Claude (Anthropic).

## Download

Get `BowerFS-<version>-win64.zip` from the **Releases** page of this repository, unpack it to any
folder (a USB stick works too) and start `BowerFS.exe`. There is no installer and nothing is
written to the registry. Windows 10 and 11, 64-bit.

Check the download: the SHA-256 of the zip is in `SHA256SUMS.txt`.

```powershell
Get-FileHash BowerFS-<version>-win64.zip -Algorithm SHA256
```

## First start

1. The program asks where to keep its data (database, thumbnail cache, logs). The default is
   `Documents\BowerFS`. You can move it later in *Tools → Settings*.
2. Windows SmartScreen may say the app is unknown, because the program is not code-signed:
   choose *More info → Run anyway*.
3. If a file cannot be renamed or deleted ("Access denied") although it is not read-only, an
   antivirus (for example AVG) or Windows "Controlled folder access" is blocking the unknown
   program. Add `BowerFS.exe` to its list of allowed programs.

## What it does

- Up to four panels (two above, two below), each with tabs; folder tree, favourites, tags.
- Preview of images (JPG, PNG, WebP, GIF, TIFF, BMP, HEIC, RAW, PSD, SVG), video, audio, PDF,
  DOCX, XLSX, text and code, archives (ZIP, 7z), fonts and 3D models (STL, OBJ, PLY, GLB, glTF).
- Exact duplicate search by content, with preview side by side; duplicates go to the Recycle Bin.
- Copy, move, rename and batch rename with a preview of every change, an operation journal and undo.
- Compare two files side by side, blended, as a difference or flipping between them.
- Drag and drop between panels and to or from Windows Explorer.
- Interface in English, Deutsch and Українська, light and dark theme, configurable shortcuts.

Files on drives without a Recycle Bin (network, USB) are deleted permanently, so the program asks
twice there.

## Keys

F3 preview, F5 copy, F6 move, F2 rename, Ctrl+M batch rename, F8 / Del to the Recycle Bin,
F9 compare, Ctrl+D duplicates, Ctrl+Z undo, Ctrl+T / Ctrl+W new / close tab,
Ctrl+Shift+N another panel, Tab next panel, F1 about. All of them can be changed in the settings.

## Optional tools

Put `ffmpeg.exe` and `ffprobe.exe` into the `tools` folder next to `BowerFS.exe` for video
thumbnails and storyboards (otherwise they are looked up in PATH). They are not included.

## Privacy

BowerFS makes no network connections. Your files are never changed except by the operations you
confirm. Tags and the index live in the data folder you chose.

## Licence

See [LICENSE.txt](LICENSE.txt) and [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md).
The source code is in a private repository.

## Problems and wishes

Open an issue on this page. Please do not attach private photos, and check the log file
`logs\bowerfs.log` in your data folder before you attach it.
