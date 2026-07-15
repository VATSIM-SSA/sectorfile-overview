# VATSSA's Sector File Development Overview Repository

## How to Contribute

Branch Naming Conventions

- feature/
- bug/
- hotfix/
- docs/

## Commit Message Conventions

- <type>([optional scope]): <description> # subject
- type can be feat:, fix:, style:, doc:

## Current Global Plugins
### TopSky
- Stable: 2.5
- Beta: 2.6 beta 4

### GroundRadar
- Stable: 1.5
- Beta: 1.6 beta 6


## Deploying shared files to the sector-file repos

Files every sector-file repo should carry — plugin binaries, vATIS profile data,
GitHub issue templates — live **here** and are pushed out automatically on merge
to `main`.

**It is all controlled by one file: [`.github/sync.yml`](.github/sync.yml).**

| I want to… | Do this |
|---|---|
| Sync a new file or folder | Add one `src`/`dest` entry under `sync:` |
| Onboard a new sector-file repo | Add one line under `targets:` |
| Stop syncing something | Delete its entry |
| Remove a file from every repo | Delete it here — the mirror removes it there |

Nothing else needs editing. The workflow
([`sync-to-sectorfiles.yml`](.github/workflows/sync-to-sectorfiles.yml)) reads
`sync.yml` and does the rest.

### How it behaves

- **Folders are mirrored** (`rsync --delete`) — add, change, or **delete** a file
  here and the same happens in every target repo. Both the stable and beta DLLs
  in a plugin folder are covered without listing them.
- **`src` and `dest` may differ** — e.g. `vatis/airports-json` lands at
  `Plugins/vATIS Profile/Airports`.
- **A missing `src` fails the run loudly.** A sync that quietly does nothing is
  worse than one that visibly breaks.
- Repos sync **independently** (`fail-fast: false`) — one broken repo never
  blocks the other 24. Each repo is serialised against itself, and a rejected
  push rebases and retries once.
- Only changed repos get a commit; the rest report "already up to date".
- Run it by hand any time from the **Actions** tab (`workflow_dispatch`). Safe —
  it only pushes where something actually differs.

## Current Sector File Repositories

> This list is documentation for humans. The list the automation actually uses is
> `targets:` in [`.github/sync.yml`](.github/sync.yml) — keep the two in step.

- [DGAC Accra](https://github.com/VATSIM-SSA/sectorfile-dgac)
- [DNKK Kano](https://github.com/VATSIM-SSA/sectorfile-dnkk)
- [FASA South Africa](https://github.com/VATSIM-SSA/sectorfile-fasa)
- [FBGR Gaborone](https://github.com/VATSIM-SSA/sectorfile-fbgr)
- [FCCC Brazzaville](https://github.com/VATSIM-SSA/sectorfile-fccc)
- [FIMM Mauritius](https://github.com/VATSIM-SSA/sectorfile-fimm)
- [FLFI Lusaka](https://github.com/VATSIM-SSA/sectorfile-flfi)
- [FMMM Antananarivo](https://github.com/VATSIM-SSA/sectorfile-fmmm)
- [FNAN Luanda](https://github.com/VATSIM-SSA/sectorfile-fnan)
- [FQBE Beira](https://github.com/VATSIM-SSA/sectorfile-fqbe)
- [FSSS Seychelles](https://github.com/VATSIM-SSA/sectorfile-fsss)
- [FVHF Harare](https://github.com/VATSIM-SSA/sectorfile-fvhf)
- [FWLL Lilongwe](https://github.com/VATSIM-SSA/sectorfile-fwll)
- [FYWF Windhoek](https://github.com/VATSIM-SSA/sectorfile-fywf)
- [FZZA Kinshasa](https://github.com/VATSIM-SSA/sectorfile-fzza)
- [GOOO Dakar](https://github.com/VATSIM-SSA/sectorfile-gooo)
- [GVSC Sal](https://github.com/VATSIM-SSA/sectorfile-gvsc)
- [HKNA Nairobi](https://github.com/VATSIM-SSA/sectorfile-hkna)
- [HTDC Dar es Salaam](https://github.com/VATSIM-SSA/sectorfile-htdc)
- [HUEC Entebbe](https://github.com/VATSIM-SSA/sectorfile-huec)

- [GOOOO Dakar Oceanic](https://github.com/VATSIM-SSA/sectorfile-goooo)
- [FAJO Johannesburg Oceanic](https://github.com/VATSIM-SSA/sectorfile-fajo)

- [AFRC Africa Central](https://github.com/VATSIM-SSA/sectorfile-afrc)
- [AFRS Africa South](https://github.com/VATSIM-SSA/sectorfile-afrs)
- [AFRW Africa West](https://github.com/VATSIM-SSA/sectorfile-afrw)
