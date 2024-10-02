# Verslag: Databankserver

> Naam verslaggever: Ruben Van Bruyssel

## Beschrijving

Het doel van deze opdracht was om een virtuele machine aan te maken op onze laptop waarop we dan een databank server maken. Dit werd via ubuntu gedaan dus we moesten hierbij ook een paar linux commando's kunnen gebruiken en aanleren.

## Antwoorden op de vragen in de opdracht

## Vraag 1 - Controlleer welke newerkpoorten in gebruik zijn en stel vast dat MySQL enkel luisert op de "loopback interface", waaraan zie je dit?

```
State process   Recv-Q  Send-Q  Local Address:Port  Peer Address:Port
LISTEN           0      151     127.0.0.1:3306        0.0.0.0:*

het cijfer na het ip-adres toont welke poort het is
Je ziet dat het een loopback adres is via het sate process. Dit is altijd LISTEN.
```

## Vraag 2 - Controleer met ss -tlnp of de wijziging effect had. Waaraan zie je dit? Wat is het verschil met de vorige uitvoer van dit commando?

```
State process   Recv-Q  Send-Q  Local Address:Port  Peer Address:Port
LISTEN           0      151     0.0.0.0:3306        0.0.0.0:*

Poort 3306 is het IP-adres verandert naar het meegegeven adres 0.0.0.0 in /etc/mysql/mysql.conf.d/mysqld.cnf bind-address.
```

## Evaluatiecriteria

- [x] De VM start op en je kan inloggen:
  - [x] De VM heeft een host-only adapter en een NAT adapter met de correcte instellingen.
  - [x] Je kan pingen vanop je fysieke systeem naar de host-only adapter van de VM.
  - [x] Je kan aantonen dat MySQL actief is op de VM en luistert op alle interfaces.
- [x] Je kan MySQL Workbench gebruiken om een connectie aan te maken met de databankserver:
  - [x] Je hebt een **werkende** connectie voor de admin-gebruiker
  - [x] Je hebt een **werkende** connectie voor de applicatie-gebruiker
- [x] Je hebt een verslag gemaakt op basis van het template.
- [x] De cheat sheet werd aangevuld met nuttige commando's die je wenst te onthouden voor later.

## Problemen en oplossingen

geen problemen ondervonden.

## Voorbereiding demo

- Je hebt een connectie met je virtuele machine.
- `ping 192.168.56.20`
- Aantonen dat MySQL actief is op de VM en luistert.
- `systemctl status mysql`
- `sudo ss -tlnp`
- Via MySQL aantonen dat beide connecties werken.

## Reflecties

De opdracht was eenvoudig. We hebben geleerd hoe we een databank moesten aanmaken via linux.
