Projektname:
KI-gestützte Stadt- und Wetterdatenanalyse mit n8n

Projektziel:
Ziel dieses Projekts ist es, einen automatisierten Workflow zu entwickeln, der Stadtinformationen und Wetterdaten abruft, verarbeitet und mithilfe künstlicher Intelligenz auswertet.
Durch die Automatisierung sollen manuelle Arbeitsschritte reduziert und Informationen strukturiert bereitgestellt werden.

Kurze Beschreibung des Problems:
Stadtinformationen, geografische Koordinaten und Wetterdaten müssen häufig aus unterschiedlichen Quellen gesammelt und verarbeitet werden.
Die manuelle Recherche ist zeitaufwendig und kann zu Fehlern führen.
Mit n8n wurde deshalb ein Workflow erstellt, der Daten automatisch abruft, zusammenführt, nach bestimmten Bedingungen verarbeitet und mit KI-Unterstützung auswertet.

Verwendete Tools:
•	n8n: Erstellung und Steuerung des automatisierten Workflows
•	HTTP Request / API: Abrufen von Stadtkoordinaten und Wetterinformationen
•	JavaScript: Individuelle Verarbeitung von Daten
•	Groq Chat Model: KI-Modell zur intelligenten Datenverarbeitung
•	AI Agent: KI-gestützte Auswertung und Verarbeitung
•	Form: Eingabe und Ausgabe von Informationen

Workflow:
1. Daten empfangen
Der Workflow beginnt mit dem Formular „Erfrage die Stadt“.
Der Benutzer gibt eine Stadt ein, für die Informationen und Wetterdaten ermittelt werden sollen.
2. Daten abrufen
Über HTTP-Request-Nodes werden zunächst die geografischen Koordinaten der Stadt ermittelt.
Anschließend werden mithilfe dieser Koordinaten Wetterdaten von einer externen API abgerufen.
3. Datenverarbeitung
Die empfangenen Daten werden durch verschiedene n8n-Nodes verarbeitet.
Verwendete Nodes:
•	Split Out: Aufteilen von Datensätzen
•	Summarize: Zusammenfassen von Informationen
•	Switch: Unterscheiden und Weiterleiten von Daten anhand festgelegter Regeln
•	Edit Fields: Anpassen und Strukturieren einzelner Datenfelder
•	Code in JavaScript: Individuelle Datenverarbeitung
•	Merge: Zusammenführen verschiedener Datenströme
4. KI-Auswertung
Der AI Agent verarbeitet die übergebenen Informationen mithilfe des verbundenen Groq Chat Models.
Die KI-Komponente kann genutzt werden, um die Daten zu interpretieren und verständlich aufzubereiten.
5. Ergebnisse zusammenführen
Die Ergebnisse der verschiedenen Verarbeitungszweige werden mithilfe der Merge-Nodes zusammengeführt.
Dadurch entsteht eine gemeinsame Datenstruktur für die weitere Verwendung.
6. Ergebnisse ausgeben
Am Ende werden die verarbeiteten Informationen an einen Formular-Node weitergegeben.
So können die Ergebnisse dem Benutzer bereitgestellt werden.

Screenshot -Vollständiger n8n-Workflow:
Siehe Datei ‚Screenshot – Wetterstation - Vollständiger n8n-Workflow‘
<img width="948" height="548" alt="Screenshot – Wetterstation - Vollständiger n8n-Workflow" src="https://github.com/user-attachments/assets/a1f0f865-a08c-41b4-a24e-1bce60cf06cb" />

Herausforderungen:
Während der Entwicklung mussten verschiedene Herausforderungen gelöst werden:
•	Korrekte Verbindung der einzelnen n8n-Nodes
•	Abrufen und Verarbeiten von API-Daten
•	Richtige Verwendung der geografischen Koordinaten
•	Strukturierung unterschiedlicher JSON-Daten
•	Festlegung der Bedingungen im Switch-Node
•	Zusammenführung mehrerer Datenströme
•	Einbindung eines KI-Modells in den Workflow
Besonders wichtig war es, sicherzustellen, dass die Daten zwischen den Nodes korrekt übergeben werden.

Lernerfahrungen:
Durch den Nachbau dieses Projekt konnte ich wichtige praktische Erfahrungen sammeln.
Ich habe gelernt:
•	Wie automatisierte Workflows mit n8n erstellt werden
•	Wie externe APIs eingebunden werden
•	Wie JSON-Daten verarbeitet werden
•	Wie Bedingungen und Verzweigungen funktionieren
•	Wie JavaScript in n8n eingesetzt wird
•	Wie verschiedene Datenströme zusammengeführt werden
•	Wie ein KI-Agent mit einem Sprachmodell verbunden wird
