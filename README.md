# Skills

A collection of Claude skills I've built and use, shared so others can use, adapt, and learn from them.

A skill is a folder with a `SKILL.md` file (plus optional scripts, templates, or reference files) that teaches Claude how to handle a specific kind of task. Claude reads the skill's description to decide when it's relevant, then follows the instructions inside.

## Skills in this repo

| Skill | What it does |
|-------|--------------|
| [`example-skill`](./example-skill) | Short description of what the skill does and when it triggers. |

<!-- Add a row for each skill as you publish it. -->

## Repository structure

```
skills/
├── README.md
├── LICENSE
└── skill-name/
    ├── SKILL.md          # required: frontmatter (name, description) + instructions
    ├── CHANGELOG.md      # version history for this skill
    ├── scripts/          # optional: helper scripts
    ├── references/       # optional: docs Claude can load when needed
    └── assets/           # optional: templates, images, fonts
```

## Using a skill

**Claude Code:** copy the skill folder into `~/.claude/skills/` to make it available in all your projects, or into `.claude/skills/` inside a project to use it only there.

```bash
git clone https://github.com/depuschm/skills.git
cp -r skills/skill-name ~/.claude/skills/
```

**Claude apps (claude.ai / desktop):** zip the skill folder and upload it in Settings under Skills.

## Versioning

Each skill is versioned independently using [semantic versioning](https://semver.org/):

- **Major** (`2.0.0`): behavior changes that could break how you use the skill
- **Minor** (`1.1.0`): new capabilities, backwards compatible
- **Patch** (`1.0.1`): fixes and wording improvements

Releases are marked with Git tags in the format `skill-name/vX.Y.Z`, and every skill has a `CHANGELOG.md` describing what changed. To grab a specific version:

```bash
git checkout skill-name/v1.2.0
```

To see all versions of a skill:

```bash
git tag -l "skill-name/*"
```

## Contributing

Issues and suggestions are welcome. If a skill doesn't trigger when you expect it to, or produces something off, open an issue with the prompt you used and what happened.

## License

Released under the [MIT License](./LICENSE). Use, modify, and share freely.
