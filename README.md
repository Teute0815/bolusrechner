# Bolusrechner

Lokale, installierbare Web-App zur transparenten Berechnung eines Mahlzeiten- und Korrektursaldos. Die App kann je nach Ergebnis einen Sofortbolus, einen geteilten Bolus, keinen zusätzlichen Bolus oder einen Kohlenhydratausgleich anzeigen.

Diese App ist ausschließlich eine Rechen- und Orientierungshilfe und ersetzt weder eine individuelle Therapieempfehlung noch die Beratung durch medizinisches Fachpersonal. Prüfe alle Eingaben, Berechnungen und vorgeschlagenen Insulin- oder Kohlenhydratmengen eigenverantwortlich und stimme Änderungen deiner Diabetesbehandlung mit deinem Diabetesteam ab. Spätdosen und Korrekturen dürfen nur unter Berücksichtigung von aktuellem Glukoseverlauf, Trend, IOB, Aktivität und der tatsächlichen Mahlzeitenwirkung beurteilt werden.

## Versionsverlauf

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
