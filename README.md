# Bolusrechner

Lokale, installierbare Web-App zur transparenten Berechnung eines Mahlzeiten- und Korrektursaldos. Je nach Nettobilanz zeigt sie einen Sofortbolus, einen geteilten Bolus, keinen zusätzlichen Bolus oder einen Kohlenhydratausgleich an.

Diese App ist ausschließlich eine Rechen- und Orientierungshilfe und ersetzt weder eine individuelle Therapieempfehlung noch die Beratung durch medizinisches Fachpersonal. Prüfe alle Eingaben, Berechnungen und vorgeschlagenen Insulin- oder Kohlenhydratmengen eigenverantwortlich und stimme Änderungen deiner Diabetesbehandlung mit deinem Diabetesteam ab. Spätdosen und Korrekturen dürfen nur unter Berücksichtigung von aktuellem Glukoseverlauf, Trend, IOB, Aktivität und der tatsächlichen Mahlzeitenwirkung beurteilt werden.

## App und Projekt

- App: https://teute0815.github.io/bolusrechner/
- Projekt und Quellcode: https://github.com/Teute0815/bolusrechner
- Fehler und Funktionswünsche: https://github.com/Teute0815/bolusrechner/issues
- Fragen und Austausch: https://github.com/Teute0815/bolusrechner/discussions

GitHub-Beiträge sind öffentlich. Keine Gesundheitsdaten, Nightscout-Adressen, Tokens oder andere vertrauliche Informationen einstellen.

## Als App / PWA installieren

Der Bolusrechner kann im Browser verwendet oder als Progressive Web App installiert werden. Die installierte Variante besitzt ein eigenes App-Symbol, startet in einem eigenen Fenster, bleibt nach dem ersten vollständigen Laden offline nutzbar und prüft bei Internetverbindung auf Aktualisierungen.

- **Android:** in Chrome oder Edge öffnen und „App installieren“ beziehungsweise „Zum Startbildschirm hinzufügen“ wählen.
- **iPhone/iPad:** in Safari öffnen, „Teilen“ und anschließend „Zum Home-Bildschirm“ beziehungsweise „Als Web-App öffnen“ wählen.
- **Desktop:** in Chrome oder Edge über das Browsermenü installieren. Die Webversion ist in praktisch allen aktuellen Browsern nutzbar; für die Installation als eigenständige App eignen sich Chrome oder Edge.

Einstellungen, Nightscout-Zugangsdaten und persönliche KH-Helfer werden lokal im jeweiligen Browser beziehungsweise in der installierten PWA gespeichert. Für Geräte- oder Browserwechsel steht der JSON-Export zur Verfügung.

## Version 0.14.2

- geführte Ersteinrichtung mit Willkommen, JSON-Import, Nightscout-Verbindung und abschließender Prüfung persönlicher Grundwerte
- Zurück-Navigation zwischen allen Einrichtungsschritten
- einheitenabhängige Ziel- und Korrekturfaktorwerte im Einrichtungsdialog mit klarer Einheitenbeschriftung
- Aktivitätsauswahl mit vollständiger Erklärung und A0 als neutralem Basisprofil
- Import prüft Versionsmarker und ergänzt neuere fehlende Einstellungen
- Nightscout-Abgleich vergleicht lokale Werte mit aktuellen Profilwerten
- vollständige, sichtbare und bearbeitbare Tageszeitpläne für KH-Faktor und Korrekturfaktor
- Zeiträume können hinzugefügt, geändert und gelöscht werden; jeweils aktuell gültiger Wert wird verwendet
- Nightscout-Zeitpläne werden lokal als Offline-Fallback gespeichert
- Hinweis bei App-Updates, wenn neue Einstellungen geprüft werden müssen
- schwebende Erinnerung für ungespeicherte Standardeinstellungen mit Speichern, Verwerfen und Ausblenden
- „Vorschlag aktualisieren“ nur nach manueller Änderung der IOB-/KH-Saldenwerte
- überarbeitete Aktivitätsinformationen und Warnhinweise bei A2/A3
- zusätzlicher Read-only-Token-Hinweis mit Erklärung der reinen Lesezugriffe
- hervorgehobener FPE-Sicherheitshinweis in der Form „1 IE pro 1 FPE“
- aktualisierte Hilfe, Eigenverantwortungshinweis, technische Angaben und Urheberschaft
- Kontaktbereich mit Repository, Issues und Discussions
- Datensicherung ausschließlich über JSON-Dateien
- keine externen JavaScript-Frameworks oder Laufzeitbibliotheken

## Frühere Hauptversionen

### Version 0.13

- sichtbarer aktueller KH-Faktor und Korrekturfaktor mit Quellenanzeige
- Nightscout-Profilwerte werden für beide Faktoren verwendet
- getrennte Optionen „Standard statt Nightscout verwenden“
- lebende Altersangaben für Profil- und Glukosedaten

### Version 0.12

- automatischer Nightscout-Refresh und Aktualisierung bei Rückkehr in die App
- Schutz manuell angepasster IOB-/KH-Nettowerte vor automatischem Überschreiben
- PWA-Installationshilfe und Update-Erkennung

### Version 0.11

- Standard-Korrekturfaktor, einheitliches Info-System und überarbeitete Aktivitäts-/Infekteinstellungen
- FPE-Standard für neue Installationen auf 1 IE pro 1 FPE

### Version 0.10

- erweiterte KH-Helfer, Aktivitätslevel A−1 bis A3, Krank-/Infekt-Modifikator und klarere Nightscout-Statusanzeigen

### Version 0.9

- automatischer IOB-/COB-Nettovorschlag
- optionaler Tokenexport in JSON
- neu strukturierte Einstellungen und erweiterte Hilfe

### Version 0.8.1

- gewichteter 20-Minuten-Trend, stabilerer Nightscout-Abruf, kompakter Refresh und speicherbarer Standard-Zielwert

### Version 0.7

- kompakter Header, Burger-Menü und einheitlicher Sicherheitshinweis

### Version 0.6

- erweiterte Nightscout-Profil-, IOB- und COB-Anbindung
- automatische FPE-Berechnung und Mahlzeitenlevel

### Version 0.5

- Umschaltung mmol/l und mg/dl, Nightscout-Konfiguration, PWA und JSON-Import/-Export

### Version 0.4

- Splitberechnung, FPE-Spätanteil, levelabhängige Zeitfenster und Aktivitätspuffer

### Version 0.3

- gemeinsame Nettorechnung und persönliche KH-Helfer

### Version 0.2

- Kohlenhydratausgleich, differenzierter IOB-Abzug und Trendhinweise

### Version 0.1

- erste lokale Rechenversion

## Datenschutz und Technik

Die Berechnungen erfolgen lokal im Browser. Die App übermittelt keine Gesundheits-, Nightscout- oder Berechnungsdaten an einen vom Projektherausgeber betriebenen Server. Bei eingerichteter Nightscout-Verbindung kommuniziert das Endgerät direkt mit der angegebenen Nightscout-Instanz. Normale Exporte enthalten das Nightscout-Token nicht; es wird nur nach ausdrücklicher Auswahl aufgenommen.

Technische Basis: HTML, CSS, JavaScript, Web App Manifest, Service Worker und Browser Local Storage. Es werden keine externen JavaScript-Frameworks oder Laufzeitbibliotheken verwendet.

## Urheberschaft und Lizenz

Konzept, fachliche Anforderungen und inhaltliche Ausgestaltung: **Teute0815**  
Technische Umsetzung: KI-gestützt mit ChatGPT von OpenAI.

Der Quellcode steht unter der MIT-Lizenz. Geänderte Versionen dürfen nicht den Eindruck erwecken, vom ursprünglichen Projektherausgeber medizinisch geprüft, freigegeben oder empfohlen worden zu sein.
