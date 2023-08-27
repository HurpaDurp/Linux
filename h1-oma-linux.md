# Raportin kirjoittaminen
Raporttia on helpoin kirjoittaa sitä mukaa kun tekee harjoitusta. Tästä raportista tulee dokumentaatio tehdyistä asioista ja sen perusteella homma on helposti toistettavissa myös jonkun muun toimesta.

# Free Software
- Vapaa käytettäväksi miten/mihin haluaa
- Pääsy lähdekoodiin, jota voi muokata halutulla tavalla
- Oikeus kopioiden jakamiseen, myös niihin joita olet itse muokannut


# Linuxin asentaminen virtuaalikoneeseen
Homman nimi ois siis asentaa Debian (https://cdimage.debian.org/debian-cd/current-live/amd64/iso-hybrid/debian-live-12.1.0-amd64-xfce.iso) virtuaalikoneelle. Pohjana meillä on Windows 11 asennettuna AMD:n raudalle ja Oraclen Virtualbox (https://www.virtualbox.org/wiki/Downloads).

### Virtuaalikoneen luominen

VirtualBox auki ja aloitamme uuden virtuaalikoneen luomisen klikkaamalla "New". Koneelle annetaan nimi, sijainti massamuistilla ja valitaan haluttu levykuva. Tyyppi tuli automaattisesti oikeaksi (Linux), mutta versio piti vaihtaa manuaalisesti 64-bittiseksi. "Unattended Installation" skipataan, koska se ei kuulemma toimi.
   ![kuva](https://github.com/HurpaDurp/Linux/assets/143202749/cd065709-ca7b-4629-970a-63137074eb41)

Seuraavaksi varataan/määritellään virtuaalikoneelle resurssit, eli käyttömuisti, suoritinytimet ja massamuisti. Tämän jälkeen klikataan "Finish"
![kuva](https://github.com/HurpaDurp/Linux/assets/143202749/436e2062-46a3-45dd-8045-12a3cfb41032)
![kuva](https://github.com/HurpaDurp/Linux/assets/143202749/c66191bb-83b0-459e-aa84-53b501727cb2)

Debian-laitetta tuplaklikkaamalla saamme upean virtuaalikoneemme boot menun auki. Aluksi käynnistämme Linuxin live-tilassa (ensimmäinen vaihtoehto), jotta varmistumme mm. verkkoyhteyden ja hallintalaitteiden toiminnasta ja aloitamme varsinaisen asennuksen vasta sitten.
![kuva](https://github.com/HurpaDurp/Linux/assets/143202749/8bc2bcf2-78d2-4e68-8ada-1c4d8b54780a)
![kuva](https://github.com/HurpaDurp/Linux/assets/143202749/f3afe9f3-f49a-4cd0-ba59-5832b75651de)

### Asennus
  
Install Debian -kuvaketta klikkaamalla saamme luonnollisesti varoituksen epäluotettavasta lähteestä, mutta valitsemalla "launch anyway" saamme asennuksen etenemään.
![kuva](https://github.com/HurpaDurp/Linux/assets/143202749/4a3990d0-a130-49e4-bd64-5568928b83f2)
Kielivalinnassa olemme tyytyväisiä oletukseen.

![kuva](https://github.com/HurpaDurp/Linux/assets/143202749/ab6cb7b2-702e-4e7e-8abe-e1e42471b6c9)
Aikavyöhyke on hyvä valita oikein.

![kuva](https://github.com/HurpaDurp/Linux/assets/143202749/b62cb6dc-d07a-47e1-a7d7-f4f4e71c9599)
Näppäimistöasettelu riippuu käytössä olevasta näppäimistöstä ja kielestä. Itselläni se on luonnollisesti Suomi ja suomalainen.

![kuva](https://github.com/HurpaDurp/Linux/assets/143202749/2e70dc85-2581-4dfe-bfaf-bb15428f43e1)
Formatoimme virtuaalikoneelle varatun osan massamuistista "Erase disk" valinnalla ja jatkamme muuten oletusasetuksilla.

![kuva](https://github.com/HurpaDurp/Linux/assets/143202749/ccc60271-02ae-4702-8b02-7a675ceb0420)
Käyttäjänimi, salasana ja tietokoneen nimeäminen. Skandimerkkejä lienee syytä välttää näissäkin tapauksissa.

![kuva](https://github.com/HurpaDurp/Linux/assets/143202749/fd940b4f-f98f-4844-9c8a-d82fcb71803a)
Yhteenvetosivu kannattaa suurentaa oikeasta yläkulmasta, jotta saa Install-napin näkyviin. Tässä voi käydä vielä kerran valitut asetukset läpi ja varmistua että kaikki on halutulla tavalla.

![kuva](https://github.com/HurpaDurp/Linux/assets/143202749/8e34eab5-8e9a-46ee-a7b8-8fd1fe4976f8)
Install-klikkauksen jälkeen jäämme odottelemaan...

![kuva](https://github.com/HurpaDurp/Linux/assets/143202749/2c5a08fb-71a7-4bf2-8fa3-d546214fd508)
Hetken odottelun jälkeen asennus on valmis. Pidetään valinta "Restart now" ja klikataan Done, jotta virtuaalikone käynnistyy uudelleen ja saamme sen ajoon.

![kuva](https://github.com/HurpaDurp/Linux/assets/143202749/49732b2b-7411-4bb6-b5c5-4f16cd560a79)
Kirjautuminen aiemmin luodulla tilillä

![kuva](https://github.com/HurpaDurp/Linux/assets/143202749/f8ebae60-7c18-4f86-bb40-9dc80718ea47)
Ja meillä on työpöytä!

### Päivitykset ja palomuuri

Ja kuten totuttua, juuri asennettu käyttöjärjestelmä ei ole ajantasaisin. Ajetaan komentokehotteesta päivitykset komennoilla "sudo apt-get update" ja "sudo apt-get -y dist-upgrade". Jälkimmäisessä kestää hetken aikaa.
![kuva](https://github.com/HurpaDurp/Linux/assets/143202749/835b6321-c767-485f-a99d-a146ef0b5bff)

Palomuurin asennamme komennolla "sudo apt-get -y install ufw" ja otamme käyttöön komennolla "sudo ufw enable". Muutokset tulevat ilmeisesti voimaan uudelleenkäynnistyksen jälkeen.

### Guest Additions

Asennamme vielä VirtualBoxin Guest Additions -paketin, jotta saamme suurennettua virtuaalikoneemme näyttöä ja voimme ehkä tehdäkkin jotain hajoamatta liian pieneen ruutuun. Tämä tapahtuu suoraan VirtualBoxista.


![kuva](https://github.com/HurpaDurp/Linux/assets/143202749/a9b8636f-d43b-48ac-b226-c1d8d9cf4bd1)

Klikkaamme Devices ja Insert Guest Additions CD Image


![kuva](https://github.com/HurpaDurp/Linux/assets/143202749/b13fa027-7c37-45c6-88d8-d042da07aa6e)


Työpöydälle ilmestyy levykuva ja sitä tuplaklikkaamalla näemme sen sisällön. Avaamme taas komentokehotteen, navigoimme oikeaan hakemistoon ja suoritamme asennuspaketin.


![kuva](https://github.com/HurpaDurp/Linux/assets/143202749/79638b4e-8a3d-4f3e-b85f-060a02aa7804)

Tämän asennuksen jälkeen virtuaalikoneen ikkunan muuttaminen muuttaa myös virtuaalikoneen näytön kokoa, ei enää tihrustamista ahtaalla näytöllä. Virtuaalikoneen saa sammuksiin klikkaamalla käyttäjänimeä oikeasta yläkulmasta ja valitsemalla "Shut Down".


























   




