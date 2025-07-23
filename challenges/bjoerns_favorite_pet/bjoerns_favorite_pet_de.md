# Bjoern's Favorite Pet

**Broken Authentication**

> *Reset the password of Bjoern's OWASP account via the [Forgot Password](http://127.0.0.1:3000/#/forgot-password) mechanism with the original answer to his security question.*

---

## Difficulty

⭐⭐⭐☆☆☆ 3-Sterne-Challenge (medium)

---

## Beschreibung

This challenge demonstrates a common security risk where sensitive credentials are accidentally left in client-side code. Although the account is not linked to any menu item or role, it is still active and can be used to log in.

---

## Hinweis

Bei dieser Herausforderung geht es nicht um eine technische Sicherheitslücke. Stattdessen geht es darum, die Antwort auf die von Benutzer Bjoern gewählte Sicherheitsfrage herauszufinden und sie zu verwenden, um das Passwort seines OWASP-Kontos zurückzusetzen.

> Viele Website-Registrierungen verwenden Sicherheitsfragen sowohl zum Abrufen/Rücksetzen des Passworts als auch zur Überprüfung der Anmeldung. Einige stellen dieselben Sicherheitsfragen auch bei telefonischen Anrufen. Sicherheitsfragen sind eine Methode zur Verifizierung des Benutzers und zur Verhinderung von unbefugtem Zugriff. Aber es gibt Probleme mit Sicherheitsfragen. Websites können schlechte Sicherheitsfragen verwenden, die negative Folgen haben können:
> 
> Der Benutzer kann sich nicht mehr genau an die Antwort erinnern oder die Antwort hat sich geändert, die Frage funktioniert für den Benutzer nicht, die Frage ist nicht sicher und könnte von anderen entdeckt oder erraten werden. Es ist wichtig, dass wir gute Fragen verwenden. Gute Sicherheitsfragen erfüllen fünf Kriterien. Die Antwort auf eine gute Sicherheitsfrage lautet:
>
> - Sicher: kann nicht erraten oder erforscht werden
> - Stabil: ändert sich nicht im Laufe der Zeit
> - Einprägsam: kann man sich merken
> - Einfach: ist präzise, einfach, konsistent
> - Viele: hat viele mögliche Antworten
>
> Es ist schwierig, Fragen zu finden, die alle fünf Kriterien erfüllen, was bedeutet, dass einige Fragen gut, einige mittelmäßig und die meisten schlecht sind. In Wirklichkeit gibt es nur wenige, wenn überhaupt, GUTE Sicherheitsfragen. Die Menschen geben in sozialen Medien, Blogs und Websites so viele persönliche Informationen preis, dass es schwierig ist, Fragen zu finden, die die oben genannten Kriterien erfüllen. Außerdem sind viele Fragen für manche Menschen nicht zutreffend, z. B. wie lautet der Spitzname Ihres ältesten Kindes - aber Sie haben kein Kind.

- Hinweise auf die Antwort auf Björn's Frage findet man, wenn man im Internet nach ihm sucht.

- Genauer gesagt könnte sich Björn versehentlich (😜) selbst verraten haben, indem er bei mindestens einer Gelegenheit, bei der eine Kamera lief, seine Sicherheitsantwort erwähnte.

- Mit einer hinreichend umfangreichen Liste gängiger Kosenamen wäre es durchaus möglich, die Antwort zu erzwingen.

> Doxing (von dox, Abkürzung für Dokumente) oder Doxxing ist die internetbasierte Praxis, private oder identifizierbare Informationen (insbesondere persönlich identifizierbare Informationen) über eine Person oder Organisation zu recherchieren und zu verbreiten.
>
> Die Methoden zur Beschaffung dieser Informationen umfassen das Durchsuchen öffentlich zugänglicher Datenbanken und Websites sozialer Medien (wie Facebook), Hacking und Social Engineering. Es ist eng mit Internet-Vigilantismus und Hacktivismus verwandt.
>
> Doxing kann aus verschiedenen Gründen durchgeführt werden, z. B. zur Unterstützung der Strafverfolgung, Geschäftsanalyse, Risikoanalyse, Erpressung, Nötigung, Zufügung von Schaden, Belästigung, Online-Beschämung und Selbstjustiz.

---

## Vorgehen

1. Die Email rausfinden.
2. Es gibt einen beitrag auf einem Produktkarte

    > - bjoern@juice-sh.op    ->  Question: Your Zip/postal code when you were a teenager
    > - bjoern@owasp.org      ->  Question: Name of your favorite pet?

- Bild name des Produkts -> snakes_ladders.jpg
- Link to [Steam Community](https://steamcommunity.com/sharedfiles/filedetails/?id=1969196030)

![bjoern@juice-shop](/img/bjoern@juice-shop.png)
![reviews](/img/reviews.png)
![bjoern@owasp](/img/bjoern@owasp.png)

3. Wir haben den richtigen Björn/Email gefunden.
4. Weiteren Hinweisen suchen wir auf in den **Sozialen Netzwerken** mit der gefunden Email adresse.

5. Auf Twitter finden wir unter der `bjoern@owasp.org` den account von **"Björn Kimminich"**.
6. Unter dem Reiter `Media` finden wir mehere Katzen Bilder/Videos mit kommentaren. Darin taucht ab und zu der Name **Zaya** auf.

[https://x.com/bkimminich/media](https://x.com/bkimminich/media)
![Zaya](/img/zaya.png)
![Zaya2](/img/zaya2.png)

7. Wir gehen zurück auf den Juice-Shop auf [Forgot Password](http://127.0.0.1:3000/#/forgot-password) und geben `Zaya` als antwort ein.

8. Challenge wurde beim erfolgreichen ändern [Change] automatisch als **gelöst** markiert.

---

## Beweis (Screenshot)

![new_pw](/img/new_pw.png)
