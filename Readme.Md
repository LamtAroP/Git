# 📌 Collaboration avec Git & GitHub

## 1. Contexte du projet

Le projet QueueManager existe en local et a déjà atteint un certain niveau de développement.  
Afin d’améliorer la collaboration, le suivi des modifications et la qualité du code, il a été décidé de migrer le projet vers **GitHub** et d’adopter un **mode de travail collaboratif basé sur Git**.

Git est utilisé pour la gestion des versions, tandis que GitHub sert de plateforme centrale pour :
- le partage du code,
- la collaboration entre développeurs,
- la revue de code,
- le suivi des évolutions et des corrections.

---

## 2. Prérequis

Avant de commencer, chacun doit :
- Avoir **Git installé** sur sa machine
- Disposer d’un **compte GitHub**
- Avoir configuré son identité Git :

```bash
git config --global user.name "Votre Nom"
git config --global user.email "votre.email@example.com"
```

## 3. Initialisation du projet sur GitHub
### 3.1 Lier le projet local au dépôt GitHub

```bash
git init
git add .
git commit -m "Initial commit : ajout du projet existant"
git branch -M main
git remote add origin https://github.com/organisation/nom-du-projet.git
git push -u origin main
```

## 4. Organisation du travail en équipe
### 4.1 Principe général
- La branche **main** contient le code stable
- Chaque nouvelle fonctionnalité ou correction se fait dans une **branche dédiée**
- Aucun commit direct sur **main**


## 5. Workflow de collaboration
### 5.1 Récupérer le projet
```bash
git clone https://github.com/AroaPartners/QUEUEMANAGER.git
cd nom-du-projet
```
### 5.2 Créer une branche de travail
```bash
git switch -c nom_de_la_personne_concerné/nom-de-la-fonctionnalite
```
- Exemple : git switch -c lamine/create-notifacation ou  git switch -c gael/update-notifacation

### 5.3 Travailler et enregistrer ses modifications
```bash
git status
git add . ou git add nom_fichier1 nom_fichier2 ...... nom_fichierx
git commit -m "Ajout de la fonctionnalité X"
```

Bonnes pratiques :
- Faire des commits petits et cohérents
- Utiliser des messages clairs et explicites

### 5.4 Envoyer son travail sur GitHub
```bash
git push origin -u nom_de_la_personne_concerné/nom-de-la-fonctionnalite
```

## 6. Pull Request (PR)
Une fois le travail terminé :
### 1. Ouvrir une Pull Request sur GitHub
### 2. Décrire clairement :
- l'objectif de la modification
- les changements effectués

### 3. Attendre la revue et la validation
Aucune modification n’est fusionnée sans validation.

## 7. Mise à jour du projet local

```bash
Avant de commencer une nouvelle tâche :
git switch main
git pull origin main
```
### 8.1 Résolution des conflits
- Lire attentivement les fichiers concernés
- Corriger manuellement les parties conflictuelles
- Valider la résolution avec un commit
