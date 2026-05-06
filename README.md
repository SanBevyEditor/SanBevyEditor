# SanBevyEditor

3D scene editor for the [Bevy](https://bevyengine.org/) engine — Rust-native, ECS-driven, with REST API control suitable for AI agents.

> **This repo hosts binary releases only.** The editor source is closed.
> See the project homepage for changelogs, documentation, and demos.

🌐 **Homepage** : <https://www.koolwww.com/SanBevyEditor/>

## Download

The latest Windows build is published as a release asset. Always-current URL :

`https://github.com/SanBevyEditor/SanBevyEditor/releases/latest/download/SanBevyEditor.7z`

1. Download `SanBevyEditor.7z`
2. Extract with [7-Zip](https://www.7-zip.org/) (or any modern archive tool — Windows 11 24H2+ supports `.7z` natively)
3. Run `SanBevyEditor.<version>.exe`

The editor checks for updates on startup and shows a notification if a newer version is available.

## Verifying release integrity

Each `.7z` is signed Ed25519 and ships with a detached `.7z.sig` (64 bytes). The matching public key lives in the [SanBevyEditor/sanlauncher](https://github.com/SanBevyEditor/sanlauncher) project (`keys/sandata.pub`).

```powershell
sansign verify --key keys/sandata.pub --in SanBevyEditor.7z
```

## Demos

- [BountyMaze](https://github.com/SanBevyEditor/BountyMaze-SanBevyEditor-Demo) — western-themed maze chase, built end-to-end by an LLM agent driving the editor's REST API.

## Reporting an antivirus false positive

If your AV flags `SanBevyEditor.<version>.exe` as malicious, it's a heuristic false positive on a small unsigned closed-source Rust binary. Report it back to the AV vendor :

- **Microsoft Defender** : <https://www.microsoft.com/en-us/wdsi/filesubmission> → "Software developer" → "I believe this is incorrectly detected"
- **Other AVs** : check the vendor's submission page

## License

Binaries are distributed under the SanBevyEditor EULA. All rights reserved on the source code; this repository does not grant any license to the binaries beyond what the EULA permits.
