# Introduction au web design

- Personne ne va sur Internet

  - schema client | serveur et technologies liées
  - technologies front-end (navigateur)
  - technologies back-end (serveur, bases de données, API)

*Exercices: DNS et traceroute*

- Web vs Native

  - avantages native
  - avantages web

- Internet entre contenus et interactivité

  - tous les sites de contenus ont des éléments interactifs (recherche, compte utilisateur, etc)
  - tous les sites intaractifs ou applicatifs ont des élements de contenus

*Exercice: évaluer divers sites*

- Internet un medium fluide

 - Première inconnue: le canevas
 - Deuxième inconnue: les capacités (techniques) du navigateur et du terminal
 - Troisième inconnue: le contexte (humain) d’utilisation

Pour résoudre ces inconnues, on part des contenus (content first) et des contraintes maximales (mobile first et progessive enhancement)

## 1. Technologies web front-end: HTML/CSS/JS

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

## 2. Typographie

90% d'un site web ou d'une application c'est du texte. Commençons par là. Peut-on utiliser toutes les polices de caractères online. La réponse est "non, mais cela va mieux qu'auparavant" où l'on ne disposait que des fontes disponibles sur l'ordinateur du client. Il fallait travailler avec seulement quelques fontes et offrir à l'ordianteur client une série limitée d'options possibles. Aujourd'hui, il est possible de demander au navigateur client de télécharger un ou plusieurs fichiers de police précis et de les utiliser pour faire le rendu de la page ou de la vue.

*Excercice: différence entre un font-stack avec polices clientes et avec polices téléchargées @font-face*

- problème technique (hinting / linting)
- problème de license
- solutions les services de distribution de fontes (Google Fonts, Typekit, FontDeck)

*Exercice: Google Font*

### Choisir une ou plusiseures polices

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

@TODO

## 4. Layout: Grilles et outils CSS

@TODO

## 5. Transitions et Animations

@TODO
