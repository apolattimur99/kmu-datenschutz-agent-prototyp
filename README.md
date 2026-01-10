# CustomGPT – Datenschutzfreundlicher Angebotsassistent (Prototyp)

Dieses Repository dokumentiert den Prototypen eines CustomGPT, der aus strukturierten Kundenanfragen einen Angebotsentwurf erzeugt und dabei personenbezogene Daten konsequent anonymisiert.

## Was macht der Prototyp?
Der CustomGPT verarbeitet eine Anfrage in drei Schritten:
1. Anonymisierung (Entfernung von personenbezogenen Daten)
2. Strukturierung der Anfrage (Use Case, Leistungen, Rahmenbedingungen)
3. Erstellung eines Angebotsentwurfs auf Basis eines simulierten Produktkatalogs

Die Ausgabe erfolgt in drei Blöcken:
- **Block 1:** JSON (maschinenlesbar)
- **Block 2:** Tabelle (übersichtliche Angebotspositionen)
- **Block 3:** Text (Zusammenfassung und Hinweise)

## Prototyp nachbauen (Voraussetzungen & Schritte)

### Voraussetzungen
- Ein ChatGPT-Konto.
- **Zum Nachbauen/Erstellen des Custom GPT:** Zugriff auf den GPT-Builder (in der Regel mit **ChatGPT Plus/Pro** bzw. Team/Enterprise/Edu).
- Zugriff auf die Dateien aus diesem Repository:
  - `customgpt/systemprompt.txt`
  - `customgpt/wissenslog.txt`

### Link zum Custom GPT
- Custom GPT: <https://chatgpt.com/?utm_source=google&utm_medium=paid_search&utm_campaign=GOOG_C_SEM_GBR_Core_CHT_BAU_ACQ_PER_MIX_ALL_EMEA_DE_EN_041425&c_id=22443203663&c_agid=183247730852&c_crid=746237886139&c_kwid=%7Bkeywordid%7D&c_ims=&c_pms=9042212&c_nw=g&c_dvc=c&gad_source=1&gad_campaignid=22443203663&gbraid=0AAAAA-I0E5d5SAr_sgkavajwv2RaiATpj&gclid=CjwKCAiA64LLBhBhEiwA-Pxgu7QmlYNZ8sEF0MGxcRmycPaYv3hVzEhS1sdqEkR_lrFrsksmYEpnZxoC5UcQAvD_BwE>

### Schritt-für-Schritt (GPT-Builder)
1. Öffne den GPT-Builder und wähle **„Neuer GPT“**.
2. Wechsle in den Tab **„Konfigurieren“**.
3. Kopiere den Inhalt aus `custom-gpt/systemprompt.txt` in das Feld **„Hinweise“**.
4. Lade unter **„Wissen“** die Datei `custom-gpt/wissenslog.txt` hoch.
5. Deaktiviere (falls vorhanden) Funktionen, die nicht benötigt werden (z. B. Internetsuche, Bildgenerierung).
6. Speichere den Custom GPT und öffne anschließend die **Vorschau** (rechts), um Tests durchzuführen.

> Hinweis: Die Ausgabe ist als 3-Block-Format definiert (JSON / Tabelle / Text). Der JSON-Block ist maschinenlesbar und dient als Referenz für die Testfälle in `tests/`.

## Repository-Inhalt
- `custom-gpt/` – Systemprompt und Wissenslog (Produktkatalog/Regeln)
- `tests/` – Testfälle (Eingaben/Ausgaben) inkl. Promptfallen
- `docs/` – Screenshots und zusätzliche Dokumentation
