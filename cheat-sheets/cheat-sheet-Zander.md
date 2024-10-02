# Cheat sheets en checklists

> Student: Zander Van Kerckhove

## Basiscommando's

| Taak                                                   | Commando                         |
| :----------------------------------------------------- | :------------------------------- |
| Bekijk IP-adressen van alle netwerkadapters            | `ip a`                           |
| Bekijk de status van een service                       | `systemctl status SERVICE`       |
| Start een service                                      | `sudo systemctl start SERVICE`   |
| Stop een service                                       | `sudo systemctl stop SERVICE`    |
| Herstart een service                                   | `sudo systemctl restart SERVICE` |
| Update de package repositories (Ubuntu & Debian based) | `sudo apt update`                |
| Installeer een package (Ubuntu & Debian based)         | `sudo apt install PACKAGE`       |

## Git workflow

Simpele git workflow voor projecten met een enkele branch en zonder contributors.

| Task                                                               | Command                   |
| :----------------------------------------------------------------- | :------------------------ |
| Status van het huidige project                                     | `git status`              |
| Selecteer te committen bestanden                                   | `git add FILE...`         |
| Commit alle wijzigingen naar de lokale repository                  | `git commit -m 'MESSAGE'` |
| Push lokale wijzigingen naar de remote repository                  | `git push`                |
| Haal alle wijzigingen van de remote repository binnen in de lokale | `git pull`                |

## Checklist netwerkconfiguratie

1. Is het IP-adres correct? `ip a`
2. Is de router/default gateway correct? `ip r -n`
3. Is een DNS-server ingesteld? `cat /etc/resolv.conf`
4. het pingen van een ip adres `ping 192.168.56.20`

## installeren van programmas

1. update `sudo apt update`
2. installeren `sudo apt install -y programmanaam`

kijken of een service draait `systemctl status programma`
bekijken netwerkpoorten `sudo ss -tlnp`
herstarten `sudo systemctl restart programma`

## mysql

1. mysql openen `sudo mysql`
2. user aanmaken `alter user 'root'@'localhost' identified with mysql_native_password by 'letmein';`
3. user aanmaken met permissies `create user 'admin'@'%' identified by 'letmein'; grant all privileges on *.* to 'admin'@'%' with grant option; flush privileges; exit;`
4. verbinding maken met MySQL op de databankserver `-h <host> -u <user> -p`

## ufw

1. deny incoming `sudo ufw default deny incoming`
2. allow outgoing `sudo ufw default allow outgoing`
3. applicatie toevoegen met naam `sudo ufw allow OpenSSH`
4. applicatie toevoegen with port number `sudo ufw allow 22`
5. toegelaten applicaties tonen `sudo ufw app list`
6. de firewall aanzetten `sudo ufw enable`

## inloggen applicatie server

ssh wordpressapp@zvk-wordpressapp.northeurope.cloudapp.azure.com

## inloggen databank via de applicatieserver

-u wordpressdb -p -h zvk-wordpressdb.mysql.database.azure.com

## docker

```shell
sudo usermod -aG docker ${USER}
```

```shell
docker compose version
```

-> kijkt naar versie van docker compose

```shell
docker run --name vaultwarden -v "${HOME}/.files-vaultwarden:/data/" -p 4123:80 vaultwarden/server:latest
```

```shell
docker compose up -d
```

-> docker compose bestand activeren
