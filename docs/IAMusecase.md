# Der Entwurf eines sichern Zugriffs auf AWS Ressourcen

## 1. IAM Rollen und Benutzer erstellen
a) IAM Rollen für verschiedene:
* Aufgaben
* Funktionen
b) IAM Benutzerkonnten für Einzelpersonen
c) Passwortvergabe und MFA (Multi-Faktor-Authentifizierungs)- Aktivierung

## 2. Berechtigungen und Zugriffsrichtlinien verwalten.
a) Definition von Berechtigungen, mit Hilfe von:
* Zugriffsrichtlinien
* d. Prinzip der geringsten Privilegien
b) regelmäßige Kontrolle der Zugriffsrichtlinien, um sicherzustellen, dass sie:
* den aktuellen Anforderungen entsprechen
* noch nötig sind.

## 3. Verwaltung des Verbundzugriffes
Implementation des Single-Sign-On Zugriff [SSO], um:
a) den Zugriff auf meherere Konten:
* zu zentralisiseren, und
* zu vereinfachen...
b) den Verbund mit externen Identitätsanbietern zu konfigurieren, um:
* eine nahtlose, und 
* sichere Authentifizierung zu ermöglichen...

## 4. Netzwerksicherheit gewährleisten
a) Verwendung der VPC (virtual private cloud) um:
* Netzwerksegmentierung, und
* isolierte Umgebungen zu ermöglichen...
b) Konfiguration der
* Sicherheitsgruppen
* Netzwerk ACL's, um:
- den Datenverkehr zu kontrollieren, und
- unerlaubte Zugriffe zu blockieren...
c) Implementation einer sicheren Datenübertragung über:
* verschlüsselte Verbindungen z. B. (SSL/TLS) für HTTPS

## 5. Überwachung und Protokollierung
Aktivierung des Cloud Trail Protokollierungstool, um:
a) alle Aktionen auf dem AWS Konto aufzuzeichnen.
* Einbindung von Cloud Watch um Alarme für:
- verdächtige Aktivitäten
- oder Anomalien

zu konfigurieren.
