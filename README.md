# Adatb-zis_2024_Csapat4

# Fordítóiroda

Futtassa le a **iroda.sql** állományt az alábbi táblák(`dokumentumok`, `nyelvek`, `forditok`) létrehozásához!

1. Készítsen új adatbázist iroda néven! A mellékelt állományokat importálja az adatbázisba
a fájlnévvel azonos táblanéven! Az állományok tabulátorral tagolt, UTF-8 kódolású
szövegfájlok, az első soruk a mezőneveket tartalmazza. Állítsa be a megfelelő típusokat és
a kulcsokat! 

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

|**fordito**|(nyelvid, szemelyid)                                                                        |  
|:---------:|:--------:                                                                                  |                                
|`nyelvid`  | Annak a nyelvpárnak az azonosítója, amit a fordító vállal (szám), az összetett kulcs része |
|`szemelyid`|          A fordító azonosítója (szám), az összetett kulcs része                            |
</br>
</br>

|**szemely**|(id, nev, elerheto)                                |
|:------:   |:--------:                                         |
|`id`       | A fordító azonosítója (szám), ez a kulcs          |
|`nev`      | A fordító neve (szöveg) – azonos nevűek nincsenek |
|`elerheto` |  A fordító aktuális munkaképessége (logikai)      |
</br>
</br>

![A táblázatok képe](diagram.PNG)