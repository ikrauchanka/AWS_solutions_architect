# Der Entwurf eines sichern Zugriffs auf AWS Ressourcen

## 1. IAM Rollen und Benutzer erstellen
IAM Rollen für verschiedene:
* Aufgaben
* Funktionen

IAM Benutzerkonnten für Einzelpersonen
Passwortvergabe und MFA (Multi-Faktor-Authentifizierungs)- Aktivierung

## 2. Berechtigungen und Zugriffsrichtlinien verwalten.
Definition von Berechtigungen, mit Hilfe von:
* Zugriffsrichtlinien
* d. Prinzip der geringsten Privilegien


Regelmäßige Kontrolle der Zugriffsrichtlinien, um sicherzustellen, dass sie:
* den aktuellen Anforderungen entsprechen
* noch nötig sind.

## 3. Verwaltung des Verbundzugriffes
Implementation des Single-Sign-On Zugriff [SSO], um:
den Zugriff auf meherere Konten:
* zu zentralisiseren, und
* zu vereinfachen...

den Verbund mit externen Identitätsanbietern zu konfigurieren, um:
* eine nahtlose, und 
* sichere Authentifizierung zu ermöglichen...

## 4. Netzwerksicherheit gewährleisten
Verwendung der VPC (virtual private cloud) um:
* Netzwerksegmentierung, und
* isolierte Umgebungen zu ermöglichen...

Konfiguration der Sicherheitsgruppen, und Netzwerk ACL's, um:
- den Datenverkehr zu kontrollieren, und
- unerlaubte Zugriffe zu blockieren...

Implementation einer sicheren Datenübertragung über:
* verschlüsselte Verbindungen z. B. (SSL/TLS) für HTTPS

## 5. Überwachung und Protokollierung
Aktivierung des Cloud Trail Protokollierungstool, um:
alle Aktionen auf dem AWS Konto aufzuzeichnen.
* Einbindung von Cloud Watch um Alarme für:
- verdächtige Aktivitäten
- oder Anomalien

zu konfigurieren.
