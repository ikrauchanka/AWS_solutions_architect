# IAM Identitäts-Zugriffs-Verwaltung

## Kurz und bündig:

**IAM** bietet einen **_zentralen_ Kontrollpunkt** innerhalb von AWS und ist in allen anderen AWS-Diensten integriert. **IAM** bietet die Möglichkeit, den *Zugriff* auf verschiedenen **_Berechtigungsebenen_ freizugeben**, und unterstützt die Möglichkeit, *Identitätsverbund* (den Prozess der Delegierung der Authentifizierung an eine vertrauenswürdige externe Partei wie Facebook oder Google) für vorübergehenden oder begrenzten Zugriff zu nutzen. **IAM** bietet **MFA**-Device-Support (**Multi-Faktor-Authentifizierung**) und ermöglicht dir die Einrichtung einer **_benutzerdefinierten_ Passwort-Rotationsrichtlinie** für das gesamte Unternehmen. Außerdem ist es **_PCI_ _DSS_-konform**, d. h. dem Datensicherheitsstandard der Kreditkartenindustrie. (der Service erfüllt sozusagen die von der Regierung erlassenen *Sicherheitsvorschriften* für Kreditkarten).

## IAM [Entitäten](https://de.wikipedia.org/wiki/Entität)

### Benutzer:
jeder einzelne Endbenutzer, z. B. ein 
* Mitarbeiter,
* Systemarchitekt,
* CTO usw.

### Gruppen: 
eine beliebige Ansammlung ähnlicher Personen mit gemeinsamen Berechtigungen, z. B. 
* Systemadministratoren,
* HR-Mitarbeiter,
* Finanzteams usw.

Jeder Benutzer innerhalb der angegebenen Gruppe erbt die für die Gruppe festgelegten Berechtigungen.

