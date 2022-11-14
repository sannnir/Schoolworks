# Schoolworks
Schooltasks of Configuration Management Systems

# h3 Git

## a) Tee tehtävän raportti Markdwonina.
Tämä kotitehtävä on osa Tero Karvisen palvelinten hallinta (Configuration Management Systems) -kurssia.
Kotitehtävät on toteutettu Virtual Box:iin (Versio 6.1)asennetulla Ubuntun käyttöjärjestelmällä (versio 22.04.1).
Tehtevät on tehty 11.11.2022 ja lähteinä on käytetty luennolla hyödynnettyjä muistiinpanoja.
Tehtävä tehdään MarkDownilla ja julkaistaan GitHubissa.


## b) Offline. Tee paikallinen offline-varasto git:illä. Varaston nimessä tulee olla sana "cat".
Aseta itsellesi sähköpostiosoite ja nimi.

Ensin luodaan varasto komennolla.

	git catproject

Tämän jälkeen siirrytään varastoon, jotta saadaaan luotua tämä raportti.

	cd catproject/

Loin tiedoston README.md microlla. Tässä välissä tallennetaan tiedosto ja annetaan komennot:

	git add .
	git commit

Tässä kohtaa itselläni kävi ensin pieni typo, kun olin kirjoittanut git add.
Eli tarkkana, että git add_välilyönti_.

Jotta commit komento onnistuu, tulee määritellä, kuka olen, joten configuroidaan käyttäjän tiedot:
- nimi
- sähköposti

Komennot ovat seuraavat:
käyttäjänimi:

	git congif --global user.name "Etunimi Sukunimi"

sähköpostiosoite:

	git config --global user.email "nimi.sukunimi@xx.xx"


<img width="294" alt="1" src="https://user-images.githubusercontent.com/117899949/201630764-aa57c9ca-dc3c-4450-b445-e759ed7e17bf.png">
	
Kun tämä on määritelty , niin päästään kokeilemaan uudelleen committia.

	git commit

Tässä kohtaa tätä tiedostoa on muokattu jo muutamaan otteeseen, joten on hyvä kurkata, miltä lokitiedot näyttää. 
Lokeissa näkyy, mitä muutoksia tiedostoon on tehty, kenen toimesta ja milloin.
Komento on

	git log

	git log --patch
	
<img width="361" alt="2" src="https://user-images.githubusercontent.com/117899949/201631083-40027c3e-de70-4b9b-bbe8-850f7266329c.png">


## c) Tee tyhmä muutos gittiin, älä tee commit:tia. Tuhoa huonot muutokset 'git reset --hard'
Tämä tehtävä ei lukeutunut suosikkeihini, koska onnistuin yrityksestä huolimatta poistamaan puolet tehdystä raportista.
Argh.
Ennen kun alotin tekemään tehtävää, aavistin onneksi, että joku voi mennä pieleen ja teinkin kopion tästä rapostista

	cp <source> <destination>

Yritin siis tehdä muokkauksia, mutta en tiedä, missä tarkalleen meni pieleen, sillä komennon 'git reset --hard' jälkeen raportti palautui tilaan, jossa siitä puuttui puolet.
Päätin kokeilla tätä uudelleen vielä kerran.

Kävin tässä välissä heittämässä komennot git add . sekä git commit. 
Sitten muutosten pariin. Kirjoitin pari riviä siansaksaa. Tallensin ja sitten kokeilin uudelleen komentoa 'git reset --hard'.

Huh. Tällä kertaa homma meni maaliin, ja raportista poistuivat vain väärät merkinnät.

<img width="354" alt="4" src="https://user-images.githubusercontent.com/117899949/201631176-bb302c68-ba84-4260-9cf2-8499e4641e9d.png">


## d) Online. Tee uusi varasto GitHubiin. Varaston nimessä ja lyhyessä kuvauksessa tulee olla sana "car".
Loin GitHubiin projektin nimeltä "Catcarproject", jonne luotiin valmiiksi README.md-tiedosto sekä lisenssiksi valittiin GNU General Public License v3.0

## e) Kloonaa edellisessa kohdassa tehty varasto itsellesi, tee muutoksia, puske ne palvelimelle ja näytä, että ne ilmestyvät webbiliittymään.
Ensin luodaan avain

	ssh-keygen

Tämän jälkeen katsotaan ssh-kansiosta julkisen avaimen tiedosto, joka kannattaa kopioida hyödyntämällä esim. microa

	cd .ssh/
	micro <open public key>

Tämän jälkeen lisätään GitHubiin luotuun CatcarProjectiin julkinen avain. Se löytyy oikeasta ylänurkasta kohdasta "clone".
Valitaan SSH ja kopioidaan osoite.
Tämän jälkeen avataan SSH-yhteys:

	git clone git@<kopiotu osoite>

Tämän jälkeen päästään käsiksi varastoon (CatcarProject).

<img width="238" alt="5" src="https://user-images.githubusercontent.com/117899949/201631374-7afbbaaf-941d-4c40-9f43-488d8142bf36.png">


Vedetään" (pull) uusin versio komennolla ja "työnnetään" (push) uusin versio.
Tehdään muokkauksia readme.tiedostoon ja "työnnetään" uusin versio GitHubiin. 
Alla komennot:

	cd CatcarProject/

	Tehdään muokkauksia. Kirjoitin dokumenttiin "making changes here"

	git add .
	git commit
	git pull
	git push

Päivitin tämän jälkeen selaimen GitHibussa ja muutokset olivat ilmestyneet sinne ja sivulla näkyi, että committeihin oli tullut uusi merkintä.

<img width="513" alt="6" src="https://user-images.githubusercontent.com/117899949/201631461-05abdb82-1138-4132-b0fc-27ae0a6e5bd2.png">
<img width="901" alt="7" src="https://user-images.githubusercontent.com/117899949/201631496-179dc102-e231-4cfc-bc9f-35573ed34de8.png">

Lisäsin tämän koulutyöraportin samalla tavalla GitHubiin luomaani Schoolworks-kansioon.
