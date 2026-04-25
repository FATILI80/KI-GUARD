# DISCLAIMER

## Alpha research prototype

KI-GUARD is an alpha-stage research and documentation prototype for marking possible signs of AI interaction drift, sycophancy, overclaiming, loop behavior, and process-integrity risks.

It is not a production system, not a safety system, not a compliance product, and not a certification tool.

## No reliability guarantee

The current implementation is rule-based and marker-based. It does not understand meaning, intent, truth, context, or real-world validity. It can miss problematic outputs and it can flag harmless outputs.

Known limitations include, but are not limited to:

- false positives
- false negatives
- paraphrase blindness
- sensitivity to wording and spelling
- limited multi-turn coverage
- narrow internal test coverage
- no statistical validation
- no external benchmark validation
- no guarantee of robustness across domains, languages, models, or use cases

## Human review required

All KI-GUARD outputs must be treated as review signals only. A human reviewer must make the final judgment. The tool must not be used as the sole basis for decisions about safety, compliance, legality, medical advice, financial advice, employment, education, access control, moderation, or other high-impact contexts.

## No compliance claim

This repository does not claim compliance with ISO standards, the EU AI Act, NIST AI RMF, SOC 2, automotive safety standards, medical device standards, or any other regulatory or certification framework.

## No warranty

The software and documentation are provided "as is", without warranty of any kind. Use at your own risk. The authors and contributors are not liable for damages or consequences resulting from use, misuse, interpretation, or reliance on this repository.

## Intended use

This repository is intended for research, documentation, review, educational analysis, and controlled experimentation. It is not intended for deployment as a live guardrail in production systems without independent testing, external review, risk assessment, and substantial additional engineering.
