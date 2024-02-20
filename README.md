# Adatb-zis_2024_Csapat4

# Fordítóiroda

Futtassa le a **iroda.sql** állományt az alábbi táblák(`dokumentumok`, `nyelvek`, `forditok`) létrehozásához!

**1. Készítsen új adatbázist iroda néven! A mellékelt állományokat importálja az adatbázisba**
**a fájlnévvel azonos táblanéven! Az állományok tabulátorral tagolt, UTF-8 kódolású**
**szövegfájlok, az első soruk a mezőneveket tartalmazza. Állítsa be a megfelelő típusokat és**
**a kulcsokat!**

## Táblák:

|**dokumentumok**| (id, terjedelem, szakterulet, nyelvid, munkaido)      |
|:--------------:|:--------:                                             |
|`id `           | A fordítandó dokumentum azonosítója (szám), ez a kulcs|
|`terjedelem`    | A dokumentum karaktereinek száma (szám)               |
|`szakterulet`   |  A dokumentum szakterülete (szöveg)                   |
|`nyelvid`       | A forrás- és a célnyelv párok azonosítója (szám)      |
|`munkaido`      |  A fordítás elvégzésére becsült idő órában (szám)     |
</br>
</br>

|**nyelvek**| (id, fnyelv, cnyelv, egysegar)                                 |
|:---------:|:--------:                                                      |
|`id`       | A fordítási nyelvpár azonosítója (szám), ez a kulcs            |
|`fnyelv`   | A forrás dokumentum nyelve (szöveg)                            |
|`cnyelv`   | A cél dokumentum nyelve (szöveg)                               |
|`egysegar` |5000 karakternél nem hosszabb fordítás ára adott nyelvpár esetén|
</br>
</br>

|**forditok**|(nyelvid, szemelyid)                                                                        |  
|:---------:|:--------:                                                                                  |                                
|`nyelvid`  | Annak a nyelvpárnak az azonosítója, amit a fordító vállal (szám), az összetett kulcs része |
|`szemelyid`|          A fordító azonosítója (szám), az összetett kulcs része                            |
</br>
</br>

|**szemelyek**|(id, nev, elerheto)                                |
|:------:   |:--------:                                         |
|`id`       | A fordító azonosítója (szám), ez a kulcs          |
|`nev`      | A fordító neve (szöveg) – azonos nevűek nincsenek |
|`elerheto` |  A fordító aktuális munkaképessége (logikai)      |
</br>
</br>

![A táblázatok képe](diagram.PNG)
</br>
</br>

**2. A fordítóiroda utólag vállalt egy új nyelvről való fordítást. Adja hozzá a nyelvek adattáblához a következőket. Az id legyen 145, forrás nyelve török, a cél dokumentum nyelve román, illetve az egységár pedig legyen 3000Ft.**

![2. feladat megoldása:](<képek/2.feladat(kód).PNG>)
![2. feladat megoldása:](<képek/2.feladat(tábla).PNG>)
</br>
</br>

**3. A személyek adattáblában elírtak egy nevet. Módosítsa Nagy Tímea nevét Kiss Tímeára.**

   ![3. feladat megoldása:](<képek/3.feladat(kód).PNG>)
   ![3. feladat megoldása:](<képek/3.feladat(tábla).PNG>)
   </br>
   </br>

**4. A dokumentumok táblában történt egy tévedés, és a rendszerbe valamilyen módon bekerült a 25-ös id-val rendelkező sport szakterületű dokumentum. Keresse meg és törölje ki az adattáblából.**

   ![4. feladat megoldása:](<képek/4.feladat(kód).PNG>)
   ![4. feladat megoldása:](<képek/4.feladat(tábla).PNG>)
   </br>
   </br>

**5. Készítsen lekérdezést, amely ábécérendben megjeleníti azoknak a fordítóknak a nevét, akik új munkát tudnak vállalni!**

![5. feladat megoldása:](<képek/5.feladat(kód).PNG>)
![5. feladat megoldása:](<képek/5.feladat(tábla).PNG>)
</br>
</br>

**6. Készítsen lekérdezést, amely meghatározza az 5000 és az annál kisebb karakterszámú dokumentumok számát és az ezek fordításáért járó összbevételt!**

![6. feladat megoldása:](<képek/6.feladat(kód).PNG>)
![6. feladat megoldása:](<képek/6.feladat(tábla).PNG>)
</br>
</br>

**7. Készítsen lekérdezést, amely megadja az angolról magyarra fordítandó dokumentumok terjedelmét és szakterületét! A lista terjedelem szerint csökkenően jelenjen meg!**

![7. feladat megoldása:](<képek/7.feladat(kód).PNG>)
![7. feladat megoldása:](<képek/7.feladat(tábla).PNG>)
</br>
</br>

**8. Melyik szakterülethez tartoznak és melyik nyelvről melyikre kell azokat a dokumentumot fordítani, amelyekre majdnem pontosan egy munkanapnyi (7-9 óra) fordítási időt becsültek? Adja meg lekérdezés segítségével a szakterületeket, a forrás- és a célnyelvek nevét a forrásnyelv szerint ábécé sorrendben!**

![8. feladat megoldása:](<képek/8.feladat(kód).PNG>)
![8. feladat megoldása:](<képek/8.feladat(tábla).PNG>)
</br>
</br>

**9. Lekérdezés segítségével adja meg azoknak a fordítóknak a nevét, akik magyarról a legtöbb célnyelvre vállalnak fordítást! Több ilyen fordító esetén elegendő egyet megjeleníteni.**
</br>

![9. feladat megoldása:](<képek/9.feladat(kód).PNG>)
![9. feladat megoldása:](<képek/9.feladat(tábla).PNG>)
</br>
</br>

**11. Készítsen lekérdezést, amely kilistázza szakterületenként, hogy melyik nyelvről melyikre kell fordítani a megrendelt dokumentumokat. A listát szakterületenként csoportosítsa és azon belül minden nyelvpár egyszer jelenjen meg a forrásnyelv szerint ábécé-rendben! A lekérdezés elkészítésekor a mintából a mezők sorrendjét, a címet és a mezőnevek megjelenítését vegye figyelembe! A jelentés formázásában a mintától eltérhet.**

![11. feladat megoldása:](<képek/11.feladat(kód).PNG>)
![11. feladat megoldása:](<képek/11.feladat(tábla).PNG>)
</br>
</br>