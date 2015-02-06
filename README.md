# bilisliiga
This is the repository for the pool billiard system, deployed at Fonhel. To learn more, learn Finnish.

## Pelijärjestelmä
Päätettävät asiat ennen liigakauden alkua:
* Runkosarja
* Pudotuspelit
* Harjoitusottelut

## Maksut ja palkinnot
Päätettävät asiat ennen liigakauden alkua:
* Ilmoittautumisajat
* Osallistumismaksu
* Palkinto runkosarjan voittamisesta
* Palkinnot pudotuspelien N:lle parhaalle

## Säännöt
* Ottelut voidaan käydä ainoastaan virallisella, sinisarkaisella Fonhel-biljardipöydällä.
* Ennen ottelun aloittamista kilpailijat valitsevat biljardilajin seuraavista vaihtoehdoista: 8-pallo, 9-pallo, 10-pallo, 14.1, Killeri, One pocket, Rotaatio. Ottelua ei saa aloittaa ennenkuin laji on valittu.
* Otteluissa noudatetaan [Suomen biljardiliiton virallisia sääntöjä](http://pool.sbil.fi/saannot/), seuraavin poikkeuksin:
  1. TBD
  1. ..

## Tukijärjestelmät
### Informaatiotekniset apuvälineet pallon reittien ennustamisessa
Ennustamisalgoritmin hyödyntämiseksi pallot tulee varustaa yksilöllisillä RFID-tunnuksilla. Tarkan paikannuksen ja kierteen seuraamiseksi kuhunkin palloon kiinnitetään parillinen määrä RFID-tunnisteita, tunnisteparin tulee sijaita mahdollisimman tarkasti pallon vastakkaisilla puolilla. Yksinkertaisemman ja epätarkemman ennustamisen saavuttamiseksi palloihin kiinnitetään yksi RFID-tunniste [kaavion](http://www.faqs.org/patents/img/20120255999_11.png) mukaisesti.

Ennustamisjärjestelmää ei ole pakko käyttää Fonhel-biljardiotteluissa, mutta se on sallittua.

### Tilastot ja raportointi
Jokainen ottelu tilastoidaan. Raportit generoidaan subsekunneissa sellaisessa Hadoop-sandboxissa, jonka ajoympäristö on joko kannettavaan tietokoneeseen asennetussa virtuaalikoneessa tai omakustanteisessa palvelinympäristössä. Tilastointia voidaan tehdä taulukkolaskentaohjelmassa ainoastaan jos se on yhdistetty vähintään yhden solmun klusteriin esim. ODBC-yhteydellä. Tilastoimatonta ottelua ei voida hyväksyä viralliseksi Fonhel-Bilisliigan runkosarja- tai pudotuspeliotteluksi. Harjoitusotteluita ei tarvitse tilastoida, mutta siihen kannustetaan.
