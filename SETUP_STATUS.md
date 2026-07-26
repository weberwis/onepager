# Entwicklungsumgebung – Status

Stand: 26. Juli 2026

## Git

- Git ist installiert: `git version 2.55.0.windows.3`
- Globaler Benutzername: `weberwis`
- Globale E-Mail-Adresse: `309399581+weberwis@users.noreply.github.com`

## GitHub CLI

- GitHub CLI ist installiert: `gh version 2.96.0`
- Aktives GitHub-Konto: `weberwis`
- Der Zugriffstoken ist aktiv und sicher im Windows-Schlüsselspeicher hinterlegt.
- Berechtigungen: `repo`, `read:org`, `gist`, `admin:public_key`
- Für Git-Operationen ist in der GitHub CLI das SSH-Protokoll ausgewählt.

Der Tokenwert wird aus Sicherheitsgründen nicht in diesem Projekt gespeichert.

## SSH

Ein ED25519-Schlüsselpaar ist vorhanden:

- Privater Schlüssel: `%USERPROFILE%\.ssh\id_ed25519_laptopsshkey`
- Öffentlicher Schlüssel: `%USERPROFILE%\.ssh\id_ed25519_laptopsshkey.pub`

Der private Schlüssel darf weder veröffentlicht noch in ein Git-Repository
übernommen werden.

### Aktueller Zustand

Die SSH-Authentifizierung bei GitHub ist derzeit noch nicht aktiv. Der Test

```powershell
ssh -T git@github.com
```

endet mit:

```text
Permission denied (publickey).
```

Außerdem ist aktuell kein SSH-Agent erreichbar. Der Schlüssel ist somit zwar
vorhanden, wird aber noch nicht automatisch für die Verbindung zu GitHub
verwendet.

## Projektstatus

Dieser Ordner ist derzeit noch kein Git-Repository und besitzt deshalb noch
kein GitHub-Remote.
