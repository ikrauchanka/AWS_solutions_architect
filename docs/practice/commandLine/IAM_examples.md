# IAM Rolle erstellen
`aws iam create-role --role-name <role-name> --assume-role-policy-document file://trust-policy.json`

# IAM Benutzer erstellen
aws iam create-user --user-name <user-name>

# Passwort für den IAM Benutzer festlegen
aws iam create-login-profile --user-name <user-name> --password <password>

# MFA für den IAM Benutzer aktivieren
aws iam enable-mfa-device --user-name <user-name> --serial-number <mfa-serial-number> --authentication-code1 <code1> --authentication-code2 <code2>

