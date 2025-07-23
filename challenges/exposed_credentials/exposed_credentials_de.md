# Exposed credentials

**Sensitive Data Exposure**

> *A developer was careless with hardcoding unused, but still valid credentials for a testing account on the client-side.*

---

## Schwierigkeit

⭐⭐☆☆☆☆ 2-Sterne-Challenge (leicht)

---

## Beschreibung

Diese Aufgabe demonstriert ein häufiges Sicherheitsrisiko, bei dem sensible Anmeldeinformationen versehentlich in clientseitigem Code hinterlassen werden. Obwohl das Konto nicht mit einem Menüpunkt oder einer Rolle verknüpft ist, ist es immer noch aktiv und kann zum Einloggen verwendet werden.

---

## Hinweis

Ein Entwickler hat unvorsichtigerweise unbenutzte, aber immer noch gültige Anmeldeinformationen hart kodiert.

---

## Vorgehen

1. Öffnen Sie die Anwendung unter:  
   [http://127.0.0.1:3000](http://127.0.0.1:3000)

2. Öffnen Sie im Browser **DevTools(`F12`) -> `Sources`** die Datei `main.*.js`.

3. Benutze die Suchfunktion (`Strg+F`) um nach Schlüsselwörtern zu suchen wie:
   - `E-Mail`, `Passwort`
   - Berechtigungsnachweise
   - `test@`, `user@` oder `admin@`
   - `@juice-sh.op`

4. Sie finden hartkodierte Anmeldeinformationen:
```js
   { 
      testingUsername = "testing@juice-sh.op",
      testingPassword = "IamUsedForTesting"
   }
```
5. Loggen Sie sich mit den Test-Zugangsdaten ein und die Aufgabe wird automatisch als **gelöst** markiert.

---

## Beweis (Screenshot)

![test_login](/img/test_login.png)