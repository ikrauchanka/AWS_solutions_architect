# Snow Ball

Snowballs sind große physische Datenträger, die dazu verwendet werden, große Mengen an Daten in AWS zu migrieren. Es handelt sich um eine Daten-Transportlösung im Peta-Byte-Maßstab. Die Verwendung physischer Datenträger wie Snowballs hilft, gängige Probleme bei der Übertragung großer Datenmengen zu umgehen, wie hohe Netzwerkkosten, lange Übertragungszeiten und Sicherheitsbedenken. Snowballs sind von Design her äußerst sicher, und sobald der Datentransfer abgeschlossen ist, werden die Snowballs von deinen Daten bereinigt.

[AWS Snow Ball Dokumentation](https://aws.amazon.com/de/snowball/features/)

## Snowball Schlüsselinformationen:
Snowball ist eine gute Wahl für einen Datentransfer-Job, wenn du:
* eine sichere und schnelle Datenübertragung im Terabyte- bis Petabyte-Bereich in AWS benötigst.
Snowball kann auch die richtige Wahl sein, wenn du:
* keine teuren Upgrades an deiner bestehenden Netzwerkinfrastruktur vornehmen möchtest, wenn du:
* häufig große Datenrückstände hast, wenn du dich in einer physisch isolierten Umgebung befindest oder wenn du:
* in einer Region bist, in der Hochgeschwindigkeits-Internetverbindungen nicht verfügbar oder kostspielig sind.

### Als Faustregel gilt: 

* Wenn es länger als eine Woche dauert, um deine Daten mit der ungenutzten Kapazität deiner bestehenden Internetverbindung in AWS hochzuladen, solltest du in Betracht ziehen, Snowball zu verwenden.

Zum Beispiel, wenn du über eine 100 Mb-Verbindung verfügst, die du ausschließlich für die Übertragung deiner Daten verwenden kannst, und du insgesamt 100 TB Daten übertragen musst, wird die Übertragung über diese Verbindung mehr als 100 Tage dauern. Du kannst die gleiche Übertragung in etwa einer Woche mit mehreren Snowballs durchführen.
Hier ist eine Referenz dafür, wann Snowball in Betracht gezogen werden sollte, basierend auf der Anzahl der Tage, die für dieselbe Übertragung über eine Internetverbindung benötigt würden:

Snowball Edge und Snowmobile:

Snowball Edge ist eine spezielle Art von Snowball, die sowohl über Rechen- als auch über Speicherfunktionen über AWS Lambda und bestimmte EC2-Instanztypen verfügt. Das bedeutet, dass du Code in deinem Snowball ausführen kannst, während deine Daten auf dem Weg zu einem Amazon Rechenzentrum sind. Dies ermöglicht die Unterstützung von lokalen Workloads an abgelegenen oder offline befindlichen Standorten, und daher muss Snowball Edge nicht auf einen Datentransferservice beschränkt sein. Ein interessanter Anwendungsfall ist bei Flugzeugen. Flugzeuge fliegen manchmal mit Snowball Edges an Bord, damit sie große Mengen von Flugdaten speichern und die für die eigenen Systeme des Flugzeugs erforderlichen Funktionen berechnen können. Snowball Edges können auch lokal gruppiert werden, um eine noch bessere Leistung zu erzielen.
Snowmobile ist eine Daten-Transportlösung im Exabyte-Maßstab. Es handelt sich um eine Lösung für den Transport von 100 Petabyte Daten und befindet sich in einem 45 Fuß langen Frachtcontainer, der von einem Sattelschlepper gezogen wird. Diese massive Übertragung macht Sinn, wenn du dein gesamtes Rechenzentrum mit Jahren an Daten in die Cloud verschieben möchtest.

[Zurück zum Leitfaden](../../README.md)
