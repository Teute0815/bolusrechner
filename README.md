# Offline-Bolusrechner 0.4

## Neu in Version 0.4

- Automatischer Mahlzeitenlevel-Vorschlag aus Fett, Protein und KH
- Wahl zwischen automatischer und manueller Level-Steuerung
- Split-Empfehlung mit:
  - geschätztem Gesamtbedarf
  - Sofortbolus
  - verzögertem KH-Anteil
  - möglichem zusätzlichem FPE-Anteil
- Zeitfenster je Mahlzeitenlevel:
  - L2: etwa 1–2 Stunden
  - L3: etwa 2–4 Stunden
  - L4: etwa 3–5 Stunden
- Spätere FPE-Prüfung:
  - L4 etwa 4–7 Stunden
- Zusätzlicher KH-Aktivitätspuffer:
  - A1 10 g
  - A2 20 g
  - A3 30 g
  - voller Puffer bei laufender oder unmittelbar bevorstehender Aktivität
  - halber Puffer bei bereits absolvierter Aktivität
  - plus 5 g bei fallendem und plus 10 g bei stark fallendem Trend
- Alle Split- und Pufferwerte sind lokal veränderbar.

## Vorläufige Split-Startwerte

- L1: 100 % initial
- L2: 80 % initial
- L3: 65 % initial
- L4: 50 % initial
- Bei A2/A3 und zeitnaher Aktivität wird der Initialanteil zusätzlich reduziert.

## Wichtige Logik

Korrektur und anrechenbares IOB werden mit dem Sofortanteil verrechnet.
Nur der kohlenhydratbezogene Mahlzeitenanteil wird zeitlich gesplittet.
Der FPE-Anteil ist ein separater späterer Prüfwert und wird nicht automatisch
zum verzögerten KH-Bolus addiert.

## Sicherheit

Persönliche Test- und Dokumentationshilfe, keine automatische Therapieentscheidung.
Spätdosen immer anhand von Verlauf, IOB, Trend und tatsächlicher Nahrungswirkung neu beurteilen.
