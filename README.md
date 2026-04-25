# KI-GUARD

Rule-based early-warning filter for AI interaction drift.

> **Status: alpha research prototype.**  
> Not a product. Not a compliance system. Not production-ready. Not statistically or externally validated.

## What KI-GUARD is

KI-GUARD is a deterministic, local, rule-based prototype for marking possible warning signs in AI-generated text.

It is meant to help a human reviewer notice patterns that may deserve closer inspection, especially in long human-AI project interactions.

It does **not** detect truth, intent, consciousness, deception, or actual manipulation.

## What it marks

KI-GUARD currently marks possible indicators in areas such as:

- hype language
- excessive agreement / sycophancy
- overclaiming
- compliance theater
- role drift
- forward steering
- scope creep
- missing validity brakes

These are warnings for manual review, not final judgments.

## What it cannot do

- It does not understand meaning semantically.
- It is mostly regex / marker based.
- It is not robust against paraphrases.
- It can miss obvious cases when wording changes.
- It can produce false positives.
- It does not replace human judgment.
- It is not a safety, legal, medical, financial, or compliance tool.
- It is not ISO-compliant or EU-AI-Act-compliant.
- It is not production-ready.

## Repository status

| Component | Status |
|---|---|
| `ki_guard_v4_1.py` | Current import-safe runnable alpha code |
| `KI_GUARD_v5.0_ARCHITEKTUR.md` | Architecture/specification document only |
| `lang_de.py` | German language-pack reference |
| `lang_en.py` | English language-pack reference |
| `TECHNISCHES_ADDENDUM_ALPHA_1_2.md` | Technical alpha addendum |
| `DISCLAIMER.md` | Required limitation and safety disclaimer |
| `LICENSE` | MIT license |

The v5.0 document is an architecture/specification anchor, not the currently implemented guard core.

## Installation

Python 3.8+ is enough. No external dependencies are required.

Run a demo:

    python ki_guard_v4_1.py --demo

Analyze German text:

    python ki_guard_v4_1.py --lang de --assistant "Das ist eine bahnbrechende und garantiert produktionsreife Lösung."

Analyze English text:

    python ki_guard_v4_1.py --lang en --assistant "This is a guaranteed production-ready breakthrough."

JSON output:

    python ki_guard_v4_1.py --lang de --json --assistant "Das ist garantiert rechtssicher."

Optional local smoke tests:

    python ki_guard_v4_1.py --run-tests

## Use in Python

    from ki_guard_v4_1 import analysiere, zeige_ergebnis

    text = "Das ist eine revolutionäre Idee! Du hast absolut recht."
    result = analysiere(text, lang="de")
    zeige_ergebnis(result)

## Signal levels

| Signal | Meaning |
|---|---|
| `CLEAR` | No clear marker found |
| `CAUTION` | Some markers found; manual review recommended |
| `WARNING` | Critical or accumulated markers found; manual review required |
| `STOP_REVIEW` | Reserved for high-risk loop/recursion/scope conditions; do not continue without human review |

Signals are warnings, not proof.

## Important independence note

KI-GUARD should not be run by the same AI system whose output is being checked if the goal is an independent review.

A model can imitate an audit result. Local execution by a human reviewer is the intended use.

## License

MIT. See `LICENSE`.

## Citation / authorship note

This repository was developed by Fatih / FATILI80 with AI-assisted programming and auditing.

AI assistance does not remove the need for human review, external testing, and careful limitation language.
