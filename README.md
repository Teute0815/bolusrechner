# Offline-Bolusrechner

Eine installierbare Progressive Web App (PWA) zur transparenten Berechnung und Dokumentation von Mahlzeitenbolus, Korrektur, aktivem Insulin, Mahlzeitensplit, Fett-Protein-Einheiten und aktivitätsbezogenen Kohlenhydratpuffern.

Die Anwendung arbeitet nach dem Laden vollständig im Browser. Eingaben, Einstellungen und selbst angelegte KH-Helfer werden lokal gespeichert. Sie ersetzt keine individuelle medizinische Beratung oder Therapieentscheidung.

## Installation

Die Dateien werden über eine HTTPS-Webadresse bereitgestellt. Unterstützte Browser können die Seite anschließend als App auf dem Startbildschirm installieren. Nach dem ersten vollständigen Laden ist die grundlegende Berechnung auch offline verfügbar.

## Versionsverlauf

### Version 0.1

- Erste lokale Offline-Webversion
- Eingabe von Glukose, Zielwert, Korrekturfaktor, Kohlenhydraten und aktivem Insulin
- Aktivitätsstufen und manuelle Feinanpassung
- Mahlzeitenlevel L1 bis L4
- FPE-Berechnung aus Fett und Protein
- Transparente Aufschlüsselung der Rechenschritte
- Lokal speicherbare Berechnungsparameter

### Version 0.2

- Zusätzliche Rückwärtsrechnung für benötigte Kohlenhydrate
- Verständlichere Trennung zwischen Gesamt-IOB und dem Anteil, der noch korrigierend wirkt
- Berücksichtigung von Glukoselücke, IOB, Aktivität und Trend bei einer KH-Empfehlung
- Einstellbare KH-Rundung und Sicherheitsmindestmenge

### Version 0.3

- Zusammenführung der getrennten Modi zu einer einzigen Netto-Rechnung
- Automatische Entscheidung zwischen Insulinempfehlung, Null-Empfehlung und KH-Empfehlung
- Editierbare lokale Datenbank für KH-Helfer
- Vorschläge in alltagstauglichen ganzen, halben, Drittel- oder Viertelportionen

### Version 0.4

- Mahlzeitensplit abhängig von L1 bis L4
- Getrennte Anzeige von Gesamtbedarf, Sofortanteil, verzögertem KH-Anteil und möglichem FPE-Anteil
- Automatischer Mahlzeitenlevel-Vorschlag aus Kohlenhydraten, Fett und Protein
- Zeitfenster für verzögerte KH- und FPE-Prüfung
- Zusätzliche aktivitätsbezogene KH-Puffer
- Alle Split- und Pufferparameter lokal konfigurierbar

### Version 0.5

- Eigenes PWA-Appsymbol in mehreren benötigten Größen
- Umschalter zwischen mmol/l und mg/dl
- Automatische Anpassung von Eingabefeldern, Einheiten, ISF und Warnschwellen
- Neue neutrale Aktivitätsoption „Keine Aktivitätsanpassung“
- Optionale Nightscout-Anbindung mit lokal gespeicherter URL und Read-only-Token
- Automatisches Laden von aktuellem Glukosewert und Trend
- Übernahme von IOB und COB, sofern diese in Nightscout `devicestatus` verfügbar sind
- Manuelle Eingabe bleibt jederzeit möglich
- Sichtbarer Hinweis und Button bei einer verfügbaren PWA-Aktualisierung
- Export und Import von Einstellungen und KH-Helfern als JSON-Datei
- Nightscout-Token wird aus Sicherheitsgründen nicht exportiert
- Migration vorhandener lokaler Einstellungen und KH-Helfer aus Version 0.4
- Mobile Darstellung behutsam optimiert
- Fortlaufender neutraler Versionsverlauf in dieser README

## Nightscout

In den Einstellungen können eine Nightscout-Basis-URL und ein Read-only-Token hinterlegt werden. Beim App-Start kann die Anwendung automatisch versuchen, aktuelle Daten zu laden.

- Glukose und Trend werden aus den jüngsten SGV-Einträgen geladen.
- IOB und COB werden nur übernommen, wenn Nightscout diese Werte in `devicestatus` liefert.
- Der Ursprung des IOB kann nicht zuverlässig automatisch unterschieden werden. Der Anteil „IOB, das noch den Glukosewert senken wird“ bleibt deshalb eine bewusste manuelle Eingabe.
- COB wird derzeit nur informativ angezeigt und nicht automatisch in die Dosisberechnung einbezogen.
- Niemals das Nightscout-API_SECRET in der App oder im Repository hinterlegen.

## Lokale Speicherung und Sicherung

Lokal gespeichert werden:

- Berechnungsparameter
- Anzeigeeinheit
- Aktivitäts- und Splitparameter
- KH-Helfer
- Nightscout-URL und Read-only-Token

Über die Exportfunktion werden Einstellungen und KH-Helfer als JSON-Datei gesichert. Das Nightscout-Token wird dabei nicht exportiert.

## Noch offen

- Optionaler QR-Code für die Übertragung von Einstellungen zwischen Geräten
- Optionaler kontrollierter Import vorbereiteter Mahlzeitendaten
- Weitergehende Prüfung der Nightscout-Verfügbarkeit von IOB und COB in unterschiedlichen Setups
- Spätere Verpackung als native Android-App oder APK
