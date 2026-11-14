# Team 4 — Track 1: AI Task Factory

Click-based task generation and validation prototype for the Innodata Hackathon.

## Contents

- `track1_freestyle/`: implementation, five generated tasks, development candidates, demo task, validation evidence, run logs, and resource records.
- `track1_submission/`: the submission folder `team4_Track1/` and `team4_Track1.zip` (validated: `validate_submission.py` → 0 errors).
- `organizer/`: Track 1 instructions, harness, worked example, general event brief, and presentation template. Track 2 materials are excluded.

## Demo and presentation (quick links)

- **Live demo script** (commands, timings, talking points): [`track1_submission/team4_Track1/DEMO.md`](track1_submission/team4_Track1/DEMO.md)
- **Live demo run**: the commands and results (fresh task in 48 s; Harbor self-check `ALL SOUND`, gold 1.0 / nop 0.0) are in [`track1_submission/demo_live/`](track1_submission/demo_live/)
- **Demo task as the AI agent sees it** (rendered): [open in browser](https://htmlpreview.github.io/?https://github.com/tianluoboding/team4_track1/blob/main/track1_submission/demo_live/demo_task.html)
- **Presentation** (5 slides): [`track1_submission/team4_presentation_FINAL.pptx`](track1_submission/team4_presentation_FINAL.pptx)
- **Submitted ZIP**: [`track1_submission/team4_Track1.zip`](track1_submission/team4_Track1.zip) (SHA-256 in `team4_Track1.zip.sha256`, `validate_submission.py` 0 errors)
- **Experimental LLM generator + difficulty feedback loop** (not scored): [`track1_llm_factory/`](track1_llm_factory/)

## Current status

The developer report states that all five tasks passed Harbor oracle/nop self-checks and the organizer submission validator reported zero errors and warnings. These historical results have not been rerun during this GitHub import.

The generator uses five predefined feature blueprints with parameterized variations. It does not independently discover new feature families. No model benchmark has run, so task difficulty and resolve@k are unproven. Validation used rootless Podman; Docker execution and a cache-free image build remain unverified.

See [implementation instructions](track1_freestyle/README.md), [variation strategy](track1_freestyle/VARIATION_WRITEUP.md), and `track1_freestyle/evidence/` for details. Paths referring to the original Erdos machine may need adapting locally. The downloaded virtual environment and nested Git metadata are excluded; recreate dependencies from the requirements files.

## Archive integrity

The first import (`945f5f5`) contained a truncated `track1_submission/TeamName_Track1.zip` (786,432 bytes) and many empty or missing files. Commits `88ea287` and `ee74c0e` replaced both folders with the complete originals from the Erdos machine. `TeamName_Track1.zip` is now 3,584,863 bytes, passes `unzip -t`, and passes `harness/validate_submission.py` with 0 errors. It has since been renamed to `team4_Track1.zip` (team name: team4) and rebuilt with the updated README; the rebuilt ZIP also passes `validate_submission.py` with 0 errors.
