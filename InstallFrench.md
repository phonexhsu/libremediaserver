 

Libre Media Server – Un Média serveur open-source.
(C) 2012-2013 Santi Noren

 

Développement et support: libremediaserver@gmail.com

Page du projet: http://code.google.com/p/libremediaserver

 

Ce programme est un logiciel libre. Vous pouvez le redistribuer et / ou le modifier selon les termes de la Licence Publique Générale GNU, telle que publiée par la Free Software Foundation, soit la version 3 de la Licence, ou (à votre choix) toute version ultérieure.

Ce programme est distribué avec l'espoir qu'il puisse être utile, mais SANS AUCUNE GARANTIE, sans même la garantie implicite de COMMERCIALISATION ou D'ADAPTATION À UN USAGE PARTICULIER. Voir la Licence Publique Générale GNU pour plus de détails.

Vous devriez avoir reçu une copie de la Licence Publique Générale GNU avec ce programme, sinon, écrivez à la Free Software Foundation, Inc., 59 Temple Place - Suite 330, Boston, MA 02111-1307, USA.

 

I. Conditions requises

LMS est développé et testé sur Debian Wheezy et dérivés.

Le logiciel nécessite une carte graphique OpenGL avec  des pilotes Xorg et l'accélération matérielle correctement installés. Entrer "glxgears" dans un terminal devrait ouvrir une fenêtre avec trois roues d’engrenage qui doivent tourner. Si ce n’est pas le cas, consultez la documentation de votre distribution.

Pour résoudre les dépendances, vous devez avoir une connexion Internet sur l'ordinateur pendant le processus d'installation.

LMS communique avec Pure Data via le port TCP de 9195 à 9198. Open Lighting Architecture utilise le port 9090 de votre serveur web. Il est primordial que ces ports ne soient pas utilisés par d'autres applications.

Vous n'avez pas besoin de deux ordinateurs pour gérer LibreMediaServer, mais le CTIP / MSEX ne fonctionnera pas sur localhost.
Au moment où le programme commence, vous devez disposer d'une interface réseau active, après avoir démarré. Si vous voulez contrôler le media serveur à partir d'un autre ordinateur, vous devez configurer la carte réseau du système d'exploitation selon le protocole que vous utilisez. Pour artnet utiliser une adresse IP de type 2.x.x.x avec un masque de sous réseau 255.0.0.0.

II. Installation d’OLA
Ouvrez un terminal en tant que root et éditez le fichier source.list
sudo gedit /etc/apt/sources.list

Ajoutez la ligne suivante :
Sous debian > deb http://apt.openlighting.org/debian/ wheezy main
Sous ubuntu > deb http://apt.openlighting.org/debian/ precise main

Enregistrez et fermez l’éditeur de texte.
Exécutez la commande « apt-get update » pour mettre à jour la liste des dépôts.
Installez le logiciel OLA avec la commande apt-get
apt-get install ola
Lancer OLA
/etc/init.d/olad start

III. Installation de libremediaserver.

Ouvrez un terminal en tant que root et allez dans le répertoire des scripts avec la commande
cd /répertoire racine/scripts
Exécutez le fichier d’installation selon votre système d’exploitation.
./Install\_wheezy.sh

ou

./Install\_precise.sh

Confirmez Oui  lorsqu’il vous est demandé confirmation pour  télécharger les fichiers et assurez-vous que vous êtes connecté à Internet. Ensuite, cliquez sur Non lorsque vous êtes invité à démarrer  OLA daemon au démarrage du système.

Lancer libremediaserver
cd/repertoire LMS
puis
./libremediaserver
IV. Configuration

Cette étape n'est nécessaire qu’à la première exécution de LMS

a. Dans le menu fichier de l’application, cliquez sur « setup OLA »

b. Cliquez sur le bouton "Ajouter un univers"

c. Spécifiez le numéro de l’univers concerné (ID) et donnez-lui un nom. Cochez dans la liste le ou les protocoles que vous souhaitez utilisez en vous assurant de faire attention au sens (input ou output) des données.
Si vous choisissez le protocole Artnet,  entrez dans "Univers Id" le numéro de l'univers ArtNet pour lesquels vous souhaitez recevoir les signaux dmx. L’univers et le subnet peuvent être ultérieurement modifiés dans le fichier  ~ /. Ola / wave-artnet.conf. L’univers par défaut est 0 et le subnet 0.

Vous pouvez vérifier que l'information dmx circule en cliquant sur l'univers dans le menu de gauche, puis sur l’onglet "DMX Monitor".
Une fois la configuration terminée, fermez la fenêtre du logiciel OLA.
d. Configurez la réception dmx du logiciel en cochant la case « Read DMX » et en spécifiant le numéro de l’univers dmx précédemment configuré dans OLA (OLA universe).
e. Dans le logiciel LMS, cliquez sur le menu Fichier puis « Changer le répertoire de média » et sélectionnez le répertoire où sont vos médias. L’arborescence de ce dossier doit respecter un ordre particulier pour fonctionner. Référez-vous à la section correspondante dans le manuel d’utilisation. Définissez ensuite l'adresse DMX de chaque couche selon le patch de la table via les boites de dialogue sous chaque couche.

Si vous utilisez le CITP / MSEX afin de générer les vignettes de vos couches, allez dans le menu CITP / MSEX et cliquez sur « créer des vignettes ». Les vignettes sont générées automatiquement.