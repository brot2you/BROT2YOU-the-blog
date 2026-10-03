# BROT2YOU, le blog d'un prof d'anglais (et pas que !)

Blog présentant les applications BROT2YOU et bien plus. Un seul fichier (`index.html`, images incluses), sans dépendance, publié avec GitHub Pages.

## Mettre le site en ligne

1. Sur GitHub, crée un nouveau dépôt public nommé `articles` dans le compte `brot2you`.
2. Dépose les fichiers `index.html`, `README.md` et `.nojekyll` (bouton « Add file », puis « Upload files »).
3. Va dans « Settings », puis « Pages ». Dans « Branch », choisis `main` et le dossier `/ (root)`, puis « Save ».
4. Après une à deux minutes, le site est en ligne à l'adresse : https://brot2you.github.io/articles/

Le fichier `.nojekyll` commence par un point : sur Mac et Windows il peut être masqué. S'il n'apparaît pas, crée-le directement sur GitHub (« Add file », puis « Create new file », nom `.nojekyll`, contenu vide).

## Ajouter un article

1. Ouvre `index.html` sur GitHub et clique sur le crayon pour le modifier.
2. Repère le bloc `<script type="application/json" id="articles">`.
3. Copie un article entier, de `{` à `}`, et colle-le juste après le `[` d'ouverture, suivi d'une virgule.
4. Modifie les champs :
   - `id` : court, sans espace ni accent, par exemple `phonix`. Il devient l'adresse de l'article : `.../articles/#/phonix`.
   - `date` : au format `AAAA-MM-JJ`. Les articles sont triés du plus récent au plus ancien.
   - `rubrique` : `apps` (Mes apps & outils numériques), `classe` (Classe & pédagogie, qui regroupe aussi les conseils et les réflexions), `ia` (IA en classe), `ressources` (Ressources à télécharger), `liens` (Liens utiles) ou `culture` (English & Culture).
   - `appNom` et `appUrl` : le nom et l'adresse de l'application, ou `""` pour un article sans appli (voyage, réflexion…).
   - `tutoUrl` : l'adresse d'un tuto, ou `""` s'il n'y en a pas.
   - `liens` : des boutons de téléchargement ou de liens, affichés à la fin de l'article. Exemple : `[{"texte": "Fiche élève (PDF)", "url": "ressources/fiche.pdf"}, {"texte": "BBC Learning English", "url": "https://www.bbc.co.uk/learningenglish"}]`. Pour un fichier à télécharger, dépose-le dans un dossier `ressources` du dépôt et indique son chemin : le bouton le télécharge directement. Laisse `[]` ou supprime la ligne s'il n'y en a pas.
   - `icone` : l'icône kawaii de l'appli. Sept icônes sont intégrées : `"arbre"`, `"cible"`, `"gomme"`, `"cerveau"`, `"dojo"`, `"loupe"` et `"livre"`. Pour une autre appli, dépose une image carrée dans un dossier `images` du dépôt et indique son chemin (par exemple `"images/phonix.png"`). Laisse `""` pour afficher la vignette de la rubrique.
   - `public` : un ou plusieurs choix parmi `"Élèves"`, `"Collègues"`, `"Familles"`, ou `[]`.
   - `resume` : une ou deux phrases affichées sur la page d'accueil.
   - `contenu` : un paragraphe par ligne, entre guillemets, séparés par des virgules. Une ligne qui commence par `## ` devient un intertitre. `**texte**` met en gras, `[texte](https://...)` crée un lien.
5. Clique sur « Commit changes ». Le site se met à jour en une à deux minutes.

Si la page affiche un message d'erreur de format, vérifie les virgules entre les blocs (aucune après le dernier) et qu'aucun guillemet droit `"` n'apparaît à l'intérieur d'un texte : utilise plutôt les guillemets français « ».

## Ajouter un tuto

Chaque appli peut avoir son tuto, affiché dans le blog avec la même mise en page que les articles, un bouton « Imprimer le tuto » et son propre lien à partager (par exemple https://brot2you.github.io/articles/#/tuto/cognicoach).

1. Dans `index.html`, repère les blocs `<script type="text/markdown" id="tuto-…">`.
2. Copie un bloc entier, de `<script` à `</script>`, et colle-le juste après le dernier.
3. Remplace l'id par `tuto-` suivi de l'id de l'article (par exemple `tuto-phonix` pour l'article `phonix`).
4. Écris le tuto en Markdown simple : `## Intertitre`, `### Sous-titre`, listes `1.` ou `-` (trois espaces devant pour une sous-liste), tableaux avec des barres `|`, `**gras**`, `` `code` ``, `[lien](https://...)`.

Dès que le bloc existe, un bouton jaune « 📘 Tuto » apparaît sur la carte de l'article et à la fin de l'article. Le texte du tuto ne doit simplement pas contenir `</script>`.

## Réglages

Le bloc `<script type="application/json" id="reglages">` contient le titre, l'auteur et les liens de la barre d'icônes : `hubUrl` (page de toutes tes apps), `email`, `instagram`, `youtube` et `x`. Chaque lien laissé vide (`""`) est masqué ; dès que tu le remplis, son icône apparaît.

## Rubriques

Les six vignettes sous la bannière servent de filtres. Un article encore classé avec une ancienne rubrique (`outils`, `conseils`, `reflexions`) est rangé automatiquement dans la nouvelle. Une pastille rouge indique le nombre d'articles de chaque rubrique ; une rubrique vide affiche un message invitant à voir tous les articles.

## Partager un article

Chaque article a sa propre adresse (par exemple https://brot2you.github.io/articles/#/mind-the-mistake). Le bouton « Copier le lien de l'article » la copie directement.
