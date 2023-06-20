# Der Entwurf eines sichern Zugriffs auf AWS Ressourcen

## IAM Rollen und Benutzer erstellen
IAM Rollen für verschiedene:
* Aufgaben
* Funktionen

	- IAM Benutzerkonnten für Einzelpersonen

	- Passwortvergabe und MFA (Multi-Faktor-Authentifizierungs)- Aktivierung

2) Berechtigungen und Zugriffsrichtlinien verwalten.

	- Definition von Berechtigungen, mit Hilfe von:

	a) Zugriffsrichtlinien

	b) d. Prinzip der geringsten Privilegien

	- regelmäßige Kontrolle der Zugriffsrichtlinien, um sicherzustellen, dass sie:

	a) den aktuellen Anforderungen entsprechen

	b) noch nötig sind.

3) Verwaltung des Verbundzugriffes

	- Implementation des Single-Sign-On Zugriff [SSO], um:

	a) den Zugriff auf meherere Konten:

		* zu zentralisiseren, und
 
		* zu vereinfachen...

	b) den Verbund mit externen Identitätsanbietern zu konfigurieren, um:

		* eine nahtlose, und 

		* sichere Authentifizierung zu ermöglichen...

4) Netzwerksicherheit gewährleisten

	- Verwendung der VPC (virtual private cloud) um:

	a) Netzwerksegmentierung, und

	b) isolierte Umgebungen zu ermöglichen...

	- Konfiguration der

	a) Sicherheitsgruppen

	b) Netzwerk ACL's, um:

		* den Datenverkehr zu kontrollieren, und

		* unerlaubte Zugriffe zu blockieren...

	- Implementation einer sicheren Datenübertragung über:

	a) verschlüsselte Verbindungen z. B. (SSL/TLS) für HTTPS

5) Überwachung und Protokollierung

	- Aktivierung des Cloud Trail Protokollierungstool, um:

	a) alle Aktionen auf dem AWS Konto aufzuzeichnen.

	- Einbindung von Cloud Watch um Alarme für:

	a) verdächtige Aktivitäten

	b) oder Anomalien

zu konfigurieren.
