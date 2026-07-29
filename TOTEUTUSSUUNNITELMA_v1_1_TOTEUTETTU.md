# Kodin Talousstudio – toteutussuunnitelma ja toteumatilanne

## Versio 1.1 – toteutettu

- [x] Uusi versioitu tietomalli ja version 1.0 localStorage-tietojen automaattinen migraatio.
- [x] Suunnitelman nimi, aloituskuukausi, päättymiskuukausi ja oletustarkasteluajankohta.
- [x] Menneisyyden, nykyhetken ja tulevaisuuden tarkastelu valittavalla kuukaudella.
- [x] Pikavalinnat: Aloitus, Tänään, Vuoden loppu ja Loppu.
- [x] Yhteenvedon sijoitus-, velka-, kassavirta- ja nettovarallisuusluvut valitulla ajankohdalla.
- [x] Budjettierien voimassaoloajat.
- [x] Hallinta-sivu meno- ja tulokategorioille.
- [x] Kategorian luonti, nimeäminen, väri, arkistointi, turvallinen poisto ja oletusten palautus.
- [x] Korjattu velkalaskenta: korko, kulut, kuukausierä, lisälyhennys ja pääoman muutos.
- [x] Velan kasvu 0 euron tai korkoa pienemmän maksun tilanteessa.
- [x] Pääomittuvan koron varoitus.
- [x] Velkakohtainen seuraavan kuukauden erittely.
- [x] Kokonaiskorot, velan huippusaldo ja sijoitusten kattavuus.
- [x] Viisi selaimessa ajettavaa velkalaskennan automaattitestiä.
- [x] Vuosikohtainen sijoituskalenteri.
- [x] Kompaktinäkymä: yksi kuukausitalletus per vuosi.
- [x] Laaja näkymä: jokaisen vuoden kuukausikohtaiset summat.
- [x] Vuoden kopiointi eteenpäin, tyhjennys ja vuosittainen prosenttikorotus.
- [x] Excel-vientiin kuukausittaiset sijoitukset, suunnitelma, kategoriat ja skenaario.
- [x] Excel-tuonti sijoituksille ja veloille.
- [x] PDF-raporttiin suunnitelman ajanjakso, tarkasteluajankohta ja vuosittainen sijoitusyhteenveto.
- [x] JSON-varmuuskopiointi ja palautus.
- [x] Responsiivinen työpöytä- ja mobiilinäkymä.

## Laskentaperiaatteet

Velan uusi saldo lasketaan kuukausittain:

`uusi saldo = vanha saldo + korko + kulut − kuukausierä − lisälyhennys`

Maksu rajataan jäljellä olevaan velkaan, joten saldo ei voi muuttua negatiiviseksi. Pääoman muutos on vanhan ja uuden saldon erotus. Negatiivinen pääoman muutos tarkoittaa velan kasvua.

Sijoitusten efektiivinen kuukausituotto lasketaan vuosituotosta:

`kuukausituotto = (1 + vuosituotto)^(1/12) − 1`

## Seuraava kehitysvaihe – versio 1.2

- Budjettierien ja velkojen muokkaus käyttöliittymässä.
- Toteuma vastaan budjetti ja toteutuneiden tapahtumien kirjaus.
- Velkakohtaiset vaihtuvat korot, viitekorot ja kertaluonteiset lisälyhennykset.
- Sijoitusten kulut, verotus ja inflaatio.
- Kategorioiden järjestäminen vetämällä sekä käytössä olevan kategorian yhdistäminen toiseen.
- Excel-tuonnin esikatselu ja täydellinen kaikkien välilehtien tuonti.
- PDF-kuvaajat ja yksityiskohtainen velkakohtainen maksuaikataulu.
- Useita rinnakkaisia skenaarioita.

## Käyttöönotto

Avaa `index.html` modernissa selaimessa. Vanha `kodin_talousstudio_v1_1.html` ohjaa yhteensopivuussyistä samaan sovellukseen. Chart.js-, Excel- ja PDF-kirjastot ladataan CDN-palvelusta, joten kuvaajat ja vientitoiminnot tarvitsevat verkkoyhteyden. Taloustiedot tallennetaan selaimen paikalliseen tallennustilaan.
