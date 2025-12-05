# Steam & Steel Battlegrounds — Projet LOG3900 (Automne 2025)
Client léger (Flutter) • Client lourd (Angular) • Serveur (NestJS)

Ce dépôt présente la version finale du projet PolyRPG développée dans le cadre du cours **LOG3900 – Projet de développement logiciel**.  
Il s’agit de l’évolution complète du projet LOG2990 vers une plateforme **multiplateforme**, comprenant :

- un **client lourd** (Angular)
- un **client léger** (Flutter / Android)
- un **serveur** (NestJS, MongoDB)
- un protocole de synchronisation en temps réel (WebSocket)

Le présent README se concentre principalement sur le **client léger**, qui constitue la plus grande nouveauté du Projet 3.

---

# 📌 Aperçu général

Steam & Steel Battlegrounds est une plateforme de jeu tactique multijoueur dans laquelle les utilisateurs peuvent :

- créer un compte et personnaliser leur profil  
- rejoindre / créer des parties sur différentes cartes  
- clavarder avant et pendant la partie  
- jouer en temps réel sur des cartes interactives  
- réaliser des défis, gagner de la monnaie virtuelle et progresser en niveau  

---

# ⭐ Fonctionnalités implémentées (Client léger)

## 🗨️ Clavardage intégré et canuax de discussion
- Fenêtre de chat intégrée en tout temps dans l’application
- Messages horodatés, avatar + nom du joueur
- Défilement complet + indicateur de nouveaux messages
- C2Canal général
- Canal spécifique à chaque partie
- Historique complet des messages
![Screenshot](/demo-images/C2.png)

## 👤 Compte utilisateur & paramètres
- Création et authentification
- Modification du profil : pseudo, avatar, courriel
- Capture d’une photo via la caméra de la tablette
- Statistiques : parties jouées, victoires, temps moyen
- Historique des connexions et des parties
![Screenshot](/demo-images/C1.png)
## ⚔️ Modes de jeu
- Mode Classique
- Mode Capture-the-Flag
![Screenshot](/demo-images/C3.png)
## Options de jeux
- Élimination rapide
- Drop in drop out
- Prix d’entrée
- Amis seulement
![Screenshot](/demo-images/C4.png)

## 💰 Système de monnaie virtuelle
- Dépenses et gains
- **Prix d’entrée** pour rejoindre certaines parties

## 🎨 Personnalisation de l’application
- Thème visuel (clair / sombre)
- Persistant localement

## 🫂 Système d’amis
- Ajout / suppression d’amis
- Recherche d’utilisateurs
- **Création de parties “amis seulement”**

## 🎯 Défis de partie
5 défis implémentés :
1. Bouger 25 % des cases  
2. Infliger 5 dommages  
3. Ne perdre aucune vie  
4. Ouvrir 2 portes  
5. Collecter 2 objets  

## 🔍 Filtres de recherche de parties
- Filtre par mode de jeu  
- Filtre par nombre de joueurs  
- Filtre alphabétique

## 🟢 Statut en ligne / hors ligne des amis
- Affichage du statut dans :
  - le chat
  - la liste d’amis
  - le profil utilisateur

## 🛒 Boutique virtuelle
- 5 bannières achetables
- 5 avatars achetables
- Intégration au système de monnaie virtuelle

## ⭐ Système de niveau
- Gain d’XP via les défis  
- Niveau affiché dans :
  - la salle d’attente
  - la liste d’amis
  - le profil

## 📩 Invitations en temps réel
- Un joueur peut inviter ses amis connectés
- Pop-up d’invitation avec "Accepter" / "Refuser"

## 👁️ Mode Observateur
- Rejoindre une partie sans interagir
- Icône “œil” pour distinguer les spectateurs
- Chat disponible

---

# 📱 Aperçu visuel (captures à ajouter)

## Menu principal
*(Insérer capture)*

## Profil utilisateur & avatar caméra
*(Insérer capture)*

## Liste d'amis & statut en ligne
*(Insérer capture)*

## Salle d’attente & invitations
*(Insérer capture)*

## Chat & canaux
*(Insérer capture)*

## Défis & niveaux
*(Insérer capture)*

## Boutique
*(Insérer capture)*

## Modes de jeu
*(Insérer capture)*

---

# 🧪 Technologies utilisées

## Client léger (mobile)
- **Flutter**, Dart  
- Provider / Riverpod  
- Camera plugin  
- HTTP + WebSocket  
- Architecture modulaire MVVM

## Client lourd (web)
- **Angular**, TypeScript  
- Services + Components  
- WebSocket + HTTP  
- Hérite du projet LOG2990

## Serveur
- **NestJS**, Node.js  
- MongoDB  
- WebSocket Gateway  
- DTO + validation

---

# 🚀 Exécution du projet

## Serveur
```bash
cd server
npm install
npm start
```
## 🖥️ Client lourd (Angular)
```bash
cd client
npm install
npm start
```
## 📱 Client léger (Flutter / Android)
```bash
cd mobile
flutter pub get
flutter run
```
