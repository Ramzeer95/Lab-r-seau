Nous voici à notre première étape ! 

Outils utilisés : VirtualBox, iso debian 12.2.0, et (en petite quantité) nos cerveaux :)

1/Installation des machines.
  Nous installerons les machines en mode terminal (pas besoin d'interface graphique !). Je vous passe l'installation (ou je dédierai un autre repository à cet effet on verra) de debian, passons au vif du sujet : la configuration réseau de nos VM.
    Pour notre réseau nous avons le schéma suivant 
    ...(le schéma arrive)...
    Une machine "principale" qui fera office de passerelle que l'on nommera... passerelle.
    2 réseaux internes : intnet et DMZ (pour notre projet de mise en place d'une DMZ) avec respectivement node1 (une VM) dans l'un et node2 (une autre VM) dans l'autre.
    
2/L'adressage
  Dèsormais passons à l'adressage.
    la passerelle aura un total de 3 interfaces réseaux d'activées : intnet, DMZ mais aussi une en NAT (évidemment nous souhaitons pouvoir encore sortir sur internet).
    Le réseau intnet sera en 192.168.45.0/24
    Le réseau DMZ sera en 192.168.46.0/24
    Dans les 2 cas l'interface de la passerelle sera 192.168.45-46.254/24
    Node1 : 192.168.45.11/24
    Node2 : 192.168.46.11/24

3/Les fichiers de configuration 
  Nos VM étant installées et notre adressage IP étant réalisé, il faut maintenant éditer les fichiers de configuration des machines, notamment concernant les interfaces réseaux, dans le répertoire /etc/network/interfaces
LES MACHINES NODE1 ET NODE2 AURONT LES MEME CONFIGURATIONS POUR L'INSTANT DONC POUR M'ALLEGER LA TACHE TOUT CE QUI SERA FAIT SUR NODE1 SERA A TRANSPOSER SUR NODE2.

  1)/etc/network/interfaces
      Dans ce fichier, nous allons configurer notre interface réseau qui est enp0s3 : 
        vim.tiny /etc/network/interfaces : 
        allow-hotplug enp0s3
        iface enp0s3 inet dhcp
            address 192.168.45.11 (mettre 192.168.46.11 sur l'autre machine)

REBOOT LES MACHINES.

Il reste une dernière chose à faire. En effet, si on effectue la commande ping 192.168.46.11 (depuis la machine en 45.11) le message sera le suivant : HOST UNREACHABLE
Pour se faire, il faut autoriser les sauts de réseaux depuis notre passerelle.
On se rend dans /etc/sysctl.com
    On y décommente la ligne ....

Et voilà, première partie configuration terminée ! :)
