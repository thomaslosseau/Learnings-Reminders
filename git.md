# 🧾 Antisèche Git — Commandes indispensables

---

## 📌 1. Initialiser et configurer

Créer un dépôt Git dans un dossier :
git init

Cloner un dépôt :
git clone URL_DU_DEPOT

---

## 📌 2. Gestion des fichiers

Voir l’état du dépôt :
git status

Ajouter un fichier :
git add fichier.txt

Ajouter un dossier :
git add nom_du_dossier/

Ajouter tous les fichiers non ignorés :
git add .

Enlever un fichier du suivi (sans le supprimer du disque) :
git rm --cached fichier.txt

---

## 📌 3. Commit

Créer un commit :
git commit -m "Message clair"

Modifier le dernier commit (message ou contenu) :
git commit --amend

---

## 📌 4. Récupérer & envoyer (pull / push)

Récupérer les dernières modifications :
git pull

Récupérer depuis une branche précise :
git pull origin main

Envoyer les commits vers la branche distante :
git push

Envoyer vers une branche précise :
git push origin nom_branche

---

## 📌 5. Branches (voir, créer, changer, supprimer)

Voir les branches locales :
git branch

Voir toutes les branches (locales + distantes) :
git branch -a

Créer une nouvelle branche :
git branch nom_branche

Créer puis se déplacer dessus :
git checkout -b nom_branche

Changer de branche :
git checkout nom_branche

Fusionner une branche dans la branche actuelle :
git merge nom_branche

Supprimer une branche locale :
git branch -d nom_branche

Supprimer une branche distante :
git push origin --delete nom_branche

---

## 📌 6. Historique / logs

Voir l’historique complet :
git log

Version simplifiée (graphique) :
git log --oneline --graph --all

---

## 📌 7. Annulation / Reset

Annuler les modifications d’un fichier (avant add) :
git checkout -- fichier.txt

Retirer un fichier du staging (avant commit) :
git reset fichier.txt

Revenir au commit précédent (sans perdre les fichiers) :
git reset --soft HEAD~1

---

## 📌 8. .gitignore

Exemple de contenu :
node_modules/
*.log
*.tmp
config.local.json

---

## 📌 9. Remote (GitHub, GitLab…)

Voir les remotes :
git remote -v

Ajouter un remote :
git remote add origin URL

Modifier l’URL du remote :
git remote set-url origin nouvelle_URL

---