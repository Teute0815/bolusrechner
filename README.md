# Offline-Bolusrechner

Lokale, installierbare Web-App zur transparenten Berechnung eines Mahlzeiten- und Korrektursaldos. Die App kann je nach Ergebnis einen Sofortbolus, einen geteilten Bolus, keinen zusätzlichen Bolus oder einen Kohlenhydratausgleich anzeigen.

Die Berechnungen laufen im Browser. Die App ist als persönliche Test- und Dokumentationshilfe gedacht und ersetzt keine individuelle medizinische Therapieentscheidung.

## Versionsverlauf

### Version 0.1

- Erste vollständig lokale Rechenversion
- Eingabe von Glukose, Zielwert, ISF, Kohlenhydraten und IOB
- Aktivitätsstufen mit editierbaren Reduktionen
- Mahlzeitenlevel L1 bis L4
- FPE-Berechnung aus Fett und Protein
- Transparente Aufschlüsselung der Rechnung
- Lokale Speicherung der Einstellungen

### Version 0.2

- Ergänzter Kohlenhydrat-Ausgleich
- Verständlichere Trennung zwischen Gesamt-IOB und dem für die aktuelle Rechnung anrechenbaren Anteil
- Trend- und Aktivitätshinweise
- Einstellbare Rundung für Insulin und Kohlenhydrate

### Version 0.3

- Eine gemeinsame Netto-Rechnung ohne Modus-Umschalter
- Automatische Entscheidung zwischen Insulin, keiner zusätzlichen Maßnahme und Kohlenhydraten
- Editierbare Datenbank für persönliche KH-Helfer
- Vorschläge in alltagstauglichen Portionen

### Version 0.4

- Getrennte Darstellung von Gesamtbedarf, Sofortbolus, verzögertem KH-Anteil und möglichem FPE-Anteil
- Levelabhängige Split-Zeitfenster
- Automatische Makronährstoff-Einstufung
- Zusätzlicher Aktivitätspuffer
- Editierbare Split- und Pufferparameter

### Version 0.5

- Umschaltung zwischen mmol/l und mg/dl
- Nightscout-Konfiguration mit URL, Read-only-Token und automatischem Laden
- PWA-Icon in mehreren Größen
- Sichtbarer Update-Hinweis
- JSON-Export und -Import von Einstellungen und KH-Helfern
- Neutrale Aktivitätsoption ohne Anpassung
- Behutsam optimierte mobile Darstellung

### Version 0.6

- Nightscout-IOB und -COB werden bevorzugt über `/api/v2/properties` übernommen
- Fallback über CarePortal-Behandlungen und Profilwerte, wenn direkte Pluginwerte fehlen
- Aktueller ISF, DIA, KH-Faktor und Kohlenhydrat-Absorptionsrate werden aus dem aktiven Nightscout-Profil gelesen
- Verbesserter Nightscout-Verbindungstest mit Glukose, Trend, Alter, Profil, IOB und COB
- Quellenhinweise direkt unter Glukose, Trend, ISF, IOB und COB
- Kompaktere mobile Anordnung der wichtigsten Eingabefelder
- Fett, Protein und FPE stehen mobil kompakt nebeneinander
- FPE wird bei Änderungen von Fett oder Protein sofort neu berechnet
- Das Mahlzeitenlevel-Dropdown wird automatisch gesetzt und kann manuell überschrieben werden
- Hinweise unterscheiden zwischen automatischer und manueller Levelauswahl
- Export und Import von Einstellungen und KH-Helfern per QR-Code
- Nightscout-Token wird nur nach ausdrücklicher Auswahl in einen QR-Code aufgenommen

## Nightscout

Die App kann folgende Informationen laden, sofern sie von der jeweiligen Nightscout-Instanz und dem Read-only-Token bereitgestellt werden:

- aktueller Glukosewert und Trend
- IOB und COB aus Nightscouts Plugin-Eigenschaften
- Profilwerte wie ISF, DIA, KH-Faktor und Kohlenhydrat-Absorptionsrate
- CarePortal-Behandlungen als Fallback

Manuelle Eingaben bleiben jederzeit möglich. Der zusätzliche Eingabewert für das tatsächlich noch senkende IOB bleibt bewusst manuell, weil eine App nicht sicher erkennen kann, welcher IOB-Anteil noch zu einer laufenden Mahlzeit gehört.

## Datenschutz

- Berechnungen und lokale Einstellungen werden im Browser verarbeitet.
- Zugangstoken gehören nicht in das öffentliche Repository.
- Der normale JSON- und QR-Export lässt das Nightscout-Token weg.
- Ein Token kann nur nach ausdrücklicher Auswahl in einen QR-Code aufgenommen werden.

## Installation und Updates

Die App kann über HTTPS als PWA installiert werden. Nach dem ersten Laden ist die Kernfunktion offline verfügbar. Bei einer neuen Programmversion erscheint ein sichtbarer Aktualisierungshinweis.

## Technischer Inhalt

- `index.html`
- `manifest.webmanifest`
- `sw.js`
- `icons/`
