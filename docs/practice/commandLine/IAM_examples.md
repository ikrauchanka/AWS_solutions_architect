## IAM Rolle erstellen
`aws iam create-role --role-name <role-name> --assume-role-policy-document file://trust-policy.json`

## IAM Benutzer erstellen
`aws iam create-user --user-name <user-name>`

## Passwort für den IAM Benutzer festlegen
`aws iam create-login-profile --user-name <user-name> --password <password>`

## MFA für den IAM Benutzer aktivieren
`aws iam enable-mfa-device --user-name <user-name> --serial-number <mfa-serial-number> --authentication-code1 <code1> --authentication-code2 <code2>`

## Zugriffsrichtlinie erstellen
`aws iam create-policy --policy-name <policy-name> --policy-document file://policy.json`

## Richtlinie einer Rolle oder eines Benutzers hinzufügen
`aws iam attach-role-policy --role-name <role-name> --policy-arn <policy-arn>`

## Aktuelle Zugriffsrichtlinien anzeigen
`aws iam list-policies`

[Zurück zum Leitfaden](../../../README.md)
