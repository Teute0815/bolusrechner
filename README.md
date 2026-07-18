# Bolusrechner

Lokale, installierbare Web-App zur transparenten Berechnung eines Mahlzeiten- und Korrektursaldos. Die App kann je nach Ergebnis einen Sofortbolus, einen geteilten Bolus, keinen zusätzlichen Bolus oder einen Kohlenhydratausgleich anzeigen.

Diese App ist ausschließlich eine Rechen- und Orientierungshilfe und ersetzt weder eine individuelle Therapieempfehlung noch die Beratung durch medizinisches Fachpersonal. Prüfe alle Eingaben, Berechnungen und vorgeschlagenen Insulin- oder Kohlenhydratmengen eigenverantwortlich und stimme Änderungen deiner Diabetesbehandlung mit deinem Diabetesteam ab. Spätdosen und Korrekturen dürfen nur unter Berücksichtigung von aktuellem Glukoseverlauf, Trend, IOB, Aktivität und der tatsächlichen Mahlzeitenwirkung beurteilt werden.

## Versionsverlauf

### Version 0.11

- Standard-Korrekturfaktor unter „Aktuelle Situation“ ergänzt
- Standardwert 2,0 mmol/l beziehungsweise 36 mg/dl je IE
- Nightscout-Profilwert überschreibt bei erfolgreichem Abruf weiterhin den aktuellen Hauptwert
- Ohne Nightscout wird der gespeicherte App-Standard verwendet
- Einheitliches Info-System für nahezu alle fachlichen Einstellungen
- Info-Pop-ups erklären Bedeutung, Einheit, Formel, Beispiele und Grenzen
- KH-Rundung ausdrücklich als Aufrundung auf den nächsten Schritt dokumentiert
- „Mindestmenge Ausgleichs-KH“ kürzer und verständlicher benannt
- FPE-Standard für neue Installationen auf 1 FPE pro IE gesetzt
- Mahlzeitenlevel als „Mahlzeitenlevel L1–L4 – Initialbolus“ beschriftet
- Aktivitätseinstellungen nach Level paarweise geordnet
- A−1 und A0 ohne sichtbaren Aktivitätspuffer
- Einheitliche Bezeichnung „Bolusanpassung“
- Aktivitätspuffer-Hilfe an die tatsächliche App-Formel angepasst
- Krank-/Infekt-Zuschlag erscheint nur nach Aktivierung
- Aktueller Krank-/Infekt-Zuschlag direkt in der Hauptmaske editierbar
- Situative Änderung überschreibt den gespeicherten Standard nicht


### Version 0.10.2

- Direkt auf der funktionierenden Version 0.10 aufgebaut
- Einrichten-Button öffnet den Nightscout-Bereich
- URL und Read-only-Token sind beide erforderlich
- Direkter Speichern-Button neben dem Nightscout-Test ist verdrahtet
- Erfolgreicher Nightscout-Abruf speichert die Nightscout-Felder automatisch
- Nightscout-Kernlogik aus Version 0.10 unverändert beibehalten
- Bestehende KH-Helfer bieten ebenfalls „sehr schnell“
- Bestehende Klassifizierungen bleiben erhalten
- Sicherheitshinweis im Infofenster hat normale Infotextgröße
- Krank-/Infekt-Modifikator zeigt den angewendeten Prozentwert


### Version 0.10

- QR-Code bleibt ein einzelner Code, wird aber durch Kurzschlüssel, Standardwert-Auslassung und Kompression verkleinert
- Alle Pop-ups besitzen zusätzlich ein dauerhaft sichtbares X oben rechts
- Gesamt-COB wird ohne den Zusatz „nur Information“ dargestellt
- Warnhinweise unter IOB/COB und im Infofenster sind größer
- KH-Helfer-Kategorie „sehr schnell“ ergänzt; „nachhaltiger“ bleibt bestehen
- Standardhelfer „Apfel groß (200 g) – 29 g KH – halbierbar – schnell“
- Versionsnummer im Header kleiner und optisch abgesetzt
- Aktivitätslevel A−1 bis A3 neutral benannt
- A−1 „Sehr ruhiger Tag“ mit vorsichtiger Standarderhöhung von 10 %
- Persönliches Standard-Aktivitätslevel auswählbar
- Separater Modifikator „Krank / Infekt“ mit editierbarem Standardzuschlag von 10 %
- Ketone-Info mit vier Blutketon-Stufen und Handlungsorientierung
- Nightscout-Status unterscheidet nicht eingerichtet, offline und Abruffehler
- „Einrichten“-Button ersetzt Refresh, solange keine Nightscout-URL gespeichert ist
- Nightscout-Profilinformationen werden zeilenweise dargestellt


### Version 0.9

- Mobile Weiter-Navigation überspringt Dropdown-Menüs
- Noch senkendes IOB und noch wirksame KH stehen nebeneinander
- Automatischer Rechenvorschlag aus Gesamt-IOB, Gesamt-COB und KH-Faktor
- Beide Vorschlagswerte bleiben manuell überschreibbar
- Read-only-Token-Hinweis direkt am Nightscout-Feld
- Präzisere HTTP-401-Meldung mit Hinweis auf die Rolle readable
- Nightscout-Token kann optional in den JSON-Export aufgenommen werden
- Beim JSON-Import kann zwischen enthaltenem und vorhandenem Token gewählt werden
- Einstellungen neu nach Nightscout, Aktuelle Situation, Mahlzeit, Aktivität und Allgemein gruppiert
- Burger-Menü um Meine KH-Helfer und Import/Export ergänzt
- Hilfe um KH-Helfer und Einstellungen erweitert
- Jeder Hilfebereich besitzt eine ausführliche Mehr-Info-Ansicht
- Header zeigt die aktuelle Versionsnummer


### Version 0.8.1

- Nightscout-Verbindungsaufbau korrigiert
- Aktueller Glukosewert wird zuerst allein über den bewährten Zwei-Werte-Endpunkt geladen
- Profil, IOB, COB und 20-Minuten-Historie werden erst nach erfolgreichem Glukoseabruf geladen
- Zusatzabfragen können die Grundverbindung nicht mehr blockieren
- Fehlermeldung zeigt den tatsächlichen Abruffehler genauer an

### Version 0.8

- Nightscout-Abruf für den aktuellen Glukosewert wieder auf den bewährten Zwei-Werte-Endpunkt getrennt
- 20-Minuten-Historie wird separat geladen und darf bei einem Fehler den aktuellen Wert nicht mehr blockieren
- Kompakter Refresh-Button
- Standard-Zielwert in den Einstellungen speicherbar
- Zielwert wird beim Start und Zurücksetzen automatisch übernommen

### Version 0.7

- Kompakter Header mit App-Icon und Burger-Menü
- Menübereiche für Info, Hilfe, Versionsverlauf, Kontakt und Einstellungen
- Einheitlicher Sicherheitshinweis im Infofenster und Footer
- Eigener gewichteter Trend über 20 Minuten
- Jüngere Werte und die letzten fünf Minuten werden stärker gewichtet
- Ausreißerbegrenzung, Mindestanzahl und Richtungsbestätigung
- Warnung bei deutlicher Abweichung zum Nightscout-Einzeltrend
- Kompaktere Beschriftungen in „Aktuelle Situation“
- Eingabewerte werden beim Antippen vollständig markiert
- Mahlzeit-/Notizfeld vorerst entfernt
- Manuelle Feinanpassung als optionale Einstellung
- Versionsverlauf absteigend sortiert

### Version 0.6

- Erweiterte Nightscout-Profil-, IOB- und COB-Anbindung
- Fallback über CarePortal-Behandlungen und Profilwerte
- QR-Export und QR-Import
- Automatische FPE-Berechnung und Mahlzeitenlevel

### Version 0.5

- Umschaltung mmol/l und mg/dl
- Nightscout-Konfiguration
- PWA-Icon und Update-Hinweis
- JSON-Export und -Import
- Aktivitätsoption ohne Anpassung

### Version 0.4

- Splitberechnung
- FPE-Spätanteil
- Levelabhängige Zeitfenster
- Aktivitätspuffer

### Version 0.3

- Gemeinsame Netto-Rechnung
- KH-Helfer-Datenbank
- Alltagstaugliche Portionsvorschläge

### Version 0.2

- Kohlenhydrat-Ausgleich
- Differenzierter IOB-Abzug
- Trend- und Aktivitätshinweise

### Version 0.1

- Erste lokale Rechenversion
- Grundlegende Eingaben und Rechenaufschlüsselung
- Lokale Speicherung

## Nightscout

Die App kann – abhängig von der jeweiligen Instanz – Glukose, Trend, IOB, COB und Profilwerte laden. Manuelle Eingaben bleiben möglich. Das tatsächlich noch senkende IOB bleibt eine bewusste manuelle Einschätzung.

## Datenschutz

Berechnungen und Einstellungen werden im Browser verarbeitet. Zugangstoken gehören nicht in ein öffentliches Repository. Normale Exporte enthalten das Nightscout-Token nicht.

## Technischer Inhalt

- `index.html`
- `manifest.webmanifest`
- `sw.js`
- `icons/`
