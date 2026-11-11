# Mnemonica Coach

Deutschsprachige Lern-App für die 26 Gedächtnisorte aus *The Memory Arts – Mnemonica Special Edition* von Sarah und David Trustman. Die App besteht aus einer statischen HTML-Datei. GitHub Pages stellt den Hauptzweig bereit.

## Lernmethode

Die Ortsillustrationen stehen in der verwendeten PDF auf den Dateiseiten 21–46. Die App folgt ihrer Reihenfolge und verwendet deutsche Ortsnamen. Das Buch empfiehlt, die Form der jeweiligen Nummer im Motiv zu erkennen und die Reise als lebendige Geschichte mit Sinneseindrücken nachzuvollziehen. Die App leitet zum Betrachten und Nacherzählen an. Etappen, Multiple-Choice-Prüfungen, Lernstatistiken und adaptives Training sind Ergänzungen der App.

Der Kartenschlüssel verwendet Figuren und Motive für die 13 Werte. Danach ordnet das Buch die Farben räumlich in vier Quadranten an und unterscheidet die erste und zweite Karte durch Vorder- und Hintergrund beziehungsweise Größe. Die Übungen führen von einer Karte pro Ort bis zum kompletten Deck mit zwei Karten pro Ort. Die Mnemonica-Beispiele stehen auf den PDF-Seiten 59–84. Lerncoach 2.0 erweitert ausschließlich die Ortsübungen.

## Lokaler Speicher

| Speicher | Inhalt |
| --- | --- |
| localStorage `mnemonica-coach-v1` | Bestehender Kartenmodus mit Freischaltungen, Antworten, Notizen und Runden |
| localStorage `mnemonica-grundkurs-v1` | Etappen, Freischaltungen und Prüfungsversuche |
| localStorage `mnemonica-place-1` bis `mnemonica-place-26` | Persönliche Ortsnotizen |
| localStorage `mnemonica-place-coach-v2` | Profile pro Ort und Fragetyp sowie abgeschlossene Runden |
| IndexedDB `mnemonica-originalbilder-v1`, Version 1, Store `images` | Kartenbilder unter numerischen Schlüsseln 1–26 und Ortsbilder unter 101–126 |

Der Coach ergänzt vorhandene Profile schrittweise um begrenzte Antwort- und Zeitstichproben. Alte Trefferzahlen und Runden bleiben lesbar. Eine PDF kann über „Bilder“ lokal importiert werden. Sie und ihre Illustrationen gehören nicht in das Repository.

## Lerncoach 2.0

- Der Coach bewertet jede verfügbare Fragerichtung getrennt. Er braucht mindestens fünf Antworten. Sobald fünf neue Antworten vorliegen, zählt ein Fenster von bis zu acht Antworten. Die Gesamtzahlen bleiben im Dashboard sichtbar.
- Ab 80 % gilt eine Richtung als sicher. Ein einzelner Fehler kann einen zuvor sicheren Status nicht aufheben. Bei höchstens 60 % und mindestens zwei Fehlern besteht Übungsbedarf. Dazwischen gilt die Richtung als unsicher.
- Zeiten werden nur als Orientierung angezeigt. Die Anzeige vergleicht bei ausreichenden Daten zwei Mediane von jeweils fünf richtigen Antworten derselben Fragerichtung.
- Eine Empfehlung zu zwei verwechselten Orten setzt mindestens zwei tatsächlich erfasste gleiche Fehlwahlen voraus. Frühere Summendaten liefern dafür keinen Beleg.
- Von 20 adaptiven Fragen dienen acht der breiten Wiederholung. Die übrigen zwölf gewichten unsichere Verbindungen stärker. Die Prüfungslogik verwendet weiterhin 90 % richtige Antworten und mindestens zwei richtige Antworten pro neuem Ort.
