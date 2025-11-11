cs4500-f18-fest

# IMPORTANT CHANGES BY ME (Luc)
```
The teams are no longer in the manifest file.
To decouple it, there's a require line in main.rkt
(file "/course/cs4400f25/ta4400/TEAMS_DONT_TOUCH.rkt")
- There should be a list of strings of team names in this file.
- The manifest still has team-name*, but it is empty

There is an other-exe-names variable in this same TEAMS_DONT_TOUCH.rkt file. This is for alternative exe names.
- This can be used if I'm rerunning for a group that made a small typo in the exe name. 
```
===

Package for running a TEST FEST on student submissions.

Abilities:
- `git checkout` students last commit before a deadline
- run student executables (if present) against staff tests
- use staff executable to validate student tests (if any)
- run a TESTFEST of all student executables on all other student tests


Install
---

In this directory:

```
  $ raco pkg install
```


Documentation
---

After installing, run:

```
  $ raco docs cs4500-f18-fest
```

For the source, check the `scribblings` entry in `./info.rkt`


Usage
---

Basically,

1. Make a `#lang cs4500-f18-fest/manifest` file with paths to executables
2. Run `./xfest <FILE.cs4500>` on your manifest
3. Follow the interactive prompts
4. Results get saved to a directory

See the documentation for details.
