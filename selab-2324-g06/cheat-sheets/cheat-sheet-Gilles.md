# Cheat sheets en checklists

> Student: Gilles De Meerleer

## Package manager commando's

| Opdracht                            | Commando                          |
| :---------------------------------- | :-------------------------------- |
| Installeer een package              | `choco install PACKAGENAME`       |
| Verwijder een package               | `choco uninstall PACKAGENAME`     |
| Bekijk geïnstalleerde packages      | `choco list`                      |
| Zoek naar beschikbare packages      | `choco search SEARCHTERM SERVICE` |
| Update alle geïnstalleerde packages | `choco upgrade all`               |

## Gebruik van markdown

| Symbool                                                         | Functie                                   |
| :-------------------------------------------------------------- | :---------------------------------------- |
| #                                                               | Kopteksten, hoe meer # hoe kleiner de kop |
| \*\*                                                            | In vet zetten                             |
| \*                                                              | In italics zetten                         |
| ``                                                              | Als code formateren                       |
| `[Dit is een link](https://www.example.com)`                    | Een link leggen                           |
| `![Dit is een afbeelding](https://www.example.com/image.jpg)  ` | Een afbeelding invoegen                   |

## Databankserver

| Opdracht                            | Commando                                           |
| :---------------------------------- | :------------------------------------------------- |
| MySQL Server installeren            | `sudo apt update sudo apt install -y mysql-server` |
| Status van de MySQL server opvragen | `systemctl status mysql`                           |
| MySQL configuratie aanpassen        | `sudo nano /etc/mysql/mysql.conf.d/mysqld.cnf`     |
| MySQL server herstarten             | `sudo systemctl restart mysql`                     |
| MySQL console openen                | `sudo mysql`                                       |
| Pingen naar een IP-adres            | `ping <ip-adres>`                                  |
| Installeer een package (Ubuntu)     | `sudo apt install PACKAGE`                         |

## Webserver

| Opdracht                                                      | Commando                                           |
| :------------------------------------------------------------ | :------------------------------------------------- |
| Luisterende netwerksockets weergeven                          | `sudo ss -tlnp`                                    |
| Kijken of een service standaard opstart                       | `sudo systemctl is-enabled <service>`              |
| Controleren of een service draaid                             | `sudo systemctl status ssh`                        |
| Firewall activeren                                            | `sudo ufw enable`                                  |
| Bepaalde zaken toegang geven om langs de firewall te passeren | `sudo ufw allow 22/tcp`                            |
| SSH connectie maken                                           | `ssh gilles@192.168.56.20`                         |
| Kijken welke IP's er geblokkeerd zijn                         | `sudo fail2ban-client status sshd`                 |
| IP-adres ontbannen                                            | `sudo fail2ban-client set sshd unbanip [IP-adres]` |

## Wordpress in Azure

| Opdracht                                           | Commando                                                 |
| :------------------------------------------------- | :------------------------------------------------------- |
| Een ssh verbinding opzetten met server in de cloud | `ssh <gebruikersnaam>@<dns-naam>`                        |
| Installer de mysql client op de ubuntu server      | `sudo apt install mysql-client`                          |
| Verbinding maken met de database host              | `mysql -h <host> -u <user> -p`                           |
| Website activeren                                  | `sudo a2ensite wordpress`                                |
| Apache herstarten                                  | `sudo service apache2 reload`                            |
| De WP-config file openen in de nano text editor    | `sudo -u www-data nano /srv/www/wordpress/wp-config.php` |
| Certbot installeren                                | `sudo snap install --classic certbot`                    |
| Certbot voorbereiden                               | `sudo ln -s /snap/bin/certbot /usr/bin/certbot`          |
| Certificaat installeren                            | `sudo certbot --apache`                                  |

## Docker

| Opdracht                                                                               | Commando                  |
| :------------------------------------------------------------------------------------- | :------------------------ |
| Gebruiker opvragen in Linux                                                            | `whoami`                  |
| Lokale docker images bekijken                                                          | `docker images`           |
| Lokale docker containers bekijken                                                      | `docker ps -a`            |
| Controleren of docker compose geinstalleerd is                                         | `docker compose version`  |
| Docker compose bestand activeren                                                       | `docker compose up -d`    |
| Alle containers stoppen en verwijderen                                                 | `docker-compose down`     |
| Alle containers, images, networks en volumes verwijderen die niet meer in gebruik zijn | `docker system prune -a`  |
| De logs van een docker container opvragen                                              | `docker logs vaultwarden` |

## Troubleshooting

| Opdracht                                                                               | Commando                          |
| :------------------------------------------------------------------------------------- | :-------------------------------- |
| Status van een serivce opvragen in Linux                                               | `sudo service apache2 status`     |
| Service opstarten in Linux                                                             | `sudo service apache2 start   `   |
| Service stoppen in Linux                                                               | `sudo service apache2 stop`       |
| Service herstarten in Linux                                                            | `sudo service apache2 restart`    |
| Inloggen op MySQL console                                                              | `mysql -u <gebruiker> -p`         |
| Alle docker containers oplijsten                                                       | `docker ps -a`                    |
| Alle containers, images, networks en volumes verwijderen die niet meer in gebruik zijn | `docker logs <container_id>     ` |

## Cisco IOS

| Opdracht                                          | Commando                                            |
| ------------------------------------------------- | --------------------------------------------------- |
| Toon de versie van de software                    | `show version`                                      |
| Configureer de terminal                           | `configure terminal`                                |
| Toon de huidige configuratie                      | `show running-config`                               |
| Toon de routeringstabel                           | `show ip route`                                     |
| Toon een overzicht van de interfaces              | `show ip interface brief`                           |
| Toon een overzicht van de IPv6 interfaces         | `show ipv6 interface brief`                         |
| Toon de MAC-adressen van de interfaces            | `show interfaces`                                   |
| Genereer een RSA-sleutelpaar                      | `crypto key generate rsa general-keys modulus 2048` |
| Stel de domeinnaam in                             | `ip domain-name selabs.local`                       |
| Schakel SSH versie 2 in                           | `ip ssh version 2`                                  |
| Stel een lokale gebruiker in voor SSH             | `username admin secret class`                       |
| Schakel SSH in op de VTY lines                    | `line vty 0 15`                                     |
| Stel de SSH timeout in                            | `ip ssh time-out 60`                                |
| Stel het maximum aantal authentication retries in | `ip ssh authentication-retries 3`                   |

# Checklists

## Checklist databankserver

1. VM in virtualbox?
2. MySQL workbench op extern toestel?
3. Host only adapter aangemaakt?
4. MySQL server installeren?
5. Status controlleren?
6. IP instellingen wijzigen?
7. Loopback adres veranderen in configuratiebestand?
8. Service herstarten?
9. Admin gebruiker aanmaken?
10. Verbinden met workbench?

## Wordpress in Azure

1. SQL databank in Azure?
2. VM in de Azure cloud?
3. Client IP toegevoegd aan de firewall?
4. Poorten op applicatieserver voor HTTP, HTTPS en SSH toevoegen?
5. Automatisch afsluiten instellen?
6. DNS naam instellen?
7. IP van app server toevoegen aan firewall van databank server?
8. Alle benodigdheden voor wordpress installeren op de ubuntu machine?
9. Config file aanpassen?
10. De site openen via de DNS naam?
11. HTTPS gebruiken om website te bereiken
12. Surfen via een eigen domein
