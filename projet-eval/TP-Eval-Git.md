# TP Git - Évaluation

**Formation BTS/Licence - CI/CD (Docker / Git)**  
**Durée** : 10 minutes  
**Date** : 05 février 2026

---

## Objectifs

Ce TP vise à évaluer vos compétences sur :
- La manipulation d'un dépôt Git local avec les commandes fondamentales
- La gestion des branches et la fusion avec git merge

---

## Partie 1 : Commandes Git de base et commits (5 minutes)

### Objectif
Manipuler un dépôt Git local avec les commandes fondamentales

### Consignes

Réalisez les opérations suivantes dans l'ordre :

1. **Configurez** votre identité Git avec votre nom et email
```bash
git config --global user.name "Aijing LI"
git config --global user.email renoxevans@gmail.com
```

2. **Créez** un nouveau dossier `projet-eval` et **initialisez** un dépôt Git
```bash
mkdir projet-eval
git init
```

3. **Créez** trois fichiers : `index.html`, `style.css`, et `README.md`
```bash
touch index.html style.css README.md
```

4. **Ajoutez** uniquement `index.html` au staging
```bash
git add index.html
```

5. **Créez** un commit avec le message "feat: Ajoute index.html"
```bash
git commit -m "feat: Ajoute index.html"
```

6. **Modifiez** le fichier `index.html` en ajoutant une ligne de code
```bash
cat >> index.html
<!DOCTYPE html>
```

7. **Ajoutez** tous les fichiers restants (y compris le `index.html` modifié) au staging
```bash
git add *
```

8. **Créez** un second commit avec le message "feat: Ajoute style.css et README"
```bash
git commit -m "feat: Ajoute style.css et README" 
```

9. **Affichez** l'historique des commits en mode condensé
```bash
git log --oneline
```


### Barème : 5 points

- Configuration identité (`git config`) : **0.5 pt**
- Initialisation dépôt (`git init`) : **0.5 pt**
- Ajout sélectif au staging (`git add`) : **1 pt**
- Premier commit correct : **0.5 pt**
- Modification et ajout de tous les fichiers : **1 pt**
- Second commit correct : **1 pt**
- Affichage historique (`git log --oneline`) : **0.5 pt**

---

## Partie 2 : Branches et fusion (5 minutes)

### Objectif
Créer des branches, effectuer des commits et fusionner avec merge

### Consignes

Réalisez les opérations suivantes dans l'ordre :

1. **Créez** une branche nommée `feature/ajout-script`

2. **Basculez** vers cette nouvelle branche
```bash
# pour 1 & 2 :
git checkout -b feature/ajout-script
```

3. **Créez** un fichier `script.js` contenant le texte "console.log('Hello Git');"
```bash
touch script.js
cat >> script.js
console.log('Hello Git');     
```

4. **Ajoutez** et **committez** ce fichier avec le message "feat: Ajoute script.js"
```bash
git add *
git commit -m "feat: Ajoute script.js"
```

5. **Revenez** sur la branche `main`
```bash
git checkout main
```

6. **Créez** un fichier `config.json` sur la branche `main`

7. **Ajoutez** et **committez** ce fichier avec le message "feat: Ajoute config.json"
```bash
git add *
git commit -m "feat: Ajoute config.json" 
```

9. **Fusionnez** la branche `feature/ajout-script` dans `main`
```bash
git merge feature/ajout-script 
```

11. **Affichez** l'historique graphique avec `git log --oneline --graph --all`
```

```


12. **Listez** toutes les branches existantes
```
git branch -a
git branch --remote
```

```
main
feature/ajout-script
```

### Barème : 5 points

- Création de la branche : **0.5 pt**
- Basculement vers la branche : **0.5 pt**
- Commit sur `feature/ajout-script` : **1 pt**
- Retour sur `main` et commit : **1 pt**
- Fusion : **1.5 pt**
- Affichage historique graphique : **0.5 pt**

---

## Note finale

**Total** : 10 points

---

## Consignes générales

- Vous travaillez **individuellement**
- Vous pouvez consulter vos notes de cours
- Testez vos commandes pour vous assurer qu'elles fonctionnent
- Notez toutes les commandes que vous exécutez
- Utilisez `git status` régulièrement pour vérifier l'état de votre dépôt

**Bon courage !**

---