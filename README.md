# Projet: Les pays en chiffres
Utilisation du langage SQL pour créer et manipuler une base de données PostgreSql.
La base de données est hébergée sur un saas ElephantSql


# Pré-requis
* créer une instance sur ElephantSql
* installer pgAdmin

# Etapes du projet

## Création de la base de données                                                                        
* La base de données est crée automatiquement avec la création de l'instance sur ElephantSql  
* ouvrir pgAdmin et cliquer sur la base de données crée

## Installation
L'exécution du code du fichier "script.sql" va permettre de:
* Créer la table "countries_2020" avec toute les colonnes
* Insérer les données dans la table "countries_2020"
* Créer la fonction "get_country_proprieties(country_name)" avec un paramètre d'entrée "nom du pays" et qui nous retourne une table avec toutes les propriétés du pays
* Créer la procédure "insert_country(new_country)" qui insert un nouveau pays
* Créer 
* Créer le trigger qui met à jour la colonne de la date d'insertion du nouveau pays
* Créer la fonction qui va retourner les pays regroupés par 4 tranches de densité de population "get_country_tranche()"

## Requêtes

* pour afficher toutes les colonnes de la table, on utilise la requête:

select * from countries_2020;

* pour afficher les données en utilisant  la fonction  "get_country_proprieties(country_name)", on utilise la requête:

select * from get_country_proprieties('Algeria');      

dans cet exemple le pays utilisé comme paramètre est  "Algeria

* pour insérer le nouveau pays avec la procédure  "insert_country(new_country )", on utilise la requête:

call insert_country('Dubai');

dans cet exemple le nouveau pays inséré est Dubai.

* pour vérifier que le nouveau pays est bien inéré et la colonne date d'insertion est bien mise à jour, on utilise la requête:

select * from get_country_proprieties('Dubai');  

* pour afficher les pays regroupés par les 4 tranches de densité de population en utilisant la fonction "get_country_tranche()", on utilise la requête:

select * from get_country_tranche();
