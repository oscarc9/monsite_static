# Conversion du site PHP vers HTML statique pour GitHub Pages

## Changements effectués

### 1. Fichiers convertis
- ✅ `acceuil.php` → `index.html` (page d'accueil, renommée selon les conventions GitHub Pages)
- ✅ `Produits.php` → `Produits.html`
- ✅ `logiciel.php` → `Logiciel.html`
- ✅ `contact.php` → `contact.html`
- ✅ `connexion.php` → `connexion.html`
- ✅ `login.php` → `login.html`
- ✅ `panier.php` → `panier.html`
- ✅ `micro.php` → `micro.html`
- ✅ `souris.php` → `souris.html`
- ✅ `x60.php` → `x60.html`

### 2. Liens mis à jour
Tous les liens internes ont été mis à jour pour pointer vers les fichiers .html :
- `acceuil.php` → `index.html`
- `Produits.php` → `Produits.html`
- `logiciel.php` → `Logiciel.html`
- `contact.php` → `contact.html`
- `connexion.php` → `connexion.html`
- `login.php` → `login.html`
- `panier.php` → `panier.html`
- `micro.php` → `micro.html`
- `souris.php` → `souris.html`
- `x60.php` → `x60.html`

### 3. Fonctionnalités remplacées

#### Système de panier
- **Avant** : Base de données PHP + sessions
- **Après** : LocalStorage JavaScript
- Fonctionnalités : Ajout/suppression/modification des quantités

#### Formulaires
- **Avant** : Traitement PHP côté serveur
- **Après** : Validation JavaScript côté client
- **Connexion** : Simulation avec redirection
- **Inscription** : Validation des mots de passe + simulation
- **Contact** : Validation + message de confirmation

#### Navigation
- Tous les liens de navigation mis à jour
- Header cohérent sur toutes les pages
- Navigation responsive préservée

### 4. Fichiers conservés
- Tous les fichiers CSS (`*.css`)
- Toutes les images (`*.png`, `*.jpg`, `*.svg`)
- Vidéo (`*.mp4`)
- Fichiers de configuration CSS

### 5. Fonctionnalités supprimées (incompatibles avec GitHub Pages)
- Base de données PHP
- Sessions PHP
- Traitement de formulaires côté serveur
- Fichiers de connexion PDO
- Scripts PHP de traitement du panier

## Instructions pour l'hébergement GitHub Pages

### 1. Création du repository
```bash
# Créer un nouveau repository sur GitHub
# Nommer le repository : votre-nom-utilisateur.github.io
# Ou utiliser un nom personnalisé
```

### 2. Upload des fichiers
```bash
git init
git add .
git commit -m "Conversion du site PHP vers HTML statique"
git remote add origin https://github.com/votre-nom/votre-repository.git
git push -u origin main
```

### 3. Configuration GitHub Pages
1. Aller dans Settings → Pages
2. Source : Deploy from a branch
3. Branch : main
4. Folder : / (root)
5. Save

### 4. Accès au site
- URL : `https://votre-nom-utilisateur.github.io/nom-du-repository/`
- Ou : `https://votre-nom-utilisateur.github.io/` (si le repository s'appelle `votre-nom-utilisateur.github.io`)

## Notes importantes

### Limitations
- Pas de traitement côté serveur (pas de PHP)
- Pas de base de données
- Formulaires en mode "simulation"
- Panier non persistant entre sessions

### Avantages
- Hébergement gratuit sur GitHub Pages
- Site rapide et responsive
- Toutes les fonctionnalités visuelles préservées
- Navigation fluide
- Compatible avec tous les navigateurs modernes

### Améliorations possibles
- Intégration avec un service tiers pour les formulaires (Formspree, Netlify Forms)
- Utilisation d'un CMS headless pour le contenu dynamique
- Intégration avec un service de panier tiers (Snipcart, etc.)

## Structure finale des fichiers

```
monsite/
├── index.html              # Page d'accueil (ex-acceuil.php)
├── Produits.html            # Page produits
├── Logiciel.html            # Page logiciel
├── contact.html             # Page contact
├── connexion.html           # Page connexion
├── login.html               # Page inscription
├── panier.html              # Page panier
├── micro.html               # Page produit micro
├── souris.html              # Page produit souris
├── x60.html                 # Page produit x60
├── *.css                    # Fichiers de style
├── *.png, *.jpg, *.svg      # Images
├── *.mp4                    # Vidéos
└── README.md                # Cette documentation
```

Le site est maintenant prêt à être hébergé sur GitHub Pages ! 