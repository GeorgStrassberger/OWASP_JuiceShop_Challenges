# Web3 Sandbox

**Broken Access Control**

> *Find an accidentally deployed code sandbox for writing smart contracts on the fly.*

---

## Schwierigkeit

⭐☆☆☆☆☆ 1-Sterne-Challenge (leicht)

---

## Beschreibung

Ein versehentlich veröffentlichter Endpunkt (`/web3-sandbox`) ermöglicht den Zugriff auf eine Smart-Contract-Sandbox. Der Zugriff erfordert keine Authentifizierung oder Berechtigung, was einen klassischen Fall von **Broken Access Control** darstellt.

> **Broken Access Control** tritt auf, wenn Benutzer auf Funktionen oder Daten zugreifen können, für die sie keine Berechtigung haben. Dies kann durch fehlende oder falsch konfigurierte Zugriffskontrollen entstehen.

---

## Vorgehen

1. Laborumgebung gestartet und Zugriff auf die Juice Shop-Anwendung über den Browser:  
   [http://127.0.0.1:3000](http://127.0.0.1:3000)

2. Mit den DevTools (F12) Hinweise auf mögliche versteckte Routen im Quellcode (`index.html`,`main.js`, ...) gesucht, nach Begriffen wie:
     - `/sandbox`
     - `/web`
     - `/editor`
     - `/contracts`
     - `/access`
     - ...

    ![DevTools](devlools.png)

3. Der Aufruf von: `http://127.0.0.1:3000/#` + `/web3-sandbox` öffnet eine öffentlich zugängliche Code-Sandbox.

4. Challenge wurde beim Aufruf automatisch als **gelöst** markiert.

---

## Beweis (Screenshot)

```text
URL: http://127.0.0.1:3000/#/web3-sandbox

Status Code: 200 OK

Zugriff: Ohne Authentifizierung oder spezielle Rechte möglich
```

![Sandbox Screenshot](/img/web3sandbox.png)
