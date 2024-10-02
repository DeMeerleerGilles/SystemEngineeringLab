# Cheat sheets en checklists

> Student: Ruben Van Bruyssel

## Opdracht 1 - Package manager commando's

| Opdracht                            | Commando                                         |
| :---------------------------------- | :----------------------------------------------- |
| Bekijk geïnstalleerde packages      | `choco list <filter> [<options/switches>]`       |
| Zoek naar beschikbare packages      | `choco search <filter> [<options/switches>]`     |
| Update alle geïnstalleerde packages | `choco upgrade all`                              |
| Installeer een package              | `choco install <package> [<options/switches>]`   |
| Verwijder een package               | `choco uninstall <package> [<options/switches>]` |

## Gebruik van markdown

| Symbool                                                                       | Functie                                           |
| :---------------------------------------------------------------------------- | :------------------------------------------------ |
| #                                                                             | Kopteksten, hoe meer # hoe kleiner de kop         |
| \*\*                                                                          | In vet zetten                                     |
| \*                                                                            | In italics zetten                                 |
| ``                                                                            | Als code formateren                               |
| ```                                                                           | Hiermee is het mogelijk paragrafen te formatteren |
| `[HoGent](https://hogent.be/)`                                                | Een link leggen                                   |
| `![HoGent](https://hogent.be/sites/hogent/assets/Image/hogentenaar-lana.jpg)` | Een afbeelding invoegen                           |

# Opdracht 2 - Een databankserver opzetten in een virtuele machine

## Linux commando's

| Beschrijving                                             | Commando's                       |
| :------------------------------------------------------- | :------------------------------- |
| Update alle repos                                        | `sudo apt update`                |
| Installeerd gekozen package                              | `sudo apt instal <Package>`      |
| Toont welke poorten actief zijn met bijhoorende adressen | `sudo ss -tlnp`                  |
| Controleren of het programma draait                      | `systemctl status mysql`         |
| Herstart een service                                     | `sudo systemctl restart SERVICE` |

## SQL commando's

| Beschrijving                         | Commando's    |
| :----------------------------------- | :------------ |
| Hiermee kan je de gegevens aanpassen | `atler user`  |
| Hiermee kan je een user aanmaken     | `create user` |

## Opdracht 3 - webserver opstellen

## Linux commando's

| Beschrijving                            | Commando's                                         |
| :-------------------------------------- | :------------------------------------------------- |
| controleren of services enabled zijn    | `sudo systemctl is-enabled apache2`                |
| alle poorten te sluiten bij uw firwall  | `sudo ufw default deny incoming`                   |
| een specifieke poort toegang geven      | `sudo ufw allow poort`                             |
| zien welke IP-adressen geblokkeerd zijn | `sudo fail2ban-client status sshd`                 |
| een ip adress vrijmaken                 | `sudo fail2ban-client set sshd unbanip [IP-adres]` |

## fail2ban

| Beschrijving                            | Commando's |
| :-------------------------------------- | :--------- |
| tijd dat hij terug kijkt naar pogingen  | `findtime` |
| kansen om aan te melden                 | `maxretry` |
| tijd dat het ip-adress wordt geblokeerd | `bantime`  |

## Opdracht 4 - azure wordpress

| Beschrijving                                 | Commando's                        |
| :------------------------------------------- | :-------------------------------- |
| Dient om in te loggen op wordpress app       | `ssh <gebruikersnaam>@<dns-naam>` |
| Dient om verbinding te maken met uw databank | `mysql -h <host> -u <user> -p`    |

## Opdracht 5 - docker

| Beschrijving                    | Commando's                            |
| :------------------------------ | :------------------------------------ |
| iets laten lopen met docker     | `docker run`                          |
| draaiende containers zien       | `docker ps`                           |
| een portainer creeren           | `docker volume create`                |
| dingen in de docker verwijderen | `docker system prune --all --volumes` |

## Opdracht 6 - troubleshooting

## Linux commando's

| Beschrijving               | Commando's        |
| :------------------------- | :---------------- |
| alle poorten te laten zien | `sudo ufw status` |

## SQL commando's

| Beschrijving                      | Commando's                         |
| :-------------------------------- | :--------------------------------- |
| alle users te laten zien in de db | `SELECT User,Host FROM mysql.user` |
