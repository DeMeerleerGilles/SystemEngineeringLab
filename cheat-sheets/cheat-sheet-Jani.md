# Cheat sheets en checklists

> Student: Jani Aelterman

## winget package manager commando's

| Opdracht                            | Commando                          |
| :---------------------------------- | :-------------------------------- |
| Installeer een package              | `sudo winget install PACKAGENAME`       |
| Verwijder een package               | `sudo winget uninstall PACKAGENAME`     |
| Bekijk geïnstalleerde packages      | `winget list`                      |
| Zoek naar beschikbare packages      | `winget search PACKAGENAME` |
| Update alle geïnstalleerde packages | `sudo winget upgrade --all`               |
> **Opgelet:** sudo is optioneel en is enkel beschikbaar als de package 'gsudo' geinstalleerd is.

## Gebruik van markdown

| Symbool                                                         | Functie                                   |
| :-------------------------------------------------------------- | :---------------------------------------- |
| #                                                               | Kopteksten, hoe meer # hoe kleiner de kop |
| \*\*                                                            | In vet zetten                             |
| \*                                                              | In italics zetten                         |
| ``                                                              | Als code formateren                       |
| `[Dit is een link](https://www.example.com)`                    | Een link leggen                           |
| `![Dit is een afbeelding](https://www.example.com/image.jpg)`   | Een afbeelding invoegen                   |
| `>`                                                             | Een quote invoegen                        |
| `-`                                                             | Een lijst maken                           |
| `1.`                                                            | Een genummerde lijst maken                |
| `---`                                                           | Een horizontale lijn maken                |

## Webserver

| Opdracht                            | Commando                          |
| :---------------------------------- | :-------------------------------- |
| Luisterende netwerksockets weergeven           | `sudo ss -tlnp` |
| Kijken of een service standaard opstart | `sudo systemctl is-enabled <service>`                           |
|Controleren of een service draaid      | `sudo systemctl status ssh`     |
| Firewall activeren           | `sudo ufw enable`                     |
| Bepaalde zaken toegang geven om langs de firewall te passeren              | `sudo ufw allow 22/tcp`                                       |
| SSH connectie maken          | `ssh jani@192.168.56.20`                                  |
| Kijken welke IP's er geblokkeerd zijn   | `sudo fail2ban-client status sshd`                         |
| IP-adres ontbannen   | `sudo fail2ban-client set sshd unbanip [IP-adres]`   |
| whitelist ip-adres in fail2ban  | ignoreip = 127.0.0.1/8 your_ip_address in /etc/fail2ban/jail.local |

## Azure

| Opdracht                            | Commando                          |
| :---------------------------------- | :-------------------------------- |
| Verbinden met de virtuele machine   | `ssh <user>@<host>` |
| Verbinden met de mysql database           | `mysql -u <user> -p -h <host>` |
| Website aanzetten           | `sudo a2ensite wordpress`                     |
| wordpress configureren              | `sudo -u www-data nano /srv/www/wordpress/wp-config.php` |

## Docker

| Opdracht                            | Commando                          |
| :---------------------------------- | :-------------------------------- |
| Docker container starten            | `docker start <container>` |
| Docker container stoppen            | `docker stop <container>` |
| Docker container verwijderen        | `docker rm <container>` |
| Docker container aanmaken           | `docker run -d --name <container> <image>` |
| Docker image downloaden             | `docker pull <image>` |
| Alle Docker containers weergeven         | `docker ps -a` |
| Alle Docker images weergeven         | `docker images` |

## Cisco IOS

| Opdracht                            | Commando                          |
| :---------------------------------- | :-------------------------------- |
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
