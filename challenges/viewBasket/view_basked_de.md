# View Basket

**Broken Access Control**

> *View another user's shopping basket.*

---

## Schwierigkeit

⭐⭐☆☆☆☆ 2-Sterne-Challenge (leicht)

---

## Beschreibung

Diese Herausforderung demonstriert die **horizontale Privilegienerweiterung**, bei der ein Benutzer auf Daten zugreifen kann, die einem anderen Benutzer mit der gleichen Privilegstufe gehören. Konkret kann ein Angreifer den Warenkorb eines anderen Benutzers einsehen, indem er clientseitige Daten manipuliert.

Wenn ein Angreifer in der Lage ist, seine Sitzung mit einer anderen `basketId` zu verknüpfen, kann er die Artikel im Einkaufskorb eines anderen Benutzers sehen und manipulieren - möglicherweise sogar dessen Bestellvorgang stören. Dies stellt ein Versäumnis dar, Benutzersitzungen sicher mit ihren eigenen Daten auf der Serverseite zu verknüpfen.

---

## Hinweis
This horizontal privilege escalation challenge demands you to access the shopping basket of another user. Being able to do so would give an attacker the opportunity to spy on the victims shopping behaviour. He could also play a prank on the victim by manipulating the items or their quantity, hoping this will go unnoticed during checkout. This could lead to some arguments between the victim and the vendor.

- Try out all existing functionality involving the shopping basket while having an eye on the HTTP traffic.
- There might be a client-side association of user to basket that you can try to manipulate.
- In case you manage to update the database via SQL Injection so that a user is linked to another shopping basket, the application will not notice this challenge as solved.

---

## Vorgehen

1. **Eingeloggt** als normaler Benutzer und ein Produkt in den Warenkorb gelegt.
2. In den Browser DevTools(F12) unter *Application -> Session storage* finden wir die key's bid (BaskedID) & itemTotal (Gesamtpreis).
3. Beobachten Sie die folgenden Schlüssel:
   - `bid`: Aktuelle Warenkorb-ID
   - `itemTotal`: Gesamtwert des Korbs
4. **Manuelles Ändern des „Gebots“-Werts** in eine andere Zahl (z. B. „3“, ‚1‘, „2“).
5. **Die Seite wird neu geladen**.
6. Die Anwendung hat Artikel aus dem Warenkorb eines anderen Benutzers angezeigt.
7. Daraufhin erscheint ein Banner, das bestätigt, dass die Aufgabe gelöst wurde.

---

## Beweis (Screenshot)

Mein Warenkorb
![alt text](/img/your_basket.png)

Fremder Warenkorb
![alt text](/img/any_basket.png)

Admin Warenkorb zum vergleich
![alt text](/img/admin_basked.png)

:::
You successfully solved a challenge: View Basket (View another user's shopping basket.)
:::