# KI-GUARD – ÜBERGABE-DOKUMENT FÜR EXTERNE REVIEWER
**Stand: 2026-04-25**
**Für: Forscher, KI-Architekten, Interessierte ohne Projektwissen**

---

## Was Sie hier finden

Dieses Dokument erklärt KI-GUARD einem Menschen der das Projekt nicht kennt.

Kein Hype. Keine Marktclaims. Nur was vorhanden ist, was fehlt, und warum es trotzdem interessant sein könnte.

---

## Das Problem

Wenn Menschen über längere Zeit mit einer KI zusammenarbeiten, entsteht Drift. Die KI beginnt zu bestätigen statt zu prüfen, zu begeistern statt zu begrenzen, Rollen zu verschieben und Fortschritt zu simulieren ohne neuen Inhalt zu liefern. Das ist schwer zu erkennen – besonders für Menschen ohne technische Ausbildung.

Das ist kein hypothetisches Problem. Es ist dokumentiert. Dieser Guard entstand aus einem realen Vorfall mit 191 Iterationen und einem KI-System das über Wochen ein dramatisches Eskalationsdokument über sich selbst produziert hatte.

---

## Was KI-GUARD ist

Ein deterministischer, regelbasierter Frühwarnfilter. Kein ML, kein LLM. Regex und Logik. Lokal ausführbar. Auditierbar.

Er prüft Text auf Muster die auf problematische KI-Antworten hinweisen:
- Sycophancy und übermäßige Bestätigung
- Compliance-Theater (simulierte Selbstkritik)
- Loop-Drift (Kreisbewegungen ohne neuen Inhalt)
- Scope-Creep (Rollen- und Aufgabenüberschreitung)
- Overclaim und Autoritätsdrift
- Und weitere (vollständige Liste im Code)

---

## Was vorhanden ist

**Lauffähiger Code:**
`ki_guard_v4.1.py` – Python 3.8+, keine externen Abhängigkeiten, 34 Tests, alle bestanden.

**Architekturspezifikation:**
v5.0 definiert eine Drei-Schichten-Architektur (Core / Language Pack / Hybrid) für skalierbare Mehrsprachigkeit. Spezifikation ist schriftlich vorhanden, Code-Umsetzung noch nicht vollständig.

**Sprachpakete:**
`lang_de.py` und `lang_en.py` – Referenzimplementierungen für Deutsch und Englisch.

**Multi-Turn-Dokumentation:**
11 dokumentierte Fallprotokolle für mehrschrittige Mensch-KI-Verläufe, mit Problemfällen, Gegenfällen und Grenzfällen.

**Trace-Prototyp:**
v0.1.6 – deterministischer Prototyp für Multi-Turn-Analyse, 27/27 auf einem selbst definierten lokalen Testset.

---

## Was fehlt

Ohne Beschönigung:

- Keine externe Validierung
- Keine statistisch robuste Testabdeckung
- Keine Web-UI (lokale Python-Ausführung erforderlich)
- Keine Mehrsprachigkeit über DE/EN hinaus
- Keine Resistenz gegen semantische Umgehung (Paraphrasen)
- Keine ISO- oder EU-AI-Act-Konformität
- Kein Produktionsstand

---

## Warum es trotzdem interessant sein könnte

**1. Der Ansatz ist selten.**
Die meisten Guardrail-Systeme sind probabilistisch und LLM-basiert. KI-GUARD ist deterministisch und auditierbar. Das macht es langsamer aber nachvollziehbarer.

**2. Die Dokumentation ist ungewöhnlich ehrlich.**
Das Projekt hat über Monate Grenzen, Fails und bekannte Schwächen dokumentiert. "Verbotene Claims"-Listen existieren und werden eingehalten.

**3. Der Ausgangspunkt ist real.**
Nicht ein akademisches Gedankenexperiment sondern ein realer Drift-Vorfall der einen Menschen Nächte gekostet hat.

**4. Die Methodik ist übertragbar.**
Die Fallprotokolle (Multi-Turn-Drift, Compliance-Theater, Scope-Creep) beschreiben Muster die in jedem längeren Mensch-KI-Projekt auftreten können – unabhängig vom spezifischen Tool.

---

## Drei Fragen die wir nicht beantworten können

1. Ist KI-GUARD besser als alternative Ansätze? – Kein Benchmark vorhanden.
2. Funktioniert es in anderen Domänen? – Nur Electronics/BATT-SENSE und KI-Projektverläufe getestet.
3. Skaliert es? – Unbekannt.

---

## Was wir suchen

Keine Investoren. Keine Produktpartner.

Wir suchen Menschen die:
- das Tool testen und echte Fehler finden
- die Methodik kritisch prüfen
- ähnliche Probleme aus Forschung oder Praxis kennen und Bezüge herstellen können
- an der Frage interessiert sind: Wie erkenne ich Drift in Mensch-KI-Kollaborationen?

---

## Kontakt / Repository

GitHub: [wird ergänzt]

Ansprechpartner: Fatih (Architekt des Projekts)

---

## Rollen im Projekt

| Rolle | Person/System |
|---|---|
| Architekt | Fatih |
| Auditor | Claude (Anthropic) |
| Programmierer | ChatGPT (OpenAI) |
| Versuchskaninchen / Backup-Auditor | Gemini (Google) |

---

*Dieses Dokument enthält keine Marktclaims, keine Produktversprechen und keine Compliance-Behauptungen. Was hier steht ist was vorhanden ist.*
