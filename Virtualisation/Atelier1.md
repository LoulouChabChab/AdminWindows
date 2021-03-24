## Hypervisuer de type 1
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
