Composant Custom pour ESPhome permettant de récupérer le flux TéléInformation depuis son compteur électronique ou linky (en mode historique). Les informations seront ensuite automatiquement ajoutée dans Home Assistant. 

Compatible ESP8266 et ESP32.

---
> **/!\ Il ne faut surtout pas connecter votre ESP32 directement au compteur      /!\\**<br/>
> **/!\ Il faut passer par un octocoupleur comme indiqué dans montage-de-base.jpg /!\\**

---

N'ayant pas d'abonnement HP/HC seules les étiquettes suivantes ont été implémentées : IINST, ISOUSC, PAPP, BASE et ADCO, n

# Exemple de montage :
![](https://raw.githubusercontent.com/schmurtzm/Teleinfo-TIC-with-ESPhome/master/example%20Wemos%20D1/example%20Wemos%20D1%20(1).jpg)
([Un fichier .STL](https://github.com/schmurtzm/Teleinfo-TIC-with-ESPhome/blob/master/example%20Wemos%20D1/Teleinfo%20box%20Schmurtz.stl) est également fourni dans les sources pour imprimer [un boitier adapté à ce montage](https://raw.githubusercontent.com/schmurtzm/Teleinfo-TIC-with-ESPhome/master/example%20Wemos%20D1/example%20Wemos%20D1%20(5).jpg)).




# Quelques informations complémentaires :

- Compatible uniquement avec les linky en mode historique (mode standard non supporté)
   le mode actuel de votre linky peut-être consulté directement sur celui-ci.
   Pour un linky, il convient de changer la résistance d'entrée du TIC par une valeur plus faible (1kΩ ou 1.2kΩ au lieu de 4.7kΩ)
# Aide mémoire pour le montage :

- Schéma de montage :<br/>
    * bien vérifier la polarité de l'optocoupleur et du mosfet<br/>
    * RXD = GPIO 13 = D7 sur Wemos D1 Mini<br/>
    * R1 = 1kΩ si linky ,4.7kΩ si compteur électronique (acienne génération)<br/>
    * V+ = 3.3v

![](https://raw.githubusercontent.com/schmurtzm/LibTeleinfo/Autoconnect/doc/Teleinfo-Details.png)


- Beaucoup d'informations complémentaires sur le blog de [Charles Hallard](https://hallard.me/wifinfo/) :


# diagnostiquer votre montage
- Aide mémoire pour le diagnostique si aucune donnée n'est remontée :

Si votre montage ne fonctionne pas utilisez un oscilloscope en sortie de TIC, puis derrière l'optocoupleur et enfin derrière le Mosfet. Vous devez systématiquement avoir un signal de ce genre :
![](https://raw.githubusercontent.com/schmurtzm/LibTeleinfo/Autoconnect/doc/Teleinfo-Diag.png)

- Vous pouvez également utiliser un FTDI connecté sur un PC sous Windows en vous inspirant de ce montage :

![](https://raw.githubusercontent.com/schmurtzm/LibTeleinfo/Autoconnect/doc/FTDI-diag-schema.png)
source du schéma https://www.kzenjoy.net/2015/la-teleinformation-sous-jeedom/

Ensuite installez [termite](https://www.compuphase.com/software_termite.htm) (1200 Baud)

## Help is welcome ! 
Vous voulez améliorer ce projet ? N'hésitez pas, **Participez !** : éditez et publiez vos modification :)<br/>
Vous pouvez également m'acheter un café pour garder ma mtoviation au top !<br/>
[![Buy me a coffee][buymeacoffee-shield]][buymeacoffee]
<br/><br/>



Merci à Gael Benoit, auteur originel de ce Yaml.

[buymeacoffee-shield]: https://www.buymeacoffee.com/assets/img/guidelines/download-assets-sm-2.svg
[buymeacoffee]: https://www.buymeacoffee.com/schmurtz
