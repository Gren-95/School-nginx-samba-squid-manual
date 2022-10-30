##**    1. Virtuaalmasinate tegemine**
####		1.1 ISO failide saamine
Laen alla Ubuntu veebilehelt:
[Ubuntu 20.04 server](https://ubuntu.com/download/server)
 ja 
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
####    2.1 SSH
Luban ssh tulemüürist läbi:
`sudo ufw allow ssh && sudo ufw enable`
####    2.2 Nginx Veebileht
#####    2.2.1 Paigaldan nginx
`sudo apt install nginx`
#####    2.2.2 Luban nginx läbi tulemüüri:
`sudo ufw allow ‘Nginx FULL’`
#####    2.2.3 Käivitan nginx-i
`sudo systemctl start nginx && sudo systemctl enable nginx`
#####    2.2.4 Teen Kausta, kus veebileht tuleb:
`sudo mkdir /var/www/tutorial`
#####    2.2.5 Teen veebilehe faili:
`sudo nano /var/www/tutorial/index.html` 
#####    2.2.6 Lisan faili sisse jägmise:
`<!doctype html> 

<html> 

<head> 

    <meta charset="utf-8"> 

    <title>Hello, Nginx!</title> 

</head> 

<body> 

    <h1>Hello, Nginx!</h1> 

    <p>We have just configured our Nginx web server on Ubuntu Server!</p> 

</body> 

</html> 

  

cd /etc/nginx/sites-enabled 

sudo nano tutorial 

  

in tutorial 

  

server { 

       listen 81; 

       listen [::]:81; 

  

       server_name example.com www.example.com; 

  

       root /var/www/tutorial; 

       index index.html; 

  

       location / { 

               try_files $uri $uri/ =404; 

       } 

}`
#####    2.2.4
#####    2.2.4
#####    2.2.4
#####    2.2.4
#####    2.2.4
