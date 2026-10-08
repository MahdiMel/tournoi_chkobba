# ♦️ Chkobba Leaderboard - Système de Classement Serverless

![Statut](https://img.shields.io/badge/Statut-Projet_1%2F7-brightgreen)

## 📖 L'Histoire derrière le projet

**Le Problème :** 
Tout au long de l'année scolaire, nos tournois de Chkobba (le célèbre jeu de cartes tunisien) souffraient d'un mal récurrent : la perte des scores. Entre les feuilles volantes égarées, les notes effacées et les contestations de points (ou la triche amicale), il devenait impossible de maintenir un classement fiable sur l'ensemble de l'année.

**La Solution :** 
Plutôt que d'utiliser une application de notes générique, j'ai développé notre propre plateforme sur-mesure. Un site web accessible instantanément sur mobile via un simple lien, doté d'un classement en temps réel et, surtout, infalsifiable grâce à une base de données verrouillée.

## 🚀 Le Défi "7 Projets en 7 Jours"

Ce projet marque le **Jour 1 de mon défi de codage sur 7 jours**. L'objectif ? Concevoir, coder et déployer 7 projets complets consécutifs pour consolider mes compétences techniques avant que le rythme des cours du cycle préparatoire ne devienne trop sérieux. 

## 📸 Aperçu du Projet

https://mahdimel.github.io/tournoi_chkobba

### Vue Publique (Classement en temps réel)
<img width="566" height="926" alt="image" src="https://github.com/user-attachments/assets/7a5b69ca-6880-4de1-b2f1-545f49315902" />


### Panneau d'Administration (Sécurisé)
<img width="692" height="887" alt="image" src="https://github.com/user-attachments/assets/22af0c70-968e-4a4f-a047-c1164be4fc7e" />


## ✨ Fonctionnalités Clés

*   **Logique de Départage :** Tri automatique par ordre décroissant des scores, avec un avantage accordé au plus petit nombre de matchs joués en cas d'égalité,Incrémentation automatique du compteur de matchs lors de l'ajout de points positifs, avec boutons de correction manuelle.
*   **Synchronisation en Temps Réel :** Les scores et le fil d'actualité se mettent à jour instantanément sur les écrans de tous les joueurs sans rechargement (WebSockets).
*   **Sécurité PostgreSQL (RLS) :** L'écriture dans la base de données est strictement limitée à l'administrateur authentifié. La triche côté client est impossible.
*   **Historique Traçable :** Fil d'actualité affichant les derniers mouvements de points pour une transparence totale.

## 🛠️ Stack Technique

*   **Frontend :** HTML5, CSS3, JavaScript (Vanilla)
*   **Backend & BDD :** Supabase (PostgreSQL, Authentication, Realtime)
*   **Hébergement :** GitHub Pages

## ⚙️ Comment exécuter le projet (Installation)

1. Récupérer le code localement
> git clone https://github.com/VOTRE-PSEUDO/classement-chkobba.git

2. Configuration du Backend (Supabase)

Créez un projet gratuit sur Supabase.

Ouvrez le SQL Editor et exécutez votre script SQL initial pour générer le schéma `chkobba`, les tables `joueurs` et `historique`, ainsi que les politiques de sécurité (RLS).

Dans les paramètres de la base de données (ou via SQL), activez la fonctionnalité Realtime pour ces deux tables.

Allez dans l'onglet Authentication et créez manuellement un utilisateur (Email / Mot de passe) qui servira de compte administrateur.

3. Liaison de l'API

Allez dans Project Settings > API sur votre tableau de bord Supabase.

Copiez l'URL du projet et la clé publique (`anon` / `public`).

Ouvrez `index.html` et `admin.html` dans votre éditeur de code et remplacez les variables `supabaseUrl` et `supabaseKey` par vos propres valeurs.

4. Lancement et Test

Localement : Ouvrez simplement `index.html` dans votre navigateur web, ou utilisez l'extension Live Server dans VS Code. Accédez ensuite à la page `admin.html` pour tester la connexion avec vos identifiants.

En ligne : Hébergez les fichiers statiques sur GitHub Pages (comme configuré dans ce dépôt) pour rendre le classement accessible à tous les joueurs.

## ⚖️ Droits d'utilisation

Le code source de ce projet est rendu public à des fins de démonstration, de portfolio et d'apprentissage.

*Toute réutilisation, modification, distribution ou exploitation de ce code (en partie ou dans sa totalité) à des fins commerciales est strictement interdite* sans l'autorisation préalable et explicite de l'auteur.*

*Libre réutilisation (Non-commerciale) :*
Vous êtes totalement libre de vous inspirer de ce projet, de le télécharger et de le modifier pour vos propres besoins personnels, éducatifs ou associatifs. Que ce soit pour gérer les scores de vos propres jeux de société, organiser un tournoi sportif local, ...
