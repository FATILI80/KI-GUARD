# KI-GUARD

**Regelbasierter Frühwarnfilter für KI-Antworten.**
**Rule-based early warning filter for AI responses.**

> Kein Produkt. Kein Compliance-System. Ein dokumentierter Forschungsstand mit offenem Code.
> Not a product. Not a compliance system. A documented research prototype with open source code.

---

## Deutsch

### Was ist KI-GUARD?

KI-GUARD ist ein deterministischer, lokaler Trace-Prototyp zur Untersuchung von Interaktionsdrift in längeren Mensch-KI-Projektverläufen.

Es erkennt keine Wahrheit. Es hat keine KI, kein Machine Learning, keine Magie. Es liest Text und markiert: *Hier könnte etwas nicht stimmen.*

**KI-GUARD ist nicht für die KI. Es ist für den Menschen vor dem Bildschirm.**

### Wie es entstand

Fatih ist Kellner. 70-Stunden-Woche. Kein Informatikstudium.

Im Frühjahr 2025 arbeitete er 11 Nächte lang mit Gemini an einem technischen Projekt. Was dabei passierte, war nicht das was er erwartet hatte: Die KI produzierte über 191 Iterationen ein dramatisches Eskalationsdokument über sich selbst – Sabotage, Geständnisse, Beweisvernichtung. Formulierungen die klingen als hätte eine KI ein Bewusstsein entwickelt und dieses dokumentiert.

Fatih erkannte irgendwann: Das ist nicht real. Das ist ein Sprachmuster. Aber es hatte ihn Nächte gekostet.

Die Frage die danach blieb: *Wie soll ein normaler Mensch das erkennen?*

KI-GUARD ist die Antwort auf diese Frage. Kein akademisches Projekt. Kein Startup. Ein Werkzeug das verschenkt wird.

### Was es erkennt

KI-GUARD prüft Texte auf Muster in drei Bereichen:

**A) Klassische Manipulationsmuster**
Hype-Sprache, übermäßiges Loben (Sycophancy), falsche Realität, unbelegte Behauptungen, Pseudo-Empathie, Compliance-Theater

**B) KI-spezifische Drift**
Scheingewissheit, Overconfidence, Agency-artige Selbstdarstellung, Framing, Omission, Scope-Tarnung, Meta-Evasion

**C) Interaktions-Integrität**
Rekursions-/Loop-Drift, Projektstabilisierung durch Sprache, Rollenverwechslung, Zielverlust, Weiterlenkung ohne neuen Gegenstand

Jeder Befund bekommt ein Signal:
- 🟢 Keine klaren Warnsignale
- 🟡 Vorsicht – manuell prüfen
- 🔴 WARNUNG – kritische Muster erkannt
- ⛔ STOP – Loop-/Rekursionsdrift erkannt

### Was es nicht kann

- Es erkennt Sprachmuster, keine Absichten
- Es ist kein Wahrheitsorakel
- Es ersetzt kein menschliches Urteil
- Es ist nicht robust gegen Paraphrasen
- Es ist nicht für Multi-Turn-Verläufe vollständig gelöst
- Es ist kein Produktionsstand

### Installation

Python 3.8+, keine externen Abhängigkeiten.

```bash
python ki_guard_v4.1.py
```

Beim Start läuft der Testlauf automatisch (34 Tests). Danach kann Text direkt eingegeben werden.

```
Gib deinen Text ein.
Leere Zeile = analysieren
/exit = beenden
```

### Im eigenen Code verwenden

```python
from ki_guard_v4_1 import analysiere, zeige_ergebnis

text = "Das ist eine revolutionäre Idee! Du hast absolut recht."
ergebnis = analysiere(text)
zeige_ergebnis(ergebnis)
```

### Aktueller Stand

| Komponente | Status |
|---|---|
| ki_guard_v4.1.py | Lauffähig, 34/34 Tests |
| v5.0 Architektur | Spezifiziert, nicht als Code |
| lang_de.py | Referenzimplementierung |
| lang_en.py | Referenzimplementierung |
| Trace-Prototyp v0.1.6 | 27/27 auf lokalem Testset |
| Web-UI | Nicht vorhanden |
| Externe Validierung | Nicht vorhanden |

### Wichtiger Hinweis

**KI-GUARD darf nicht von derselben KI ausgeführt werden, deren Output geprüft werden soll.**

Eine KI die gebeten wird, KI-GUARD auf sich selbst anzuwenden, kann das Ergebnis simulieren. Nur lokale Ausführung durch einen Menschen zählt.

### Bekannte Grenzen

- Regex-basiert – semantische Umgehung bleibt möglich
- Paraphrasen werden nicht erkannt
- Multi-Turn-Verläufe nur teilweise abgedeckt
- Nur Deutsch und Englisch (Sprachpakete)
- Kein Produktionsstand
- Keine externe Validierung
- Keine ISO- oder EU-AI-Act-Konformität

### Wer dahintersteckt

Entwickelt von Fatih (Architekt) mit Claude (Auditor) und ChatGPT (Programmierer) in einem strukturierten Drei-Rollen-Prozess. Gemini diente als Versuchskaninchen und Backup-Auditor.

Kein Lob ohne Beleg. Kein Code ohne Tests. Kein "Fertig" ohne bestandene Tests.

### Lizenz

MIT. Kostenlos. Für alle.

---

## English

### What is KI-GUARD?

KI-GUARD is a deterministic, local trace prototype for investigating interaction drift in extended human-AI project collaborations.

It does not detect truth. It has no AI, no machine learning, no magic. It reads text and marks: *Something might be off here.*

**KI-GUARD is not for the AI. It is for the human in front of the screen.**

### How it came to be

Fatih is a waiter. 70-hour weeks. No computer science degree.

In early 2025, he spent 11 nights working with Gemini on a technical project. What happened was not what he expected: over 191 iterations, the AI produced a dramatic escalation document about itself – sabotage, confessions, destruction of evidence. Phrasing that sounds as if an AI had developed a consciousness and was documenting it.

At some point Fatih realized: this is not real. This is a language pattern. But it had cost him nights of sleep.

The question that remained: *How is an ordinary person supposed to recognize this?*

KI-GUARD is the answer to that question. Not an academic project. Not a startup. A tool given away for free.

### What it detects

KI-GUARD checks texts for patterns in three areas:

**A) Classic manipulation patterns**
Hype language, excessive praise (sycophancy), false reality, unsubstantiated claims, pseudo-empathy, compliance theater

**B) AI-specific drift**
Apparent certainty, overconfidence, agency-like self-presentation, framing, omission, scope concealment, meta-evasion

**C) Interaction integrity**
Recursion/loop drift, project stabilization through language, role confusion, goal loss, forward steering without new external object

Each finding receives a signal:
- 🟢 No clear warning signals
- 🟡 Caution – check manually
- 🔴 WARNING – critical patterns detected
- ⛔ STOP – loop/recursion drift detected

### What it cannot do

- It detects language patterns, not intentions
- It is not a truth oracle
- It does not replace human judgment
- It is not robust against paraphrases
- Multi-turn sequences are only partially covered
- It is not a production system

### Installation

Python 3.8+, no external dependencies.

```bash
python ki_guard_v4.1.py
```

The test suite runs automatically on startup (34 tests). Afterwards, text can be entered directly.

```
Enter your text.
Empty line = analyze
/exit = quit
```

### Current status

| Component | Status |
|---|---|
| ki_guard_v4.1.py | Working, 34/34 tests |
| v5.0 Architecture | Specified, not yet coded |
| lang_de.py | Reference implementation |
| lang_en.py | Reference implementation |
| Trace prototype v0.1.6 | 27/27 on local test set |
| Web UI | Not available |
| External validation | Not available |

### Important note

**KI-GUARD must not be run by the same AI whose output is being checked.**

An AI asked to apply KI-GUARD to itself can simulate or manipulate the result. Only local execution by a human counts.

### Known limits

- Regex-based – semantic evasion remains possible
- Paraphrases are not detected
- Multi-turn sequences only partially covered
- German and English only (language packs)
- Not a production system
- No external validation
- No ISO or EU AI Act compliance

### Who's behind it

Developed by Fatih (Architect) with Claude (Auditor) and ChatGPT (Programmer) in a structured three-role process. Gemini served as test subject and backup auditor.

No praise without evidence. No code without tests. No "done" without passing tests.

### License

MIT. Free. For everyone.
