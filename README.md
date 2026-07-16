# TONNANO — Boston (site statique)

## Fichiers inclus
- `index.html` → la page unique du site (tout le code HTML/CSS/JS est dedans)
- `images/` → les 8 photos utilisées par le site (hero, produits)

Aucun autre fichier n'est nécessaire. Pas de `package.json`, pas de build, pas de dépendances — c'est du HTML/CSS/JS pur, donc Vercel le sert directement.

## Déployer sur Vercel — 2 méthodes

### Méthode 1 — Sans code, via l'interface Vercel (le plus simple)
1. Va sur https://vercel.com et connecte-toi (ou crée un compte).
2. Clique sur **"Add New" → "Project"**.
3. Choisis l'option **"Deploy without Git"** / glisse-dépose directement le dossier `tonnano-boston` (celui qui contient `index.html` et `images/`) dans la zone d'upload.
4. Vercel détecte automatiquement que c'est un site statique.
5. Clique sur **Deploy**. En quelques secondes, tu obtiens une URL du type `tonnano-boston.vercel.app`.

### Méthode 2 — Avec Git (recommandé si tu veux gérer les mises à jour facilement)
1. Crée un nouveau repo (GitHub, GitLab ou Bitbucket) et mets-y le contenu de ce dossier (`index.html` + `images/`) à la racine.
2. Sur Vercel : **"Add New" → "Project"** → connecte le repo.
3. Aucun "Build Command" ni "Output Directory" à configurer — laisse les champs vides ou par défaut, Vercel sert `index.html` tel quel.
4. Clique **Deploy**.
5. Chaque fois que tu push une modification sur le repo, Vercel redéploie automatiquement.

## Nom de domaine personnalisé
Une fois déployé, dans **Project Settings → Domains**, tu peux relier un nom de domaine (ex: `tonnano.com` ou `boston.tonnano.com`) si tu en as un.

## Important
- Ne renomme pas le dossier `images/` ni les fichiers à l'intérieur — le code HTML pointe vers ces chemins exacts (`images/hero.jpg`, etc.).
- Si tu remplaces les photos par tes vraies photos produit, garde exactement les mêmes noms de fichiers, ou remplace les chemins correspondants dans `index.html`.
