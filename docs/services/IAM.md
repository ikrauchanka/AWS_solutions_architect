# IAM (Identitäts-Zugriffs-Verwaltung)

## Kurz und bündig:

**IAM** bietet einen **_zentralen_ Kontrollpunkt** innerhalb von AWS und ist in allen anderen AWS-Diensten integriert. **IAM** bietet die Möglichkeit, den *Zugriff* auf verschiedenen **_Berechtigungsebenen_ freizugeben**, und unterstützt die Möglichkeit, *Identitätsverbund* (den Prozess der Delegierung der Authentifizierung an eine vertrauenswürdige externe Partei wie Facebook oder Google) für vorübergehenden oder begrenzten Zugriff zu nutzen. **IAM** bietet **MFA**-Device-Support (**Multi-Faktor-Authentifizierung**) z. B den [Google Authenticator](https://play.google.com/store/apps/details?id=com.google.android.apps.authenticator2&pli=1), und ermöglicht dir die Einrichtung einer **_benutzerdefinierten_ Passwort-Rotationsrichtlinie** für das gesamte Unternehmen. Außerdem ist es **[_PCI_ _DSS_](https://de.wikipedia.org/wiki/Payment_Card_Industry_Data_Security_Standard)-konform**, d. h. dem Datensicherheitsstandard der Kreditkartenindustrie. (Der Service erfüllt sozusagen die von der Regierung erlassenen *Sicherheitsvorschriften* für Kreditkarten).

## IAM [Entitäten](https://de.wikipedia.org/wiki/Entität)

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
* AWS [Lambda](services/Lambda.md),

das Schreibberechtigungen für [S3](docs/s3.md) benötigt, oder eine 
* eine Flotte von [EC2](docs/EC2.md)-Instanzen,

die Leseberechtigungen für eine RDS-MySQL-Datenbank benötigen.

### Richtlinien:
Die dokumentierten Regelsätze, die angewendet werden, um den Zugriff zu gewähren oder einzuschränken. Damit 
* Benutzer,
* Gruppen oder
* Rollen

die Berechtigungen richtig festlegen können, verwenden sie Richtlinien. Richtlinien werden in [JSON](https://de.wikipedia.org/wiki/JavaScript_Object_Notation) geschrieben und Sie können entweder benutzerdefinierte Richtlinien für Ihre spezifischen Anforderungen oder die von AWS festgelegten Standardrichtlinien verwenden.
