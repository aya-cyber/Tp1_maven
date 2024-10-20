Description
Ce projet implémente un mécanisme d'Inversion de Contrôle (IoC) et d'Injection de Dépendances (DI) en Java en utilisant la réflexion pour instancier dynamiquement des classes et injecter des dépendances. Le programme lit les noms des classes à partir d'un fichier de configuration, charge les classes à l'exécution, et injecte les dépendances en utilisant la réflexion.j
Le but est de démontrer comment mettre en œuvre l'injection des dépendances sans utiliser de framework comme Spring.

Fonctionnalités
Lecture du nom des classes DAO et Métiers à partir d'un fichier de configuration (config.txt).
Utilisation de la réflexion pour charger les classes DAO et Métiers, et instanciation dynamique.
Injection du DAO dans le Métier à l'aide de la méthode setDao() via réflexion.
Calcul du résultat via l'interface IMetier et affichage du résultat.
Structure du Projet
Le projet contient les fichiers suivants :

IMetier.java : Interface qui déclare la méthode calcul().
MetierImpl.java : Classe implémentant IMetier. Cette classe utilise un objet DAO pour obtenir des données.
IDao.java : Interface représentant le Data Access Object (DAO).
DaoImpl.java : Implémentation de l'interface IDao, représentant la source de données.
Presentation2.java : Point d'entrée du programme. Ce fichier lit les noms des classes dans un fichier de configuration, les charge dynamiquement via la réflexion, injecte les dépendances, et exécute la logique métier.
