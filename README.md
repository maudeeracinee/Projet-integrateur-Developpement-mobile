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
Avec des aperçues visuelles

## Menu principal
![Screenshot](/demo-images/C8.png)

## ⚔️ Modes de jeu
- Mode Classique
- Mode Capture-the-Flag
- Filtre par mode de jeu, nombre de joueurs, alphabétique
![Screenshot](/demo-images/C3.png)

## ⚙️ Options de jeux
- Élimination rapide
- Drop in drop out
- Prix d’entrée
- Amis seulement
![Screenshot](/demo-images/C4.png)

## 🎮 Jeu
### Rejoindre une partie
![Screenshot](/demo-images/C16.png)
### Création de personnage
![Screenshot](/demo-images/C11.png)
### Salle d'attente
![Screenshot](/demo-images/C12.png)
### Partie
![Screenshot](/demo-images/C13.png)
### Fin de partie
![Screenshot](/demo-images/C14.png)

## 👁️ Mode Observateur
- Rejoindre une partie sans interagir
- Icône “œil” pour distinguer les spectateurs
- Chat disponible
![Screenshot](/demo-images/C10.png)

## 🎯 Défis de partie
- Gains de monnaie virtuelle suite a la complétion d'un défi lors d'une partie

5 défis implémentés :
1. Bouger 25 % des cases  
2. Infliger 5 dommages  
3. Ne perdre aucune vie  
4. Ouvrir 2 portes  
5. Collecter 2 objets

## 🗨️ Clavardage intégré et canaux de discussion
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

## 🫂 Système d’amis
- Ajout / suppression d’amis
- Recherche d’utilisateurs
![Screenshot](/demo-images/C7.png)

## 📩 Invitations en temps réel
- Un joueur peut inviter ses amis connectés
- Pop-up d’invitation avec "Accepter" / "Refuser"
![Screenshot](/demo-images/C9.png)

## 🌐 Statut des amis
- Affichage du statut des amis dans le chat, la liste d’amis et le compte
- Statut possible:
   🟢 En ligne
   🟠 En jeu 
   ⚪ Hors ligne

## 🛒 Boutique virtuelle
- Dépenses
- Possibilité d'acheter: des personnages, des photos de profil (avatars), des bannières et des musiques d'ambiance
![Screenshot](/demo-images/C5.png)

## 🎨 Personnalisation de l’application
- Thème visuel (clair / sombre)
- Persistant localement
![Screenshot](/demo-images/C6.png)

## ⭐ Système de niveau
- Gagner 5 parties et augmenter d'un niveau
- Niveau affiché dans la salle d’attente, la liste d’amis et le profil
![Screenshot](/demo-images/C15.png)
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

# 🚀 Exécution et génération des exécutables
## Serveur
Dans le cadre du projet LOG3900, le serveur était déployé via GitLab CI/CD et hébergé sur AWS.  
Cette version GitHub n’est pas connectée à AWS ; le serveur doit donc être exécuté localement.
### ▶️ Exécution (mode développement)
```bash
cd server
npm install
npm start
```
Le serveur roule ensuite sur :
```bash
http://localhost:3000
```
### 📦 Exécutable (mode release)
Aucun déploiement infonuagique n’est inclus dans cette version GitHub.
Le serveur peut toutefois être déployé sur AWS, Render, Railway, etc. en configurant :
- un fichier .env
- la connexion MongoDB
- un service Node.js
## 🖥️ Client lourd (Angular)
Le client lourd s’exécute localement via Angular et est accessible à l’adresse http://localhost:4200.
### ▶️ Exécution (mode développement)
```bash
cd client
npm install
npm start
```
### 📦 Exécutable (mode release)
Pour générer l’exécutable desktop :
```bash
npm run start:electron
```
L’exécutable sera produit dans le dossier de build configuré (ex.: dist/, out/).
## 📱 Client léger (Flutter / Android)
Pour pouvoir l’exécuter en mode développement ou tester l’APK généré en mode release,  
vous devez disposer d’un **émulateur Android** ou d’un **appareil Android réel**.
### ▶️ Exécution (mode développement)
```bash
cd mobile
flutter pub get
flutter run
```
### 📦 Exécutable (mode release)
Pour générer le fichier APK final :
```bash
flutter build apk --release
```
L’APK se retrouve ici :
```bash
mobile/build/app/outputs/flutter-apk/app-release.apk
```
