# Előadások

Egy tudománynépszerűsítő előadássorozat keretében neves kutatók, tudósok tartottak
közérthető előadásokat érdekes tudományos témákról és jelentős kutatási eredményekről.

Az `eloadasok.sql` állományban az előadó tudósok és az elhangzott előadások adatai állnak rendelkezésére az első 5 évből.

### A tábla mezői a következők:

`azon`: az előadás azonosítója. Ez az elsődleges kulcs, egész szám.

`tema`: Az előadás címe. Szöveg. pl.: Mindennapi kenyerünk, mindennapi kalóriánk.

`hossz`: Az előadás hossza percben. Egész szám. Pl.: 55

`eloado`: Az előadó neve. Szöveg. Pl.: Ádám Veronika

`tudomanyag`: Az előadás mely tudományágba tartozik. Szöveg. Pl.: természettudományok

`jegy`: A jegy ár euróban. Egész szám. Pl.: 7

`resztvevok`: Az előadáson résztvevők száma. Egész szám. Pl.: 211

---

Az alábbi feladatok SQL utasátását mentse a `neve.txt` állományba! Minden kód elé írja fel a feladat sorszámát!

**1.** Készítsen adatbázist konferencia néven. Az adatbázis alapértelmezett kódolása és rendezése UTF-8, magyar legyen! Importálja az `eloadasok.sql` állományt az adatbázisba!

**2.** Hány előadást tartottak az egyes tudományágakban? Jelenítse meg a tudományág nevét és az előadások számát! A számított mező címkéje eloadasszam legyen! A listát rendezze az előadások száma szerint csökkenő sorrendbe!

**3.** Összesen hányan nézték meg a műszaki tudományok témakörbe tartozó előadásokat?

**4.** Átlagos nézőszám alapján melyik a 3 legnépszerűbb tudományág? Jelenítse meg a tudományág nevét és a nézők átlagos számát!

**5.** Összesen hány olyan előadás volt, melynek címében szerepel az energia kifejezés?

**6.** Az orvostudományi előadásoknak mennyi volt a jegyekből származó bevétele? Jelenjen meg a listában az előadás címe, az előadó neve valamint a bevétel! A listát rendezze bevétel alapján csökkenő sorrendbe!

**7.** Jelenítse meg azoknak az előadóknak a nevét, akik egynél több előadást tartottak meg! A listát rendezze névsorba!

**8.** Ki és hány előadást tartott?
