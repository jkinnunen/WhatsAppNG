# WhatsApp NG

NVDA-Add-on, das Barrierefreiheitsverbesserungen für die webbasierte WhatsApp-Desktop-Version bietet.

## Funktionen

- **Alt+1**: Zur WhatsApp-Konversationsliste wechseln
- **Alt+2**: Zur WhatsApp-Nachrichtenliste wechseln
- **Alt+D**: Zum Nachrichteneingabefeld wechseln
- **Enter**: Sprachnachricht abspielen (funktioniert in einzelnen Chats und Gruppen)
- **Umschalt+Enter**: Kontextmenü für Nachrichten öffnen
- **Strg+C**: Aktuelle Nachricht in die Zwischenablage kopieren
- **Strg+R**: Vollständige Nachricht vorlesen (klickt bei Bedarf auf "Mehr lesen"-Schaltfläche)

### Umschalt-Skripte (keine Standard-Tastenkürzel - in Eingabegesten konfigurieren)

- Telefonnummernfilter in der Konversationsliste umschalten
- Telefonnummernfilter in der Nachrichtenliste umschalten
- Automatischen Fokusmodus umschalten (ermöglicht den Browse-Modus bei Bedarf)

## Anforderungen

- NVDA 2021.1 oder neuer
- WhatsApp Desktop (webbasierte Version)

## Installation

1. Laden Sie die Datei `whatsAppNG.nvda-addon` herunter
2. Gehen Sie in NVDA zu **Extras → Add-on-Manager**
3. Klicken Sie auf **Installieren** und wählen Sie die Datei aus
4. Starten Sie NVDA neu

## Konfiguration

Die Telefonnummernfilter können umgeschaltet werden:
- In der Konversationsliste: Tastenkürzel in Eingabegesten konfigurieren
- In der Nachrichtenliste: Tastenkürzel in Eingabegesten konfigurieren

Konfigurieren Sie Tastenkürzel unter:
**NVDA-Menü → Einstellungen → Eingabegesten → WhatsApp NG**

## Änderungsprotokoll

### Version 1.4.0 (2026-02-23)

**Hinzugefügt:**
- Vollständige Sprachunterstützung für: Arabisch, Deutsch, Spanisch, Italienisch und Russisch
- Ukrainische Übersetzung mit aktuellen Strings aktualisiert

**Behoben:**
- "Text nicht gefunden"-Fehler in Strg+R nach dem Klicken auf "Mehr lesen"-Schaltfläche
- Strg+R funktioniert jetzt nur bei Textnachrichten (zeigt "Keine Textnachricht" für Sprachnachrichten/Bilder an)

**Geändert:**
- Repository-Links zum neuen Repository aktualisiert (nunotfc/WhatsAppNG)
- Dokumentation: Alle lokalisierten READMEs enthalten nun das vollständige Änderungsprotokoll bis Version 1.3.0

### Version 1.3.0 (2026-02-07)

**Hinzugefügt:**
- Türkische Übersetzungsunterstützung
- Option zum Umschalten des automatischen Fokusmodus (Geste in Eingabegesten konfigurieren)

**Geändert:**
- Verbesserte Leistung: Navigationsbefehle sind bei wiederholter Verwendung jetzt schneller
- Die Escape-Taste wird nun korrekt an WhatsApp weitergeleitet

**Behoben:**
- Enter spielt jetzt Videonachrichten ab (funktionierte previously nur für Audio)

### Version 1.1.1 (2025-01-31)

**Hinzugefügt:**
- Strg+R: Vollständige Nachricht vorlesen (klickt automatisch auf "Mehr lesen"-Schaltfläche)
- Strg+C: Aktuelle Nachricht in die Zwischenablage kopieren
- Automatisches Deaktivieren des Browse-Modus (hält den Fokusmodus für eine bessere WhatsApp-Erfahrung aktiv)

**Geändert:**
- Verbesserte Fehlermeldungen: Alle Skripte bieten nun ein klares Feedback bei Fehlern
- Navigationsbefehle (Alt+1, Alt+2, Alt+D) sind bei Erfolg nun still

**Behoben:**
- Alt+1 und Alt+2 melden Fehler korrekt, wenn alle Pfade fehlschlagen
- Objektfilterung optimiert, um Eingabeverzögerungen zu reduzieren
- Enter: Slider-basierte Erkennung statt Button-Zählung (zuverlässiger)

### Version 1.1.0 (2025-01-30)

**Hinzugefügt:**
- Strg+R: Vollständige Nachricht vorlesen
- Intelligente Sprachnachrichten-Wiedergabe mithilfe der Slider-Erkennung

**Geändert:**
- Enter: Verbesserte Logik unter Verwendung der Slider-Erkennung anstatt des Zählens von Buttons

**Behoben:**
- Alt+2 versucht nun korrekt alle Navigationspfade, wenn der erste Versuch fehlschlägt

### Version 1.0.0 (2025-01-29)

**Erste Version:**
- Navigationskurzbefehle für Konversationsliste, Nachrichtenliste und Nachrichten-Composer
- Sprachnachrichten-Wiedergabe mit Unterstützung für einzelne Chats und Gruppen
- Kontextmenüzugriff für Nachrichtenaktionen
- Umschalten der Telefonnummernfilter für Konversationen und Nachrichten
- Automatische Fokusmodus-Aktivierung in WhatsApp Desktop

## Credits

Entwickelt von Nuno Costa, um Barrierefreiheitsverbesserungen für das moderne WhatsApp Desktop Erlebnis zu bieten.

## Support

Für Probleme oder Vorschläge besuchen Sie bitte:
https://github.com/nunotfc/whatsAppNG/issues

## Übersetzungskompilierung

Um Übersetzungen zu aktualisieren oder zu kompilieren:
```bash
scons pot
```

Dies erfordert die Installation der GNU Gettext-Tools.
