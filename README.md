# Lolo's Home Assistant Configuration Files
# Version FR

Bonjour, vous trouverez ci dessous ma partage d'expérience concernant mon installation Home Assistant que j'ai réalisé ces dernières semaines.

## A- Raspberry Pi 3B+ installation avec PiDrive
Comme j'ai lu que la carte SD n'était pas la meilleure installation pérènne pour une installation de Home Assistant, j'ai utilisé un PiDrive que j'avais à disposition.

1- Dans un premier temps, j'ai installé Home Assistant en mode standard sur une carte SD de 8Go comme indiqué dans [Installation Home Assistant](https://hacf.fr/installer-et-regler-home-assistant-sur-un-raspberry-pi/).

2- J'ai installé le Add-On [Serveur SSH](http://www.lacavernedefred.ovh/blog/2018/03/08/debuter-avec-home-assistant/) pour autoriser un accès SSH à Home Assistant 

3- Ensuite, il faut utiliser la commande DATACTL. pour réaliser cela, il faut autoriser la connexion SSH depuis l'extérieur. 
Pour cela, il faut suivre les instructions présentes [ici](https://community.home-assistant.io/t/ssh-into-hassos/84909/39?u=lolopicolo)

Ensuite, une fois l'accès autorisé, voici les commandes à utiliser 
login, puis fdisk -l pur identifier le disque dur et ensuite datactl move /dev/sdX où X est la lettre correspondant au disque PiDrive
Toutes les explicatione en anglais sont [ici](https://community.home-assistant.io/t/hass-io-transfer-from-sd-card-to-ssd-or-usb/97452/270?u=lolopicolo)
Une fois le transfert réalisé, aucun moyen de vérifier que cela s'est bien passé sauf à tenter de reproduire l'opération. Un message d'erreur indiquera que le disque source et destination ne peuvent être le même.

4- Pour redimensionner la partition de la zone configuration, il faut utiliser GParted en bootant votre pc sur une clé USB disposant de GParted et en connectant le disque utilisé sur Home Assistant. Pour utiliser GParted, la procédure est [ici](https://gparted.org/liveusb.php#windows-method-a)

## B- Premières implémentations

1- J'ai installé Samba Share, File Editor, Duck DNS, Home Assistant Community Store, Backup & Restore Google, motionEye, Gigaset Elements, Méteo france, Garbage Collection, Renault Zoe, Waze, Calendar, Enedis

  - Pour Samba Share, File Editor et Duck DNS, j'ai utilisé le sous-menu Add-on Store dans le menu supervisor. 
  - Pour [Samba](https://hacf.fr/partager-votre-installation-home-assistant-via-samba-share/), j'ai créer un ensemble utilisateur/mot de passeport pour me donner accès aux répertoires de configuration directemetn depuis mon PC.
  - Pour [File Editor](https://hacf.fr/file-editor-et-home-assistant-modifier-vos-fichiers/), vous pouvez éditer les fichiers de configuration directement depuis l'interface web. Mais ce n'est pas la manière la plus simple.
  - Pour [DuckDNS](https://hacf.fr/acceder-a-home-assistant-depuis-lexterieur-via-duckdns/), c'est pour l'accès externe. J'ai cré un compte pour avoir accès à un lien externe myhomeassistant.duckdns.org pour l'accès externe de mon système.

- Pour le HACS (Home Assistant Community Store), J'ai suivi les instructions sur [HACS installation HACF](https://hacf.fr/installer-ajouter-integrations-customisations-avec-hacs/)

- Pour le système de sauvegarde Backup & Restore Google, J'ai suivi les instructions sur [Backup Google installation HACF](https://hacf.fr/sauvegarder-votre-home-assistant-sur-le-cloud-google/)

## C- MotionEye
## D- Gigaset Elements
## E- Méteo France
## F- Garbage Collection
## G- Renault Zoe
## H- Waze
## I- Calendar
## J- Enedis
## K- Thermometre/Hydromètre Xiaomi
## L- Module Sonoff / Module TP Link
## M- Installation du pilotage Chauffage
























Version EN

My Personal Home Assistant Configuration

Hi all, please find below my shared experience on Home Assistant Installation and setup i've done the previsous weeks.

# A- Raspberry Pi 3B+ installation with PiDrive
as i've read that SD is not the best way to store my Home assistant installation, i used a PiDrive i have in house to install Home Assistant.
first i use dedicated distribution of Raspbian

1- PiDrive Community Foundation can be found here : [CommunityFoundationEdition](https://github.com/PiDrive/CommunityFoundationEdition)

- i downloaded the package that i extracted on a 8Gb MicroSD (can be 4Gb if you have).
- RPi3 has started on this SD Card and my pidrive was connected.
- i choose in NOOBS Raspbian Lite in France with FR Keyboard.
- i enabled SSH in Raspi-config for remote installation and control.

2- Then i followed instructions from [Community Site](https://community.home-assistant.io/t/installing-home-assistant-supervised-on-a-raspberry-pi-with-debian-10/247116)

As i've done this migration after few weeks of setup, i used Full Snaptshot on my SD installation to move to PiDrive. Worked fine.

# B- First implementations

1- I've installed Samba Share, File Editor, Duck DNS, Home Assistant Community Store, Backup & Restore Google, motionEye, Gigaset Elements, Méteo france, Garbage Collection, Renault Zoe, Waze, Calendar, Enedis

- For Samba Share, File Editor and Duck DNS, i used standard Add-on Store menu in supervisor item. 
  - For Samba, i create user/password to let me access to config folder.
  - For File Editor, we can have access directly from Web UI.
  - For DuckDNS, this is for external use. i create an account to let me have a myhomeassistant.duckdns.org link to my personnel home assistant system.

- For Home Assistant Community Store, i installed package following [Home Assistant installation link](https://hacs.xyz/docs/installation/manual) and [Home Assistant installation French link](https://hacf.fr/installer-ajouter-integrations-customisations-avec-hacs/)

- For Backup & Restore Google, i use HACS and follow [French instructions](https://hacf.fr/sauvegarder-votre-home-assistant-sur-le-cloud-google/)
