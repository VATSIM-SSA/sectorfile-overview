# VATSSA's Sector File Development Overview Repository

## Managing Sector File Repositories

### Managing the Git Ignore

In order to avoid the commit, merge and upload of irrelevant static (PDF, Sounds) files or GNG Generated Files, all Sector File Repositories will contain a .gitignore file with the following Structure:

`// File Type Exclusions
_.prf
_.ese
_.sct
_.rwy
\*.pdf

// Folder Exclusions
FBGR/Alias/_
FBGR/NavData/_
FBGR/ICAO/_
FBGR/Sounds/_

// File Exclusions
\*aeronav_copyright.txt`
