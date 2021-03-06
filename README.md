# assistant-lilo

Ce plugin de [`assistant-plugins`](https://aymkdn.github.io/assistant-plugins/) permet de gérer la lumière du potager d'intérieur [« Lilo » de *Prêt à Pousser*](https://pretapousser.fr/le-potager-d-interieur/smart-lilo-potager-connecte-174.html).

**ATTENTION**, il y a plusieurs restrictions pour utiliser ce plugin :
  - faire tourner `assistant-plugins` sur une machine Linux
  - avoir une connectivité Bluetooth sur cette machine
  - avoir NodeJS installé en version supérieure ou égale à 8

## Installation

Si vous n'avez pas installé [`assistant-plugins`](https://aymkdn.github.io/assistant-plugins/), alors il faut le faire.

Une fois installé, vous devez ajouter ce plugin en ouvrant une console dans le répertoire `assistant-plugins` et en tapant :  
  `npm install assistant-lilo@latest --save && npm run-script postinstall`
  
Enfin, il faut exécuter le script [`lilo-preinstall.sh`](https://github.com/jzarca01/assistant-lilo/blob/master/lilo-preinstall.sh). Il est préférable de savoir ce que vous faites avant de passer à cette étape ! Pour installer les composants supplémentaires, taper :
  `bash node_modules/assistant-lilo/lilo-preinstall.sh`
  
## Configuration

Deux paramètres sont obligatoires: `semaine` et `weekend`.

### Paramètre `semaine`

Indique l'heure et minute de début et l'heure et minute de fin de l'éclairage durant la semaine.

Par exemple, pour commencer l'éclairage à 8h00 du matin et le terminer à 22h00, on indiquera :
```json
"semaine": ["08", "00", "22", "00"]
```

### Paramètre `weekend`

Même principe que pour la semaine.

Par exemple, pour commencer l'éclairage à 12h00 et le terminer à 23h59, on indiquera :

```json

"weekend": ["12", "00", "23", "59"]

```

## Utilisation

Des applets ont été créés et peuvent être utilisées :

- [Allume la lumière](https://ifttt.com/applets/f39jPDYZ-assistant-plugins-allume-lilo) --> https://ifttt.com/applets/f39jPDYZ-assistant-plugins-allume-lilo
- [Éteins la lumière](https://ifttt.com/applets/UMDezSUs-assistant-plugins-eteins-lilo) --> https://ifttt.com/applets/UMDezSUs-assistant-plugins-eteins-lilo
- [Mode weekend](https://ifttt.com/applets/BdtjD2RA-assistant-plugins-mets-lilo-en-mode-weekend) --> https://ifttt.com/applets/BdtjD2RA-assistant-plugins-mets-lilo-en-mode-weekend
- [Mode semaine](https://ifttt.com/applets/VqBzdVsc-assistant-plugins-mets-lilo-en-mode-semaine) --> https://ifttt.com/applets/VqBzdVsc-assistant-plugins-mets-lilo-en-mode-semaine
