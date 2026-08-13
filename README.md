# life_is_a_game_unity_game

Container for the third-party Unity assets and demo scenes intended for
the `life-is-a-game` project.

> **Status: half-real Unity project.** Correct `Assets/` casing, but
> missing `ProjectSettings/` and `Packages/manifest.json`, so Unity
> will refuse to open it cleanly. See "Known issues" below.

## What's actually here

The bulk of the tracked files are third-party Asset Store packages,
not custom code:

- **Advanced Waypoint System** — asset-store waypoint navigation.
- **MK Glass Free** — glass shader.
- **#NVJOB Simple Water Shaders** — water shaders.
- A full copy of **Unity PostProcessing v1** (`PostProcessing/`).
- 5 `.unity` demo scenes (all inside the Advanced Waypoint System
  demos folder).
- 97 `.cs`, 28 `.shader`, 30 `.cginc`, 35 `.mat`, 101 `.png`,
  427 `.meta`.
- `LICENSE` — GPL-3.

## Known issues

- **No `ProjectSettings/`** — Unity uses
  `ProjectSettings/ProjectVersion.txt` to pick the editor version.
  Without it, the editor can't open the project without resetting
  everything.
- **No `Packages/manifest.json`** — the Unity package resolver has
  nothing to work from.
- **Third-party Asset Store content** — Advanced Waypoint System, MK
  Glass, NVJOB shaders are (or were) sold on the Unity Asset Store.
  Redistributing paid store content is against the Asset Store
  Provider Agreement; free / OSS items are usually fine but check
  each package's individual LICENSE file (`license_unity.txt`,
  `license_nvjob.txt` etc.) before pushing to a public fork.
- **PostProcessing v1 is deprecated.** Unity moved to URP/HDRP
  Volumes; v1 was hard-EOL'd around Unity 2019. If the project ever
  gets rebuilt against modern Unity, this whole folder should be
  removed and replaced with the URP `Volume` component.
- **Committed `.vs/` and `.csproj` files** — Visual Studio /
  Rider-generated cruft. Adding them to `.gitignore` (new this
  commit); the existing tracked copies are left in place.

## Related repos

- [`s-b-repo/life-is-a-game`](https://github.com/s-b-repo/life-is-a-game)
  — the sibling repo with the custom gameplay code and main scene
  (uses lowercase `assets/`).
- [`s-b-repo/life_is_a_game`](https://github.com/s-b-repo/life_is_a_game)
  — empty placeholder; recommended consolidation target.

## License

GPL-3 (from the pre-existing top-level `LICENSE`). Note that GPL-3 is
almost certainly incompatible with the redistribution terms of some
of the bundled Asset Store packages here — resolve on a per-package
basis if publishing.
