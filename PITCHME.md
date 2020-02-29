
# Express**JS**

+++

# Express**TS**

---

![express](assets/images/express-mongo.jpg)

---

@snap[midpoint span-50]
![node](assets/images/nodejs.svg)
@snapend

+++

![nodememe](assets/images/nodememe.png)

---

## A Node futtatókörnyezet

@ul[list-square-bullets list-spaced-bullets font-righteous]
* Nem backend keretrendszer
* Inkább szerver oldali platform
* Webszerverek kiszolgálására
* V8 motor
* Event-loop és aszinkron I/O
@ulend

--- 

## Express
A legnépszerűbb Node alapú backend keretrendszer

---

### Egyszerű, gyors és skálázható webalkalmazások

#### Fő építő elemei:
 - Útvonal választás
 - Middleware függvények

--- 

### App objektum és a routing

+++

```js 
const express = require('express')
const app = express()
const port = 3000

app.listen(port, () => console.log(`Example app listening on port ${port}!`))

```

@[1,2]
@[3]
@[5]

+++

```js
app.use('/user', middlewareA(), (req, resp, next) =>{ });

app.get('/user/:id', middlewareA(), middlewareB());
app.post('/user', middlewareB());
app.delete('/user/:id', middlewareA(), middlewareB());

```
@snap[south]
@[1](Összes kérés beérkezik, ami az URL-re illeszkedik)
@[3-5](Csak a megfelelő kérés beérkezésekor reagál)
@snapend

---

## Middlewarek

+++

### Request objektum

```js
const bodyParser = require('body-parser')
// for parsing application/json
app.use(bodyParser.json()) 

...

//Valami middleware
(req, res, next) => {
    const formData = req.body;
    const userid = req.params.id;
    const path = req.path;
    const colorQuery = req.query.color;
    console.log(req.method);
}
```

@snap[south]
@[1-3](Body-parser kell a HTTP body eléréséhez)
@[7-14]
@[9](Body-ban található JSON adatok)
@[10](Url paraméterek itt pl. user/:id)
@[11](Relative elérési út)
@[12](Query paraméterek pl. ?color=black)
@[13](A kérés HTTP metódusa)
@snapend

+++

### Response objektum

kód

+++

### A next() függvény

---

### Hibakezelés

+++

Kód

---

## Perzisztens adattárolás MongoDB-vel

![mongo](assets/image/mongo)

---

@ul
- NoSQL adatbázis
- JSON dokumentumok tárolása
- Struktúrálatlan adatok
- Nincs validáció
@ulend
---

### Mongoose package

@ul
- ODM könyvtár
- JavaScript objektumok mappelése
- MongoDB kezelése
@ulend

+++

Kód

---


