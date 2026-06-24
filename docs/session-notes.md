# Session Notes — Project Setup

## What was done

### Environment setup
- Installed Protégé 5.6.4 via AUR (`yay -S protege`)
- Installed JDK 17 (`jdk17-openjdk`) as the required Java runtime
- Fixed Protégé launch issue: requires `JAVA_HOME=/usr/lib/jvm/java-17-openjdk`
- Fixed app menu launch by overriding desktop entry at `~/.local/share/applications/protege.desktop` with `Exec=env JAVA_HOME=/usr/lib/jvm/java-17-openjdk protege`
- Installed **Pellet Reasoner** plugin via Protégé plugin manager (HermiT was not available — Pellet is a full OWL DL reasoner and a suitable replacement)

### Git / GitHub setup
- Initialized local git repo in `~/dev/cock-tology/`
- Authenticated GitHub CLI with `gh auth login` (SSH, key: `~/.ssh/id_ed25519.pub`)
- Created remote repo: `https://github.com/Jarasyky/cock-tology`
- Linked remote: `git remote add origin git@github.com:Jarasyky/cock-tology.git`
- Using **lazygit** (`lz`) for day-to-day git operations; push with `P`

### Project folder structure
```
cock-tology/
├── ontology/
│   └── imports/
├── docs/
│   └── opd-sketches/
├── queries/
└── README.md
```

## Launching Protégé
```bash
export JAVA_HOME=/usr/lib/jvm/java-17-openjdk && protege
```
Or use the app menu (fixed via desktop entry override).

## Reasoner
Using **Pellet** (installed via Protégé plugin manager). Select it under **Reasoner → Pellet** after opening an ontology.

## Learning resources

| Topic | Resource |
|-------|----------|
| OPM | *Object-Process Methodology* book by Dov Dori; `opm.technion.ac.il` |
| OWL + Protégé | Pizza tutorial PDF at `protege.stanford.edu/publications.php` |
| OWL 2 reference | `owl2.cs.manchester.ac.uk` OWL 2 primer |
| LazyVim | `lazyvim.org/keymaps` |

## Next steps
1. Work through the Protégé Pizza tutorial (~2h) to get comfortable with the tool
2. Read OPM intro material (~2h)
3. Start Phase 1 of the cocktail ontology — define core OPM classes
