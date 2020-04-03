Ceci permet d'utiliser un ESP8266/ESP32 pour récupérer les informations d'un compteur électrique via ESPhome

Composant Custom permettant de récupérer le flux TéléInformation depuis son compteur électronique ou linky (en mode historique)

/!\ Il ne faut surtout pas connecter votre ESP32 directement au compteur      /!\
/!\ Il faut passer par un octocoupleur comme indiqué dans montage-de-base.jpg /!\

N'ayant pas d'abonnement HP/HC seules les étiquettes suivantes ont été implémentées : IINST, ISOUSC, PAPP, BASE et ADCO, n


# Quelques informations complémentaires :

- Compatible uniquement avec les linky en mode historique (mode standard non supporté)
   le mode actuel de votre linky peut-être consulté directement sur celui-ci.
   Pour un linky, il convient de changer la résistance d'entrée du TIC par une valeur plus faible (1kΩ ou 1.2kΩ au lieu de 4.7kΩ)
# Aide mémoire pour le montage :

- Illustration pour vérifier la polarité de l'optocoupleur et du mosfet:
![](https://raw.githubusercontent.com/schmurtzm/LibTeleinfo/Autoconnect/doc/Teleinfo-Details.png)


- Rappel du schema complet pour ESP :
![](https://raw.githubusercontent.com/schmurtzm/LibTeleinfo/Autoconnect/doc/Wifinfo-sch.png)


# diagnostiquer votre montage
- Aide mémoire pour le diagnostique si aucune donnée n'est remontée :

Si votre montage ne fonctionne pas utilisez un oscilloscope en sortie de TIC, puis derrière l'optocoupleur et enfin derrière le Mosfet. Vous devez systématiquement avoir un signal de ce genre :
![](https://raw.githubusercontent.com/schmurtzm/LibTeleinfo/Autoconnect/doc/Teleinfo-Diag.png)

- Vous pouvez également utiliser un FTDI connecté sur un PC sous Windows en vous inspirant de ce montage :

![](https://raw.githubusercontent.com/schmurtzm/LibTeleinfo/Autoconnect/doc/FTDI-diag-schema.png)
source du schéma https://www.kzenjoy.net/2015/la-teleinformation-sous-jeedom/

Ensuite installez [termite](https://www.compuphase.com/software_termite.htm) avec le paramétrage suivant : 


Merci à Gael Benoit, auteur originel de ce Yaml.