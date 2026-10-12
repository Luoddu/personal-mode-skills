# Personal conversation modes

Four Chinese language Codex skills:

| Skill | Purpose |
| --- | --- |
| `think-clearly`（澄清模式） | Clarify the goal one question at a time and test assumptions before recommending a direction. |
| `battle-plan`（作战模式） | Agree on deliverables, scope, and acceptance before starting a larger task. |
| `present-clearly`（呈现模式） | Turn your views or findings into a clear paragraph, adjust conversational or formal expression, and keep material cautions outside the draft. |

| `research-figure-demo`（科研绘图示范模式） | Analyze figure choices, offer two visible layout candidates or draw directly, and use the confirmed Origin-style statistical-plot template. |

## Install

Copy each skill directory into your personal skills directory, for example `~/.agents/skills/`. Copy the complete directory, including `SKILL.md`, `agents/openai.yaml`, and `references/`; copying only SKILL.md omits the plotting template.

Start them with `澄清模式：`, `作战模式：`, `呈现模式：`, or `进入示范模式`. The full trigger and exit rules are in each `SKILL.md`.

## Presentation mode

Use `呈现模式，自然一点：` followed by your material for conversational expression, or `呈现模式，书面一点：` for more formal writing. After receiving a draft, say `再自然一点` or `再书面一点` to adjust the latest version while keeping your main point and stance.

The default output is one ready-to-use paragraph. Material cautions appear separately when needed. The skill supports papers, reports, and personal reflections; it preserves your viewpoint without inventing facts or evidence.

## Research figure demonstration mode

Use `进入示范模式` or `请你分析并示范` with research figures, paper panels, or academic slides. The default is to explain choices and provide two visible layout candidates before refinement. Use `直接示范` for one completed version. Revisions to a chosen figure proceed directly. Ordinary software demonstrations do not activate the scientific style.

The bundled [Origin-style plot template](research-figure-demo/references/origin-report-style.md) defines the 272×208 mm page, layer geometry, 36 pt axis titles, 34 pt tick labels, 3 pt frame and error-bar lines, 10 pt symbols, and 8 pt full cap width. It also records axis-endpoint rules and the explicit baseline-margin exception.

Artwork defaults to transparent backgrounds and removes unnecessary white backdrops, invisible placeholders, and redundant clipping objects. Meaningful axes, outlines, and scientific data are preserved. The template includes font checks, error-bar semantics, editable SVG and PNG delivery, and render verification. It contains no experiment data.

### Access on another device

1. Download or clone this repository.
2. Copy the complete `research-figure-demo` folder into the personal skills directory used on that device (for example `~/.agents/skills/`, alongside the other modes).
3. Make Times New Roman Bold/Bold Italic and Microsoft YaHei Bold available for matching typography. The rules do not depend on a machine-specific font path.
4. Invoke `进入示范模式`. To update later, pull/download the latest repository and replace the installed folder after preserving any local customizations. GitHub access alone does not automatically update installed local copies.

These skills are conversation instructions. Installing them does not connect them to another project's runtime or grant permission for external actions.
