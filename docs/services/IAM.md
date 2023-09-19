# IAM (Identitäts-Zugriffs-Verwaltung)
## Kurz und bündig:

**IAM** ist ein globaler Service, bietet einen **_zentralen_ Kontrollpunkt** innerhalb von AWS und ist in allen anderen AWS-Diensten integriert. **IAM** bietet die Möglichkeit, den *Zugriff* auf verschiedenen **_Berechtigungsebenen_ freizugeben**, und unterstützt die Möglichkeit, *Identitätsverbund* (den Prozess der Delegierung der Authentifizierung an eine vertrauenswürdige externe Partei wie Facebook oder Google) für vorübergehenden oder begrenzten Zugriff zu nutzen. **IAM** bietet **MFA**-Device-Support (**Multi-Faktor-Authentifizierung**) z. B den [Google Authenticator](https://play.google.com/store/apps/details?id=com.google.android.apps.authenticator2&pli=1), und ermöglicht dir die Einrichtung einer **_benutzerdefinierten_ Passwort-Rotationsrichtlinie** für das gesamte Unternehmen. Außerdem ist es **[_PCI_ _DSS_](https://de.wikipedia.org/wiki/Payment_Card_Industry_Data_Security_Standard)-konform**, d. h. mit dem Datensicherheitsstandard der Kreditkartenindustrie. (Der Service erfüllt sozusagen die von der Regierung erlassenen *Sicherheitsvorschriften* für Kreditkarten).

## IAM [Entitäten](https://de.wikipedia.org/wiki/Entität)

### Root User:
Der AWS Root User ist der erste Benutzeraccount, der bei der Erstellung eines neuen AWS-Kontos erstellt wird. Dieser Benutzer hat die höchsten Berechtigungen und Kontrollen über das AWS-Konto und ist daher von entscheidender Bedeutung für die Sicherheit und Verwaltung des AWS-Kontos.
* Vermeiden sie die Standartnutzung des Root Users
  
  - Der Root User sollte nur in seltenen Fällen verwendet werden, z. B. wenn Sie Ihr Konto erstellen oder grundlegende Sicherheitsänderungen vornehmen müssen. Für den täglichen Betrieb und die Verwaltung von AWS-Ressourcen sollten IAM (Identity and Access Management)-Benutzer mit den entsprechenden Berechtigungen erstellt werden.
### Benutzer:
Jeder einzelne Endbenutzer, z. B. ein 
* Mitarbeiter,
* Systemarchitekt,
* CTO (Chief Technology Officer) usw.

### Gruppen: 
Eine beliebige Ansammlung ähnlicher Personen mit gemeinsamen Berechtigungen, z. B. 
* Systemadministratoren,
* HR-Mitarbeiter,
* Finanzteams usw.

Jeder Benutzer innerhalb der angegebenen Gruppe erbt die für die Gruppe festgelegten Berechtigungen.

### Rollen:
Jeder Softwareservice, der Berechtigungen benötigt, um seine Aufgabe zu erfüllen, z. B. 
* AWS [Lambda](../services/Lambda.md),

das Schreibberechtigungen für [s3](../services/s3.md) benötigt, oder eine 
* eine Flotte von [EC2](../services/EC2.md)-Instanzen,

die Leseberechtigungen für eine RDS-MySQL-Datenbank benötigen.

### Richtlinien (Policies):
Die dokumentierten Regelsätze, die angewendet werden, um den Zugriff zu gewähren oder einzuschränken. Damit 
* Benutzer,
* Gruppen oder
* Rollen

die Berechtigungen richtig festlegen können, verwenden sie Richtlinien. Richtlinien werden in [JSON](https://de.wikipedia.org/wiki/JavaScript_Object_Notation) geschrieben und Sie können entweder benutzerdefinierte Richtlinien für Ihre spezifischen Anforderungen oder die von AWS festgelegten Standardrichtlinien verwenden.

[Entwurf](../practice/drafts/IAM_usecase.md) und [Beispiele](../practice/commandLine/IAM_examples.md)

[Zurück zum Leitfaden](../../README.md)

![Zugriffsmanagement](../../docs/pngs/policies.png)

