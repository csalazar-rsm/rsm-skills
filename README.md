# RSM Codex Skills

Internal repository for sharing Codex skills used at RSM.

## Contents

- `rsm-pptx-design-system/`: Skill for the RSM presentation design system (palette, typography, layouts, spacing rules).

## Installation

> Requirement: `CODEX_HOME` is configured (e.g., `~/.codex`).

### Option A — Install with the built-in skill installer (recommended)

In a Codex session, run:

```
$skill-installer install https://github.com/csalazar-rsm/rsm-skills/tree/main/rsm-pptx-design-system
```

After installing a skill, restart Codex so it can load the new skill.

### Option B — Copy the skill manually

```bash
# from the directory where you cloned this repo
cp -R rsm-pptx-design-system "$CODEX_HOME/skills/"
```

## Usage

In a Codex session, you can explicitly invoke the skill by name:

```
$rsm-pptx-design-system
```

You can discover skills with the `/skills` command, or start typing `$` to mention one. Codex can also select the skill automatically if your prompt matches the task.
