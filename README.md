# projet_etl_dw_pentaho_olap : Installation, Prise en Main et Application OLTP → OLAP

## Objectifs du projet
- Installer et configurer Pentaho PDI (Spoon)
- Découvrir les étapes principales et les hops
- Réaliser une data pipeline complète : nettoyage de données, agrégations, construction d'un schéma en étoile
- Charger les données vers un mini Data Warehouse (SQLite)
- Exécuter des requêtes OLAP pour l’analyse décisionnelle

## Technologies utilisées
- Pentaho PDI (Spoon)
- Java 8 ou 11 (nécessaire pour PDI)
- SQLite (base locale)
- CSV (jeu de données)
- SQL pour validation OLAP
- Windows ou macOS

## Organisation du dépôt

- `/data/` : fichiers CSV sources pour les exercices
- `/ktr/`  : transformations PDI pour chaque TP (`.ktr`)
  - TP1 : installation et transformation de base (Hello)
  - TP2 : nettoyage enrichi, agrégations et gestion d’erreurs
- `/schema/` : captures d’écran des schémas de hops par TP
- `rapport.pdf` : rapport final détaillant toutes les étapes, difficultés et solutions

## Instructions pour exécuter le TP

1. **Installer Java** (8 ou 11 selon la plateforme)
2. **Télécharger et décompresser Pentaho PDI** ([lien officiel](https://sourceforge.net/projects/pentaho/files/Data%20Integration/))
3. **Lancer Spoon** :
   - Windows : `data-integration\Spoon.bat`
   - macOS : `data-integration/./Spoon.sh`
4. **Importer les jeux de données CSV** depuis `/data/`   
5. **Ouvrir chaque transformation `.ktr` dans `/ktr/`** et exécuter étape par étape (instructions détaillées dans le rapport)
6. **Valider la structure des tables SQLite** avec `/sql/create_tables.sql`
7. **Exécuter les requêtes OLAP** via `/sql/queries_olap.sql` dans votre outil SQL favori
8. **Vérifier les résultats, consulter le rapport pour dépannage**

## Membres du groupe

- Khadija Nachid Idrissi
- Rajae Fdili
- Aya Hamim


## Difficultés fréquentes & Solutions

- Problèmes Java (Spoon ne démarre pas, erreur SWT/AWT) → cf. rapport & README
- JDBC SQLite introuvable : placer sqlite-jdbc.jar dans `data-integration/lib/`
- Bon paramétrage des hops et gestion des erreurs
- Rejouer les chargements avec « Truncate table »

