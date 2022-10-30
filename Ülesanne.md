**##		1. Virtuaalmasinate tegemine**
####		1.1 ISO failide saamine
Laen alla Ubuntu veebilehelt:
[Ubuntu 20.04 server](https://ubuntu.com/download/server)
[Ubuntu desktop 22.04 ISO](https://ubuntu.com/download/desktop/thank-you?version=22.04.1&architecture=amd64)

####		1.2 Virtuaalmasinate paigaldamine
Teen 3 virtuaalmasinat (2 serverit ja 1 desktop) omal vabalt valitud virtuaalmasina tarkvaraga.
Mina valisin selleks tarkvaraks virt-manager.
Andsin srveritele 1 tuum, 1024MB RAM ja 10GB kettaruumi ja
töölauaga masinale 2 tuuma 4096MB RAM ja 35 GB kettaruumi
####		1.3 Paigaldan OP süsteemid
Seda saab lihtsalt teha ning, kuid seda pead ise uurima,
####		1.4 Uuendan kõik virtuaalmasinad käsuga:
`sudo apt update && sudo apt upgrade`

**##    2. Server 1 (ilma töölauata)**
