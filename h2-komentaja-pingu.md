# Komentorivi
- Komentorivi on tehokas tapa käyttää Linuxia ja se on ollut olemassa pitkään ennen internetiä
- Komennos suoritetaan aina jossain kansiossa, komennolla 'pwd' näkee nykyisen sijainnin
- Tiedostoja poistaessa, luodessa tai uudelleennimetessä tulee olla tarkkana, koska komentorivi ei pyydä vahvistuksia toiminnoille
- Komentorivillä voidaan ottaa turvalloinen etäyhteys laitteisiin SSH:n avulla
- Tabulaattoria kannattaa käyttää täydentämään komentoja

# Micro-editori
sudo apt-get install micro

![kuva](https://github.com/HurpaDurp/Linux/assets/143202749/aac3b774-1d49-4955-8daf-546cf58ad764)

# Rautalistaus
Listauksen tietokoneen raudasta saa komennolla ‘sudo lshw -short -sanitize’, tätä ei kuitenkaan ole asennettuna oletuksena.

![kuva](https://github.com/HurpaDurp/Linux/assets/143202749/5b6c9bf7-8849-4e38-8796-196192ec0c05)

![kuva](https://github.com/HurpaDurp/Linux/assets/143202749/2e474ad1-f108-47da-abd4-fabbf52490a8)

Virtuaalikoneen rautalistaus näyttää aika erikoiselta omaan silmään, koska virtuaalikoneita en ole kovinkaan paljoa pyöritellyt. Selkeitä asioita ovat käyttömuisti (8GiB), suoritin (5800X) ja massamuistiosiot (/dev/sda1 ja sda2). Kaikki muu lienee Virtualboxin virtuaalijuttua?

# Sovellukset

Asennetaan sovellukset cowsay, lolcat ja cmatrix. Tämä voidaan tehdä yhdellä komennolla 'sudo apt-get -y install cowsay lolcat cmatrix

![kuva](https://github.com/HurpaDurp/Linux/assets/143202749/5dea5b42-1a67-4138-bfa1-5f1b64bb8432)

![kuva](https://github.com/HurpaDurp/Linux/assets/143202749/2be74d16-8ff4-42c6-ad4b-5b7ca5976d61)
![kuva](https://github.com/HurpaDurp/Linux/assets/143202749/5380450f-5bc7-4615-81f3-b8ace269eed3)

# FHS

Juurikansio /

![kuva](https://github.com/HurpaDurp/Linux/assets/143202749/13b629d0-e3ff-40ad-a320-52efd3fc38e9)

Kotikansio /home/

![kuva](https://github.com/HurpaDurp/Linux/assets/143202749/275817c2-20a2-4c46-a50e-f71b0f428ee3)

Käyttäjän "mikael" kotikansio /home/mikael/

![kuva](https://github.com/HurpaDurp/Linux/assets/143202749/c230b450-9bba-4294-a4a7-f201e2d1149f)

Järjestelmän asetukset /etc/

![kuva](https://github.com/HurpaDurp/Linux/assets/143202749/5ba2d9df-9a32-4357-93bc-7a07e5a25bca)

Irrotettavat mediat, kuten optinen asema tai usb-tikku /media/

![kuva](https://github.com/HurpaDurp/Linux/assets/143202749/042a5590-3181-4a0a-b78e-e1cc7550df5f)

Järjestelmän lokitiedostot /var/log/

![kuva](https://github.com/HurpaDurp/Linux/assets/143202749/3464acf3-77b0-47b1-8106-7c004e1f3c52)

# The Friendly M

Grep-komennolla voidaan etsiä ja tulostaa tiedostosta rivit, joissa hakuehto esiintyy





