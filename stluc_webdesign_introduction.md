# Introduction au web design

## Comment fonctionne Internet ?

"Aller sur Internet" la phrase est courante mais ne peut pas être plus dénuée de sens. Personne ne va nulle part. Lorsque vous lancez votre navigateur et vous tapez une URL ou que vous suivez un lien, vous envoyez une requête vers un serveur web qui, comme le nom l'indique, va "servir" à votre navigateur les fichiers composant le site ou l'application que vous cherchez à utiliser.

Il y a un certain nombre de ces serveurs ... comment votre requête va-t-elle être dirigée vers le bon et ce depuis n'importe où dans le monde ? C'est le rôle d'un autre type de serveur dédié au routing: les serveurs DNS (Domain Name Server). Ces serveurs DNS vont transcrire le domaine de votre requête en une adresse IP numérique et former une chaîne pour trouver le serveur web ayant l'adresse IP correspondante et lui transmettre votre requête. Chaque machine connectée à Internet possède une adresse IP unique.

Une fois la connection établie entre le serveur web et vous, les serveurs DNS ont joué leur rôle, jusqu'à ce que vous fassiez une autre requête vers un autre nom de domaine.

*Exercices: nslookup et traceroute / tracert*

"Aller sur Internet" c'est finalement envoyer, via votre navigateur, une requête vers un serveur web qui va vous renvoyer des fichiers HTML, CSS, JS ainsi que des assets (images, fontes, videos, etc.) que votre navigateur va lire et interpréter pour composer la page que vous voyez et avec laquelle vous pouvez interagir. Il ya donc un client (votre navigateur et la machine sur laquelle il tourne) et un serveur (le serveur web qui vous sert les fichiers) qui peut également être connecté à une base de données.

Nous nous concentrerons essentiellement ici sur les technologies **front-end**, c'est à dire celles qui sont utilisées par votre navigateur. Il s'agit principalement de HTML, CSS, et Javascript. Chacune de ces technologies est suffisamment complexe que pour que certains frameworks facilitant la vie des développeurs aient été construites en plus (Sass, Less, Vue, React, Angular, Ember, etc.).

Le monde du **back-end** est celui de la logique qui se produit côté serveur et qui sert essentiellement à fournir des données au site ou à l'application que vous utilisez. Ces données sont fournies par une base de données ou par des API (Application Programming Interface). Les technologies du back-end sont des langages de programmation comme Ruby, PHP, Python, Go, Node et des frameworks qui y sont liés (Rails, YII, Laravel, Django, etc.).

N'oublions pas non plus l'infrastructure: les bases de données (MySQL, PostGresSQL, MongoDB, etc.), les serveurs web eux-mêmes comme Apache, NginX ou encore UNIX et Linux, les OS sur lesquels tournent la plupart d'entre eux.

## Technologies front-end

Comme dit plus haut les technologies front-end sont principalement au nombre de trois: HTML, CSS et Javascript. Chacune de ces technologies est passée par de multiples évolutions et évolue constamment encore aujourd'hui.

Ces technologies sont disponibles pour tous et sont des standards ouverts à l'élaboration desquels participent des académiques, des chercheurs mais aussi des représentants des principaux acteurs d'Internet comme les Sociétés conceptrices des divers navigateurs.

### HTML: structure et sémantique

HTML (Hypertext Markup language) est la language de markup du web qui défini la structure et la sémantique des éléments qui composent une vue ou un document. Grâce aux balises et aux attributs c'est lui qui indique la langue du document, le set de caractères (alphabet) utilisé et qui défini quel texte est un titre, un paragraphe, une liste, etc. C'est le premier document qui chargé par le navigateurs et qui lie et affiche les fichiers externes tels que les images, les icônes, les vidéos, les sons, etc. C'est également les fichiers HTML qui définissent quels feuilles de styles CSS et fichiers Javascript doivent être utilisés.

HTML est un langage déclaratif de markup qui fonctionne par emboitement hiérarchisé (DOM) un peu comme des Matrioshka Russes. Outre la balise `<html>`, la balise `<head>` referme les meta-informations sur un document ou la vue (langue, charset, titre, CSS liée(s), etc.), tandis que la balise `<body>` renferme les contenus du document ou de la vue.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Minimal HTML document</title>
  </head>
  <body>
    <p>Hello <a href="https://home.cern/topics/birth-web">World Wide Web</a></p>
  </body>
</html>
```

La balise la plus importante du HTML est sans conteste la balise de lien `<a>` qui, grâce à son attribut `href` permet de lier entre eux des fichiers HTML soit appartenant au même domaine, soit de domaines complètement différents.

*Exercice: visualiser la structure en emboitement d'un document HTML online*
*Exercice: créer un premier document HTML*
*Exercice: créer un second document HTML, lier les documents entre eux avec des balises `<a>`, établir un lien externe vers un autre site*

Si le sujet vous intéresse, [Mozilla Developer Network (MDN) possède un très bon guide en français](https://developer.mozilla.org/fr/docs/Web/HTML) qui vous permettra de débuter avec HTML.

### CSS: mise en page et styles graphiques

CSS (Cascading Style Sheets) est le language de mise en page du web et défini les styles graphiques des divers éléments qui composent une vue ou un document. CSS  utilise des sélecteurs (pour sélectionner les éléments du DOM auxquels appliquer les styles) ainsi que des propriétés et des valeurs pour définir les styles à appliquer aux éléments ou aux divers types de conteneurs ou boites dans lequels ils se trouvent.

CSS est un langage déclaratif qui fonctionne selons les principes de cascade, de spécificité et de poids pour déterminer quels styles s'appliquent à quels éléments.

```css
body {
  background-color: #ff0000;
}
```

ou

```css
.navigation {
  list-style: none;
  margin: 0;
  padding: 0;

  display: flex;
  flex-direction: row;
  justify-content: flex-end;
  align-items: center;
  flex-wrap: nowrap;
}
```

*Exercice: créer un premier fichier CSS et le lier au document HTML*
*Exercice: sélécteurs de type et de classe comme sélecteurs les plus courants*
*Exercice: expérimenter avec cascade, spécificité et poids*

Si le sujet vous intéresse, [Mozilla Developer Network (MDN) possède un très bon guide en français](https://developer.mozilla.org/fr/docs/Web/CSS) qui vous permettra de débuter avec CSS.

### Javascript: scripting, interactivité et programmation

Javascript est le language de programmation côté client permettant de scripter le navigateur pour créer des interactions complexes et pour utiliser les API du navigateurs ou des API externes. Au départ un langage de scripting, l'évolution actuelle de Javascript tend de plus en plus vers un langage de programmation à part entière qui peut aujourd'hui également être utilisé côté serveur (Node).

De nombreux sites ou applications ont également porté une grande partie de la logique vers le côté client. C'est particulioèrement vrai pour tout ce qui est single page applications (SPA) qui sont devenues très populaires. Ces dernières font usage de frameworks JavaScript (React, Vue, Ember, Angular, etc.) permettant de gérer les différents états d'une application et d'avoir des composants qui y répondent.

```js
window.addEventLister("load", function() {
  alert("Hello Javascript");
});
```

*Exercice: inspecter le code d'une page web et montrer les divers types de code*
*Exercice: faire un premier projet web avec un fichier HTML, un fichier CSS, un fichier JS*

Si le sujet vous intéresse, [Mozilla Developer Network (MDN) possède un très bon guide en français](https://developer.mozilla.org/fr/docs/Web/JavaScript) qui vous permettra de débuter avec JavaScript.

### Assets et fichiers externes

En plus du code HTML, CSS et JavaScript, votre navigateur reçoit également bon nombre de fichers externes tels que des images, des videos, des fichiers sons, des fichiers de polices, etc.

Ces fichiers ne sont pas contenus dans le code HTML, CSS ou JavaScript mais sont appellés comme des fichiers pour êtres intégrés à ou utilisé dans le rendu de la vue ou de la page.

*Exercice, voir l'onglet "network" dans Google Chrome.*

### Images

Commençons par les images. Sur le web, les formats les plus utilisés sont:

- JPG: utilisé pour les images de type photographique, pas de transparence, lossy
- GIF: utilisé pour les images avec aplats de couleurs, transparence simple, animations frame by frame, lossy. GIF est un format de moins en moins utilisé depuis l'avènement de PNG et de SVG
- PNG: utilisé pour les images avec aplats de couleurs, transparence simple et transparence d'alpha, lossy.
- SVG: format vectoriel, est une sorte de mini-document qui peut être scripté et manipulé par CSS lorsqu'il est intégré au document (inline), lossless.
- WEBP: format encore en dévelopement mais qui permet d'avoir des fichiers moins lourds et d'utiliser des algorythmes de compression lossless et lossy.

Une fois ces éléments intégrés à un document HTML, CSS et JavaScript peuvent être utilisé pour en définir les styles graphiques et/ou pour les manipuler.

```html
<img src="img/rainbow.jpg" alt="Rainbow over my house">
```

Voici comment intégrer une image avec une légende

```html
<figure>
  <img src="img/rainbow.jpg" alt="Rainbow over my house">
  <figcaption>
    <p>A lovely rainbow over my house on a Saturday morning</p>
  </figcaption>
</figure>
```

*Exercice: intégrer une image à un document HTML*

### Videos

Tous les navigateurs web ne supportent pas les mêmes formats video. Pour être certain de pouvoir être vues par l'ensemble des navigateurs modernes, votre video doit donc être disponibles en plusieurs formats. Actuellement MP4 et WEBM sont suffisants.

Les videos peuvent très facilement être intégrées à vos documents HTML. Une fois ces videos intégrées, CSS et JavaScript peuvent être utilisé pour en définir les styles graphiques et/ou pour les manipuler.

```html
<video width="800" height="600" controls>
  <source src="assets/videos/myvideo.mp4" type="video/mp4">
  <source src="assets/videos/myvideo.webm" type="video/webm">
  <p>Sorry, your browser doesn't support embedded videos. Download the video in <a href="video/myvideo.mp4">MPEG</a> or <a href="video/myvideo.webm">WEBM</a>.</p>
</video>
```

*Exercice: intégrer une vidéo à un document HTML*

### Fontes

Initialement, il n'était possible que de travailler à l'aide des polices installées sur l'ordinateur client. Toutes les polices n'étant pas disponibles partout, les développeurs utilisaient un "font-stack", une liste de polices spécifiant la police souhaitée ainsi que des alternatives au cas ou cette dernière n'est pas disponible.

```css
body {
  font-family: "Helvetica Neue", "Helvetica", "Arial", sans-serif;
}
```

ou

```css
@font-face {
  font-family: "Open Sans";
  src: url("../fonts/OpenSans-Regular-webfont.woff2") format("woff2"),
       url("../fonts/OpenSans-Regular-webfont.woff") format("woff");
  font-weight: 400;
  font-style: normal;
}

@font-face {
  font-family: "Open Sans";
  src: url("../fonts/OpenSans-Bold-webfont.woff2") format("woff2"),
       url("../fonts/OpenSans-Bold-webfont.woff") format("woff");
  font-weight: 600;
  font-style: normal;
}

body {
  font-family: "Open Sans", "Helvetica Neue", "Helvetica", "Arial", sans-serif;
}
```

Aujourd'hui il est possible de charger des fichiers de polices et de demander au navigateur de les utiliser pour le rendu. Les problématiques sont maintenant d'ordre technique (hinting, optimisation) et au niveau des licences (les fichiers de polices pouvant être facilement téléchargés, ils sont ipossible à protéger). C'est pour répondre à ce deux problèmes que des services de distribution de polices (Typekit, Google fonts, Fontdeck) ont été créés.

*Exercice: intégrer une police custom à un projet HTML/CSS*

## Design Web: spécificités du medium

Le design print est un domaine qui a déjà derrière lui des centaines d'années d'existence et qui à intégré un série de règles, de canons et de bonnes pratiques qui, pour la plupart, prennent pour base le canevas sur lequel on travaille et les possibilités techniques au niveau de l'impression. Il est en général facile d'avoir une bonne idée du contexte dans lequel le produit va être utilisé et ous sommes façe à un médium qui est statique.

Bref, avec le print, nous sommes dans un envrionnement de design statique et dont les paramètres sont connus et maîtrisés de bout en bout. Le designer contrôle parfaitement tous les aspects de son projet.

Il en va tout autrement pour le web et le digital en général, comme l'explique fort bien John Allsopp dans son article "[A Dao of Web Design](https://alistapart.com/article/dao)":

  The control which designers know in the print medium, and often desire in the web medium, is simply a function of the limitation of the printed page. We should embrace the fact that the web doesn’t have the same constraints, and design for this flexibility. But first, we must “accept the ebb and flow of things”.

  "[A Dao of Web Design](https://alistapart.com/article/dao)" - John Allsopp, 2000

Accepter la flexibilité du medium se traduit par une impossibilité de tout contrôler. En tant que designer, il nous faut se réconcilier avec les inconnues inhérentes au web et les apprivoiser, les intégrer dans notre travail. Depuis les débuts du web, les designers digitaux ont du réinventer leur métier et mettre en place des outils, workflows et stratégies pour aborder un medium qui lie contenus et interactivité dans un contexte fluide où les iconnues sont nombreuses.

### Entre contenus et interactivité

Comme avec le print, le design digital vise à présenter des contenus de nature diverses mais éjoute une diemnsion d'interactivité, au niveau des types de contenus (son, videos, animations, etc) comme au niveau des objectifs (acheter un billet d'avion, faire une réservation, etc.). Bref, le design digital est un continuum entre contenus et interactivité. Chaque site ou application est par essence un mélange des deux, dans des proportion diverses.

- Site de presse: site axé sur les conetnus et donc vers la trasmission d'information (articles, recettes, opinions, etc). Certains aspects applicatifs sont néanmoins présents et visent à faire accomplir des tâches aux utilisateurs: moteur de recherche, abonnement, espace membres, etc.
- Site bancaire: site axé sur l'applicatif et donc la réalisation de tâches (transferts, téléchargement de documents). certains aspects de contenus et de transmission d'information sont présents également: conditions générales, présentation des formules de prêts, consultation des soldes, etc.

Ces deux aspects sont tujours présents dans un site web et doivent tous deux être pris en compte à divers niveaux:

- Stratégie: quels sont les objectifs en termes de transission d'information / d'accomplissement de tâches?
- Contenus: quels contenus doivent être mis en place? Quels types de contenus vont au mieux servir les objectifs du site (blogposts, tutoriax, videos, etc.)? Quelles sont les ressources disponible pour publier et à quelle fréquence?
- Interactivité: quelles interactions avec le site doivent être créées? Comment les rendre visibles et attractive pour les utilisateurs? Quelles ressources sont disponible pour le support et les tests utilisateurs?
- Structure: quelle va être l'architecture d'information? Quelles seront les structures de données des contenus,? Quels sont les flux utilisateurs, les diverses étapes dans la réalisation de chaque tâche et comment les structurer pour que chaque étape soit simple et pour le que nombre d'étapes soit le plus bas possible?
- Présentation: comment la présentation va-t-elle soutenir les autres dimensions

### Design for the unknown

#### Première inconnue: le canevas

En print, le format, le support, le canevas du produit fini est connu. Il s’agit d’une affiche de telle dimensions, d’une brochure en format A5 de 20 pages, etc.). Il en va tout autrement sur le web où le concept même de canevas sur lequel baser un design disparait devant la diversité des supports sur lesquels les sites et appolications doivent fonctionner: tailles, résolutions et orientations d’écrans.

Si nous ne pouvons plus baser nos design sur le canevas, nous devons alors [partir des contenus](https://markboulton.co.uk/journal/a-richer-canvas) pour designer non plus des pages mais bien des [systèmes de composants flexibles](http://styleguides.io/) pouvant s’agencer de diverses façons pour occuper et s’adapter à un maximum de canevas possibles.

*Exercice: spotify en téléphone, tablette, desktop*

#### Deuxième inconnue: les capacités du navigateur et du terminal

En print, une fois un design créé, son rendu est contrôlable et contrôlé de bout en bout: de la conception jusqu’à l’impression finale.

En web, tout passe par deux canaux que le concepteur ne contrôle pas: le navigateur et le terminal sur lequel celui-ci est hébergé et dont vont largement dépendre l'expérience utilisateur. Là aussi, nous avons affaire à une large diversité et à une échelle de capacités très importante: capacités tactiles, bande passante, support images, support vidéos, support CSS, support javascript, gyroscope, appareil photo, géolocalisation, etc.

Lorsque nous envisageons des solution de design, nous devons tenir compte de cette seconde inconnue. Dans l’industrie, on se réfère souvent au concept de "[progresssive enhancement](https://resilientwebdesign.com/chapter6/)" selon lequel on va d’abord se concentrer sur le fait de délivrer une bonne expérience utilisateur de base, que l’on va enrichir pour les navigateurs et terminaux disposant de capacités plus avancées.

*Discussion: [Do websites need to look exactly the same in every browser](http://dowebsitesneedtolookexactlythesameineverybrowser.com/)*

#### Troisième inconnue: le contexte (humain) d’utilisation

Si nous pouvons en général définir assez précisément nos publics cibles (à travers des études de marché, des personas, etc.), le contexte d’utilisation de notre site ou application peut varier grandement et nous est la plupart du temps complètement inconnu.

L’utilisateur mobile peut utiliser son téléphone debout dans son train matinal, être facilement distrait, ne disposer que d’une seule main et d’une connectivité faible. Ce même utilisateur mobile peut utiliser sa tablette, confortablement installé dans le canapé du lobby de son hôtel. Il est dans ce cas très concentré et dispose d’une connexion à haut débit. Les circonstances et le contexte d’utilisation est tout aussi divers pour un utilisateur d’ordinateur fixe.

La solution est ici de toujours center les solutions sur l'utilisateur. Typiquement les projets web impliquent les utilisaturs très tôt dans la définition des solutions envisagées et passent par des cycles d'itérations relativement courts dans lesquels les feedbacks utilisateurs et les tests sont extrèmement important. Un aspect intéressant du medium Internet étant la capacité d'avoir très rapidement des retours (analytics, interviews utilisateurs, tests, etc.).

### Grands principes du design web

Les principales différences entre le design web et le design print ou audiovisuel viennent de ces inconnues et de la nécessité d'y répondre.

#### Mobile first responsive web design

Afin de répondre à la diversité croisssante des tailles d'écrans et des résolutions existant sur le marché, un des grands principes est de commencer à designer pour les contraintes maximales, celles des petits écrans de smartphones et des bandes passantes limitées. C'est le principe du "[mobile first](https://www.lukew.com/ff/entry.asp?933)" qui a des implications tant en termes de performance que de mise en page.

Une fois que votre site ou votre application web fonctionne pour ces derniers, vous pouvez petit à petit passer aux écrans de taille moyenne et puis aux écrans plus larges et aux débits de connections pus stables et plus puissantes. L'idée centrale du "Responsive Web Design" lancée par Ethan Marcotte est celle d'un continuum tout au long duqel votre design "répond" à l'espace utile disponible et à la résolution de l'écran.

Les trois pières angulaires du responsive sont:

- grilles fluides: d'une grille simple à une ou deux colonnes sur petits écrans, on peut passer à une grille de plus en plus complexe au fur et à mesure que l'espace disponible augmente. Les nouvelles spécifications de layout en CSS (Flexbox et Grid) sont sous tendures par cette approche.
- media flexibles: pour s'intégrer à une grille fluides, vos media (images, video, etc.) doivent être flexible et non de taille fixe. Grâce à quelques règles CSS, il est possible d'adapter la taille de vos media aux containers dans lesquels ils se trouvent.
- media queries: le mécanisme CSS grâce auquel le code CSS (layout, typographie, etc) est capable de "répondre" à une grande palettes de paramètres du navigateur client (largeur d'écran, orientation, couleurs, etc.)

Ces principes sont aplliqués au niveau macro (layout global) mais également au niveau micro (celui des composants). Si le layout de votre page réagit à l'espace disponible à l'écran, il en va de même pour une navigation, un footer ou encore à un composant "news" dans un site de presse.

Les media fluides ont également des implications au niveau de la performance. Cela ne sert à rien de charger une image de 1000 pixels de large sur un écran qui en fait 320, même chose pour les videos. Un standard a été développé pour les images responsives avec `srcset`, `sizes` et la balise `<picture>` si des images différentes sont nécessaires pour des raisons de direction artistique. En ce qui concerne les videos, des services tels que Youtube ou Vimeo restent la meilleure option au niveau de la performance. Ces services vont transcoder votre video dans divers formats ainsi que dans différentes résolutions, ce qui vous garantira une compatibilité et des performances maximales.

*Exercice: inspecter quelques sites et applications responsives [Stripe](https://stripe.com/), [Opera de Paris](https://www.operadeparis.fr/), [AirBnB](https://www.airbnb.com/), [Google Drive](https://drive.google.com/)). Prêter attention à la typographie, aux grilles, aux interfaces de navigation, aux images et aux videos*

#### Progressive enhancement

L'idée du progressive enjancement est similaire à celle du Responsive Web Design mais dans le domaine des capacités du navigateur et du terminal. Selon Jeremy Keith dans "[Resilient Web Design](https://resilientwebdesign.com/chapter6/)", cette idée repose sur trois étapes simples:

- Identifier les contenus ou les fonctionalités principaux / essentiels
- Rendre disponibles ces contenus ou ces fonctionalités à l'aide des technologies les plus silmples possibles
- Construire sur cette base en utilisant les technologies plus modernes

Cette philosophie permet de toujours disposer des fonctionnalités ou des contenus essentiels au minimum et de passer ensuite du temps à construire des experiences plus raffinées et abouties sur une fondation solide. Le principe du "Prograssive Enhancement" permet donc de répondre à l'inconnue des capacités du navigateur et du terminal client.

Cette manière de développer et de designer a depuis toujours été mise en pratique au niveau des sites orientés vers les contenus et la transmission d'information. Avec l'avènement des "[Progressive Web Apps](https://developers.google.com/web/progressive-web-apps/)" (PWA) chères à Google, cette idée fait son chemin au niveau des projets plus applicatifs.

#### User centered design et Design Thinking

Cette méthodologie consiste à se centrer sur les utilisateurs d'un site ou d'une application et leurs besoins tout au long d'un processus de design itératif. A travers des techniques de recherche investigatives (interviews, sondages, shadowing, etc.) et génératives (brainstormings, exercices de groupes, etc.), l'idée est d'en savoir le plus possible sur les utilisateurs, leurs besoins et le contexte d'utilisation du site ou de la'application. De cette phase de recherche on extrait les prérequis et les objectifs du produit, pour ensuite proposer les solutions possibles que l'on va tester avec les utilisateurs pour voir si les objectifs sont remplis.

L'inconnue des contextes d'utilisation couplée aux ressources, budgets et délais importants nécessaires pour créer un site ou une application web font qu'il vaut mieux savoir où l'on va. Toutes les methodologies liées au User Centered Design et au Design Thinking (Lean UX, Design Sprint, etc.) permettent de tester rapidement ses concepts et prototypes auprès d'utilisateurs réels.

Depuis quelques années, [Thoughtbot](https://thoughtbot.com/) et [Google Ventures](http://www.gv.com/sprint/) ont popularisé un outil: le Design Sprint. L'idée est de passer en 5 jours seulement d'un simple concept à un prototype concret et testé par des utilisateurs.

- jour 1: comprendre les utilisateurs, leurs besoins et leurs contextes (côté utilisateurs) ainsi que le les objectifs à atteindre et les KPIs (côté business). Identifier aussi les risques potentiels et les moyens de les réduire
- jour 2: diverger en proposant (sketch et pitch) différentes solutions possibles aux problèmes posés
- jour 3: converger en se mettant d'accord sur une ou deux solutions à prototyper
- jour 4: prototyper les solutions en ayant un degré de fidélité juste suffisant que pour pouvoir réaliser les tests utilisateurs
- jour 5: tester le(s) prototype(s) avec des utilisateurs et évaluer

Si vous souhaitez en savoir plus concernant le design sprint, [le petit guide online de Thoughtbot](https://thoughtbot.com/product-design-sprint/guide) est très bien fait et vous donne quelques examples d'activités ou d'exercices à réaliser avec vos clients.

Cette méthodologie forme également une bonne base si vous n'avez qu'un u deux jours à passer sur la phase de recherche avec vos clients.

## Design web en pratique

Après avoir introduit le sujet par un peu de théorie, passons à la pratique. La suite de ce cours essaye d'être un petit guide pratique pour réaliser efficacement des designs pour le web, qu'il s'agisse d'un site ou d'une application. Voici le plan de bataille.

1. Recherche et stratégie
2. Couleurs et palette
3. Typographie
4. Media (Images et Illustrations, icones, videos, sons, etc.)
5. Layout et mise en page
6. Transitions et animations
7. Livrables pour le design web

## 1. Recherche et stratégie

- publics cibles
- Besoins et aubjectifs
- competitive audit
- contenus et structure de données
- Design brief
- concepts

## 2. Couleurs

- couleurs principales, couleurs secondaires, couleurs neutres
- créer une palette à partir d'une photo / de la nature
- créer une palette à partir des règles de la color wheel
- ne jamais utiliser de noir
- outils pratiques: layers blend
- outils pratiques: adobe colors ou colors

## 3. Typographie

Comme le dit fort justement Oliver Reichenstein, [le texte compose 95% d'un site web ou d'une application](https://ia.net/topics/the-web-is-all-about-typography-period). La typographie est donc une étape importante dans la conception de tout produit digital. Comme nous l'avons vu plus haut, nous disposons maintenant avec `@font-face` et les services de distribution de fontes tels que Google Fonts ou Typekit d'une grande variété de polices.

Se pose donc la question du choix des fonts à utiliser pour un projet donné. Comment faire un choix pertinent ?

### Choisir une ou plusieurs polices

Pour commencer, il est important de poser des limtes. Les fichiers de polices sont des ressources externe et charger une police, une graisse ou un style supplémanetaire ajoutera au poinds de vos pages. En
général on travaillera donc avec une ou deux polices maximum et un nombre limité de variantes en terme de graisses et de styles.

*Exercice: Google Font et poids des fichiers de police*

Votre premier choix devra sans doute être la police que vous utiliserez pour votre corps de texte. Il vous faut une police solide et de lisible qui permettra aux autres éléments textuels importants (titres, calls to action) de ressortir. Préférez des polices avec une x-height élevée et peu de fioritures. Soyez également attentif à ce que la police choisie possède plusieurs graisses et variantes (au moins bold et italique). Les polices avec plusieurs graisses sont intéressantes de par la variété potentielle qu'elles proposent.

Si vous vous posez des questions, regardez simplment dans quel but ou contexte la police que vous considérez a été dévelopée, explorez son histoire. Des services tels que Typekit ou Google fonts vous donnerons des reseignements précieux. Ces services possèdent également des spécimens qui vous permettrons de mieux appréhender les caractéristiques des divers fontes proposées. Allez également faire un petit tour du côté des sites tels que [Typewolf](https://www.typewolf.com/) ou

- se renseigner sur l'oirigine de la fonte
- super families
- polices du même designer / fondrie
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

## 4. Media: Images, Icônes, Video et Sons

### Icônes

- SVG est le standard
- Avantages de SVG: styling avec CSS et animations

### Images et illustrations

- Images de contenus
  - Images fluides (CSS)
  - Images responsives (performance)
- Images de background
- Filtres CSS
- Filtres et masques SVG

### Videos

- Videos HTML5
- Services: Youtube et Vimeo
- Videos fluides
- API video

## 5. Layout: Grilles et outils CSS

- Grilles fluides simples (10, 12, etc)
- Grilles fluides proportionnelles (golden ratio)
- Flexbox
- Grid Layout
- Responsive design et flexbox
- Responsive design et CSS Grid

## 6. Transitions et Animations

- Transitions CSS
- Animations CSS
- Animations Javascript (GSAP / Greensock)
- Animations au scroll
- Data visualisation

## 7. Design web: document de delivery

- Style tiles
- Styles guides
- Components library
