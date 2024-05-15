# Projekt: Numbriline Klaviatuur Kiirendusmõõturiga

Projekti eesmärk oli luua numbriline klaviatuur, mis kasutab ADXL345 kiirendusmõõturi mooduliga plastikust prototüüpi. 
Klaviatuur suudab registreerida kindlat koordinaatide vahemikku ning genereerida seotud numbrilisi väljundeid vastavalt mõõdetud kiirendustele.

## Tööpõhimõte

Projekt kasutab ADXL345 kiirendusandurit ja Arduino mikrokontrollerit plastitüki asendi mõõtmiseks surumise ajal. 
Kiirendusandur suudab registreerida kiirendust kolmes teljes (X, Y, Z) vastavalt Newtoni teisele seadusele. 
Plastitüki surumisel tekib jõud, mis põhjustab kiirenduse muutust, mis omakorda on proportsionaalne punktiga, kuhu peale vajutati.

## Programm

Programm algab kiirendusanduri õige ühenduse ja kommunikatsiooni kontrollimisega Arduino mikrokontrolleriga. 
Seejärel käivitub mõõtmistsükkel, kus analüüsitakse regulaarselt mõõdetud kiirendusi, et tuvastada muutusi üle tavapärase müra.

Oluline osa on plastitüki asendi määramine vastavalt mõõdetud kiirendustele. Programm kasutab tingimusi ja vahemikke, 
et eristada erinevaid asendeid. Kui tuvastatakse konkreetne asend, genereeritakse vastav väljund Arduino abil, mis edastatakse arvutisse serial ühenduse kaudu.

## Stabiilsus ja Täpsus

Projekt rakendab erinevaid kalibreerimisvõtteid ja tarkvaralisi lahendusi, et vähendada juhuslike signaalide esinemist ja parandada süsteemi stabiilsust. 
Kuigi täielikku stabiilsust ei saavutatud kiirendusmõõturi tundlikkuse tõttu, pakub süsteem siiski mitmekülgset kasutust objektide liikumise või asendi jälgimiseks reaalajas.

## Märkused

Kuigi Serial monitor võib aeg-ajalt kuvada juhuslikke signaale, tuleneb see kiirendusmõõturi tajutud puuteplaadi "kumeruse" muutumisest. 
Projekti käigus töötati välja erinevaid kalibreerimisvõtteid ja tarkvaralisi lahendusi, 
et vähendada juhuslike signaalide esinemist Serial monitoris ning parandada süsteemi stabiilsust. 
Päris täielikku stabiilsust ei suudetud aga saavutada, mis on tingitud sellest, 
et kiirendusmõõturi tundlikkuse tase on väga kõrge ka kõige madalama tundlikkuse seades.
