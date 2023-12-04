# Lab-r-seau
Ensemble de projet en réseau

Bonjour ! 

Ici vous me suivrez à travers un ensemble de petits projets réseaux, de difficulté croissante, donnés par mon professeur Greneche Nicolas ! 

Table des matières : 

- Mise en place d'un réseau à l'aide d'une passerelle permettant d'aller à l'extérieur, 2 réseaux internes passant par cette passerelle. Je configurerai les machines ainsi qu'un serveur DNS et les zones associées à l'aide de Bind9.
- Mise en place d'une DMZ. Je vais transformer 1 de nos 2 réseaux internes en DMZ dont le principe et le suivant : Toutes connexions depuis l'extérieur de la DMZ sont autorisées à y entrer mais rien n'est t'autorisé à sortir depuis le DMZ. En d'autre terme, un serveur/machine à l'intérieur de la DMZ ne pourra pas initier de connexion vers l'extérieur. IPTABLES sera le principal outil utilisé pour ce projet.
- Mise en place du NIDS : installation de snort (ou alors surricata). On l'utilisera pour log les paquets ICMP
- Mise en place d'un système de capture de paquet : j'utiliserai pour ce faire l'outil libcap

LE RESTE ARRIVE...
