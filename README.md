# Claude Pretzel Cutter

WAT framework skeleton for Claude agent-driven workflows.

## Project layout

- `CLAUDE.md` — agent instructions and project conventions
- `tools/` — deterministic Python scripts for execution
- `workflows/` — SOP-style workflow documentation
- `.tmp/` — disposable temporary outputs
- `.env` — local secrets and API keys (gitignored)
- `credentials.json`, `token.json` — Google OAuth artifacts (gitignored)

## Setup

1. Create a `.env` file from `.env.example`.
2. Add any required API keys or credentials.
3. Add tools into `tools/` and workflows into `workflows/`.

## Pretzel Cutter prototype

A simple desktop prototype is available in `pretzel_cut.py`.

### Run the game

1. Install Python 3.11 or newer from python.org if you don't already have it.
2. Open a terminal in this folder.
3. Install the dependency:
   - `python3 -m pip install -r requirements.txt`
4. Start the game:
   - `python3 pretzel_cut.py`

### How to play

- Move the mouse to position the knife over the pretzel.
- Use the left/right arrow keys to rotate the knife.
- The goal is to get the weight on each side as balanced as possible.

## Notes

- Do not commit `.env`, `.tmp`, `credentials.json`, or `token.json`.
- Keep workflows simple: one objective, required inputs, tool references, expected outputs.
- Keep tools deterministic and reusable.
