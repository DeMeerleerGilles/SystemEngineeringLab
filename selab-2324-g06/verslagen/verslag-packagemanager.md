# Verslag: 1 Package-manager en markdown

> Naam verslaggever: Gilles De Meerleer

## Beschrijving

Het doel van deze opdracht was om een package manager te installeren op onze laptop zodat we op een eenvoudige en efficiente manier software kunnen instaleren en updaten op onze laptops. Bovendien moesten we onszelf aanleren hoe we markdown kunnen gebruiken voor het opmaken van tekstbestanden.


## Antwoorden op de vragen in de opdracht

### Vraag 1 - De PowerShell-prompt toont de map waar we ons nu bevinden. Wat is de naam van deze directory?
De directory waarin we ons momenteel bevinden heeft de naam **system32**.
### Vraag 2 - In welke map heb je het script bewaard?
In de map **SEL**.
### Vraag 3 - In welke map is het script bewaard in de screenshot in Figuur 10?
In de map **SELab**.
### Vraag 4 - Lijstje met commando's opbouwen
| **Taak**                                                                | **Commando**      |
| ----------------------------------------------------------------------- | ------------      |
| Een lijst tonen van de software die nu geïnstalleerd is via Chocolatey  | choco list        |
| Alle packages die nu geïnstalleerd zijn bijwerken tot de laatste versie | choco upgrade all |
| Via de console een package opzoeken                                     | choco search      |
| Een geïnstalleerde applicatie verwijderen                               | choco uninstall   |
### Vraag 5 - Installatiescript?
```
Automatiseren software-installatie
Write-Host "Installatie algemene applicaties"
choco install -y git 
choco install -y adobereader
choco install -y firefox
choco install -y github-desktop
choco install -y vscode
choco install -y vlc
```
## Evaluatiecriteria
- [x] Je hebt een package manager voor jouw besturingssysteem geïnstalleerd.
- [x] Je hebt een script (PowerShell of Bash, afhankelijk van je besturingssysteem) geschreven en gebruikt om de opgesomde applicaties te installeren.
- [x] Je toont inzicht in de werking van een package manager en kan deze vlot kan gebruiken om basistaken uit te voeren.
- [x] Je hebt een verslag gemaakt op basis van het template.
- [x] De cheat sheet werd aangevuld met nuttige commando's die je wenst te onthouden voor later.

## Problemen en oplossingen

Error in powershell,
oplossing uit opgave:
   ```console
$  Set-ExecutionPolicy Bypass -Scope Process
```



## Voorbereiding demo
* Je hebt een package manager voor jouw besturingssysteem geïnstalleerd.
* `choco --version`
* Je hebt een script (PowerShell of Bash, afhankelijk van je besturingssysteem) geschreven en gebruikt om de opgesomde applicaties te installeren.
* `cd .\Users\gille\OneDrive\Bureaublad\HOGent\SEL`
* `.\installatieSoftware.ps1`
* Je toont inzicht in de werking van een package manager en kan deze vlot kan gebruiken om basistaken uit te voeren.
* `choco install notepadplusplus.install`


## Reflecties

De volledige opdracht verliep eenvoudig.

## Bronnen
Chocolatey Community. (z.d), Chocolatey Software, https://community.chocolatey.org/ Geraadpleegd op 22/02/2024.
