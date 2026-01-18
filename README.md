# Portfolio Professionnel

Un portfolio moderne et responsive créé avec HTML, CSS et JavaScript vanilla. Parfait pour présenter vos projets, compétences et expériences professionnelles sur le web.

## ✨ Caractéristiques

- **Design moderne** : Interface élégante avec un thème sombre professionnel
- **Responsive** : S'adapte parfaitement à tous les écrans (mobile, tablette, desktop)
- **Animations fluides** : Transitions et animations douces pour une meilleure expérience utilisateur
- **Navigation intuitive** : Menu de navigation fixe avec scroll fluide
- **Section compétences** : Barres de progression animées
- **Portfolio de projets** : Galerie de projets avec effets au survol
- **Formulaire de contact** : Formulaire prêt à être connecté à un backend
- **Optimisé** : Code propre et performant sans dépendances externes lourdes

## 📁 Structure du projet

```
portfolio/
│
├── index.html              # Page principale HTML
├── styles.css              # Fichier de styles CSS
├── script.js               # JavaScript pour interactions
├── .gitignore              # Fichiers à ignorer par Git
├── netlify.toml            # Configuration Netlify
├── vercel.json             # Configuration Vercel
├── .github/
│   └── workflows/
│       └── deploy.yml      # Workflow GitHub Actions pour CI/CD
└── README.md               # Documentation
```

## 🚀 Installation et utilisation

### Option 1 : Ouverture directe (local)

1. Téléchargez ou clonez le dossier `portfolio`
2. Ouvrez le fichier `index.html` dans votre navigateur web
3. C'est tout ! Le portfolio est prêt à être utilisé

### Option 2 : Serveur local (recommandé)

Pour éviter les problèmes CORS et tester correctement :

#### Avec Python :
```bash
cd portfolio
python -m http.server 8000
```
Puis ouvrez `http://localhost:8000` dans votre navigateur.

#### Avec Node.js (http-server) :
```bash
cd portfolio
npx http-server -p 8000
```

#### Avec PHP :
```bash
cd portfolio
php -S localhost:8000
```

## 🌐 Déploiement sur le web avec CI/CD

### 🔄 GitHub Pages avec CI/CD Automatique (Recommandé)

Le projet inclut un workflow GitHub Actions pour un déploiement automatique à chaque push.

#### Configuration initiale :

1. **Créer un repository GitHub** :
   ```bash
   git init
   git add .
   git commit -m "Initial commit - Portfolio with CI/CD"
   git branch -M main
   git remote add origin https://github.com/votre-username/votre-repo.git
   git push -u origin main
   ```

2. **Activer GitHub Pages** :
   - Allez sur GitHub → Votre repository
   - **Settings** → **Pages**
   - **Source** : Sélectionnez "GitHub Actions"
   - Le workflow `.github/workflows/deploy.yml` se chargera du reste

3. **Déploiement automatique** :
   - Chaque push sur `main` ou `master` déclenche automatiquement le déploiement
   - Votre site sera accessible à : `https://votre-username.github.io/nom-du-repo`

#### Avantages :
- ✅ Déploiement automatique à chaque modification
- ✅ Versionning de votre code
- ✅ Historique des changements
- ✅ Gratuit et illimité

### 🚀 Netlify avec CI/CD Automatique

Le fichier `netlify.toml` configure automatiquement le déploiement.

#### Méthode 1 : Via l'interface web

1. Allez sur [netlify.com](https://www.netlify.com) et connectez-vous
2. Cliquez sur **"New site from Git"**
3. Choisissez votre repository GitHub
4. Netlify détectera automatiquement `netlify.toml`
5. Cliquez sur **"Deploy site"**

#### Méthode 2 : Drag & Drop (premier déploiement)

1. Allez sur [netlify.com](https://www.netlify.com)
2. Glissez-déposez le dossier `portfolio`
3. Votre site sera déployé avec une URL gratuite
4. Pour activer CI/CD, connectez ensuite votre repository Git

#### Méthode 3 : Via Netlify CLI

```bash
# Installation de Netlify CLI
npm install -g netlify-cli

# Connexion
netlify login

# Déploiement
cd portfolio
netlify deploy --prod
```

#### Avantages :
- ✅ Déploiement automatique depuis Git
- ✅ Prévisualisation des pull requests
- ✅ Configuration via `netlify.toml` incluse
- ✅ Headers de sécurité et cache configurés

### ⚡ Vercel avec CI/CD Automatique

Le fichier `vercel.json` est déjà configuré pour le déploiement.

#### Méthode 1 : Via l'interface web

1. Allez sur [vercel.com](https://vercel.com) et connectez-vous
2. Cliquez sur **"New Project"**
3. Importez votre repository GitHub
4. Vercel détectera automatiquement `vercel.json`
5. Cliquez sur **"Deploy"**

#### Méthode 2 : Via Vercel CLI

```bash
# Installation de Vercel CLI
npm install -g vercel

# Déploiement
cd portfolio
vercel --prod
```

#### Avantages :
- ✅ Déploiement automatique depuis Git
- ✅ Prévisualisation des commits
- ✅ Configuration via `vercel.json` incluse
- ✅ Performance optimisée

### 📋 Résumé des configurations CI/CD

| Service | Fichier de config | Déploiement auto | Prévisualisation PR |
|---------|------------------|------------------|---------------------|
| GitHub Pages | `.github/workflows/deploy.yml` | ✅ | ❌ |
| Netlify | `netlify.toml` | ✅ | ✅ |
| Vercel | `vercel.json` | ✅ | ✅ |

### Autres options

- **Firebase Hosting**
- **Surge.sh**
- **AWS S3 + CloudFront**
- **Votre propre serveur web**

## 🎨 Personnalisation

### Modifier les informations personnelles

1. **Nom et titre** : Éditez la section `<h1>` dans `index.html` (lignes ~35-40)
2. **Description** : Modifiez le texte dans la section "À propos" (`#about`)
3. **Compétences** : Ajoutez ou modifiez les compétences dans `#skills`
4. **Projets** : Remplacez les projets exemple dans `#projects`
5. **Contact** : Mettez à jour les informations de contact dans `#contact`

### Modifier les couleurs

Dans `styles.css`, modifiez les variables CSS au début du fichier :

```css
:root {
    --primary-color: #6366f1;      /* Couleur principale */
    --secondary-color: #8b5cf6;    /* Couleur secondaire */
    --dark-bg: #0f172a;            /* Arrière-plan sombre */
    --accent-color: #f59e0b;       /* Couleur d'accentuation */
}
```

### Ajouter votre photo

Remplacez le placeholder dans la section "À propos" :

```html
<div class="about-image">
    <img src="chemin/vers/votre-photo.jpg" alt="Votre nom">
</div>
```

Et ajustez le CSS si nécessaire pour la photo.

### Modifier les projets

Pour chaque projet dans `#projects`, modifiez :
- Le titre (`<h3>`)
- La description (`<p>`)
- Les technologies utilisées (`<div class="project-tags">`)
- Les liens vers le projet en direct et le code source

### Connecter le formulaire de contact

Dans `script.js`, modifiez la fonction de soumission du formulaire pour envoyer les données à votre backend :

```javascript
fetch('/api/contact', {
    method: 'POST',
    headers: {
        'Content-Type': 'application/json',
    },
    body: JSON.stringify(formData)
})
.then(response => response.json())
.then(data => {
    alert('Message envoyé avec succès!');
    contactForm.reset();
});
```

Ou utilisez un service comme :
- **Formspree** : https://formspree.io
- **EmailJS** : https://www.emailjs.com
- **Netlify Forms** : Si vous déployez sur Netlify

## 📱 Compatibilité

- ✅ Chrome (dernières versions)
- ✅ Firefox (dernières versions)
- ✅ Safari (dernières versions)
- ✅ Edge (dernières versions)
- ✅ Mobile browsers (iOS Safari, Chrome Mobile)

## 🔧 Technologies utilisées

- **HTML5** : Structure sémantique
- **CSS3** : Styles modernes avec Grid, Flexbox, animations
- **JavaScript (Vanilla)** : Interactions et animations
- **Font Awesome** : Icônes (via CDN)

## 🛠️ CI/CD et Déploiement Automatique

Le projet est configuré pour un déploiement automatique (CI/CD) :

### Workflow GitHub Actions

Le fichier `.github/workflows/deploy.yml` configure :
- Déploiement automatique sur GitHub Pages à chaque push
- Déploiement uniquement sur la branche `main` ou `master`
- Annulation des déploiements en cours lors d'un nouveau push

### Configuration Netlify

Le fichier `netlify.toml` inclut :
- Configuration de build et publication
- Headers de sécurité (X-Frame-Options, CSP, etc.)
- Cache optimisé pour les fichiers statiques
- Redirections pour le routing côté client

### Configuration Vercel

Le fichier `vercel.json` configure :
- Build et routes optimisées
- Headers de sécurité
- Cache pour les ressources statiques

### Commandes Git utiles

```bash
# Initialiser le repository
git init

# Ajouter tous les fichiers
git add .

# Créer le premier commit
git commit -m "Initial commit - Portfolio with CI/CD"

# Créer la branche main
git branch -M main

# Ajouter le remote (remplacez par votre URL)
git remote add origin https://github.com/votre-username/votre-repo.git

# Pousser vers GitHub (déclenchera le déploiement automatique)
git push -u origin main

# Pour les prochaines modifications
git add .
git commit -m "Description des changements"
git push
```

## 📝 Notes

- Le portfolio est entièrement statique et ne nécessite pas de backend
- Toutes les animations sont optimisées pour les performances
- Le code est commenté pour faciliter la personnalisation
- Compatible avec tous les navigateurs modernes

## 🤝 Support

Si vous rencontrez des problèmes ou avez des questions :
1. Vérifiez que tous les fichiers sont dans le même dossier
2. Assurez-vous que votre navigateur supporte les fonctionnalités CSS modernes
3. Vérifiez la console du navigateur pour d'éventuelles erreurs

## 📄 Licence

Ce projet est libre d'utilisation pour vos besoins personnels et professionnels.

---

**Bon développement ! 🚀**