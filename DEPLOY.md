# 🚀 Guide de Déploiement Rapide

Guide étape par étape pour déployer votre portfolio en production avec CI/CD.

## 📦 Préparation du projet

### 1. Initialiser Git (si pas déjà fait)

```bash
cd C:\Users\beddi\portfolio
git init
git add .
git commit -m "Initial commit - Portfolio with CI/CD"
```

### 2. Créer un repository sur GitHub

1. Allez sur [github.com](https://github.com)
2. Cliquez sur **"New repository"**
3. Nommez-le (ex: `portfolio`)
4. Choisissez **Public** ou **Private**
5. Ne cochez PAS "Add README" (vous en avez déjà un)
6. Cliquez sur **"Create repository"**

### 3. Connecter le projet local à GitHub

```bash
git branch -M main
git remote add origin https://github.com/VOTRE-USERNAME/VOTRE-REPO.git
git push -u origin main
```

**Remplacez `VOTRE-USERNAME` et `VOTRE-REPO` par vos informations.**

---

## 🌐 Option 1 : GitHub Pages (Recommandé pour débuter)

### Avantages
- ✅ Gratuit et illimité
- ✅ Déploiement automatique via GitHub Actions
- ✅ Intégration native avec GitHub
- ✅ URL : `https://username.github.io/repo-name`

### Étapes

1. **Votre code est déjà sur GitHub** (étape ci-dessus)

2. **Activer GitHub Pages** :
   - Allez sur votre repository GitHub
   - **Settings** → **Pages** (dans le menu de gauche)
   - Sous **Source** : Sélectionnez **"GitHub Actions"**
   - Sauvegardez

3. **Déploiement automatique** :
   - Le workflow `.github/workflows/deploy.yml` sera utilisé automatiquement
   - À chaque `git push`, le site sera déployé automatiquement
   - Votre site sera disponible en 1-2 minutes

4. **Accéder à votre site** :
   ```
   https://VOTRE-USERNAME.github.io/VOTRE-REPO
   ```

---

## 🌐 Option 2 : Netlify (Recommandé pour facilité)

### Avantages
- ✅ Très simple à utiliser
- ✅ Déploiement automatique depuis Git
- ✅ Prévisualisation des pull requests
- ✅ URL personnalisée gratuite

### Étapes

#### Méthode A : Via l'interface web (le plus simple)

1. **Connecter GitHub à Netlify** :
   - Allez sur [netlify.com](https://www.netlify.com)
   - Connectez-vous avec votre compte GitHub

2. **Créer un nouveau site** :
   - Cliquez sur **"New site from Git"**
   - Sélectionnez **GitHub**
   - Autorisez Netlify à accéder à vos repositories

3. **Choisir le repository** :
   - Sélectionnez votre repository `portfolio`
   - Netlify détectera automatiquement `netlify.toml`

4. **Déployer** :
   - Cliquez sur **"Deploy site"**
   - Votre site sera disponible en quelques secondes
   - URL : `https://random-name.netlify.app`

#### Méthode B : Via CLI

```bash
# Installer Netlify CLI
npm install -g netlify-cli

# Se connecter
netlify login

# Déployer
cd C:\Users\beddi\portfolio
netlify deploy --prod
```

### Configuration automatique

Le fichier `netlify.toml` configure automatiquement :
- ✅ Headers de sécurité
- ✅ Cache optimisé
- ✅ Redirections

---

## 🌐 Option 3 : Vercel (Recommandé pour performance)

### Avantages
- ✅ Performance optimale
- ✅ Déploiement automatique depuis Git
- ✅ Prévisualisation des commits
- ✅ URL personnalisée gratuite

### Étapes

#### Méthode A : Via l'interface web

1. **Connecter GitHub à Vercel** :
   - Allez sur [vercel.com](https://vercel.com)
   - Connectez-vous avec votre compte GitHub

2. **Importer le projet** :
   - Cliquez sur **"New Project"**
   - Sélectionnez votre repository `portfolio`
   - Vercel détectera automatiquement `vercel.json`

3. **Déployer** :
   - Cliquez sur **"Deploy"**
   - Votre site sera disponible en quelques secondes
   - URL : `https://portfolio-random.vercel.app`

#### Méthode B : Via CLI

```bash
# Installer Vercel CLI
npm install -g vercel

# Déployer
cd C:\Users\beddi\portfolio
vercel --prod
```

---

## 🔄 Déploiement Continu (CI/CD)

Une fois configuré, chaque modification sera déployée automatiquement :

### Workflow automatique

```bash
# 1. Modifier vos fichiers
# 2. Commiter les changements
git add .
git commit -m "Description des changements"

# 3. Pousser vers GitHub
git push

# 4. Le déploiement se fait automatiquement ! 🎉
```

### Vérifier le statut

- **GitHub Pages** : Allez dans **Actions** de votre repository
- **Netlify** : Allez dans **Deploys** de votre dashboard
- **Vercel** : Allez dans **Deployments** de votre dashboard

---

## 📝 Checklist de déploiement

- [ ] Repository Git créé et configuré
- [ ] Code poussé sur GitHub
- [ ] GitHub Pages activé OU Netlify/Vercel connecté
- [ ] Premier déploiement réussi
- [ ] Site accessible via l'URL fournie
- [ ] Modifications testées et déployées automatiquement

---

## 🛠️ Commandes utiles

### Git

```bash
# Voir l'état
git status

# Ajouter tous les fichiers
git add .

# Commiter
git commit -m "Votre message"

# Pousser vers GitHub
git push

# Voir l'historique
git log
```

### Développement local

```bash
# Démarrer un serveur local
python -m http.server 8000
# Ou
npm start
```

---

## ❓ Problèmes courants

### Le déploiement ne fonctionne pas

1. Vérifiez que tous les fichiers sont committés
2. Vérifiez les logs dans GitHub Actions / Netlify / Vercel
3. Vérifiez que les fichiers de config sont bien présents :
   - `.github/workflows/deploy.yml` (pour GitHub Pages)
   - `netlify.toml` (pour Netlify)
   - `vercel.json` (pour Vercel)

### Le site ne s'affiche pas correctement

1. Vérifiez que tous les fichiers (HTML, CSS, JS) sont présents
2. Vérifiez la console du navigateur pour les erreurs
3. Vérifiez que les chemins des fichiers sont corrects

### URL personnalisée

- **GitHub Pages** : `https://username.github.io/repo-name`
- **Netlify** : Changez le nom dans les paramètres du site
- **Vercel** : Ajoutez un domaine personnalisé dans les paramètres

---

## 🎉 C'est fait !

Votre portfolio est maintenant en ligne avec un déploiement automatique à chaque modification !

Pour toute question, consultez le [README.md](README.md) principal.