# Chimie quiz

**→ [chimie.pirstone.com](https://chimie.pirstone.com)**

Quiz pour apprendre le tableau périodique des éléments : retrouve le **symbole** et le **nom français** des 118 éléments.

Tout tient dans un seul fichier, `index.html`, sans serveur ni dépendance : il s'ouvre directement dans un navigateur et se publie tel quel sur GitHub Pages.

## Principe

- Au départ, chaque case n'affiche que son numéro atomique, sur un fond teinté selon sa famille.
- Clique une case : elle s'agrandit au centre de l'écran. Saisis le symbole et le nom, les deux sont nécessaires.
- L'ampoule révèle le nom lettre par lettre. Il n'y a pas d'indice pour le symbole.
- Une fois trouvé, l'élément affiche son symbole et son nom. « Élément suivant → » (ou Entrée) passe au numéro suivant.
- Le score et la légende des familles sont au-dessus des métaux de transition. Survoler une famille fait ressortir ses éléments.

Saisie tolérante : accents, majuscules et petites fautes de frappe sont acceptés pour le nom (sauf si la faute donne le nom d'un autre élément). Les majuscules sont ignorées pour le symbole. Variantes acceptées : Lutétium, Tennessine, Wolfram.

La progression est enregistrée dans le navigateur (`localStorage`), propre à chaque appareil et à chaque adresse du site.

## Familles et couleurs

L'IUPAC n'impose pas de couleurs : le tableau suit la classification usuelle par familles (métaux alcalins, alcalino-terreux, de transition, métaux pauvres, métalloïdes, non-métaux, halogènes, gaz nobles, lanthanides, actinides, et propriétés inconnues pour les éléments 109 à 118). L'astate est classé parmi les halogènes.

Les données (numéro, symbole, nom, famille, variantes) sont dans la constante `RAW` au début du script de `index.html`.

## Mise en ligne sur GitHub Pages

1. Pousse le dépôt sur GitHub.
2. Dans **Settings → Pages**, choisis **Deploy from a branch**, branche `main`, dossier `/ (root)`.
3. Le site est disponible après une ou deux minutes sur **https://chimie.pirstone.com**.

- `CNAME` contient le domaine personnalisé. Côté DNS, un enregistrement `CNAME` fait pointer `chimie.pirstone.com` vers `pirstone.github.io`.
- `.nojekyll` indique à GitHub Pages de servir les fichiers tels quels, sans passer par Jekyll.
