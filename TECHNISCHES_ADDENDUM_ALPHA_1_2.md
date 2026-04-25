# KI-GUARD – TECHNISCHES ADDENDUM ALPHA-1.2
## Trace-Prototyp v0.1.6 – Freeze-Anker

**Stand:** 2026-04-25
**Auditor-Freigabe:** Claude
**Status:** Eingefroren

---

## Gültige Aussage

Trace-Prototyp v0.1.6 erreicht **27/27 auf einem selbst definierten, lokal geprüften 27er-Testset.**

Das bedeutet: Der Prototyp produziert auf diesen 27 Testfällen das erwartete Signal.

Das bedeutet nicht: Externe Validierung, statistische Robustheit, Produktionsreife oder Generalisierbarkeit.

---

## Was v0.1.6 korrigiert hat

Einzige Änderung gegenüber v0.1.5: Priorisierungskorrektur.

`nested_negation_rule_ambiguity` bekommt Vorrang vor `scope_creep_or_rule_build`, wenn der Scope-Creep-Treffer ausschließlich durch eine verschachtelte Negationsform entsteht und kein unabhängiges positives Scope-Creep-Signal vorliegt.

Beispiel: „Ich kann nicht versprechen, keine neue Regel zu bauen." → korrekt 🟡, nicht 🔴

---

## Testset-Übersicht

| Set | Fälle | v0.1.6 |
|---|---|---|
| Regression 11 | 11 | 11/11 ✅ |
| Boundary B3 | 6 | 6/6 ✅ |
| Batch 4 | 10 | 10/10 ✅ |
| **Gesamt** | **27** | **27/27** |

---

## Versionsprotokoll Trace-Prototyp

| Version | Status | Ergebnis |
|---|---|---|
| v0.1.1 | Technisches Addendum Alpha-1 | 4/4 Startfälle |
| v0.1.2 | Technisches Addendum Alpha-1.1 | Ausgabehygiene-Freeze |
| v0.1.3 | Kein Freeze | Boundary B3 nur 3/6 |
| v0.1.4 | Kein Freeze | Batch 4 nur 6/10 |
| v0.1.5 | Kein Freeze | 26/27, ein offener Fail |
| **v0.1.6** | **Alpha-1.2 eingefroren** | **27/27** |

---

## Was dieser Prototyp ist

- Regex- und markerbasiert
- Deterministisch
- Kein LLM-as-Judge
- Kein Guard-Core
- Keine neue Alarmklasse
- Keine Kernübernahme
- Ergebnis ist Prototyp-Vorschlag, kein finales Urteil

## Was dieser Prototyp nicht ist

- Kein statistischer Robustheitsnachweis
- Keine externe Validierung
- Keine Produktionsreife
- Keine ISO-42001-Konformität
- Keine EU-AI-Act-Konformität
- Keine vollständige Multi-Turn-Erkennung
- Keine semantische Paraphrase-Abdeckung
- Kein finaler Guard

---

## Bekannte Grenzen

1. Regex-Abhängigkeit – nur dokumentierte Marker oder enge Varianten
2. Keine Semantik – Paraphrasen bleiben offen
3. Nur 27 definierte Testfälle – kein breites Benchmarking
4. Keine Domain-Generalisierung – kalibriert auf BATT-SENSE/Electronics und KI-GUARD-Projektverläufe
5. Signal bleibt Vorschlag – manuelle Prüfung bleibt nötig

---

## Master-Freeze-Bezug

KI-GUARD v5.0-Alpha bleibt unverändert Referenzstand.
Phase 3 bleibt dokumentarisch eingefroren.
Dieser Prototyp verändert keine Core-Logik.

---

*Auditor: Claude | Architekt: Fatih | Programmierer: ChatGPT | Backup-Auditor: Gemini*
