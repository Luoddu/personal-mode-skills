# Personal conversation modes

Three Chinese language Codex skills:

| Skill | Purpose |
| --- | --- |
| `think-clearly`（澄清模式） | Clarify the goal one question at a time and test assumptions before recommending a direction. |
| `battle-plan`（作战模式） | Agree on deliverables, scope, and acceptance before starting a larger task. |
| `present-clearly`（呈现模式） | Turn your views or findings into a clear paragraph, adjust conversational or formal expression, and keep material cautions outside the draft. |

## Install

Copy each skill directory into your personal skills directory, for example `~/.agents/skills/`. Keep `SKILL.md` and `agents/openai.yaml` together.

Start them with `澄清模式：`, `作战模式：`, or `呈现模式：`. The full trigger and exit rules are in each `SKILL.md`.

## Presentation mode

Use `呈现模式，自然一点：` followed by your material for conversational expression, or `呈现模式，书面一点：` for more formal writing. After receiving a draft, say `再自然一点` or `再书面一点` to adjust the latest version while keeping your main point and stance.

The default output is one ready-to-use paragraph. Material cautions appear separately when needed. The skill supports papers, reports, and personal reflections; it preserves your viewpoint without inventing facts or evidence.

These skills are conversation instructions. Installing them does not connect them to another project's runtime or grant permission for external actions.
