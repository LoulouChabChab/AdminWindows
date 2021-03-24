## Hyperviseur de type 1
Par abus de langage, lorsque l'on parle d'hyperviseur on parle généralement de ce type d'hyperviseur.

La principale caractéristique d'un hyperviseur de type 1 c'est qu'il s'installe directement sur la couche matérielle du serveur. Au démarrage d'une machine physique, 
ces hyperviseurs prennent directement le contrôle du matériel.

Avantages : Un maximum de ressources peut être alloué aux machines virtuelles car ce type d'hyperviseur est directement lié à la couche matérielle.

Inconvénients : Il n'est possible d'exécuter qu'un seul hyperviseur à la fois. Cette problématique n'est toutefois pas vraiment impactante puisque dans la 
grande majorité des cas, un seul et même hyperviseur est capable de gérer tous les applicatifs d'une entreprise.

### Usage de ce type d'hyperviseur

Les hyperviseurs de type 1 peuvent être utilisés pour virtualiser des serveurs de fichiers, de bases de données, de messageries, etc... Ce type d'hyperviseur est à privilégier lorsque l'on souhaite exécuter des applicatifs en continu. 
La quasi-totalité des serveurs peut être virtualisée via un hyperviseur de type 1


## Hyperviseur de type 2

Un hyperviseur de type 2 est assez comparable à un émulateur car celui-ci s'installe sur un système d'exploitation déjà en place. 
Il se démarre la plupart du temps comme une simple application.

Hyperviseur de type 2
Avantages : Il est possible d'exécuter plusieurs hyperviseurs en même temps car ceux-ci ne s'installent pas directement sur la couche matérielle.

Inconvénients : Ce type d'hyperviseur ne peut pas fournir autant de ressources matérielles que les hyperviseurs de type 1 puisqu'ils sont installés $
sur un système d'exploitation, lui-même consommateur de ressources.

### Usage de ce type d'hyperviseur

Les hyperviseurs de type 2 sont utilisés pour virtualiser des OS sur des PC, la plupart du temps afin de procéder à des tests de compatibilité et/ou de sécurité.

Il existe également un environnement dans lequel ce type d'hyperviseur est particulièrement utilisé : 
pour les utilisateurs Mac OS X ayant besoin d'utiliser Windows (en raison d'applicatifs non compatibles).

## Différence entre NAS et SAN
Le NAS (Network Attached Storage)
Désigne une ressource de stockage directement connecté au LAN. Les serveurs NAS est configuré comme un filer et est accédé par les clients au travers d’un protocole réseau tel que TCP/IP, et des applications comme le NFS (Network File System) ou CIFS (Common Internet File System) pour l’accès aux fichiers. Le NAS permet donc à des clients de partager des fichiers comme s’ils étaient locaux.

### Inconvénient :
Toutefois, le stockage NAS ne peut envoyer que des fichiers, et non des blocs de données. Et le fait que celui-ci utilise le réseau IP de l’entreprise, peut engendrer des congestions de ce dernier, particulièrement pour de gros transferts de données.

### Avantage :
Son administration est simplifiée, une interface WEB accessible grâce à l’adresse IP ou le nom réseau du NAS, permet à l’administrateur de configurer 
son NAS ainsi que de gérer les groupes d’utilisateurs par exemple. Et il y a aussi un coût très faible par rapport au SAN



## Le SAN (Storage Area Network)
Il se différencie des autres systèmes de stockage tels que le NAS par un accès bas niveau aux disques. L’accès aux SAN est très similaire aux principes utilisés pour l’utilisation des disques internes (ATA, SCSI). C’est une mutualisation des ressources de stockage. Dans ce cas, les baies de stockage n’apparaissent pas comme des volumes partagés sur le réseau mais comme des disques internes. Elles sont directement accessibles en mode bloc par le système de fichiers des serveurs. En clair, chaque serveur voit l’espace disque d’une baie SAN auquel il a accès comme son propre disque dur. L’administrateur doit donc définir très précisément les Logical Unit Number (LUN, unités logiques), le masking et le zoning, pour qu’un serveur Unix n’accède pas aux mêmes ressources qu’un serveur Windows utilisant un système de fichiers différent.

### Avantage :
L’espace disque n’est plus limité par les caractéristiques des serveurs, et est évolutif à volonté par l’ajout de disques ou de baies de stockage sur le SAN. L’espace de stockage physique mutualisé pour les serveurs permet d’optimiser la gestion des disques, et de rendre plus aisées les sauvegardes de données.

Les ressources de stockage ainsi mutualisées donnent la possibilité de mettre en œuvre des fonctions de réplication (copie de données synchrone ou asynchrone entre deux baies) et de snapshot (duplication d’un volume pour l’utiliser sur un autre serveur ou pour le sauvegarder par exemple). Ces fonctions permettent de sécuriser les données (implantation physique dans des locaux distants) et d’optimiser la disponibilité des applications. Ces fonctions sont réalisées de façon transparente pour les serveurs, et la réplication et la copie de données n’affectent pas les ressources du serveur, puisqu’elles sont réalisées au niveau des contrôleurs SAN.

Certaines solutions SAN disposent de possibilité de transfert de données à distance, typiquement sur un site distant dans le cadre d’un plan de continuité d’activité (PCA).


## ZFS
ZFS est un système de fichiers open source sous licence CDDL.

Les caractéristiques de ce système de fichiers sont sa très haute capacité de stockage, l'intégration de tous les concepts précédents concernant les systèmes de fichiers
[pas clair] et la gestion de volume. Il intègre Files-11 (en)la structure On-Disk[Quoi ?], il est léger et permet facilement la mise en place d'une plateforme de gestion de stockage.
