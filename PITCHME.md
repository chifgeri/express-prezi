
# Express**JS**

+++

# Express**TS**

---

![express](assets/images/express-mongo.jpg)

---

![node](assets/images/nodejs.svg)

---


## A Node futtatókörnyezet

@ul[list-square-bullets list-spaced-bullets font-righteous]
* Nem backend keretrendszer
* Webszerverek kiszolgálására
* JavaScriptet futtat
* V8 motor
* Eventek és aszinkron IO
@ulend
--- 

# Express
A legnépszerűbb Node backend keretrendszer

---

## Egyszerű. gyors és skálázható webalkalmazások

### Fő építő elemei:
 - Útvonal választás
 - Middleware függvények

--- 

  App objektum és a routing

+++

 ```js
    
    const express = require('express')
    const app = express()
    const port = 3000

    app.listen(port, () => console.log(`Example app listening on port ${port}!`))

 ```

    @[1,2]
    @[3]
    @[4,6]

---

Middlewarek

+++

Request objektum

kód

+++

Response objektum

kód

+++

A next() függvény

---

Hibakezelés

+++

Kód

---

Perzisztens adattárolás MongoDB-vel

---

- JSON dokumentumok tárolása
- Struktúrálatlan adatok
- Nincs validáció

---

Mongoose package

- ODM könyvtár
- JavaScript objektumok mappelése
- MongoDB kezelése

+++

Kód

---


