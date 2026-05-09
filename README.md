# Page Actualites ENOES - Telechargement local

URL d'origine : https://enoes.com/actualites/
Telecharge le 09/05/2026 via wget.

## Structure

- `index.html` : la page Actualites complete, liens vers les CSS et assets locaux deja convertis
- `themes/enoes/css/style.css@ver=1.0.tmp.css` : **CSS principal du theme ENOES** (a retravailler)
- `plugins/contact-form-7/includes/css/styles.css@ver=6.1.4.tmp.css` : CSS Contact Form 7 (plugin)
- `plugins/cookies-and-content-security-policy/css/cookies-and-content-security-policy.min.css@ver=2.34.tmp.css` : CSS bandeau cookies
- `uploads/` : images et vignettes des articles
- `themes/enoes/css/bg_enoes.svg` : background SVG du theme

## Ouvrir localement

Double-cliquer sur `index.html` ou ouvrir avec un serveur local :

```bash
cd page-actualites
python3 -m http.server 8000
# Puis ouvrir http://localhost:8000/
```

Note : la police Google Fonts (Inter) est appelee depuis le CDN, donc internet requis pour le rendu typographique exact.

## Pour retravailler le template

Le fichier principal a editer pour le restyle est :

**`themes/enoes/css/style.css@ver=1.0.tmp.css`**

C'est la qu'on trouve les regles CSS de la grille de cards Actualites. Il contient la mise en page actuelle de la page hub.

## A faire (cf. brief slide audit UX)

Manques UX a corriger sur le template :

- Aucune introduction editoriale au-dessus du listing
- Pas de barre de recherche
- Categorisation invisible (dropdown peu engageant qui melange Actualites, Blog et Evenements)
- Aucune hierarchie visuelle (pas d'article epinglé, pas de "A la une")
- Images bannieres avec texte integre tres repetitives
- Pas d'auteur affiche sur les cards
- Pas de temps de lecture
- Pas de date de mise a jour
- Pas de tags par thematique ni filtre par typologie
- Aucun CTA contextuel vers les pages formations
- Pagination peu visible
