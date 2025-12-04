# 🧾 Antisèche complète — .gitignore

## 1. Rôle
Le fichier .gitignore indique à Git quels fichiers et dossiers ne doivent pas être suivis. Cela empêche :  
- qu’ils soient ajoutés avec `git add .`  
- qu’ils soient commités  
- qu’ils soient poussés sur le dépôt distant  

Il n’agit que sur les fichiers NON suivis au moment où la règle est écrite.

---

## 2. Structure générale
Le .gitignore est un simple fichier texte contenant une liste de règles, une par ligne.

Exemples :
node_modules/  
*.log  
config.local.json

---

## 3. Commentaires
Les commentaires commencent par `#` :
# Ceci est un commentaire  
*.tmp

---

## 4. Règles de base

Ignorer un fichier précis :  
secret.txt

Ignorer un dossier :  
logs/  
dist/

Ignorer une extension :  
*.log  
*.tmp  
*.zip

Ignorer une extension dans un dossier spécifique :  
src/*.map

Ignorer plusieurs extensions :  
*.png  
*.jpg  
*.jpeg

---

## 5. Exceptions (ne pas ignorer)
On utilise `!` pour annuler une règle.

Ignorer tout sauf un fichier :  
*  
!important.txt

Ignorer un dossier sauf un fichier :  
secret/*  
!secret/readme.md

---

## 6. Règles avancées

Ignorer uniquement à la racine :  
/config.json

Ignorer un dossier peu importe où il se trouve :  
**/cache/

Ignorer uniquement les fichiers :  
*.log  
!*/  (garde les dossiers)

---

## 7. Si le .gitignore ne fonctionne pas
Cause principale : le fichier est déjà suivi par Git.

Solution :  
git rm --cached fichier  
git commit -m "Stop tracking fichier"  

Ensuite, le .gitignore agira correctement.

---

## 8. Voir ce qui est ignoré
git status --ignored

---

## 9. .gitignore global (pour tout l’ordinateur)
Définir un fichier global :  
git config --global core.excludesfile ~/.gitignore_global

Exemples utiles pour un global :  
.DS_Store  
Thumbs.db  
.vscode/  
.idea/

---

## 10. Exemples de .gitignore pratiques

### Projet Node.js
node_modules/  
dist/  
.env  
*.log

### Projet Python
__pycache__/  
*.pyc  
.env

### Projet Web
build/  
.DS_Store  
npm-debug.log  
.env

### Projet C/C++
*.o  
*.exe  
build/

---

## 11. Résumé rapide

- Commentaire : `# texte`  
- Fichier précis : fichier.ext  
- Dossier : dossier/  
- Extension : *.ext  
- Ignorer tout : *  
- Ne pas ignorer : !nom  
- Ignorer à la racine : /nom  
- Ignorer partout : **/nom/  

Fin de l’antisèche.