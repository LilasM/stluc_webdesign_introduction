# Introduction au web design

## Comment fonctionne Internet ?

"Aller sur Internet" la phrase est courante mais ne peut pas être plus dénuée de sens. Personne ne va nulle part!

Lorsque vous lancez votre navigateur et vous tapez une URL ou que vous suivez un lien, vous envoyez une requête vers un serveur web qui, comme le nom l'indique, va "servir" à votre navigateur les fichiers composant le site ou l'application que vous cherchez à utiliser.

Il y a un certain nombre de ces serveurs dans le monde ... comment votre requête va-t-elle être dirigée vers le bon et ce depuis n'importe où? C'est le rôle d'un autre type de serveur dédié au routing: les serveurs DNS (Domain Name Server). Ces serveurs DNS vont transcrire le domaine de votre requête en une adresse IP numérique et former une chaîne pour trouver le serveur web ayant l'adresse IP correspondante et, finalement,  lui transmettre votre requête. Chaque machine connectée à Internet possède une adresse IP unique.

Une fois la connection établie entre le serveur web et vous, les serveurs DNS ont joué leur rôle, jusqu'à ce que vous fassiez une autre requête vers un autre nom de domaine.

*Exercices: nslookup et traceroute / tracert*

"Aller sur Internet" c'est envoyer, via votre navigateur, une requête vers un serveur web qui va vous renvoyer des fichiers HTML, CSS, JS ainsi que des assets (images, fontes, videos, etc.) que votre navigateur va lire et interpréter pour composer la page que vous voyez et avec laquelle vous pouvez interagir.

Il y a donc un client (votre navigateur et la machine sur laquelle il tourne) et un serveur (le serveur web qui vous sert les fichiers) qui peut également être connecté à une base de données.

Nous nous concentrerons essentiellement ici sur les technologies **front-end**, c'est à dire celles qui sont utilisées par votre navigateur. Il s'agit principalement de HTML, CSS, et Javascript. Chacune de ces technologies est suffisamment complexe que pour que certains frameworks aient été écrits (Sass, Less, Vue, React, Angular, Ember, etc.).

Les frameworks sont en quelque sorte des boites à outils pour les dévelopeurs, qui sont construites sur base de divers languages back-end ou front-end. Si vous voulez une analogie, c'est un peu comme disposer de Lego Technics. Ces frameworks aident les développeurs à construire rapidement des sites ou applications plus complexes.

Le monde du **back-end** est celui de la logique qui se produit côté serveur et qui sert essentiellement à fournir des données au site ou à l'application que vous utilisez. Ces données sont fournies par une base de données ou par des API (Application Programming Interface). Les technologies du back-end sont des langages de programmation comme Ruby, PHP, Python, Go, Node et les frameworks qui y sont liés (Rails, YII, Laravel, Django, etc.).

N'oublions pas non plus l'infrastructure: les bases de données (MySQL, PostGresSQL, MongoDB, etc.), les serveurs web eux-mêmes comme Apache, NginX ou encore UNIX et Linux, qui sont les OS sur lesquels tournent la plupart d'entre eux.

## Technologies front-end

Comme dit plus haut, les technologies front-end sont principalement au nombre de trois: HTML, CSS et Javascript. Chacune de ces technologies est passée par de multiples évolutions et change constamment encore aujourd'hui.

Ces technologies sont disponibles pour tous et sont des standards ouverts à l'élaboration desquels participent des académiques, des chercheurs mais aussi des représentants des principaux acteurs d'Internet comme les sociétés conceptrices des divers navigateurs. Le [W3C](https://www.w3.org/) est l'entité responsable de la conception, de l'évolution et de la publication de ces standards.

### HTML: structure et sémantique

[HTML](https://www.w3.org/standards/techs/html) (Hypertext Markup language) est la language de markup du web qui défini la structure et la sémantique des éléments qui composent une vue ou un document.

Grâce aux balises et aux attributs, c'est lui qui indique la langue du document, le set de caractères utilisé et qui défini quel texte est un titre, un paragraphe, une liste, etc. C'est le premier document qui est chargé par les navigateurs et qui lie et affiche les fichiers externes tels que les images, les icônes, les vidéos, les sons, etc.

Ce sont également les fichiers HTML qui définissent quelles feuilles de styles CSS et fichiers Javascript doivent être utilisés pour le rendu de la page ou de la vue.

HTML est un langage de markup déclaratif qui fonctionne par emboitement hiérarchisé (DOM) un peu comme des Matrioshka Russes. Outre la balise `<html>`, la balise `<head>` referme les meta-informations sur un document ou la vue (langue du document, charset, titre, CSS liée(s), etc.), tandis que la balise `<body>` renferme les contenus du document ou de la vue.

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

La balise la plus importante du HTML est sans conteste la balise de lien `<a>` qui, grâce à son attribut `href` permet de lier entre eux des fichiers HTML appartenant au même domaine, ou à des domaines complètement différents.

*Exercice: visualiser la structure en emboitement d'un document HTML online*

*Exercice: créer un premier document HTML*

*Exercice: créer un second document HTML, lier les documents entre eux avec des balises `<a>`, établir un lien externe vers un autre site*

Si le sujet vous intéresse, Mozilla Developer Network (MDN) possède [un très bon guide en français qui vous permettra de débuter avec HTML](https://developer.mozilla.org/fr/docs/Web/HTML).

### CSS: mise en page et styles graphiques

[CSS](https://www.w3.org/standards/techs/css) (Cascading Style Sheets) est le language de mise en page du web et défini les styles graphiques des divers éléments qui composent une vue ou un document. CSS  utilise des sélecteurs (pour sélectionner les éléments du DOM auxquels appliquer les styles) ainsi que des propriétés et des valeurs pour définir les styles à appliquer aux éléments ou aux divers types de conteneurs ou boites dans lequels ils se trouvent.

CSS est un langage déclaratif qui fonctionne selon les principes de [cascade](https://developer.mozilla.org/en-US/docs/Web/CSS/Cascade), de [spécificité](https://developer.mozilla.org/en-US/docs/Web/CSS/Specificity) et de poids pour déterminer quels styles s'appliquent à quels éléments.

```css
body {
  background-color: #ff0000;
}
```

ou

```css
.c-mainnav {
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

*Exercice: sélecteurs de type et de classe comme sélecteurs les plus courants*

*Exercice: expérimenter avec cascade, spécificité et poids*

Si le sujet vous intéresse, Mozilla Developer Network (MDN) possède [un très bon guide en français qui vous permettra de débuter avec CSS](https://developer.mozilla.org/fr/docs/Web/CSS).

### Javascript: scripting, interactivité et programmation

[Javascript](https://www.w3.org/standards/webdesign/script) est le language de programmation côté client permettant de scripter le navigateur pour créer des interactions complexes et utiliser les API du navigateur ou des API externes. Au départ un langage de scripting, l'évolution actuelle de Javascript tend de plus en plus vers un langage de programmation à part entière qui peut aujourd'hui également être utilisé côté serveur ([Node](https://nodejs.org/en/)).

De nombreux sites ou applications ont également porté une grande partie de la logique vers le côté client. C'est particulièrement vrai pour tout ce qui est Single Page Applications (SPA). Ces dernières font usage de frameworks JavaScript (React, Vue, Ember, Angular, etc.) permettant de gérer les différents états (states) d'une application et d'avoir des composants qui y répondent.

```js
window.addEventLister("load", function() {
  alert("Hello Javascript");
});
```

*Exercice: inspecter le code d'une page web et afficher les divers types de code (onglet network)*

*Exercice: faire un premier projet web avec un fichier HTML, un fichier CSS, un fichier JS*

Si le sujet vous intéresse, Mozilla Developer Network (MDN) possède [un très bon guide en français qui vous permettra de débuter avec JavaScript](https://developer.mozilla.org/fr/docs/Web/JavaScript).

### Assets et fichiers externes

En plus du code HTML, CSS et JavaScript, votre navigateur reçoit également bon nombre de fichiers externes tels que des images, des videos, des fichiers sons, des fichiers de polices, etc.

Ces fichiers ne sont pas contenus dans le code HTML, CSS ou JavaScript mais sont appelés comme des fichiers externes pour être intégrés au rendu de la vue ou de la page.

*Exercice, voir l'onglet "network" dans Google Chrome.*

### Images

Commençons par les images. Sur le web, les formats les plus utilisés sont:

- **JPG**: utilisé pour les images de type photographique, pas de transparence, compression avec pertes (lossy)
- **GIF**: utilisé pour les images avec aplats de couleurs, transparence simple, animations frame par frame, compression avec pertes (lossy). GIF est un format de moins en moins utilisé depuis l'avènement de PNG et de SVG
- **PNG**: utilisé pour les images avec aplats de couleurs, transparence simple et transparence d'alpha, compression avec pertes (lossy).
- **SVG**: format vectoriel, est une sorte de mini-document qui peut être scripté et manipulé par CSS lorsqu'il est intégré au document (inline), compression sans pertes (lossless).
- **WEBP**: format encore en développement mais qui permet d'avoir des fichiers moins lourds et d'utiliser des algorithmes de compression avec et sans pertes (lossy et lossless).

Une fois ces éléments intégrés à un document HTML, CSS et JavaScript peuvent être utilisés pour en définir les styles graphiques et/ou pour les manipuler.

```html
<img src="img/rainbow.jpg" alt="Rainbow over my house">
```

Voici comment intégrer une image avec une légende.

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

Tous les navigateurs web ne supportent pas les mêmes formats video. Pour pouvoir être lue par l'ensemble des navigateurs modernes, votre video doit donc être disponible en plusieurs formats. Actuellement MP4 et WEBM sont suffisants.

Les videos peuvent très facilement être intégrées à vos documents HTML. Une fois ces videos intégrées, CSS et JavaScript peuvent être utilisés pour en définir les styles graphiques et/ou pour les manipuler.

```html
<video width="800" height="600" controls>
  <source src="assets/videos/myvideo.mp4" type="video/mp4">
  <source src="assets/videos/myvideo.webm" type="video/webm">
  <p>Sorry, your browser doesn't support embedded videos. Download the video in <a href="video/myvideo.mp4">MPEG</a> or <a href="video/myvideo.webm">WEBM</a>.</p>
</video>
```

*Exercice: intégrer une vidéo à un document HTML*

### Fontes

Initialement, il était uniquement possible de travailler à l'aide des polices installées sur l'ordinateur client. Toutes les polices n'étant pas disponibles partout, les développeurs utilisaient un "font-stack", une liste de polices spécifiant la police souhaitée ainsi que des alternatives au cas ou cette dernière n'est pas disponible.

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

Aujourd'hui, il est possible de charger des fichiers de polices et de demander au navigateur de les utiliser pour le rendu. Les problématiques restantes sont d'ordre technique (hinting, optimisation) et de licences (les fichiers de polices pouvant être facilement téléchargés, ils sont difficiles à protéger). C'est pour répondre à ces deux problèmes que des services de distribution de polices (Typekit, Google fonts, Fontdeck) ont été créés.

*Exercice: intégrer une police custom à un projet HTML/CSS avec [Font Squirrel](https://www.fontsquirrel.com/) et `@font-face` puis avec [Google fonts](https://fonts.google.com/)*

## Design Web: spécificités du medium

Le design print est un domaine qui a déjà derrière lui des siècles d'existence et qui a intégré une série de règles, de canons et de bonnes pratiques qui, pour la plupart, prennent pour base le canevas du projet et les possibilités techniques au niveau de l'impression.

Avec le print, nous sommes donc dans un environnement de design statique et dont les paramètres sont connus et maîtrisés de bout en bout. Le designer contrôle parfaitement tous les aspects de son projet.

Il en va tout autrement pour le web et le digital en général, comme l'explique fort bien John Allsopp dans son article "[A Dao of Web Design](https://alistapart.com/article/dao)":

> The control which designers know in the print medium, and often desire in the web medium, is simply a function of the limitation of the printed page. We should embrace the fact that the web doesn’t have the same constraints, and design for this flexibility. But first, we must “accept the ebb and flow of things”.

> "[A Dao of Web Design](https://alistapart.com/article/dao)" - John Allsopp, 2000

Accepter la flexibilité du medium se traduit par une impossibilité de tout contrôler.

En tant que designer, nous devons nous réconcilier avec les inconnues inhérentes au web et les apprivoiser, les intégrer dans notre travail.

Depuis les débuts du web, les designers digitaux ont du réinventer leur métier et mettre en place des outils, workflows de production et des stratégies pour aborder un medium qui lie contenus et interactivité dans un contexte fluide où les inconnues sont nombreuses.

### Entre contenus et interactivité

Comme avec le print, le design digital vise à présenter des contenus de nature diverses mais ajoute une dimension d'interactivité, au niveau des types de contenus (son, videos, animations, etc) comme au niveau des objectifs (acheter un billet d'avion, faire une réservation, etc.).

Bref, le design digital est un continuum entre contenus et interactivité. Chaque site ou application est par essence un mélange des deux, dans des proportion diverses.

- Site de presse: site axé sur les contenus et donc vers la transmission d'informations (articles, recettes, opinions, etc). Certains aspects applicatifs sont néanmoins présents et visent à faire accomplir des tâches aux utilisateurs: moteur de recherche, abonnement, espace membres, etc.
- Site bancaire: site axé sur l'applicatif et donc la réalisation de tâches (transferts, téléchargement de documents). Certains aspects de contenus et de transmission d'information sont présents également: conditions générales, présentation des formules de prêts, consultation des soldes, etc.

Ces deux aspects sont toujours présents dans un site web et doivent tous deux être pris en compte à divers niveaux:

- **Stratégie**: quels sont les objectifs en termes de transmission d'information / d'accomplissement de tâches pour les divers publics ciblés?
- **Contenus**: quels contenus doivent être mis en place? Quels types de contenus vont au mieux servir les objectifs du site (blogposts, tutorial, videos, etc.)? Quelles sont les ressources disponibles pour publier et à quelle fréquence?
- **Interactivité**: quelles interactions avec le site doivent être créées? Comment les rendre visibles et attractives pour les utilisateurs? Quelles ressources sont disponibles pour le support et les tests utilisateurs?
- **Structure**: quelle va être l'architecture d'information? Quelles seront les structures de données des contenus? Quels sont les flux utilisateurs, les diverses étapes dans la réalisation de chaque tâche et comment les structurer pour que chaque étape soit simple et pour le que nombre d'étapes soit le plus bas possible?
- **Présentation**: comment la présentation va-t-elle soutenir les autres dimensions? La présentation sert-elles les divers publics ciblés?

### Design for the unknown

#### Première inconnue: le canevas

En print comme en vidéo, le canevas du produit fini est connu. Il s’agit d’une affiche de telle dimensions, d’une brochure en format A5 de 20 pages, d'un sport publicitaire de 3 minutes pour la télévision, etc. Il en va tout autrement sur le web où le concept même de canevas sur lequel baser un design disparait devant la diversité des supports sur lesquels les sites et applications doivent fonctionner (tailles, résolutions et orientations d’écrans, etc.).

Si nous ne pouvons plus baser nos designs sur le canevas, nous devons alors [partir des contenus](https://markboulton.co.uk/journal/a-richer-canvas) pour designer non plus des pages mais bien des [systèmes de composants flexibles](http://styleguides.io/) pouvant s’agencer de diverses façons pour occuper et s’adapter à un maximum de canevas possibles.

*Exercice: l'application Spotify en téléphone, tablette, desktop*

#### Deuxième inconnue: les capacités du navigateur et du terminal

En print ou en vidéo, une fois un design créé, son rendu est contrôlable et contrôlé de bout en bout: de la conception jusqu’à la diffusion finale.

Au niveau du web, tout passe par deux canaux que le concepteur ne contrôle pas et dont vont largement dépendre l'expérience utilisateur: le navigateur et le terminal sur lequel celui-ci est hébergé. Là aussi, nous avons affaire à une large diversité de capacités: support tactile, bande passante, support images, support vidéos, support CSS, support JavaScript, gyroscope, appareil photo, géolocalisation, etc.

Lorsque nous envisageons des solutions de design, nous devons tenir compte de cette seconde inconnue. Dans l’industrie, on se réfère souvent au concept de "[progresssive enhancement](https://resilientwebdesign.com/chapter6/)" selon lequel on va d’abord se concentrer sur le fait de délivrer une bonne expérience utilisateur de base, que l’on va enrichir pour les navigateurs et terminaux disposant de capacités plus avancées.

*Discussion: [Do websites need to look exactly the same in every browser](http://dowebsitesneedtolookexactlythesameineverybrowser.com/)*

#### Troisième inconnue: le contexte (humain) d’utilisation

Si nous pouvons en général définir assez précisément nos publics cibles (à travers des études de marché, des personas, etc.), le contexte d’utilisation d'un site ou d'une application peut varier grandement et nous est la plupart du temps complètement inconnu.

L’utilisateur mobile peut utiliser son téléphone debout dans son train matinal, être facilement distrait, ne disposer que d’une seule main et d’une connectivité faible. Ce même utilisateur mobile peut utiliser sa tablette, confortablement installé dans le canapé du lobby de son entreprise. Il est dans ce cas très concentré et dispose d’une connexion à haut débit. Les circonstances et le contexte d’utilisation est tout aussi divers pour un utilisateur d’ordinateur fixe.

La solution est ici de toujours centrer les solutions sur l'utilisateur. Typiquement, les projets web impliquent les utilisateurs très tôt dans la définition des solutions envisagées et passent par des cycles d'itérations relativement courts dans lesquels les feedbacks utilisateurs et les tests sont extrêmement importants.

Un autre aspect intéressant du medium Internet est la capacité d'avoir très rapidement des retours sous forme de données quantitatives et qualitatives (analytics, interviews utilisateurs, tests, etc.).

### Grands principes du design web

Les principales différences entre le design web et le design print ou audiovisuel viennent de ces inconnues et de la nécessité d'y répondre.

#### Mobile first responsive web design

Afin de répondre à la diversité croissante des tailles d'écrans et des résolutions existant sur le marché, un des grands principes est de commencer à designer pour les contraintes maximales, celles des petits écrans de smartphones et des bandes passantes limitées. C'est le principe du "[mobile first](https://www.lukew.com/ff/entry.asp?933)" qui a des implications tant en termes de performance que de mise en page.

Une fois que votre site ou votre application web fonctionne pour ces derniers, vous pouvez petit à petit passer aux écrans de taille moyenne et puis aux écrans plus larges et aux connections plus stables et de plus hauts débits. L'idée centrale du "[Responsive Web Design](https://alistapart.com/article/responsive-web-design)" lancée par Ethan Marcotte est celle d'un continuum tout au long duquel votre design "répond" à l'espace utile disponible et à la résolution de l'écran.

Les trois pierres angulaires du responsive sont:

- **grilles fluides**: d'une grille simple de deux colonnes sur petits écrans, on peut passer à une grille de plus en plus complexe au fur et à mesure que l'espace disponible augmente. Les nouvelles spécifications de layout en CSS (Flexbox et Grid) sont adaptées à cette approche.
- **media flexibles**: pour s'intégrer à une grille fluide, vos media (images, video, etc.) doivent être flexibles et non de tailles fixes. Grâce à quelques règles CSS, il est possible d'adapter la taille de vos media aux containers dans lesquels ils se trouvent.
- **media queries**: le mécanisme CSS grâce auquel le code CSS (layout, typographie, etc) est capable de "répondre" à une grande palettes de paramètres du navigateur client (largeur d'écran, orientation, couleurs, etc.)

Ces principes sont appliqués au niveau macro (layout global) mais également au niveau micro (composants). Si le layout de votre page réagit à l'espace disponible à l'écran, il en va de même pour une interface de navigation, un footer ou encore à un composant "news" dans un site de presse.

Les media fluides ont également des implications au niveau de la performance. Cela ne sert à rien de charger une image de 1000 pixels de large sur un écran qui en fait 320, même chose pour les videos. Un standard a été développé pour les images responsives avec `srcset`, `sizes`. La balise `<picture>` est à utiliser seulement si des images différentes sont nécessaires pour des raisons de direction artistique.

En ce qui concerne les videos, des services tels que Youtube ou Vimeo restent la meilleure option au niveau de la performance. Ces services vont transcoder votre video dans divers formats ainsi que dans différentes résolutions, ce qui vous garantira une compatibilité et des performances maximales.

*Exercice: inspecter quelques sites et applications responsives [Stripe](https://stripe.com/), [Opera de Paris](https://www.operadeparis.fr/), [AirBnB](https://www.airbnb.com/), [Google Drive](https://drive.google.com/)). Prêter attention à la typographie, aux grilles, aux interfaces de navigation, aux images et aux videos*

#### Progressive enhancement

L'idée du progressive enhancement est similaire à celle du Responsive Web Design mais dans le domaine des capacités du navigateur et du terminal. Selon Jeremy Keith dans "[Resilient Web Design](https://resilientwebdesign.com/chapter6/)", cette idée repose sur trois étapes simples:

1. Identifier les fonctionnalités ou les contenus principaux / essentiels
2. Rendre disponibles ces contenus ou ces fonctionnalités à l'aide des technologies les plus simples possibles
3. Construire sur cette base en utilisant les technologies plus modernes

Cette philosophie permet de toujours disposer des fonctionnalités ou des contenus essentiels et de passer ensuite du temps à construire des experiences plus raffinées et abouties sur cette fondation solide. Le principe du "Progressive Enhancement" permet donc de répondre à l'inconnue des capacités du navigateur et du terminal client.

Cette manière de développer et de designer a depuis toujours été mise en pratique au niveau des sites orientés vers les contenus et la transmission d'informations. Avec l'avènement des "[Progressive Web Apps](https://developers.google.com/web/progressive-web-apps/)" (PWA) chères à Google, cette idée fait son chemin au niveau des projets plus applicatifs.

#### User centered design et Design Thinking

Cette méthodologie consiste à se centrer sur les utilisateurs d'un site ou d'une application et leurs besoins tout au long d'un processus de design itératif. A travers des techniques de recherche investigatives (interviews, sondages, shadowing, etc.) et génératives (brainstormings, exercices de groupes, etc.), l'idée est d'en savoir le plus possible sur les utilisateurs, leurs besoins et le contexte d'utilisation du site ou de l'application. De cette phase de recherche on extrait les pré-requis et les objectifs du produit, pour ensuite proposer les solutions possibles que l'on va tester avec les utilisateurs pour voir si les objectifs sont remplis.

L'inconnue des contextes d'utilisation couplée aux ressources, budgets et délais importants nécessaires pour créer un site ou une application web font qu'il vaut mieux savoir où l'on va. Toutes les methodologies liées au User Centered Design et au Design Thinking (Lean UX, Design Sprint, etc.) permettent de tester rapidement concepts et prototypes auprès d'utilisateurs réels.

Depuis quelques années, [Thoughtbot](https://thoughtbot.com/) et [Google Ventures](http://www.gv.com/sprint/) ont popularisé un outil: le Design Sprint. L'idée est de passer en 5 jours seulement d'un simple concept à un prototype concret et testé par des utilisateurs.

- **Jour 1**: comprendre les utilisateurs, leurs besoins et leurs contextes (côté utilisateurs) ainsi que les objectifs à atteindre et les KPIs (côté business). Identifier aussi les risques potentiels et les moyens de les réduire.
- **Jour 2**: diverger en proposant (sketch et pitch) différentes solutions possibles aux problèmes et au contexte posés préalablement.
- **Jour 3**: converger en se mettant d'accord sur une ou deux solutions à prototyper
- **Jour 4**: prototyper les solutions en ayant un degré de fidélité juste suffisant que pour pouvoir réaliser les tests utilisateurs
- **Jour 5**: tester le(s) prototype(s) avec des utilisateurs et évaluer

Si vous souhaitez en savoir plus concernant le design sprint, [le petit guide online de Thoughtbot](https://thoughtbot.com/product-design-sprint/guide) est très bien fait et vous donne quelques examples d'activités ou d'exercices à réaliser avec vos clients.

Cette méthodologie forme également une bonne base si vous n'avez qu'un ou deux jours à passer sur la phase de recherche.

## Design web en pratique

Après avoir introduit le sujet par un peu de théorie, passons à la pratique. La suite de ce cours se veut être un guide pratique pour réaliser efficacement des designs pour le web, qu'il s'agisse d'un site ou d'une application.

1. Recherche et stratégie
2. Couleurs et palette
3. Typographie
4. Media (images et illustrations, icônes, videos, sons, etc.)
5. Layout et mise en page
6. Transitions et animations
7. Livrables pour le design web

## 1. Recherche et stratégie

La phase de recherche vise à cerner les tenants et aboutissants du projet, tant du point de vue des utilisateurs (publics cibles, besoins, contexte) que du business (objectifs, KPI, compétition).

La première chose à faire est de bien cerner quels sont les publics cibles. Pour cela, rien ne remplace un contact direct avec des utilisateurs ou, à défaut, avec les responsables du support ou du marketing qui sont en contact avec eux. De simples activités comme un future perfect / pitch, des [proto-personas](https://uxmag.com/articles/using-proto-personas-for-executive-alignment) (voici des [photos utilisables créées par Jason Travis](http://www.jasontravisphoto.com/persona/)) et quelques [job stories](https://jtbd.info/replacing-the-user-story-with-the-job-story-af7cdee10c27) par persona peuvent déjà s'avérer très utiles.

En regard des personas, il importe de se pencher sur les objectifs business. Pour chaque personas, demandez-vous comment votre site ou votre application peut les aider. De manière plus générale, quels sont les indicateurs (mesurables) qui vous permettront de dire si votre projet à atteint ses objectifs et rencontre les besoins des clients.

Lors de cette phase de recherche, il est bon de se pencher sur la compétition. Quels sont les sites ou les applications qui répondent aux même besoins? Quels sont leurs points forts et leurs points faibles?

Au niveau du design, deux exercices sont assez utiles.

- **Adjectifs et priorités**: demander à tous de noter sur un post-it trois adjectifs qu'ils souhaitent que les clients ressentent en visitant le site ou en utilisant l'application. Chacun vote ensuite pour deux adjectifs et les trois plus importants sont classés par priorité.
- **Design brief à l'instinct**: rassembler 15 à 20 sites ou applications avec des styles graphiques différents. Ces exemples sont passés en revue et chacun donne une note de 1 à 5. Une fois les moyennes établies, discuter des 3 premiers et des trois derniers vous donnera un bon design brief.

Les dernières choses à aborder tiennent à la structure générale de l'application ou du site. Une architecture d'information et / ou des [wireflows](https://dribbble.com/shots/2248785-Web-Wireframes-UX-Flow/attachments/420198) réalisés en petits groupes peuvent vous donner une bonne approximation de la structure souhaitée. Il s'agit d'un élément important dans la mesure où il va être matérialisé par les interfaces de navigation qui sont une contrainte importante au niveau du design.

*Exercice: phase de recherche pour le site de l'ESA Saint Luc: publics cibles, proto personas, job stories, adjectifs, design brief*

## 2. Couleurs

Ici, il vous faudra faire preuve de mesure. Dans la plupart des cas, une couleur principale (déclinée) et une couleur d'accent (déclinée également) ainsi qu'une gamme de gris (basés sur votre couleur principale) pour les couleurs neutres suffiront largement. Certaines applications ou sites ont des palettes de couleurs plus étendues mais il est préférable de rester le plus simple possible.

Commencer par choisir une couleur principale en rapport avec votre branding ou avec les adjectifs donnés par le client. Pour le choix de la couleur complémentaire, des outils peuvent vous aider, comme [Adobe Color CC](https://color.adobe.com/create/color-wheel/) ou [Coolors](https://coolors.co/). Pensez également à aller faire un tour sur [Dribbble](https://dribbble.com/colors/3116EF) et à utiliser l'outil de recherche par couleur pour immédiatement avoir un grand choix de couleurs complémentaires.

Une fois que vous avez deux (maximum trois) couleurs complémentaires, vous pouvez utiliser votre application de design favorite et [des techniques reposant sur des layers](https://www.smashingmagazine.com/2017/07/advanced-color-palettes-photoshop-sketch-affinity-designer/) pour démultiplier vos options tout en restant dans la gamme. Il vous reste ensuite à déterminer une gamme de gris contenant votre couleur principale et vous voilà paré.

Une autre méthode efficace pour créer une palette de de couleurs harmonieuse consiste à partir de photos de paysage / de nature. Adobe Color CC possède une fonction qui vous y aidera.

Un dernier conseil, [évitez le noir pur dans vos palettes](https://ianstormtaylor.com/design-tip-never-use-black/). Afin d'être dans la gamme partez plutôt de votre couleur de base et saturez-là pour obtenir une couleur proche du noir mais contenant votre couleur de base.

*Exercice: créer une palette de couleurs simple*

## 3. Typographie

Comme le dit fort justement Oliver Reichenstein, [le texte compose 95% d'un site web ou d'une application](https://ia.net/topics/the-web-is-all-about-typography-period). La typographie est donc une étape importante dans la conception de tout produit digital. Comme nous l'avons vu plus haut, nous disposons désormais d'une grande variété de polices avec `@font-face` et les services de distribution de fontes tels que [Google Fonts](https://fonts.google.com/) ou [Typekit](https://typekit.com/).

Se pose donc la question du choix des fontes à utiliser pour un projet donné. Comment faire un choix pertinent?

### Choix de polices

Pour commencer, il est important de poser des limites. Les fichiers de polices sont des ressources externes et charger une police, une graisse ou un style supplémentaire ajoutera au poids de vos pages. En général on travaillera donc avec une ou deux polices maximum et un nombre limité de variantes en termes de graisses et de styles.

*Exercice: Google Font et poids des fichiers de police*

Votre premier choix devra sans doute être la police que vous utiliserez pour votre corps de texte. Il vous faut une police solide et de lisible qui permettra aux autres éléments textuels importants (titres, calls to action) de ressortir. Préférez des polices avec une x-height élevée et peu de fioritures. Soyez également attentifs à ce que la police choisie possède plusieurs graisses et variantes (au moins bold et italique). Les polices avec plusieurs graisses sont intéressantes de par la variété potentielle qu'elles proposent.

Si vous vous posez des questions, regardez simplement dans quel but ou contexte la police que vous considérez a été développée, explorez son histoire. Des services tels que Typekit ou Google fonts vous donnerons des renseignements précieux. Ces services possèdent également des spécimens qui vous permettrons de mieux appréhender les caractéristiques des divers fontes proposées. Allez également faire un petit tour du côté des sites tels que [Typewolf](https://www.typewolf.com/), [Fonts in Use](https://fontsinuse.com/) ou [Dribbble](https://dribbble.com/).

Un exercice difficile en typographie consiste à trouver plusieurs polices qui vont fonctionner ensemble dans un design. Une fois votre police de corps de texte choisie, vous avez plusieurs options:

- **Superfamilies**: certaines polices forment une famille de polices et sont conçues comme telles. Elles contiennent souvent des polices différentes (serif et sans-serif par exemple), utilisables à différentes tailles (caption, display, etc.) ou ayant différentes approches / kernings (Normal, Condensed, Extended). En voici quelques exemples sur Typekit: Calluna et Calluna Sans, Freight Text et Freight Sans, etc.
- **Designer / Fondrie identique**: voici un raccourci par rapport au point suivant. En général, des polices même différentes au premier regard on pas mal de caractéristiques communes si elles sont conçues par la même personne ou la même fondrie. Pensez donc à aller voir de ce côté lorsque vous cherche un accord entre deux polices.
- **Caractéristiques communes**: cherchez des polices qui sont suffisamment différentes que pour êtres distinguées facilement l'une de l'autre mais qui ont des caractéristiques communes (formes des lettres, x-height, etc.) ou qui ont été développées dans un même contexte ou selon un concept similaire.
- **Outils**: des outils et services tels que Google Fonts ou Typekit vous proposent des pistes intéressantes pour le font pairing. N'hésitez pas non plus à inspecter des sites que vous appréciez au niveau typographique.

*Exercice: Voici [quelques](http://femmebot.github.io/google-type/) [exemples](http://hellohappy.org/beautiful-web-type/) de typographies réussies avec Google fonts. Analysons-les.*

*Exercice: choisir deux polices*

### Compositions typographiques

Un élément important dans vos compositions typographiques est de faire varier les caractéristiques de vos éléments pour créer du contraste, des tensions et des similitudes. Vous avez pour ce faire beaucoup d'outils à votre disposition:

- familles (`font-family`): serifs, sans-serifs, display, etc.
- graisses (`font-weight`): black, bold, medium, etc.
- taille (`font-size`): pixels, rem, em, etc.
- casse (`text-transform`): uppercase, lowercase, etc.
- styles (`font-style`): normal, italique
- ornements: glyphs, ligatures, etc.
- couleurs (`color`): noir, rouge, gris, etc.
- alignement (`text-align`): left, right, center, justify
- espace (`margin`, `padding`, `line-height`, `letter-spacing`): margins, paddings, interligne, letter spacing

*Exercice: chercher 5 compositions typographiques sur [Dribble](https://dribbble.com/) et expliquer quels sont les outils utilisés*

*Exercice: utiliser la typographie et Google fonts pour designer les divers éléments d'un blogpost et des paroles d'un track de hip-hop, d'abord dans Figma et puis dans le code*

### Echelle typographique et rythme vertical

Une fois vos polices choisies, l'étape suivante consiste à mettre en place une échelle typographique et un rythme vertical. Pour ce qui est de l'échelle typographique, vous pouvez-vous appuyer sur "[Modular Scale](https://www.modularscale.com/)" un outil développé par [Tim Brown](http://tbrown.org/).

Pour ce qui est du rythme vertical, le plus facile est de prendre une échelle à laquelle vous allez vous tenir pour ce qui est de l'interligne et de tous les espaces verticaux. Les échelles les plus populaires sont les échelles [de cinq](https://guides.area17.com/design-techniques/#baseline-grid), de six ou de [huit](https://themefoundation.com/vertical-rhythm-responsive-typography/).

Personnellement, [je ne souscris pas forcément à une grille stricte](http://jasonsantamaria.com/articles/baseline-grids-on-the-web) (baseline grid) difficile à maintenir sur un médium aussi fluide que le web. Par contre, il faut être attentif à avoir un rythme vertical aussi cohérent que possible en essayant que tous les espacements verticaux ainsi que les hauteurs de lignes soient des multiples de l'échelle de base.

Cette grille typographique sert également à la gestion des espaces dans les composants: boutons, listes et autres éléments utilisent également cette grille typographique.

*Exercice: rythme vertical et typographie pour trois cartes côte à côte avec des boutons de call to action*

*Exercice: rythme vertical et sections d'un layout*

## 4. Media: Images, Icônes, Video et Sons

Outre le texte, images, illustrations, icônes et autres média plus interactifs tels que les sons ou les videos font aujourd'hui partie intégrante d'une experience web. Ces media sont des fichiers externes appelés par les fichiers HTML, CSS ou JS.

*Exercice: voir les assets dans une page web via l'onglet Network des developer tools*

### Icônes

Après être passé par diverses options (images, icon fonts, etc.) les icônes utilisées aujourd'hui sont dans un format vectoriel appelé SVG (Scalable Vector Graphics).

Les fichiers SVG sont des fichiers textes qui ressemblent à du HTML et peuvent être liés comme une image et se comporter comme telle ou bien être intégrés au document, ce qui offre les avantages d'être manipulable directement par JS ou CSS, pour leur appliquer des transitions ou des animations.

Généralement, ces fichiers vectoriels sont exportés à partir de Figma, Sketch ou Illustrator et optimisés. Ils sont ensuite intégrés aux pages / vues.

*Exercice: exemple de fichier SVG*

*Exercice: exporter une icône à partir de Figma et l'optimiser avec [SVGOMG](https://jakearchibald.github.io/svgomg/)*

*Exercice: faire une transition avec une icône dans un lien*

### Images et illustrations

Images ou illustrations sur le web peuvent être soit des contenus (chargées depuis la page HTML) soit décoratives (chargées depuis CSS ou JS). Dans tous les cas, ce sont des assets lourds à charger, il faut donc les optimiser au mieux, en terme de format (choisir le format le moins lourd en regard de la nature de l'image) comme en terme de poids (optimisation).

*Exercice: comparer fichiers optimisés et non-optimisés*

#### Images de contenus (HTML)

Les images de contenus peuvent être dans divers formats comme vu plus haut. Les images comme éléments de contenus peuvent être fluides (layout) mais également responsives (performance) pour charger un fichier différent suivants les résolutions ou les tailles d'écran.

Pour rendre une image fluide au niveau du layout, il suffit de spécifier que sa largeur maximum est 100% de son container parent. Il faut pour cela que ses dimensions soient plus importantes que la largeur maximale de son parent.

```css
/* image fluide */
.o-fluidimage {
  max-width: 100%;
  vertical-align: middle;
}
```

Si vous souhaitez des hauteur et largeurs variables sans distordre l'image, vous pouvez utiliser la propriété `object-fit`, [dont Jen Simmons propose une démo](https://labs.jensimmons.com/2016/examples/object-fit.html), comme suit:

```css
/* image fluide */
.o-fitimage {
  width: 100%;
  height: 100%:
  object-fit: cover;
}
```

Si CSS peut régler les choses sur le plan de la mise en page, il est contre productif de charger une grande image si la page ou vue est affichée sur un petit écran comme celui d'un smartphone. Grâces aux [images responsives](https://www.smashingmagazine.com/2014/05/responsive-images-done-right-guide-picture-srcset/) et à `srcset`, `sizes` et `<picture>`, le navigateur fait une grande partie du travail pour vous.

Utilisez `srcset` et `sizes` si vous souhaiter servir une image identique mais à des tailles différentes suivant la résolution et la taille d'écran.

```html
/* image fluide */
<img src="img/myimage-small.jpg"
     srcset="img/myimage-small.jpg 500w,
             img/myimage-medium.jpg 1000w,
             img/myimage-large.jpg 1500w"
     sizes="(min-width: 1200px) 400px,
            (min-width: 760px) 33vw,
            100vw"
     alt="alternative text">
```

Si vous souhaiter charger une image différente (cadrage, orientation, etc) suivant les tailles d'écran, il vous faudra utiliser l'élément `<picture>`.

```html
<picture>
   <source media="(min-width: 750px)"
           srcset="img/bear-landscape-small.jpg 500w,
                   img/bear-landscape-medium.jpg 1000w,
                   img/bear-landscape-large.jpg 1500w"
           sizes="(min-width: 1200px) 400px,
                  33vw">
   <img src="bear-portrait-small.jpg" alt="A fluffy bear">
</picture>
```

*Exercice: responsive image et Network panel dans les outils de développement*

### Images de background

Les images sont également utilisées comme éléments d'arrière plan (background) des divers éléments (boites) qui composent une page ou une vue. Ces images de background peuvent avoir différentes caractéristiques définies par CSS (répétées ou pas, positionnées, superposées, mises à l'échelle, etc.), ce qui en fait des composants importants de n'importe quel design.

```css
/* texture répétée */
.c-header {
  background: #FCF8F8 url(../img/bkg-paper-texture.jpg) 0 0 repeat;
}
```

```css
/* image de background simple */
.c-header {
  background-color: #000000;
  background-image: url(../img/bkg-header.jpg);
  background-position: 50% 50%;
  background-repeat: no-repeat;
  background-size: cover;
}
```

```css
/* backgrounds multiples et gradient */
.c-header {
  background-color: #000000;
  background-image: linear-gradient(to left, rgba(80,227,194,0.4), rgba(80,227,194,0.4)),
                    url(../img/blackandwhite.jpg);
  background-position: 50% 50%;
  background-repeat: no-repeat;
  background-size: cover;
}
```

*Exercice: réaliser une banner avec des images de background ou des gradients dans Figma et en code*

### Effets: filtres et masques

Les dégradés, les filtres, les masques et les blend modes sont également très utilisés pour ajouter des effets aux designs web.

Commençons par [les dégradés](https://developer.mozilla.org/fr/docs/Web/CSS/Utilisation_de_d%C3%A9grad%C3%A9s_CSS) qui peuvent être créés très simplement en CSS, qu'ils soient radiaux ou linéaires.

```css
/* linear gradient */
.linear-gradient {
  background: linear-gradient(to bottom, #e66465 15%, #9198e5 80%);
}
```

CSS permet également d'utiliser [des filtres](https://css-tricks.com/almanac/properties/f/filter/) qui peuvent être facilement appliqués aux images comme vous le feriez dans photoshop. Voici deux exemples.

```css
/* grayscale filter */
.o-filter-grayscale {
  filter: grayscale(1);
}
```

```css
/* blur filter */
.o-filter-blur {
  filter: blur(2px);
}
```

Les propriétés `background-blend-mode` et `mix-blend-mode` permettent de modifier vos images de façon importante, comme vous le feriez avec des calques dans une application graphique. `background-blend-mode` se charge faire un blend mode entre deux backgrounds, tandis que `mix-blend-mode` est utilisé pour gérer un blend mode entre un élément et un autre.

```css
/* mix blend mode */
.o-blended-red {
  display: inline-block;
  background-color: red;
}

.o-blended-red > img {
  filter: grayscale(1);
  mix-blend-mode: multiply;
  vertical-align: middle;
}
```

*Exercice: expérimenter avec filtres et blend modes dans Figma et en code*

Clipping et masking peuvent également aider à apporter un peu de variété à vos images. Ces deux principes se ressemblent en ce qu'ils servent tous les deux à cacher certaines parties d'un élément. Le support au niveau des navigateurs n'est pas identique mais [voici une page de test par Yoksel](https://codepen.io/yoksel/full/fsdbu/) pour vérifier par vous mêmes.

- **masques**: sont des images. Avec `mask-mode: luminance;` les parties noires du masque sont cachés, les parties blanches sont visibles. Avec `mask-mode: alpha;` les parties opaques du masque sont visibles et les parties transparentes cachées.
- **clips**: sont des formes. ce qui est à l'intérieur de la forme est visible

```css
/* appliqué à une <img> */
.masked {
  -webkit-mask-image: url(../img/masks-scribbles.svg);
  mask-image: url(../img/masks-scribbles.svg);
  -webkit-mask-repeat: no-repeat;
  mask-repeat: no-repeat;
}
```

```css
/* appliqué à une <img> (ne fontionne qu'avec un svg interne pour Safari, Chrome et Opera) */
.clipped-svg {
  -webkit-clip-path: url(../img/clip.svg#myClip);
  clip-path: url(../img/clip.svg#myClip);
}
```

```css
/* appliqué à une <img> */
.clipped-polygon {
  -webkit-clip-path: polygon(20% 0%, 0% 20%, 30% 50%, 0% 80%, 20% 100%, 50% 70%, 80% 100%, 100% 80%, 70% 50%, 100% 20%, 80% 0%, 50% 30%);
  clip-path: polygon(20% 0%, 0% 20%, 30% 50%, 0% 80%, 20% 100%, 50% 70%, 80% 100%, 100% 80%, 70% 50%, 100% 20%, 80% 0%, 50% 30%);
}
```

[Clippy de Bennett Feely](https://bennettfeely.com/clippy/) est un petit outil qui vous permettra de créer facilement des clip paths CSS.

```css
/* appliqué à une <img> */
.c-gradient-text {
  background-image: linear-gradient(to right, #e03d52, #ffb25b);
  -webkit-background-clip: text;
  background-clip: text;
  color: transparent;
}
```

Les SVG et les polygones étant animables, ainsi que les images utilisées comme background, il est possible de réaliser des masques animés en CSS ou en JS.

*Exercice: expérimenter avec clipping et masques dans Figma et en code*

### Videos

Nous avons vu comment intégrer des videos dans vos documents HTML5. Ces videos peuvent être des éléments de contenu mais peuvent également être [utilisées de façon créative](https://www.nurturedigital.com/) [comme éléments de layout](https://www.kikk.be/2017/) sous forme de petites boucles simples. Les vidéos HTML5 offrent l'avantage contrôlables via des attributs et une API video scriptable en JavaScript.

Par contre, les services tels que Youtube et Vimeo encodent et en servent automatiquement les videos en différentes résolutions et formats suivant le navigateur et la machine utilisées. Ils utilisent également des CDN qui améliorent encore les performances en faisant en sorte que le serveur qui vous transmet la vidéo se trouve géographiquement le plus près possible de vous.

Les videos HTML5 comme les videos servies via une `<iframe>` par des services tels que Youtube et Vimeo peuvent facilement être rendues fluides et s'adapter à des layouts responsives.

Pour les videos HTML5, la technique est la même que pour les images.

```css
.o-fluidvideo {
  max-width: 100%;
  vertical-align: middle;
}
```

Pour les videos `<iframe>` il vous faut un élément autour.

```css
.o-fluidiframe {
  position: relative;
  margin: 0;
  padding: 56.25% 0 0;
  background-color: black;
}

.o-fluidiframe > iframe {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  border: none;
}
```

*Exercice: expérimenter avec des videos*

## 5. Layout: Grilles et outils CSS

En design, les grilles sont un outil essentiel. Elles vous permettent de structurer vos contenus et de créer des mises en page complexes dont les éléments sont connectés les uns au autres par une structure sous-jacente.

  > Nothing could be more useful to reach our intention than the Grid. The grid represents the basic structure of our graphic design, it helps to organize the content, it provides consistency, it gives an orderly look and it projects a level of intellectual elegance that we like to express.

  > Massimo Vignelli. [The Vignelli Canon](https://www.vignelli.com/canon.pdf)

### Rythme horizontal et colonnes

En venant du print et de ses canevas fixes, la question se pose naturellement, comment créer une grille alors que le canevas global change constamment?

La réponse est la même que pour le reste: vos grilles doivent être fluides. La technique la plus utilisée est de garder des gutters fixes, tandis que la largeur et le nombre de colonnes change. Là où un design sur petits écrans utilisera une grille de 2 ou 3 colonnes maximum, un design sur un grand écran peut utiliser 8, 10, 12 ou 16 colonnes par exemple.

*Exercice: reconstruire la grille du [New York Times](nytimes.com)*

*Exercice: reconstruire la grille de [Steele Brand Co](https://dribbble.com/shots/2899485-Steele-Brand-Co/attachments/600278)*

Il existe deux grandes méthodes pour créer ces grilles:

- **Grilles content out**: grilles conçues à partir des contenus et des contraintes du projet (publicités, unités typographiques, longueur de lignes, etc.)
- **Grilles canvas in**: partir de vos différents breakpoints et designer plusieurs grilles.

Ces grilles peuvent être de différents types:

- **Grilles symétriques**: toutes les colonnes sont de même taille. Vous avez la possibilité de combiner deux grilles pour plus de variété (une grille de 10 et une grille de 12 par exemple)
- **Grilles asymétriques**: certaines colonnes sont de différentes tailles, à nouveau en se basant sur les contraintes du projet ou certaines éléments (menu latéral, compound grids)

Les grilles les plus courantes sur le web sont des grilles symétriques, souvent de 12 colonnes car 12 offre l'avantage d'être divisible par 2, 3 ou 4.

Si un nombre de colonnes pair comme 8, 10, 12 ou 18 apporte un grand équilibre et une grande symétrie, ce genre de grille peut parfois s'avérer ennuyeux. Les grilles ayant un nombre de colonnes impair 5, 7, 9 sont légèrement plus difficiles à maîtriser mais apportent un dynamisme intéressant.

En parlant de dynamisme, n'oubliez pas que vous pouvez avoir des grilles sans gutter ou encore laisser des colonnes vides dans vos designs.

*Exercice: design d'une grille responsive symétrique pour trois tailles d'écran*

*Exercice: design d'une grille responsive asymétrique pour trois tailles d'écran*

*Exercice: expérimenter avec des colonnes vides*

### Outils CSS au niveau du layout

Au niveau du code, disposer de véritables outils de layout pour le web est assez récent. Après avoir été obligés d'employer diverses méthodes plus ou moins orthodoxes (tableaux et gif transparents, floats, inline-block, etc.) CSS dispose désormais de deux outils de layout dignes de ce nom: [Flexbox](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout) et [Grid](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout).

- **Flexbox**: gère une seule dimension (verticale ou horizontale), fonctionne à partir des caractéristiques des contenus pour gérer leurs répartition dans un container.
- **Grid**: gère deux dimensions (verticale et horizontale), fonctionne à partir des caractéristiques d'une grille dans laquelle les contenus sont placés.

Ces deux outils de layout font en outre appel au [module de Box Alignment](https://www.w3.org/TR/css-align-3/). Vous retrouverez donc des propriétés d'alignement communes à Grid et à Flexbox.

*Exercice: Flexbox - interfaces de navigation verticaux et horizontaux responsives avec Figma et dans le code*

```css
.c-mainnav {
  list-style: none;
  margin: 0;
  padding: 0;

  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: stretch;
}

@media all and (min-width: 750px) {
  .c-mainnav {
    flex-direction: row;
    justify-content: flex-end;
    align-items: center;
  }
}

.c-mainnav__item {
  border-bottom: 1px solid #cccccc;
}

.c-mainnav__item:first-child {
  border-top: 1px solid #cccccc;
}

@media all and (min-width: 750px) {
  .c-mainnav__item,
  .c-mainnav__item:first-child {
    border: none;
  }
}

.c-mainnav__link {
  display: block;
  padding: 0.5rem 0.25rem;
  font: 500 0.875rem/1 "Helvetica Neue", "Helvetica", "Arial", sans-serif;
  color: #050d0f;
  text-decoration: none;
  letter-spacing: 1px;
}

.c-mainnav__link:hover {
  color: #5cbee2;
}

@media all and (min-width: 750px) {
  .c-mainnav__link {
    padding: 0.5rem 1rem;
  }
}
```

*Exercice: Grid - layout de pages responsives avec Figma et dans le code*

```css
.c-page-container {
  box-sizing: border-box;
  margin: 0 auto;
  max-width: 1140px;
}

@media all and (min-width: 760px) {
  .c-page-container {
    display: grid;
    grid-template-columns: 1fr 3fr;
    grid-template-rows: auto;
    grid-template-areas:
      "header header"
      "sidebar content"
      "footer footer";
    grid-column-gap: 20px;
  }
}

.c-siteheader {
  grid-area: header;
  background-color: silver;
}

.c-content-secondary {
  grid-area: sidebar;
  background-color: lightseagreen;
}

.c-content-main {
  grid-area: content;
  background-color: lightblue;
}

.c-sitefooter {
  grid-area: footer;
  background-color: lightgreen;
}
```

## 6. Transitions et Animations

Le web actuel repose également sur les transitions et les animations. Celles-ci vont des plus simples aux plus complexes et mettent en jeux différentes technologies.

### Transitions CSS

Les transitions CSS sont sans doute les plus simples à comprendre. Prenons un simple bouton qui comporte un changement d'état au survol de la souris. Si nous n'avons pas de transition, le passage entre les deux états se fait immédiatement.

Les transition CSS sont applicables à [une grande variétés de propriétés CSS](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_animated_properties).

```css
.c-button {
  display: inline-block;
  padding: 1.125rem 1.5rem;
  border: none;
  cursor: pointer;

  background-color: #9ccec2;

  font: 500 1rem/1 "Helvetica Neue", "Helvetica", "Arial", sans-serif;
  text-transform: uppercase;
  text-decoration: none;
  letter-spacing: 1px;
  color: #1d4f43;

  transition: all 0.2s ease-in-out;
}

.c-button:hover {
  background-color: #80c2b3;
  color: #184137;
}
```

Les transitions CSS sont faciles à mettre en oeuvre et à manipuler via JavaScript. Elles permettent de réaliser une certaine palette d'effets mais elles ont également leurs limitations:

- les transitions se font toujours d'un état A vers un état B, sans étapes intermédiaires. Pour contrôler plus finement les étapes, il faut se tourner vers les animations CSS.
- les transitions ne peuvent pas effectuer de loop ou d'itération. Si vous souhaitez une animation en boucle ou ayant plusieurs itérations, il faut vous tourner vers les animations.
- les transitions ne sont pas réutilisables, les animations peuvent être appliquées à plusieurs éléments une fois définies.

### Animations CSS

Les animations CSS fonctionnent en spécifiant plusieurs keyframes et les changements désirés pour chacune d'entre-elles.

```css
@keyframes animatebox {
  5% {
    transform: translate3d(15px, 0, 0);
  }
  10% {
    transform: translate3d(-15px, 0, 0);
  }
  15% {
    transform: translate3d(10px, 0, 0);
  }
  20% {
    transform: translate3d(-10px, 0, 0);
  }
  25% {
    transform: translate3d(5px, 0, 0);
  }
  30% {
    transform: translate3d(-5px, 0, 0);
  }
  35% {
    transform: translate3d(0, 0, 0);
  }
  70% {
    transform: rotate3d(0, 0, 0, 0);
  }
  75% {
    transform-origin: 0 100%;
    transform: rotate3d(0, 0, 1, -20deg);
  }
  80% {
    transform: rotate3d(0, 0, 1, 0);
  }
  85% {
    transform-origin: 100% 0;
    transform: rotate3d(1, 0, 1, 20deg);
  }
  90% {
    transform: rotate3d(0, 0, 0, 0);
  }
}

.c-animbox {
  width: 40px;
  height: 40px;
  background-color: red;
  animation: animatebox 2s infinite cubic-bezier(0.165, 0.84, 0.44, 1);
}
```

Ces animations permettent un contrôle plus fin des étapes et du timing. Elles sont également réutilisables une fois définies et peuvent tourner en boucle ou un certain nombre de fois.

### Déclenchement au scroll

Avec l'aide Javascript, les transitions et animations CSS peuvent facilement être [déclenchées via le scroll](http://dogstudio.be).

`intersectionObserver` permet facilement de détecter si un ou plusieurs éléments sont affichés dans le viewport du navigateur pour déclencher des animations lorsque c'est le cas via quelques changements de classes CSS. Voici [une petite démonstration](https://github.com/jeromecoupe/onscroll_css_animations) rapide.

*Exercice: décortiquer le script et voir comment CSS et JS interagissent*

## Animations Javascript

Les animations en Javascript offrent bien plus de contrôle que les animations CSS si vous avez besoin d'interactivité, d'effets poussé ou de séquences d'animations chainées les unes aux autres.

Des librairies telles que [GSAP de Greensock](https://greensock.com/gsap) offrent une grande facilité d'utilisation et permettent de créer des animations complexes avec SVG, HTML ou Canvas. Ces librairies sont extérieures aux navigateurs mais offrent une grande palette de possibilités aux dévelopeurs. En voici un petit [exemple avec un formulaire de login](https://github.com/jeromecoupe/web_animations_demo).

Au niveau des navigateurs justement, Web animation API est un standard qui se développe bien et dont les fonctions de bases bénéficient d'un bon support dans les navigateurs récents. Cette spécification est déjà intéressante à utiliser aujourd'hui et deviendra encore plus importante lorsque le support des navigateurs augmentera pour les fonctions avancées (séquences et timeline). Il est également possible d'utiliser `requestAnimationFrame`, qui est plus complexe à gérer au niveau performance mais vous permet de créer à peu près n'importe quelle animation.

L'animation est devenue une part importante des interfaces et du web en général, en partie parce que nous y sommes habitués sur les plateformes mobiles natives comme iOS ou Androïd.

Comme à son habitude, le web intègre cela et avance en direction d'une expérience utilisateur plus riches dans lesquelles l'animation devient de plus en plus importante.

*Exercice: animations et transitions dans Figma et dans le code*

## 7. Design web: documents de delivery

Afin de présenter les designs web dans tous leurs aspects, [le plus efficace est de le faire à l’aide de prototypes interactifs](https://www.webstoemp.com/blog/to-hell-with-abstract-prescriptive-deliverables/), plutôt que d’utiliser des documents et méthodes plus statiques qui posent problème à de nombreux niveaux.

### Problèmes des documents statiques / uniques

Classiquement, les designs à l’aide de [wireframes](https://dribbble.com/shots/1893359-Exelerate-Wireframes/attachments/322535) statiques qui se transforment finalement en [chartes graphiques statiques détaillées](https://dribbble.com/shots/1874207-Exelerate-Product-view/attachments/317155) réalisées sur Sketch, Figma ou Photoshop. Cette manière de travailler provient du print mais n’est pas toujours adaptée au design web pour diverses raisons.

#### Non prise en compte des spécificités du medium

Ces documents ne sont pas à même de matérialiser efficacement les spécificités du medium Internet que sont l’interactivité (survol des boutons, menus déroulant, accordéons, slideshows, animations, etc.), l’adaptation aux diverses tailles d’écran et résolutions (desktops, tablettes, mobiles, écrans haute résolution, etc.) et l'adaptation aux capacités du navigateur ou du terminal utilisé.

#### Représentation irréaliste du produit fini

De tels documents donnent une fausse image du produit fini. On habitue ainsi le client à voir une version "irréaliste" de son futur site.

La résolution des documents imprimés est plus élevée qu’un affichage sur écran, les pages sont présentées dans leur entièreté alors que, dans un navigateur, seule une petite portion en sera visible à la fois, les polices n’ont pas du tout le même rendu à l’écran.

Enfin, ces documents donnent l’impression que le site aura toujours le même rendu. Or, selon les navigateurs utilisés, un site n’a pas toujours la même apparence ni les mêmes comportements.

#### Dissociation des aspects de design et des aspects techniques

L’utilisation de documents statiques favorise une déconnexion entre le design et le code, entre l’expérience utilisateur et les moyens techniques permettant de la réaliser. Cette fracture cause de nombreuses pertes de temps, de malentendus et de frustrations entre développeurs et designers.

### L’avènement des documents dynamiques

Pour ces diverses raisons et depuis un certain temps déjà, les web designers cherchent à travailler de façon plus rapide et itérative, en utilisant des documents moins lourds à produire, permettant des cycles de feedback plus fréquents et plus rapides et créant de ce fait une dynamique dans laquelle le client / commanditaire est plus impliqué.

#### Content prototypes

Pour ce qui est des contenus, de simples "[content prototypes](https://thomasbyttebier.be/blog/the-bold-beauty-of-content-prototypes)" réalisés en HTML brut permettent aux copywriters de travailler, à l'équipe d'avoir une référence mise à jour et au client de valider le copy.

Les avantages sont multiples:

- ces prototypes sont mobile first et permettent de tester la hiérarchie des contenus la data structure des différentes pages / vues et éléments
- une fois en ligne, ces prototypes peuvent être consultés et modifiés par tous
- les patterns de navigation et la forme des divers contenus peuvent être testés rapidement

#### Moodboards and elements collages

Plutôt que de fournir au client des “mockups” sur Sketch, Figma ou Photoshop dans lesquels les moindres éléments des pages sont spécifiés, il est plus facile et plus rapide d’explorer diverses pistes graphiques à l’aide de ce que Dan Mall appelle des "[elements collages](http://v3.danielmall.com/articles/rif-element-collages/)".

De tels elements collages ou [moodboards](https://thomasbyttebier.be/blog/mood-boards-in-a-content-first-design-process) peuvent être produits relativement rapidement pour réaliser quelques itérations autour de concepts intéressants et d'éléments centraux du site / de l’application. Présenter les choses sous forme d'une longue page web permet aussi d'utiliser des videos ou un peu de JavaScript pour présenter des concepts plus interactifs ou dynamiques.

Sketch, Figma ou Framer sont encore présents dans le processus, mais la philosophie change.

Il ne s'agit plus de produire des designs finalisés mais de pouvoir rapidement tester et valider des idées pour ensuite pouvoir travailler de façon itérative et collaborative.

### Designers hybrides

> [the design process] is about designing, prototyping and making. When you separate those, I think the final result suffers."

> Jonathan Ive, March, 2012

Cette phrase de Jonathan Ive pourrait sans problème être appliquée au web d’aujourd’hui, dans lequel le design, la création de prototypes et la réalisation technique sont de plus en plus intimement liés.

#### Les designers web doivent ils coder?

Pas forcément, mais cela aide beaucoup et cela permet de gagner du temps. Au minimum, designers et dévelopeurs doivent collaborer étroitement et avoir une bonne connaissance des modes de travail et défis rencontrés par les uns et les autres est primordial.

Le travail des designers web à grandement évolué: nous devons maintenant créer des systèmes modulaires et flexibles et plus des interfaces fixes dans photoshop. Le nombre d’inconnues et d’éléments entrant en ligne de compte dans un site ou une application Internet ne cesse d’augmenter.

Cela requiert des changements dans les processus et workflow utilisés mais aussi une plus grande collaboration et un dialogue plus étroit entre les différents intervenants

> You must also address the very human issue of communication. Earlier and more frequent collaboration among team members and the client must become the rule in your workflow, not the exception. Content, design, and development team members must review and collaborate regularly at every stage in the creation process until the site is live. We can’t ‘throw it over the wall’ anymore— at least, not if we want our sites to be excellent. There are simply too many moving parts now. Go forth and collaborate.

> Drew Clemens - [Design process in the responsive age](https://www.smashingmagazine.com/2012/05/design-process-responsive-age/) - Smashing Magazine
