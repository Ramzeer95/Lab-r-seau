Maitenant que nos machines sont configurées, il nous faut configurer notre serveur DNS !
(Tout se déroule dans notre passerelle)
Outil nécessaire : apt install bind9

AVANT DE COMMMENCER 
Nous devant configurer quelque chose : le bail DHCP. en effet, sur la passerelle, notre interface nous permettant de sortir sur internet est en DHCP.
Cela implique un bail DHCP chargé à chaque fois qui va écraser notre configuration DNS (notamment le fichier /etc/resolv.conf)
Pour cela on va éditer le fichier dhclient.conf --> vim.tiny /etc/dhcp/dhclient.conf

Rendons nous dans les fichiers de configuration bind --> 'cd /etc/bind'
Commençons par créer un répertoire pour nos zones : 'mkdir zones'

Une fois ce fichier de créer, il faut créer nos zones (on en aura une seule dans notre cas).

Une fois notre zone créee, il faut se rendre dans /etc/bind/named.conf.local afin de mettre dans la fonction forward l'ip de notre serveur DNS.
