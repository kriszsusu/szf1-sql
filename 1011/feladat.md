# 10. 11.
1.

   ```sql
   SELECT nev AS "Nevek" FROM ugyfel ORDER BY nev;
   ```
   
2.

   ```sql
   SELECT AVG(osszeg) AS "Átlag befizetések összege" FROM befiz;
   ```

3.

   ```sql
   SELECT * FROM ugyfel WHERE irszam LIKE "2%";
   ```
   
4.

   ```sql
   SELECT SUM(osszeg) AS "Összesen befizetett összeg" FROM befiz;
   ```
   
5.

   ```sql
   SELECT * FROM ugyfel ORDER BY szulev ASC LIMIT 1;
   ```
   
6.

   ```sql
   SELECT * FROM ugyfel WHERE orsz LIKE "H";
   ```
   
7.

   ```sql
   SELECT min(osszeg) AS "Legkisebb befizetett összeg", max(osszeg) AS "Legnagyobb befizetett összeg" FROM befiz;
   ```
   
8.

   ```sql
   SELECT count(*) AS "Befizetések száma" FROM befiz;
   ```
   
9.

   ```sql
   SELECT befiz.* FROM befiz JOIN ugyfel ON befiz.azon = ugyfel.azon WHERE ugyfel.nev = 'Török Bálint';
   ```
   **vagy**
   ```sql
   SELECT `datum`, `osszeg`, ugyfel.nev FROM `befiz`, `ugyfel` WHERE befiz.azon LIKE ugyfel.azon AND ugyfel.nev LIKE "Török Bálint";
   ```
   
10.

   ```sql
   SELECT ugyfel.nev AS "Ügyfél neve", SUM(befiz.osszeg) AS "Összes befizetett összeg" FROM befiz JOIN ugyfel ON befiz.azon = ugyfel.azon WHERE ugyfel.nev = 'Nagy Károly';
   ```
   **vagy**
   ```sql
   SELECT ugyfel.nev AS "Ügyfél neve", SUM(befiz.osszeg) AS "Összes befizetett összeg" FROM `befiz`, `ugyfel` WHERE befiz.azon LIKE ugyfel.azon AND ugyfel.nev LIKE "Nagy Károly";
   ```
   
11. 

   ```sql
   SELECT SUM(osszeg) AS "Összes befizetett összeg nem magyar ügyfelektől" FROM befiz JOIN ugyfel WHERE ugyfel.azon = befiz.azon AND ugyfel.orsz NOT LIKE "H";
   ```
   **vagy**
   ```sql
   SELECT SUM(osszeg) AS "Összes befizetett összeg nem magyar ügyfelektől" FROM befiz, ugyfel WHERE ugyfel.azon LIKE befiz.azon AND ugyfel.orsz NOT LIKE "H";
   ```
