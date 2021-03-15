Le partage de déploiement comprend les dossiers suivants : 
- Applications. Ce dossier contient les fichiers d’application pour l’installation par le biais 
des séquences de tâches MDT 
- Operating system. Ce dossier est l’emplacement par défaut pour les images 
d’installation du système d’exploitation 
- Out-of-Box Drivers. Ce dossier est l’emplacement par défaut pour 
stocker les pilotes 
- Packages. Ce dossier est l’emplacement par défaut pour les packages du système 
d’exploitation, tels que les mises à jour de sécurité ou les packs de langue 
- Task Sequences. Ce dossier contient des séquences de tâches dans des sous-dossiers et des 
fichiers de contrôle, tels que le fichier CustomSettings.ini 
- Modèle. Ce dossier contient les packs Objet de stratégie de groupe (GPO) Gestionnaire 
de conformité de la sécurité MDT 2012 
- Outils. Ce dossier est l’emplacement par défaut pour les outils MDT que vous pouvez 
utiliser avec des déploiements ZTI 

## Fichier de configuration
### Boostrap
BootStrap. ini : Fichier de configuration utilisé lorsque l'ordinateur cible n'est pas en mesure de se connecter au point de déploiement approprié. Cette situation survient dans un scénario de nouvel ordinateur et pour l'ordinateur de remplacement d'un scénario de remplacement d'ordinateur. Le fichier BootStrap.
Le fichier Bootstrap.ini permet de configurer les écrans bienvenu, déploiement et compte d’utilisateur. Les autres écrans sont gérés par le fichier customsettings.ini.

### CustomSettings
CustomSettings.ini : Fichier de configuration principal pour les règles de traitement utilisées dans tous les scénarios. Le fichier reste dans le dossier de déploiement.
