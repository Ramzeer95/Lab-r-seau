Maintenant que nos machines sont prêtes, nous allons installer iptables, qui va être l'outil principal permettant de réaliser ce projet.

Effectivement, un ensemble de règle va nous permettre de faire en sorte que notre réseau DMZ soit réellement une DMZ.

Pour commencer, nous allons d'abord mettre en place de règle de routage pour le natage des machines des différents sous-réseaux.

Grâce à ces 2 (pour les 2 réseaux) commandes :



Une fois cela fait, on va installer nginx sur Node1 (machine du réseau interne) et DMZ (machine du réseau DMZ) pour réaliser nos tests
APT INSTALL NGINX
SYSTEMCTL START NGINX

Ensuite, on rentre ces règles : 


(REGLES + EXPLICATIONS)

Maintenant, passons aux test

DEPUIS NODE1 : 
On voit bien que le serveur nginx de la DMZ et joignable notamment de par un curl 192.168.46.11 (ip de la machine DMZ)
Essayons la manip inverse PHOTO
On voit bien que le serveur nginx de NODE1 est innacessible depuis la DMZ.
