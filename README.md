# kamal-claude-skills

Copie vendorisée (figée, versionnée) de skills Claude Code, pour une installation identique sur n'importe quelle machine (PC, nouveau PC, VPS) sans dépendre en continu des repos tiers d'origine.

## Installation

**macOS/Linux/VPS :**
```bash
git clone https://github.com/midoxavier/kamal-claude-skills.git
mkdir -p ~/.claude/skills
for s in humanizer copywriting ad-creative marketing-psychology cro; do
  ln -s "$(pwd)/kamal-claude-skills/skills/$s" ~/.claude/skills/$s
done
```

**Windows (pas besoin de droits admin — jonction de répertoire, pas un vrai symlink) :**
```powershell
git clone https://github.com/midoxavier/kamal-claude-skills.git $env:USERPROFILE\kamal-claude-skills
New-Item -ItemType Directory -Force -Path "$env:USERPROFILE\.claude\skills" | Out-Null
foreach ($s in "humanizer","copywriting","ad-creative","marketing-psychology","cro") {
  cmd /c mklink /J "$env:USERPROFILE\.claude\skills\$s" "$env:USERPROFILE\kamal-claude-skills\skills\$s"
}
```

## Contenu

| Skill | Source d'origine | Licence |
|---|---|---|
| `humanizer` | [blader/humanizer](https://github.com/blader/humanizer) | MIT |
| `copywriting` | [coreyhaines31/marketingskills](https://github.com/coreyhaines31/marketingskills) | voir LICENSE |
| `ad-creative` | [coreyhaines31/marketingskills](https://github.com/coreyhaines31/marketingskills) | voir LICENSE |
| `marketing-psychology` | [coreyhaines31/marketingskills](https://github.com/coreyhaines31/marketingskills) | voir LICENSE |
| `cro` | [coreyhaines31/marketingskills](https://github.com/coreyhaines31/marketingskills) | voir LICENSE |

Copie figée le 2026-10-30. Pour mettre à jour un skill, re-cloner le repo source et remplacer le dossier correspondant manuellement (jamais de sync automatique — c'est le but : contrôle de version, pas de dérive silencieuse).

Utilisé par le pipeline éditorial `verdictool.com` (`contenu/pipeline-v5/`) — voir `agents/phase-01-brief.md` pour le mapping skill ↔ phase.
