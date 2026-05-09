# Page Actualites ENOES - Refonte UX/SEO

Demo de refonte de la page hub Actualites ENOES (https://enoes.com/actualites/) pour l'AO datashake.

## URLs

- **Version refondue (V2)** : https://pierregaudard.github.io/enoes-actualites-v2/ (= `index.html`)
- **Version originale** : https://pierregaudard.github.io/enoes-actualites-v2/index-original.html

## Modifications appliquees

### SEO
- Title et meta description optimises avec mot-cle "expertise comptable et audit"
- Schema.org BreadcrumbList + ItemList + Article
- H1 enrichi : "Actualites et conseils sur l'expertise comptable et l'audit"
- Breadcrumb avec niveau de categorie

### UX
- Introduction editoriale contextuelle
- Barre de recherche
- Tabs categories visibles avec compteur (au lieu d'un dropdown invisible)
- Article a la une (featured) avec layout 2 colonnes
- Auteur + temps de lecture sur chaque card (injectes via JS)
- Tags thematiques par card (DCG, DSCG, DEC, alternance, audit, etc.)
- Cards en CSS Grid a hauteur egale, peu importe la longueur du texte
- Excerpts clampes a 3 lignes pour homogeneite visuelle
- Section CTA formations en bas (DCG, DSCG, DEC, BTS, Master CCA)
- Pagination amelioree avec compteur "Page X sur Y"

### Conservation
- Meme charte graphique que l'original (couleurs ENOES #15a8b4, font Inter)
- Meme CSS theme (`themes/enoes/css/style.css`)
- Aucune modification du header / footer / menu
- HTML compatible avec le CMS WordPress existant

## Structure technique

- `index.html` : page V2 refondue (par defaut)
- `index-original.html` : page actuelle d'enoes.com/actualites pour comparaison
- `themes/enoes/css/style.css@ver=1.0.tmp.css` : CSS principal du theme ENOES (inchange)
- `plugins/` : CSS plugins WordPress (Contact Form 7, bandeau cookies)
- `uploads/` : images et vignettes des articles

Les ameliorations sont injectees via :
- Une balise `<style id="enoes-actu-v2-css">` inline dans le head
- Un `<script id="enoes-actu-v2-js">` qui injecte auteur/temps/tags sur les cards au DOMContentLoaded

Aucune modification du CSS theme original n'a ete necessaire : tous les ajouts sont surcouches via classes prefixees pour eviter les conflits.

