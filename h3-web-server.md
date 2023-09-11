# Apache web server

- Asennus tehdään luonnollisesti komentoriviltä komennolla $ sudo apt-get install apache2
- Toimivuus testataan osoitteella http://localhost
- Käyttäjien sivuja varten tulee käyttäjille lisätä oikeudet ja asentaa userdir-moduuli

# Asennus

![kuva](https://github.com/HurpaDurp/Linux/assets/143202749/bdc6be20-41ab-4658-a196-4219cbc45346)

![kuva](https://github.com/HurpaDurp/Linux/assets/143202749/4b5a34ad-6cee-47f7-97af-fed39909f992)

Ja sehän toimii.

![kuva](https://github.com/HurpaDurp/Linux/assets/143202749/b517fad0-8b9f-4ee4-a00b-6cae90e800dd)

IP-osoite näyttäisi olevan 10.0.2.15. Host-komennon ajaminen tosin antaa virheen, puuttunekko joku palanen?

![kuva](https://github.com/HurpaDurp/Linux/assets/143202749/1617d0a6-bc2d-4908-a424-8b98073065b1)

Userdir-lisäosan asentaminen vaatii apachen uudelleenkäynnistyksen, tämä vaatii luonnollisesti salasanan

![kuva](https://github.com/HurpaDurp/Linux/assets/143202749/838e780b-1b12-48de-85df-2c81942e141b)

Kansion luominen html-tiedostoille ja sen testaaminen:

![kuva](https://github.com/HurpaDurp/Linux/assets/143202749/d5cdc996-8d8a-4325-9c3c-e0abaf7ae2d3)

Pieni HTML-tiedosto luotu microlla ja korvattu alkuperäinen index-sivu sillä. Hetken aikaa meni löytää oikea tapa tehdä tämä komentorivillä, mutta kyllä se hetken päästä onnistui.

![kuva](https://github.com/HurpaDurp/Linux/assets/143202749/5a24df1a-34be-4f69-8c5d-c69faf91e439)

Testitiedosto luotu käyttäjän kotikansioon

![kuva](https://github.com/HurpaDurp/Linux/assets/143202749/0996c779-5c23-43a8-bd1e-8845bead6390)

curl -l localhost näyttää antavan sivun lähdekoodin. Tätäkö haettiin?

![kuva](https://github.com/HurpaDurp/Linux/assets/143202749/367474a4-0104-4606-8c8b-4dcf5e2d3b2a)














