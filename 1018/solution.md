**2.** Hány előadást tartottak az egyes tudományágakban? Jelenítse meg a tudományág nevét és az előadások számát! A számított mező címkéje eloadasszam legyen! A listát rendezze az előadások száma szerint csökkenő sorrendbe!
```sql
SELECT tudomanyag, COUNT(*) AS eloadasszam FROM eloadasok GROUP BY tudomanyag ORDER BY eloadasszam DESC;
```

**3.** Összesen hányan nézték meg a műszaki tudományok témakörbe tartozó előadásokat?
```sql
SELECT SUM(resztvevok) as resztvevok_ossz FROM eloadasok WHERE tudomanyag LIKE "műszaki tudományok";
```

**4.** Átlagos nézőszám alapján melyik a 3 legnépszerűbb tudományág? Jelenítse meg a tudományág nevét és a nézők átlagos számát!
```sql
SELECT tudomanyag, AVG(resztvevok) AS atlag FROM eloadasok GROUP BY tudomanyag ORDER BY atlag DESC LIMIT 3;
```

**5.** Összesen hány olyan előadás volt, melynek címében szerepel az energia kifejezés?
```sql
SELECT COUNT(*) AS eloadasszam FROM eloadasok WHERE tema LIKE "%energia%";
```

**6.** Az orvostudományi előadásoknak mennyi volt a jegyekből származó bevétele? Jelenjen meg a listában az előadás címe, az előadó neve valamint a bevétel! A listát rendezze bevétel alapján csökkenő sorrendbe!
```sql
SELECT eloadasok.tema, eloadasok.eloado, SUM(eloadasok.jegy) * eloadasok.resztvevok AS bevetel FROM eloadasok WHERE tudomanyag LIKE 'orvostudományok' GROUP BY eloadasok.tema, eloadasok.eloado ORDER BY bevetel DESC;
```

**7.** Jelenítse meg azoknak az előadóknak a nevét, akik egynél több előadást tartottak meg! A listát rendezze névsorba!
```sql
SELECT eloado, COUNT(*) AS eloadasszam FROM eloadasok GROUP BY eloado HAVING COUNT(*) > 1 ORDER BY eloado;
```

**8.** Ki és hány előadást tartott?
```sql
SELECT eloado, COUNT(*) AS eloadasok_szama FROM eloadasok GROUP BY eloado HAVING COUNT(azon) > 1;
```
