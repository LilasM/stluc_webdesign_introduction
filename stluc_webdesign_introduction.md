# Introduction au web design

## Comment cela fontionne ?

- Personne ne va sur Internet

*Exercices: DNS et traceroute*

  - schema client | serveur et technologies liées
  - technologies front-end (navigateur)
  - technologies back-end (serveur, bases de données, API)

Nous nous concentrerons sur les technologies front-end

- HTML: Utilise des balises et des attributs pour définir la structure et la sémantique du document. Fontionne par emboitement hiérarchisé (DOM). C'est le premier document qui chargé par le navigateurs et qui appelle la plupart des fichiers externes.
- CSS: Utilise des sélecteurs, des propriéts et des valeurs pour définir la mise ne page du document et les styles graphiques des divers éléments. Fontionne par cascade, spécificité et poids.
- JS: Est un language de programmation permettant de scripter le navigateur pour créer des interactions complexes et d'utiliser les API du navigateurs ou des API externes.

*Exercice: inspecter le code d'une page web et montrer les divers types de code*
*Exercice: faire un premier projet web avec un fichier HTML, un fichier CSS, un fichier JS*
*Exercice: partir à la découverte de MDN*

Une page web lie également vers de nombreux fichiers externes

- polices
- images
- videos
- scripts
- fontes

*Exercice, voir l'onglet "network" dans Google Chrome.*

## 1. The web grain

Intro et article de Frank Chimero

### Web vs Native
### Internet entre contenus et interactivité
### Design for the unknown

- Première inconnue: le canevas
- Deuxième inconnue: les capacités du navigateur et du terminal
- Troisième inconnue: le contexte (humain) d’utilisation

### Grand principes du design web

Les principales différences entre le design web et le design print ou audiovisuel viennent de ces inconnes et de la nécessité d'y répondre

- content first, mobile first, responsive pour répondre à l'inconnue du canevas
- progressive enhancement pour répondre à l'inconnue des capacités du navigateur et du terminal
- user centered design et itérations pour répondre à l'inconnue du contexte d'utilisation

## 2. Typographie

90% d'un site web ou d'une application c'est du texte. Commençons par là. Peut-on utiliser toutes les polices de caractères online. La réponse est "non, mais cela va mieux qu'auparavant" où l'on ne disposait que des fontes disponibles sur l'ordinateur du client. Il fallait travailler avec seulement quelques fontes et offrir à l'ordianteur client une série limitée d'options possibles. Aujourd'hui, il est possible de demander au navigateur client de télécharger un ou plusieurs fichiers de police précis et de les utiliser pour faire le rendu de la page ou de la vue.

*Excercice: différence entre un font-stack avec polices clientes et avec polices téléchargées @font-face*

- problème technique (hinting / linting)
- problème de license
- solutions les services de distribution de fontes (Google Fonts, Typekit, FontDeck)

*Exercice: Google Font*

### Choisir une ou plusieures polices

Limiter sses choix. On travaille en général avec une ou deux polices maximum et quelques variantes de graisse. Tout à un coût en terme de téléchargement.

*Exercice: Google Font et poids*

- super families
- polices du même designer
- polices ayant des caractéristiques communes

### Outils typographiques disponibles

- familles: serifs, sans-serifs, display, etc.
- graisses: black, bold, medium, etc.
- taille: pixels, rem, em, etc.
- casse: uppercase, lowercase, etc.
- styles: normal, italique
- ornements: glyphs, ligatures, etc.
- spacing: line spacing, letter spacing
- couleurs: noir, rouge, grid, etc.
- espace: interligne, letter spacing, rythme vertical

*Exercice: chercher chacun une composition typographique sur Dribble et expliquer*
*Exercice: utiliser la typographie et Google fonts pour designer les divers éléments d'un blogpost et des paroles d'un track de hip-hop, d'abord dans Figma et puis dans le code*

### Le futur de la typographie sur le web

- variable fonts
- glyphs et ligatures

## 3. Media: Images, Icones, Video et Sons

### Icones

- SVG est le standard

### Images

- Images de contenus
  - Images fluides (CSS)
  - Images responsives (performance)
- Images de background
- Filtres CSS
- Filtres et masques SVG

### Videos

- Videos HTML5
- Services comme Youtube et Vimeo
- Videos fluides
- API video

## 4. Layout: Grilles et outils CSS

- Grilles fluides simples (10, 12, etc)
- Grilles fluides proportionnelles (golden ratio)
- Flexbox
- Grid Layout
- Responsive design et flexbox
- Responsive design et CSS Grid

## 5. Transitions et Animations

- Transitions CSS
- Animations CSS avec changelents de classes
- Animations Javascript
- Animations au scroll
