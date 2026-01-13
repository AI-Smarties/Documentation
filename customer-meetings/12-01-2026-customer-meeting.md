# Everyday AI Productivity Interface for Even Realities G1 Smart Glasses  

## Asiakastapaaminen – 12.01.2026  
**Projektikuvaus ja lähtöarkkitehtuuri**

## 1. Tausta

Even Realities G1 -älylasit mahdollistavat uudenlaisen tavan tuoda digitaalinen tieto osaksi ihmisen arkea ja työtä. Tässä projektissa rakennetaan kokeellinen, avoimeen lähdekoodiin perustuva ohjelmistoalusta, jonka avulla tekoäly toimii käyttäjän kognitiivisena jatkeena.

Tavoitteena ei ole tuotantovalmis ratkaisu, vaan oppimisympäristö, jossa tutkitaan:

- miten tekoäly voi ymmärtää ihmisten välistä puhetta  
- miten kontekstuaalista tietoa voidaan yhdistää reaaliaikaiseen keskusteluun  
- miten tieto voidaan esittää älylaseissa häiritsemättä vuorovaikutusta  

---

## 2. Projektin tavoite

Projektin päätavoite on rakentaa geneerinen pohja, jonka avulla Even G1 -laseja voidaan käyttää tekoälyavusteisena työmuistina ja kontekstiapurina.

Tavoitteet:

- Luoda toimiva perusarkkitehtuuri ("walking skeleton")  
- Mahdollistaa puheen tallennus ja tekoälytulkinta  
- Pystyä palauttamaan käyttäjälle keskusteluun liittyvää tietoa reaaliaikaisesti  
- Tuottaa oppia ja dokumentaatiota organisaation jatkokehitystä varten  

Projektin onnistuminen mitataan oppimisella, ei valmiilla tuotteella.

---

## 3. Asiakkaan tavoitteet

Asiakas haluaa:

- Geneerisen ratkaisun, jota voidaan jatkokehittää eri käyttötarkoituksiin (esim. myynti, logistiikka, varastotyö, asiantuntijatyö)  
- Teknisen pohjan, joka mahdollistaa älylasien hyödyntämisen osana työnkulkuja  
- Käytännön kokemusta siitä, miten tekoäly ja älylasit toimivat yhdessä  

---

## 4. Ratkaisun perusidea

Tekoäly toimii käyttäjän työmuistina ja kontekstiapurina.

Kun käyttäjä keskustelee muiden ihmisten kanssa, järjestelmä:

- kuuntelee puhetta (valinnaisesti)  
- muuntaa puheen tekstiksi  
- tunnistaa avainsanat, aiheet, henkilöt ja projektit  
- tallentaa tiedon pilveen  
- vertaa uutta puhetta aiemmin tallennettuun tietoon  
- palauttaa käyttäjälle keskusteluun liittyviä vihjeitä  

Älylaseihin näytetään vain lyhyitä muistutuksia, jotta huomio pysyy keskustelussa eikä näytössä.

---

## 5. Käyttöperiaatteet

Tekoäly ei ole jatkuvasti päällä. Käyttäjä hallitsee järjestelmää.

Käyttäjä voi:

- kytkeä tekoälyn päälle ja pois sovelluksessa
- päättää, milloin keskustelua tallennetaan  
- tarkastella ja poistaa tallennettua dataa mobiilisovelluksen kautta  

Kaikkea ei tallenneta automaattisesti.

---

## 6. Järjestelmän pääkomponentit

### 6.1 Even G1 -älylasit

- Näyttävät tekoälyn palauttamat lyhyet vihjeet  
- Välittävät puheen Bluetoothin kautta puhelimeen  
- Eivät sisällä kameraa tai kuulokkeita  

### 6.2 Mobiilisovellus (Flutter)

- Toimii Bluetooth-yhteytenä laseihin  
- Ohjaa tekoälyä  
- Mahdollistaa tallennettujen tietojen tarkastelun ja hallinnan  

### 6.3 Puheentunnistus

- Android- tai iOS-pohjainen  
- Tukee ensisijaisesti suomea ja toissijaisesti englantia  
  

### 6.4 Pilvipalvelu (Azure / GCP)

Pilveen tallennetaan:

- puhetranskriptiot  
- tekoälyn tuottamat tiivistelmät  
- avainsanat ja aiheet  


### 6.5 Tekoälykerros (Azure OpenAI tai Gemini)

Tekoälyn tehtävät:

- tiivistää keskustelut  
- tunnistaa aiheet ja kontekstit  
- yhdistää uusi puhe aiempiin tietoihin  
- tuottaa lyhyitä relevantteja vihjeitä laseille  

---

## 7. Walking Skeleton (MVP)

Ensimmäinen toimiva kokonaisuus todistaa, että järjestelmä voi toimia.

Perusskenaario:

1. Käyttäjä aktivoi tekoälyn ja tallennuksen  
2. Käyttäjä puhuu  
3. Puhe muunnetaan tekstiksi  
4. Teksti tallennetaan pilveen  
5. Tekoäly luo tiivistelmän ja avainsanat  
6. Myöhemmässä keskustelussa järjestelmä tunnistaa aiheen ja näyttää laseissa siihen liittyvän vihjeen  

---

## 8. Nollasprintin tavoite

Nollasprintissä ei pyritä valmiiseen sovellukseen. Tavoitteena on:

- suunnitella ja dokumentoida arkkitehtuuri  
- saada perusyhteys toimimaan (lasit → puhelin → pilvi)  
- tallentaa puhetta ja käsitellä sitä tekoälyllä  


---

## 9. Dokumentointi

Kaikki työ dokumentoidaan GitHubiin:

- arkkitehtuuri  
- rajapinnat  
- kokeilut  
- opit älylasien käytöstä (relevantit)

Tavoitteena on, että organisaatio voi tarvittaessa hyödyntää oppeja tulevissa projekteissa.

---

## 10. Asiakastapaaminen 28.1.2026 klo 11

Tapaamisen tavoitteet:

- käydä läpi mitä on saatu aikaan  
- esitellä opit ja havainnot Even G1 -laseista ja arkkitehtuurista  
- arvioida, mihin suuntaan ratkaisua kannattaa kehittää  

