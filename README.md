# Tifosi

# Tifosi - Système de Gestion de Base de Données

Ce projet a été réalisé dans le cadre d'une mission pour le restaurant de Street-Food italien **Tifosi**. L'objectif est de concevoir et de mettre en place une base de données relationnelle pour gérer les recettes de focaccias, les stocks d'ingrédients et les menus proposés aux clients.

## Contenu du dépôt

Le projet est structuré en trois scripts SQL principaux :

1.  **`schema_base_de_données.sql`** : Script de création de la structure (tables, relations, utilisateur).
2.  **`insertion_des_données_de_test.sql`** : Script d'alimentation de la base avec les données fournies (focaccias, ingrédients, boissons, marques).
3.  **`requêtes_test.sql`** : Script contenant les 10 requêtes de test demandées pour vérifier le bon fonctionnement de la base.

---

## Installation

Pour déployer cette base de données localement :

1.  Ouvrez **phpMyAdmin**.
2.  Importez le fichier `schema_base_de_données.sql` pour générer la structure.
3.  Importez le fichier `insertion_des_données_de_test.sql` pour remplir les tables.
4.  L'utilisateur `tifosi` sera automatiquement créé avec les privilèges nécessaires.

---

## Modèle Conceptuel de Données (MCD)

La base de données respecte scrupuleusement le schéma fourni par le client, incluant les relations spécifiques :
* **Focaccia ↔ Ingrédient** (via la table `comprend`)
* **Boisson ↔ Marque** (via la table `appartient`)
* **Menu ↔ Focaccia / Boisson** (via les tables de liaison)
* **Client ↔ Menu** (via la table `achete`)

---

## Tests de vérification

Le fichier `requêtes_test.sql` répond aux 10 besoins spécifiques du restaurateur, notamment :
* Le calcul du prix moyen des produits.
* La gestion des stocks (ingrédients inutilisés).
* Le filtrage des recettes selon les allergènes (ex: sans champignons).
* La liaison entre les boissons et leurs marques respectives.

---

## Fichier de captures d'écran

Le fichier captures d'écran contient :
* La capture d'écran du concepteur.
* Les captures d'écran des résultats des différents test
*
---
