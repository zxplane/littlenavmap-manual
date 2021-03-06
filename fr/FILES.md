## Fichiers {#files}

### Logs (journaux de bord)

Les fichiers journaux de _Little Navmap_ sont stockés dans les répertoires:

* Windows: `C:\Users\YOURUSERNAME\AppData\Local\Temp\abarthel-little_navmap.log`
* Linux: `/tmp/abarthel-little_navmap.log`
* macOS: `/var/folders/RANDOMIZED_DIRECTORY_NAME/abarthel-little_navmap.log`

Le programme conserve trois fichiers journaux et les fait pivoter à chaque démarrage. Vous pouvez donc trouver jusqu' à trois logs:

`abarthel-little_navmap.log`, `abarthel-little_navmap.log.1` et `abarthel-little_navmap.log.2`.

Assurez-vous d'envoyer le bon fichier journal après un plantage. Ne redémarrez pas le programme si vous voulez rapporter puisqu'il fera effacer les fichiers journaux. En cas de doute, envoyer toutes les copies dans un fichier Zip.

### Configuration

Tous les fichiers de configuration de mes programmes sont stockés dans les répertoires:

* Windows: `C:\Users\YOURUSERNAME\AppData\Roaming\ABarthel`
* Linux et macOS: `$HOME/.config/ABarthel`

* `little_navmap.ini`: fichier de configuration du style INI Fichier texte
* `little_navmap.history`:  L'historique des positions sur la carte. Fichier binaire.
* `little_navmap.track`: La piste de l'aéronef de l'utilisateur. Fichier binaire.

Trois fichiers de configuration supplémentaires sont créés pour la personnalisation des couleurs et des styles:

* `little_navmap_fusionstyle.ini`: fichier de configuration du style INI pour personnaliser les couleurs de l'interface graphique du style `Fusion`.
* `little_navmap_nightstyle.ini`: fichier de configuration du style INI pour personnaliser les couleurs de l'interface graphique du style `Night`.
* `little_navmap_mapstyle.ini`: fichier de configuration du style INI. Fichier texte. Utilisé pour personnaliser l'affichage de la carte.

Voir [Personnalisation](CUSTOMIZE.md) pour plus dinformations.

Le cache disque qui est utilisé pour stocker toutes les images téléchargées de la carte en ligne est disponible ici:

* Windows `C:\Users\YOURUSERNAME\AppData\Local\.marble\data`
* Linux et macOS: `$HOME/.local/share/marble`

You can delete the cache manually to save space if _Little Navmap_ is not running.

### Databases {#databases}

Plusieurs bases de données sont stockées dans le répertoire :

`...\ABarthel\little_navmap_db`

Toutes ces bases de données sont des fichiers [SQLite](http://sqlite.org) qui peuvent être visualisés avec par exemple [DB Browser pour SQLite](https://github.com/sqlitebrowser/sqlitebrowser/releases) si vous êtes intéressé par les bases de données relationnelles.

**Ne pas modifier, déplacer, renommer ou supprimer des bases de données pendant que **_Little Navmap_** est en cours d'exécution.**

#### Scenery Library {#scenery-library}

Le nombre de fichiers dépend des simulateurs que vous avez installés et des bibliothèques de scènes que vous avez chargées.

Les fichiers sont:

* `little_navmap_.sqlite`: Une base de données factice vide.
* `little_navmap_fsx.sqlite`: Flight Simulator X
* `little_navmap_fsxse.sqlite`: Flight Simulator - Steam Edition
* `little_navmap_p3dv2.sqlite`: Prepar3D v2
* `little_navmap_p3dv3.sqlite`: Prepar3D v3
* `little_navmap_p3dv4.sqlite`: Prepar3D v4
* `little_navmap_xp11.sqlite`: X-Plane 11
* `little_navmap_navigraph.sqlite`: Navigraph navdatabase. Il peut s'agir de la base de données incluse ou d'une mise à jour installée par Navigraph _FMS DATA MANAGER_.

#### Données Utilisateurs

Le fichier `little_navmap_userdata.sqlite` contient les waypoints définis par l'utilisateur. 

_Little Navmap_ crée une copie de sauvegarde au démarrage et conserve jusqu'à quatre fichiers de sauvegarde: `little_navmap_userdata_backup.sqlite` vers `little_navmap_userdata_backup.sqlite.3`. Vous pouvez copier ces fichiers dans la base de données originale `little_navmap_userdata.sqlite` si vous avez fait quelque chose de mal.

#### Autres Fichiers de Base de Données

Fichiers supplémentaires comme

* `little_navmap_compiling.sqlite`,
* `little_navmap_compiling.sqlite-journal`,
* `little_navmap_temp.sqlite`,
* `little_navmap_temp.sqlite-journal`,
* `little_navmap_onlinedata.sqlite` ou
* `little_navmap_onlinedata.sqlite-journal`

sont des restes de processus temporaires comme la compilation de la base de données et peuvent être ignorés.
