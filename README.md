# Domaine Aubert — Site vitrine & boutique

Site web d'un domaine viticole fictif de Bourgogne (Meursault), transmis de père en fille
sur trois générations. Prototype interactif haute-fidélité : page d'accueil avec hero vidéo,
histoire du domaine, boutique avec panier et tunnel de commande, espace contact et espace
d'administration.

**Réalisation : B-Conseil.**

---

## ✨ Fonctionnalités

- **Le Domaine (accueil)** — hero vidéo ralentie ; le nom du domaine et le blason apparaissent
  en fondu en fin de séquence, sélection de cuvées, chiffres clés.
- **Notre Histoire** — hero plein cadre, frise chronologique animée au défilement, citation.
- **Les Vins (boutique)** — filtres par type, présentation éditoriale des 8 cuvées,
  **panier** fonctionnel, **fiche de dégustation** en pop-up, **tunnel de commande**
  (récapitulatif → livraison → simulation de paiement → confirmation).
- **Contact** — formulaire avec mention RGPD, coordonnées, carte Google Maps.
- **Espace Admin** — connexion (démo), tableau de bord avec KPIs, statuts colorés
  (stock vert/jaune/rouge, commandes vert/bleu), et **gestion de la boutique** :
  ajout / modification / masquage / suppression de produits avec upload d'image,
  répercuté en direct sur la boutique.

Entièrement **responsive** (mobile, tablette, desktop — portrait & paysage).

---

## 🗂 Structure du projet

```
.
├── Domaine Aubert.dc.html   # Le site (page unique, navigation interne)
├── support.js               # Runtime nécessaire au rendu (à conserver à côté du .html)
├── uploads/                 # Vidéo, photos des bouteilles, logo, portraits
└── README.md
```

> Le fichier `Domaine Aubert.dc.html` et `support.js` doivent rester dans le **même dossier**,
> et le dossier `uploads/` doit être présent à côté.

---

## 🚀 Lancer le site

### En local
Servez le dossier avec un petit serveur statique (les `import` ES modules exigent `http://`,
un double-clic `file://` ne suffit pas) :

```bash
# Python
python3 -m http.server 8000
# puis ouvrez http://localhost:8000/Domaine%20Aubert.dc.html
```

```bash
# ou Node
npx serve .
```

### Sur GitHub Pages
1. Poussez le dépôt sur GitHub.
2. Settings → Pages → Source : branche `main`, dossier `/root`.
3. Accédez à `https://<utilisateur>.github.io/<repo>/Domaine%20Aubert.dc.html`.

---

## 🔑 Accès à l'espace admin

Menu **Espace Admin** → la fenêtre de connexion est **pré-remplie en mode démo**
(identifiant `camille`). Cliquez sur **Se connecter**.

---

## ⚠️ Notes

- La vidéo du hero est servie depuis Cloudinary (connexion internet requise pour l'accueil).
- Les commandes et le paiement sont **simulés** (aucune transaction réelle).
- Domaine, cuvées et personnes sont **fictifs**.

L'abus d'alcool est dangereux pour la santé. À consommer avec modération.
