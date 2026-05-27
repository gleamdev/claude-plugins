# Gleam plugin skills

Each skill is a directory containing a `SKILL.md` file:

```
skills/
└── my-skill/
    └── SKILL.md
```

`SKILL.md` starts with YAML frontmatter, then the instructions:

```markdown
---
name: my-skill
description: One line describing when Claude should use this skill.
---

Instructions for the skill go here.
```

Once the plugin is installed, skills are invoked as `/gleam:my-skill`.
