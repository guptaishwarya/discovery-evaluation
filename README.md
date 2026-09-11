# Discovery Evaluation Skill — V1

A PM discovery co-pilot that helps builders identify what is necessary to solve a real problem before they overbuild.

## Core principle

> Don't encode what the model can reason. Encode what a good PM knows to ask.

## V1 mechanisms

1. Problem vs Solution
2. Two-Journey Framework
3. Assumption Challenge

## Architecture

- `SKILL.md` — orchestration instructions
- `state/schema.json` — structured discovery state
- `mechanisms/` — reusable PM questioning assets
- `tests/scenarios.md` — manual test scenarios

GitHub is the source of truth. The skill is executed by an LLM environment that loads this repository.

## V1 goal

Move a builder from:

"I have an idea and many things I could build."

to:

"I understand the problem, the user friction, why AI is or isn't useful, what assumption matters most, and what I actually need to build."

## What V1 intentionally does not include

- database or persistent storage
- UI
- API
- autonomous agent
- evaluation dashboard
- additional discovery frameworks

First prove that the discovery behavior is useful.
