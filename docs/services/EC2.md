# Elastic C-ompute C-loud (EC2) 

einfach erklärt:

EC2 ist neben [s3](../../docs/services/s3.md) und [Lambda](../../docs/services/Lambda.md) einer der drei Hauptservices der AWS Cloudlandschaft und erstellt für alle Anwendungsfälle, anpassbare Serverinstanzen, die schnell skaliert werden können. Eine Instanz ist ein virtueller [Server](https://de.wikipedia.org/wiki/Server) - ähnlich einer [Virtuellen Maschine](https://de.wikipedia.org/wiki/Virtuelle_Maschine), auf deinem PC, - jedoch in der Cloud. Mit Amazon EC2 kannst du das Betriebssystem, z. B. [Linux](https://de.wikipedia.org/wiki/Linux) - verschiedener [Distributionen](https://de.wikipedia.org/wiki/Linux-Distribution) -, MacOS oder Microsoft [Windows](https://de.wikipedia.org/wiki/Windows_Server_2022) und die Anwendungen konfigurieren, die auf deiner Instanz laufen. Die Konfiguration bei der Inbetriebnahme entspricht einer Live-Kopie des von dir angegebenen Amazon Machine Image ([AMI](../../docs/services/AMI.md)) siehe [Amazon Linux 2](https://en.wikipedia.org/wiki/Amazon_Machine_Image) (Wikipedia Artikel nur englischsprachig verfügbar). EC2 ermöglicht eine schnelle Bereitstellung und Hoch- oder Herunterskalierung von Instanzen. Du zahlst nur für die Ressourcen, die du nutzt, und nur, solange deine Instanz läuft. (pay-as-you-go) Während des Betriebs erfolgt die Abrechnung nach CPU, Speicher, Speicherplatz und Netzwerk. Im gestoppten Zustand fallen nur Kosten für den [EBS](../../docs/services/ElasticBlockStore.md)-Speicher an.

## Wichtige Details zu EC2:
Du kannst verschiedene Instanztypen aus einer einzigen AMI starten. Ein Instanztyp bestimmt im Wesentlichen die Hardware des Hostcomputers für deine Instanz. Jeder Instanztyp bietet unterschiedliche Rechen- und Speicherfähigkeiten. [Die Auswahl eines Instanztyps](https://aws.amazon.com/de/ec2/instance-types/?trk=40a4d4b5-7441-4aba-87e7-f0a009817c2a&sc_channel=ps&ef_id=Cj0KCQiAkKqsBhC3ARIsAEEjuJju6Sthg6sRIsABlpvSNIN09uZHkBiC36OJvoZob_gz5TnWXroi86waAn9mEALw_wcB:G:s&s_kwcid=AL!4422!3!645186148951!e!!g!!aws-instanztypen!19579892305!149123141230&gclid=Cj0KCQiAkKqsBhC3ARIsAEEjuJju6Sthg6sRIsABlpvSNIN09uZHkBiC36OJvoZob_gz5TnWXroi86waAn9mEALw_wcB) sollte auf den Anforderungen deiner Anwendung oder Software basieren.

Es besteht die Möglichkeit, dedizierte Hardware (dedicated tenancy) für deine Instanz zu verwenden 

(*"dediziert" bezieht sich auf die exklusive Zuweisung oder Verwendung von Ressourcen für einen bestimmten Zweck oder Benutzer. Im Kontext von Amazon EC2 und "dedicated tenancy" bedeutet dies, dass dedizierte Hardware ausschließlich einem einzelnen Kunden zur Verfügung gestellt wird. Wenn du von "dedicated tenancy" in Bezug auf Amazon EC2 sprichst, bedeutet dies, dass du die Option hast, eine EC2-Instanz auf physischer Hardware zu betreiben, die nur von dir genutzt wird. Das heißt, diese Hardware wird nicht mit Instanzen anderer Kunden geteilt. Dies ist eine spezielle Konfiguration, die oft aus Compliance- oder Lizenzgründen gewählt wird, wenn es erforderlich ist, dass die Ressourcen physisch isoliert sind und nicht mit anderen geteilt werden. Mit dedizierter Tenancy bekommst du eine höhere Kontrolle über die zugewiesenen Ressourcen, jedoch ist dies in der Regel kostspieliger im Vergleich zu den Standardoptionen, bei denen die Ressourcen auf gemeinsam genutzter Hardware bereitgestellt werden.*), 

was exklusiven Zugriff auf physische Hardware in einem AWS-Rechenzentrum bedeutet. Dies ist kostspielig, aber sinnvoll, wenn du mit Technologien arbeitest, die strenge Lizenzrichtlinien haben.

**Mit [EC2 VM Import](https://aws.amazon.com/de/ec2/vm-import/) kannst du vorhandene VMs in AWS importieren, solange diese [VMware](https://de.wikipedia.org/wiki/VMware) ESX, VMware Workstation, Microsoft [Hyper-V](https://de.wikipedia.org/wiki/Hyper-V) oder [Citrix](https://de.wikipedia.org/wiki/Citrix_Systems) Xen Virtualisierungsformate verwenden.**

Bei der Instanzenerstellung versucht EC2, die Instanz so zu platzieren, dass deine VMs auf verschiedenen Hardwarekomponenten verteilt werden, um Ausfälle an einem Ort zu begrenzen. Platzierungsgruppen können verwendet werden, um die Platzierung von voneinander abhängigen Instanzen zu beeinflussen.

Beim Starten einer neuen EC2-Instanz kannst du [Benutzerdaten](https://docs.aws.amazon.com/de_de/AWSEC2/latest/UserGuide/instancedata-add-user-data.html) (*Spezifiziere Benutzerdaten, um Befehle oder ein Befehlsskript bereitzustellen, das beim Start deiner Instance ausgeführt wird. Die Eingabe wird beim Start deiner Instance [base64](https://de.wikipedia.org/wiki/Base64)-kodiert*) an die Instanz übergeben, um automatisierte Konfigurationsaufgaben oder Skripte auszuführen.

Die Standard-IP-Adresse einer EC2-Instanz wird freigegeben, wenn die Instanz gestoppt ist. Bei Bedarf an einer dauerhaften öffentlichen IP-Adresse verwendest du eine Elastic IP-Adresse.

Wenn du eine SQL-Datenbank selbst verwalten musst, kann EC2 eine solide Alternative zu RDS sein. Für hohe Verfügbarkeit solltest du mindestens eine weitere EC2-Instanz in einer separaten Verfügbarkeitszone haben.

Ein Golden Image ist einfach ein AMI, das vollständig nach deinen Wünschen angepasst wurde und alle notwendigen Software-/Daten-/Konfigurationsdetails enthält, um neue Instanzen zu starten.

Instanzstatusüberprüfungen überwachen die Gesundheit des laufenden EC2-Servers, Systemstatusüberprüfungen überwachen die Gesundheit des zugrunde liegenden Hypervisors.

EC2-Instanzpreise:
On-Demand-Instanzen basieren auf einem festen Stundensatz und können jederzeit gestartet und gestoppt werden, ohne langfristige Verpflichtungen.

Reserved Instances bieten exklusive Nutzung zu reduzierten Preisen für 1 oder 3 Jahre.

Spot Instances nutzen überschüssige Kapazitäten von Amazon und erfordern finanzielle Gebote. Sie sind ideal für flexible Workloads mit start- und endbaren Zeiten.

Standard Reserved vs. Convertible Reserved vs. Scheduled Reserved:
Standard Reserved Instances haben unflexible Reservierungen mit 75% Rabatt. Sie können nicht zwischen Regionen verschoben werden.

Convertible Reserved Instances haben 54% Rabatt und ermöglichen die Änderung des Instanztyps.

Scheduled Reserved Instances sind nach einem festgelegten Zeitplan reserviert und eignen sich für zeitlich begrenzte Workloads.

EC2-Instanzlebenszyklus:
Die Tabelle zeigt verschiedene Zustände, die eine VM zu einem bestimmten Zeitpunkt haben kann, mit entsprechender Abrechnung.

EC2-Sicherheit:
Bei der Bereitstellung einer EC2-Instanz bist du für das Management des Gastbetriebssystems, Anwendungssoftware, und die Konfiguration der AWS-Firewall (Security Group) verantwortlich.

Die Termination Protection ist standardmäßig deaktiviert und sollte aktiviert werden, um versehentliches Löschen zu verhindern.

EC2 verwendet Public-Key-Kryptografie für die Verschlüsselung von Anmeldeinformationen.

Die Verschlüsselung der Root-Volume ist während der Erstellung der Instanz oder mit Drittanbieter-Tools möglich.

EC2 Placement Groups:
Platzierungsgruppen bieten eine Balance zwischen Risikotoleranz und Netzwerkleistung für EC2-Instanzen.

Es gibt drei Arten von Platzierungsgruppen: Clustered, Spread und Partitioned.

Clustered Gruppen sind für Anwendungen mit niedrigster Latenz und höchster Netzwerkdurchsatz empfohlen.

Spread Gruppen isolieren einzelne Instanzen für Anwendungen mit wenigen kritischen Instanzen.

Partitioned Gruppen bieten eine Balance zwischen Risiko und Netzwerkleistung.

Instanzen können in eine Platzierungsgruppe verschoben werden, wenn sie gestoppt sind. Einzigartige Namen sind erforderlich.

Bitte beachte, dass bei Instanzbeendigung Reserved Instances bis zum Ende der Vertragslaufzeit abgerechnet werden.


[Zurück zum Leitfaden](../../README.md)
