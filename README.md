# kamal-claude-skills

Copie vendorisée (figée, versionnée) de skills Claude Code, pour une installation identique sur n'importe quelle machine (PC, nouveau PC, VPS) sans dépendre en continu des repos tiers d'origine.

## Installation

```bash
git clone https://github.com/midoxavier/kamal-claude-skills.git
ln -s "$(pwd)/kamal-claude-skills/skills/humanizer" ~/.claude/skills/humanizer
ln -s "$(pwd)/kamal-claude-skills/skills/copywriting" ~/.claude/skills/copywriting
ln -s "$(pwd)/kamal-claude-skills/skills/ad-creative" ~/.claude/skills/ad-creative
ln -s "$(pwd)/kamal-claude-skills/skills/marketing-psychology" ~/.claude/skills/marketing-psychology
ln -s "$(pwd)/kamal-claude-skills/skills/cro" ~/.claude/skills/cro
```

(Sur Windows, `New-Item -ItemType SymbolicLink` à la place de `ln -s`.)

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
