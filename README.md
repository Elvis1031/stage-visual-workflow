# Stage Visual Workflow

`stage-visual-workflow` is a Codex skill for evidence-backed stage-screen visual production. It turns a concert, gala, launch event, anniversary show, or performance project folder into a stage-accurate visual plan without allowing creative generation to redefine the physical LED geometry.

## What it does

- inventories meeting recordings, synchronized audio and shared-screen frames, transcripts, music, PPT/PDF files, stage models, drawings, references, prior versions, and feedback;
- verifies meeting statements against the shared screen at the same timecode;
- classifies conclusions as confirmed, provisional, reference-only, or unknown;
- creates one authoritative stage-lock master for real LED and no-image regions;
- builds timecoded Part/Cue, exact-text, forbidden-content, and unresolved-question tables;
- plans or produces distinct screen-visual concepts for each musical and narrative function;
- turns feedback into persistent, testable production rules;
- verifies that imagery, text, glow, particles, shadows, and simulated depth remain inside the real LED boundaries.

## Operating modes

- **Audit** — inspect project evidence and report conflicts without creating visual assets.
- **Plan** — produce stage locks, cue tables, text tables, visual briefs, prompts, and delivery plans.
- **Produce** — complete the planning gates, generate requested visual concepts, and verify stage fit.
- **Revise** — convert feedback into reusable rules and update only affected outputs.

## Core production rule

The physical stage is authoritative. A generated image can never prove that a surface is an LED screen. Unknown areas default to no-screen until confirmed by the latest reliable technical evidence.

## Installation

Install directly with the Skills CLI:

```bash
npx skills add https://github.com/Elvis1031/stage-visual-workflow --skill stage-visual-workflow
```

Or copy this repository into a user-level Codex skills directory:

```bash
git clone https://github.com/Elvis1031/stage-visual-workflow.git ~/.codex/skills/stage-visual-workflow
```

Restart Codex if the newly installed skill is not discovered immediately.

## Example requests

```text
Use stage-visual-workflow to audit this concert project folder and identify all confirmed LED regions, timing conflicts, and missing evidence.
```

```text
Use stage-visual-workflow to build the stage lock, Part/Cue table, exact-text table, and one stage-fit test frame before generating the remaining Parts.
```

```text
Revise the current screen-visual plan from the latest client meeting. Treat every explicit prohibition as a persistent rule and update only affected Parts.
```

## Expected inputs

The skill can work with project folders containing meeting video/audio, shared-screen captures, transcripts, supplied music, presentation files, technical drawings, stage models, reference images, feedback records, and previous deliverables. A narrower task may use only the relevant subset.

## Typical outputs

- synchronized audio-to-screen evidence table;
- evidence authority and conflict log;
- authoritative stage-lock master;
- timecoded musical structure and Part/Cue table;
- exact-text and forbidden-content tables;
- visual briefs and generation prompts;
- stage-fit test frames and reviewed concepts;
- versioned revision records and delivery notes.

## Repository structure

```text
stage-visual-workflow/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    └── full-workflow.md
```

- `SKILL.md` contains routing rules, invariants, and the essential workflow.
- `references/full-workflow.md` contains the complete procedure for new programs and full-project analysis.
- `agents/openai.yaml` provides UI-facing skill metadata.

## Important limitations

- Automatic transcripts are navigation aids, not final evidence; material statements must be checked against the audio.
- Meeting audio and shared-screen frames must be reviewed together when they are used to establish a visual requirement.
- Generated typography that is inaccurate should be replaced by deterministic typesetting.
- This skill does not replace venue engineering approval, media-server testing, LED processor configuration, or final on-site calibration.
