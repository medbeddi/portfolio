# 🚀 Guide d'Activation GitHub Pages avec GitHub Actions

## 📋 Pré-requis ✅

- ✅ Repository GitHub créé : https://github.com/medbeddi/portfolio
- ✅ Code poussé sur GitHub
- ✅ Fichier `.github/workflows/deploy.yml` présent

## 🎯 Étapes pour Activer GitHub Pages

### 1️⃣ Accéder aux Paramètres du Repository

1. Ouvrez votre navigateur
2. Allez sur : https://github.com/medbeddi/portfolio
3. Cliquez sur l'onglet **"Settings"** (en haut à droite du repository)

![Settings](https://docs.github.com/assets/cb-24932/images/help/repository/repo-actions-settings.png)

### 2️⃣ Activer GitHub Pages

1. Dans le menu de gauche, cliquez sur **"Pages"**
2. Vous verrez une section **"Build and deployment"**
3. Sous **"Source"**, cliquez sur le menu déroulant
4. **Sélectionnez "GitHub Actions"** (IMPORTANT : pas "Deploy from a branch")

![Pages Settings](https://docs.github.com/assets/cb-11243/images/help/pages/publishing-source-drop-down.png)

### 3️⃣ Sauvegarder

- Cliquez sur **"Save"** pour enregistrer

### 4️⃣ Déclencher le Workflow

Vous avez **2 options** :

#### Option A : Déclencher depuis l'interface web (recommandé)

1. Cliquez sur l'onglet **"Actions"** (en haut du repository)
2. Vous verrez le workflow **"Deploy Portfolio to GitHub Pages"**
3. Si le workflow n'a pas encore tourné, cliquez dessus
4. Cliquez sur **"Run workflow"** (bouton en haut à droite)
5. Sélectionnez la branche **"main"**
6. Cliquez sur **"Run workflow"**

#### Option B : Déclencher avec un push Git

Dans votre terminal :

```bash
cd C:\Users\beddi\portfolio
git commit --allow-empty -m "Trigger GitHub Actions deployment"
git push
```

### 5️⃣ Vérifier le Déploiement

1. Retournez dans l'onglet **"Actions"**
2. Vous verrez un workflow en cours d'exécution (orange)
3. Attendez 1-2 minutes
4. Quand c'est terminé, vous verrez une coche verte ✅

### 6️⃣ Accéder à Votre Site

Une fois le déploiement réussi :

- Allez dans **Settings** → **Pages**
- Vous verrez le message : "Your site is live at..."
- Votre URL sera : **https://medbeddi.github.io/portfolio** 🎉

---

## ✅ Vérification

Après activation, vérifiez que :

- [ ] GitHub Pages est activé (Settings → Pages → Source = "GitHub Actions")
- [ ] Le workflow est visible dans l'onglet Actions
- [ ] Le workflow s'exécute sans erreur (coche verte)
- [ ] Le site est accessible à l'URL : https://medbeddi.github.io/portfolio

---

## 🔄 Déploiement Automatique

Désormais, **chaque modification** sera automatiquement déployée :

```bash
# 1. Modifier vos fichiers
# 2. Commiter
git add .
git commit -m "Ma modification"

# 3. Pousser (déploiement automatique !)
git push
```

Le déploiement se fera automatiquement en 1-2 minutes ! 🚀

---

## ❓ Problèmes Courants

### Le workflow ne s'exécute pas

**Solution** :
- Vérifiez que GitHub Pages est bien configuré sur "GitHub Actions"
- Vérifiez que le fichier `.github/workflows/deploy.yml` existe sur la branche `main`
- Déclenchez manuellement le workflow via l'onglet Actions

### Erreur "Workflow permissions"

**Solution** :
- Le workflow a déjà les permissions nécessaires (configuré dans `deploy.yml`)
- Si nécessaire, allez dans Settings → Actions → General → Workflow permissions

### Le site n'est pas accessible

**Solution** :
- Attendez 2-3 minutes après le déploiement (il peut y avoir un délai)
- Vérifiez que le workflow est terminé avec succès (coche verte)
- Vérifiez l'URL : https://medbeddi.github.io/portfolio

---

## 📞 Liens Utiles

- **Repository** : https://github.com/medbeddi/portfolio
- **Actions** : https://github.com/medbeddi/portfolio/actions
- **Pages Settings** : https://github.com/medbeddi/portfolio/settings/pages
- **Votre site** : https://medbeddi.github.io/portfolio (une fois activé)

---

## 🎉 C'est Fait !

Une fois ces étapes terminées, votre portfolio sera en ligne avec un déploiement automatique à chaque modification !

Pour toute question, consultez la [documentation GitHub Pages](https://docs.github.com/en/pages).