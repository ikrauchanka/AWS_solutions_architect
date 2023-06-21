## Installation der AWS CLI:
Stelle sicher, dass du Python auf deinem Computer installiert hast, da die AWS CLI eine Python-basierte Anwendung ist.
Öffne ein Terminal oder eine Befehlszeile und führe den folgenden Befehl aus, um die AWS CLI über pip zu installieren:

`pip install awscli`

## Konfiguration der AWS CLI:
Nach der Installation musst du die AWS CLI konfigurieren, um dich bei deinem AWS-Konto anzumelden.
Führe im Terminal den Befehl

`aws configure` 

aus.

Gib deine 
* AWS Access Key ID,
* Secret Access Key,
* die Region (z. B. "eu-central-1") und
* das gewünschte Ausgabeformat (z. B. "json") ein,

wenn du dazu aufgefordert wirst. Diese Informationen findest du in den Sicherheitsanmeldeinformationen deines AWS-Kontos.

## Sicherheitsanmeldung bei der AWS CLI:
Nachdem du die Konfiguration abgeschlossen hast, kannst du dich sicher bei der AWS CLI anmelden, indem du den Befehl

`aws configure` 

ausführst.
Du kannst überprüfen, ob die Anmeldung erfolgreich war, indem du den Befehl

`aws sts get-caller-identity` 

ausführst. Dies sollte Informationen über deinen IAM-Benutzer zurückgeben.

Bitte beachte, dass die genauen Schritte je nach Betriebssystem variieren können. Stelle sicher, dass du die offizielle AWS-Dokumentation für detaillierte Anweisungen zu Installation und Konfiguration der AWS CLI konsultierst.

[Zurück zum Leitfaden](../../../README.md)
