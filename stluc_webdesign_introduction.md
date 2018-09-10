# Introduction au web design

## Comment fonctionne Internet ?

"Aller sur Internet" la phrase est courante mais ne peut pas être plus dénuée de sens. Personne ne va nulle part!

Lorsque vous lancez votre navigateur et vous tapez une URL ou que vous suivez un lien, vous envoyez une requête vers un serveur web qui, comme le nom l'indique, va "servir" à votre navigateur les fichiers composant le site ou l'application que vous cherchez à utiliser.

Il y a un certain nombre de ces serveurs dans le vaste monde ... comment votre requête va-t-elle être dirigée vers le bon et ce depuis n'importe où? C'est le rôle d'un autre type de serveur dédié au routing: les serveurs DNS (Domain Name Server). Ces serveurs DNS vont transcrire le domaine de votre requête en une adresse IP numérique et former une chaîne pour trouver le serveur web ayant l'adresse IP correspondante et lui transmettre votre requête. Chaque machine connectée à Internet possède une adresse IP unique.

Une fois la connection établie entre le serveur web et vous, les serveurs DNS ont joué leur rôle, jusqu'à ce que vous fassiez une autre requête vers un autre nom de domaine.

*Exercices: nslookup et traceroute / tracert*

"Aller sur Internet" c'est envoyer, via votre navigateur, une requête vers un serveur web qui va vous renvoyer des fichiers HTML, CSS, JS ainsi que des assets (images, fontes, videos, etc.) que votre navigateur va lire et interpréter pour composer la page que vous voyez et avec laquelle vous pouvez interagir. Il y a donc un client (votre navigateur et la machine sur laquelle il tourne) et un serveur (le serveur web qui vous sert les fichiers) qui peut également être connecté à une base de données.

Nous nous concentrerons essentiellement ici sur les technologies **front-end**, c'est à dire celles qui sont utilisées par votre navigateur. Il s'agit principalement de HTML, CSS, et Javascript. Chacune de ces technologies est suffisamment complexe que pour que certains frameworks ou languages facilitant la vie des développeurs aient été écrits (Sass, Less, Vue, React, Angular, Ember, etc.).

Le monde du **back-end** est celui de la logique qui se produit côté serveur et qui sert essentiellement à fournir des données au site ou à l'application que vous utilisez. Ces données sont fournies par une base de données ou par des API (Application Programming Interface). Les technologies du back-end sont des langages de programmation comme Ruby, PHP, Python, Go, Node et des frameworks qui y sont liés (Rails, YII, Laravel, Django, etc.).

Les frameworks sont en quelque sorte des boites à outils pour les dévelopeurs, qui sont construites sur base de divers languages back-end ou front-end. Si vous voulez une analogie, c'est un peu comme disposer de Lego Technics. Ces frameworks aident les développeurs à construire des sites ou applications plus complexes.

N'oublions pas non plus l'infrastructure: les bases de données (MySQL, PostGresSQL, MongoDB, etc.), les serveurs web eux-mêmes comme Apache, NginX ou encore UNIX et Linux, qui sont les OS sur lesquels tournent la plupart d'entre eux.

## Technologies front-end

Comme dit plus haut, les technologies front-end sont principalement au nombre de trois: HTML, CSS et Javascript. Chacune de ces technologies est passée par de multiples évolutions et change constamment encore aujourd'hui.

Ces technologies sont disponibles pour tous et sont des standards ouverts à l'élaboration desquels participent des académiques, des chercheurs mais aussi des représentants des principaux acteurs d'Internet comme les sociétés conceptrices des divers navigateurs. Le [W3C](https://www.w3.org/) est l'entité responsable de la conception, de l'évolution et de la publication de ces standards.

### HTML: structure et sémantique

[HTML](https://www.w3.org/standards/techs/html) (Hypertext Markup language) est la language de markup du web qui défini la structure et la sémantique des éléments qui composent une vue ou un document.

Grâce aux balises et aux attributs c'est lui qui indique la langue du document, le set de caractères utilisé et qui défini quel texte est un titre, un paragraphe, une liste, etc. C'est le premier document qui est chargé par les navigateurs et qui lie et affiche les fichiers externes tels que les images, les icônes, les vidéos, les sons, etc.

Ce sont également les fichiers HTML qui définissent quelles feuilles de styles CSS et fichiers Javascript doivent être utilisés pour le rendu de la page ou de la vue.

HTML est un langage déclaratif de markup qui fonctionne par emboitement hiérarchisé (DOM) un peu comme des Matrioshka Russes. Outre la balise `<html>`, la balise `<head>` referme les meta-informations sur un document ou la vue (langue du document, charset, titre, CSS liée(s), etc.), tandis que la balise `<body>` renferme les contenus du document ou de la vue.

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

CSS est un langage déclaratif qui fonctionne selon les principes de cascade, de spécificité et de poids pour déterminer quels styles s'appliquent à quels éléments.

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

*Exercice: sélécteurs de type et de classe comme sélecteurs les plus courants*

*Exercice: expérimenter avec cascade, spécificité et poids*

Si le sujet vous intéresse, Mozilla Developer Network (MDN) possède [un très bon guide en français qui vous permettra de débuter avec CSS](https://developer.mozilla.org/fr/docs/Web/CSS).

### Javascript: scripting, interactivité et programmation

[Javascript](https://www.w3.org/standards/webdesign/script) est le language de programmation côté client permettant de scripter le navigateur pour créer des interactions complexes et utiliser les API du navigateurs ou des API externes. Au départ un langage de scripting, l'évolution actuelle de Javascript tend de plus en plus vers un langage de programmation à part entière qui peut aujourd'hui également être utilisé côté serveur ([Node](https://nodejs.org/en/)).

De nombreux sites ou applications ont également porté une grande partie de la logique vers le côté client. C'est particulièrement vrai pour tout ce qui est Single Page Applications (SPA). Ces dernières font usage de frameworks JavaScript (React, Vue, Ember, Angular, etc.) permettant de gérer les différents états (states) d'une application et d'avoir des composants qui y répondent.

```js
window.addEventLister("load", function() {
  alert("Hello Javascript");
});
```

*Exercice: inspecter le code d'une page web et montrer les divers types de code*

*Exercice: faire un premier projet web avec un fichier HTML, un fichier CSS, un fichier JS*

Si le sujet vous intéresse, Mozilla Developer Network (MDN) possède [un très bon guide en français qui vous permettra de débuter avec JavaScript](https://developer.mozilla.org/fr/docs/Web/JavaScript).

### Assets et fichiers externes

En plus du code HTML, CSS et JavaScript, votre navigateur reçoit également bon nombre de fichers externes tels que des images, des videos, des fichiers sons, des fichiers de polices, etc.

Ces fichiers ne sont pas contenus dans le code HTML, CSS ou JavaScript mais sont appellés comme des fichiers externes pour être intégrés au rendu de la vue ou de la page.

*Exercice, voir l'onglet "network" dans Google Chrome.*

### Images

Commençons par les images. Sur le web, les formats les plus utilisés sont:

- JPG: utilisé pour les images de type photographique, pas de transparence, lossy
- GIF: utilisé pour les images avec aplats de couleurs, transparence simple, animations frame par frame, lossy. GIF est un format de moins en moins utilisé depuis l'avènement de PNG et de SVG
- PNG: utilisé pour les images avec aplats de couleurs, transparence simple et transparence d'alpha, lossy.
- SVG: format vectoriel, est une sorte de mini-document qui peut être scripté et manipulé par CSS lorsqu'il est intégré au document (inline), lossless.
- WEBP: format encore en dévelopement mais qui permet d'avoir des fichiers moins lourds et d'utiliser des algorithmes de compression lossless et lossy.

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

Tous les navigateurs web ne supportent pas les mêmes formats video. Pour être certain de pouvoir être vue par l'ensemble des navigateurs modernes, votre video doit donc être disponibles en plusieurs formats. Actuellement MP4 et WEBM sont suffisants.

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

Aujourd'hui, il est possible de charger des fichiers de polices et de demander au navigateur de les utiliser pour le rendu. Les problématiques sont maintenant d'ordre technique (hinting, optimisation) et de licences (les fichiers de polices pouvant être facilement téléchargés, ils sont difficiles à protéger). C'est pour répondre à ces deux problèmes que des services de distribution de polices (Typekit, Google fonts, Fontdeck) ont été créés.

*Exercice: intégrer une police custom à un projet HTML/CSS*

## Design Web: spécificités du medium

Le design print est un domaine qui a déjà derrière lui des centaines d'années d'existence et qui a intégré une série de règles, de canons et de bonnes pratiques qui, pour la plupart, prennent pour base le canevas du projet et les possibilités techniques au niveau de l'impression. Il est en général facile d'avoir une bonne idée du contexte dans lequel le produit va être utilisé et ous sommes façe à un médium qui est statique.

Avec le print, nous sommes donc dans un envrionnement de design statique et dont les paramètres sont connus et maîtrisés de bout en bout. Le designer contrôle parfaitement tous les aspects de son projet.

Il en va tout autrement pour le web et le digital en général, comme l'explique fort bien John Allsopp dans son article "[A Dao of Web Design](https://alistapart.com/article/dao)":

> The control which designers know in the print medium, and often desire in the web medium, is simply a function of the limitation of the printed page. We should embrace the fact that the web doesn’t have the same constraints, and design for this flexibility. But first, we must “accept the ebb and flow of things”.

> "[A Dao of Web Design](https://alistapart.com/article/dao)" - John Allsopp, 2000

Accepter la flexibilité du medium se traduit par une impossibilité de tout contrôler.

En tant que designer, il nous faut se réconcilier avec les inconnues inhérentes au web et les apprivoiser, les intégrer dans notre travail.

Depuis les débuts du web, les designers digitaux ont du réinventer leur métier et mettre en place des outils, workflows et stratégies pour aborder un medium qui lie contenus et interactivité dans un contexte fluide où les inconnues sont nombreuses.

### Entre contenus et interactivité

Comme avec le print, le design digital vise à présenter des contenus de nature diverses mais ajoute une dimension d'interactivité, au niveau des types de contenus (son, videos, animations, etc) comme au niveau des objectifs (acheter un billet d'avion, faire une réservation, etc.).

Bref, le design digital est un continuum entre contenus et interactivité. Chaque site ou application est par essence un mélange des deux, dans des proportion diverses.

- Site de presse: site axé sur les contenus et donc vers la trasmission d'informations (articles, recettes, opinions, etc). Certains aspects applicatifs sont néanmoins présents et visent à faire accomplir des tâches aux utilisateurs: moteur de recherche, abonnement, espace membres, etc.
- Site bancaire: site axé sur l'applicatif et donc la réalisation de tâches (transferts, téléchargement de documents). Certains aspects de contenus et de transmission d'information sont présents également: conditions générales, présentation des formules de prêts, consultation des soldes, etc.

Ces deux aspects sont toujours présents dans un site web et doivent tous deux être pris en compte à divers niveaux:

- **Stratégie**: quels sont les objectifs en termes de transission d'information / d'accomplissement de tâches?
- **Contenus**: quels contenus doivent être mis en place? Quels types de contenus vont au mieux servir les objectifs du site (blogposts, tutoriax, videos, etc.)? Quelles sont les ressources disponibles pour publier et à quelle fréquence?
- **Interactivité**: quelles interactions avec le site doivent être créées? Comment les rendre visibles et attractives pour les utilisateurs? Quelles ressources sont disponible pour le support et les tests utilisateurs?
- **Structure**: quelle va être l'architecture d'information? Quelles seront les structures de données des contenus? Quels sont les flux utilisateurs, les diverses étapes dans la réalisation de chaque tâche et comment les structurer pour que chaque étape soit simple et pour le que nombre d'étapes soit le plus bas possible?
- **Présentation**: comment la présentation va-t-elle soutenir les autres dimensions? La présentation sert-elles les diverses audiences?

### Design for the unknown

#### Première inconnue: le canevas

En print, le format, le support, le canevas du produit fini est connu. Il s’agit d’une affiche de telle dimensions, d’une brochure en format A5 de 20 pages, etc. Il en va tout autrement sur le web où le concept même de canevas sur lequel baser un design disparait devant la diversité des supports sur lesquels les sites et applications doivent fonctionner (tailles, résolutions et orientations d’écrans, etc.).

Si nous ne pouvons plus baser nos designs sur le canevas, nous devons alors [partir des contenus](https://markboulton.co.uk/journal/a-richer-canvas) pour designer non plus des pages mais bien des [systèmes de composants flexibles](http://styleguides.io/) pouvant s’agencer de diverses façons pour occuper et s’adapter à un maximum de canevas possibles.

*Exercice: spotify en téléphone, tablette, desktop*

#### Deuxième inconnue: les capacités du navigateur et du terminal

En print, une fois un design créé, son rendu est contrôlable et contrôlé de bout en bout: de la conception jusqu’à l’impression finale.

En web, tout passe par deux canaux que le concepteur ne contrôle pas et dont vont largement dépendre l'expérience utilisateur: le navigateur et le terminal sur lequel celui-ci est hébergé. Là aussi, nous avons affaire à une large diversité de capacités: capacités tactiles, bande passante, support images, support vidéos, support CSS, support javascript, gyroscope, appareil photo, géolocalisation, etc.

Lorsque nous envisageons des solutions de design, nous devons tenir compte de cette seconde inconnue. Dans l’industrie, on se réfère souvent au concept de "[progresssive enhancement](https://resilientwebdesign.com/chapter6/)" selon lequel on va d’abord se concentrer sur le fait de délivrer une bonne expérience utilisateur de base, que l’on va enrichir pour les navigateurs et terminaux disposant de capacités plus avancées.

*Discussion: [Do websites need to look exactly the same in every browser](http://dowebsitesneedtolookexactlythesameineverybrowser.com/)*

#### Troisième inconnue: le contexte (humain) d’utilisation

Si nous pouvons en général définir assez précisément nos publics cibles (à travers des études de marché, des personas, etc.), le contexte d’utilisation de notre site ou application peut varier grandement et nous est la plupart du temps complètement inconnu.

L’utilisateur mobile peut utiliser son téléphone debout dans son train matinal, être facilement distrait, ne disposer que d’une seule main et d’une connectivité faible. Ce même utilisateur mobile peut utiliser sa tablette, confortablement installé dans le canapé du lobby de son hôtel. Il est dans ce cas très concentré et dispose d’une connexion à haut débit. Les circonstances et le contexte d’utilisation est tout aussi divers pour un utilisateur d’ordinateur fixe.

La solution est ici de toujours center les solutions sur l'utilisateur. Typiquement les projets web impliquent les utilisaturs très tôt dans la définition des solutions envisagées et passent par des cycles d'itérations relativement courts dans lesquels les feedbacks utilisateurs et les tests sont extrèmement importants. Un aspect intéressant du medium Internet étant la capacité d'avoir très rapidement des retours sous forme de données quantitatives et qualitatives (analytics, interviews utilisateurs, tests, etc.).

### Grands principes du design web

Les principales différences entre le design web et le design print ou audiovisuel viennent de ces inconnues et de la nécessité d'y répondre.

#### Mobile first responsive web design

Afin de répondre à la diversité croissante des tailles d'écrans et des résolutions existant sur le marché, un des grands principes est de commencer à designer pour les contraintes maximales, celles des petits écrans de smartphones et des bandes passantes limitées. C'est le principe du "[mobile first](https://www.lukew.com/ff/entry.asp?933)" qui a des implications tant en termes de performance que de mise en page.

Une fois que votre site ou votre application web fonctionne pour ces derniers, vous pouvez petit à petit passer aux écrans de taille moyenne et puis aux écrans plus larges et aux débits de connections pus stables et plus puissantes. L'idée centrale du "Responsive Web Design" lancée par Ethan Marcotte est celle d'un continuum tout au long duqel votre design "répond" à l'espace utile disponible et à la résolution de l'écran.

Les trois pières angulaires du responsive sont:

- **grilles fluides**: d'une grille simple de deux colonnes sur petits écrans, on peut passer à une grille de plus en plus complexe au fur et à mesure que l'espace disponible augmente. Les nouvelles spécifications de layout en CSS (Flexbox et Grid) sont adaptées à cette approche.
- **media flexibles**: pour s'intégrer à une grille fluides, vos media (images, video, etc.) doivent être flexibles et non de tailles fixes. Grâce à quelques règles CSS, il est possible d'adapter la taille de vos media aux containers dans lesquels ils se trouvent.
- **media queries**: le mécanisme CSS grâce auquel le code CSS (layout, typographie, etc) est capable de "répondre" à une grande palettes de paramètres du navigateur client (largeur d'écran, orientation, couleurs, etc.)

Ces principes sont aplliqués au niveau macro (layout global) mais également au niveau micro (composants). Si le layout de votre page réagit à l'espace disponible à l'écran, il en va de même pour une interface de navigation, un footer ou encore à un composant "news" dans un site de presse.

Les media fluides ont également des implications au niveau de la performance. Cela ne sert à rien de charger une image de 1000 pixels de large sur un écran qui en fait 320, même chose pour les videos. Un standard a été développé pour les images responsives avec `srcset`, `sizes`. La balise `<picture>` est à utiliser seulement si des images différentes sont nécessaires pour des raisons de direction artistique. En ce qui concerne les videos, des services tels que Youtube ou Vimeo restent la meilleure option au niveau de la performance. Ces services vont transcoder votre video dans divers formats ainsi que dans différentes résolutions, ce qui vous garantira une compatibilité et des performances maximales.

*Exercice: inspecter quelques sites et applications responsives [Stripe](https://stripe.com/), [Opera de Paris](https://www.operadeparis.fr/), [AirBnB](https://www.airbnb.com/), [Google Drive](https://drive.google.com/)). Prêter attention à la typographie, aux grilles, aux interfaces de navigation, aux images et aux videos*

#### Progressive enhancement

L'idée du progressive enhancement est similaire à celle du Responsive Web Design mais dans le domaine des capacités du navigateur et du terminal. Selon Jeremy Keith dans "[Resilient Web Design](https://resilientwebdesign.com/chapter6/)", cette idée repose sur trois étapes simples:

1. Identifier les contenus ou les fonctionalités principaux / essentiels
2. Rendre disponibles ces contenus ou ces fonctionalités à l'aide des technologies les plus silmples possibles
3. Construire sur cette base en utilisant les technologies plus modernes

Cette philosophie permet de toujours disposer des fonctionnalités ou des contenus essentiels et de passer ensuite du temps à construire des experiences plus raffinées et abouties sur cette fondation solide. Le principe du "Prograssive Enhancement" permet donc de répondre à l'inconnue des capacités du navigateur et du terminal client.

Cette manière de développer et de designer a depuis toujours été mise en pratique au niveau des sites orientés vers les contenus et la transmission d'informations. Avec l'avènement des "[Progressive Web Apps](https://developers.google.com/web/progressive-web-apps/)" (PWA) chères à Google, cette idée fait son chemin au niveau des projets plus applicatifs.

#### User centered design et Design Thinking

Cette méthodologie consiste à se centrer sur les utilisateurs d'un site ou d'une application et leurs besoins tout au long d'un processus de design itératif. A travers des techniques de recherche investigatives (interviews, sondages, shadowing, etc.) et génératives (brainstormings, exercices de groupes, etc.), l'idée est d'en savoir le plus possible sur les utilisateurs, leurs besoins et le contexte d'utilisation du site ou de l'application. De cette phase de recherche on extrait les prérequis et les objectifs du produit, pour ensuite proposer les solutions possibles que l'on va tester avec les utilisateurs pour voir si les objectifs sont remplis.

L'inconnue des contextes d'utilisation couplée aux ressources, budgets et délais importants nécessaires pour créer un site ou une application web font qu'il vaut mieux savoir où l'on va. Toutes les methodologies liées au User Centered Design et au Design Thinking (Lean UX, Design Sprint, etc.) permettent de tester rapidement concepts et prototypes auprès d'utilisateurs réels.

Depuis quelques années, [Thoughtbot](https://thoughtbot.com/) et [Google Ventures](http://www.gv.com/sprint/) ont popularisé un outil: le Design Sprint. L'idée est de passer en 5 jours seulement d'un simple concept à un prototype concret et testé par des utilisateurs.

- jour 1: comprendre les utilisateurs, leurs besoins et leurs contextes (côté utilisateurs) ainsi que les objectifs à atteindre et les KPIs (côté business). Identifier aussi les risques potentiels et les moyens de les réduire.
- jour 2: diverger en proposant (sketch et pitch) différentes solutions possibles aux problèmes et au contexte posés préalablement.
- jour 3: converger en se mettant d'accord sur une ou deux solutions à prototyper
- jour 4: prototyper les solutions en ayant un degré de fidélité juste suffisant que pour pouvoir réaliser les tests utilisateurs
- jour 5: tester le(s) prototype(s) avec des utilisateurs et évaluer

Si vous souhaitez en savoir plus concernant le design sprint, [le petit guide online de Thoughtbot](https://thoughtbot.com/product-design-sprint/guide) est très bien fait et vous donne quelques examples d'activités ou d'exercices à réaliser avec vos clients.

Cette méthodologie forme également une bonne base si vous n'avez qu'un u deux jours à passer sur la phase de recherche.

## Design web en pratique

Après avoir introduit le sujet par un peu de théorie, passons à la pratique. La suite de ce cours se veut être un guide pratique pour réaliser efficacement des designs pour le web, qu'il s'agisse d'un site ou d'une application.

Voici le plan de bataille:

1. Recherche et stratégie
2. Couleurs et palette
3. Typographie
4. Media (images et illustrations, icones, videos, sons, etc.)
5. Layout et mise en page
6. Transitions et animations
7. Livrables pour le design web

## 1. Recherche et stratégie

La phase de recherche vise à cerner les tenants et aboutissants du projet, tant du point de vue des utilisateurs (publics cibles, besoins, contexte) que du business (objectifs, KPI, compétition).

La permière chose à faire est de bien cerner quels sont les publics cibles. Pour cela, rien ne remplace un contact direct avec des utilisateurs ou, à défaut, avec les responsables du support ou du marketting qui sont en contact direct avec les utilisateurs. De simples activités comme un future perfect / pitch, des [proto-personas](https://uxmag.com/articles/using-proto-personas-for-executive-alignment) (voici des [photos utilisables créées par Jason Travis](http://www.jasontravisphoto.com/persona/)) et quelques [job stories](https://jtbd.info/replacing-the-user-story-with-the-job-story-af7cdee10c27) par persona peuvent déjà s'avérer très utiles.

En regard des personas, il importe de se pencher sur les objectifs business. Pour chaque personas, demandez-vous comment votre site ou votre application peut les aider. De manière plus générale, quels sont les indicateurs (mesurables) qui vous permettrons de dire si votre projet à atteint ses objectifs et rencontre les besoins des clients.

Lors de cette phase de recherche, il est bon de se pencher sur la compétition. Quels sont les sites ou les aplications qui répondent aux même besoins? Quels sont leurs points forts et leurs points faibles?

Au niveau du design, deux exercices sont assez utiles.

- *Adjectifs et priorités*: demander à tous de noter sur un post-it trois adjectifs qu'ils souhaitent que les clients ressentent en visitant le site ou en utilisant l'application. Chacun vote ensuite pour deux adjectifs et les trois plus importants sont classés par priorité.
- *Design brief à l'instinct*: rassembler 15 à 20 sites ou applications avec des styles graphiques très différents. Ces exemples sont passés en revue et chacun donne une note de 1 à 5. Une fois les moyennes établies, discuter des 3 premiers et des trois derniers vous donnera un bon design brief.

Les dernières choses à aborder tiennent à la structure générale de l'application ou du site. Une architecture d'information et / ou des [wireflows](https://dribbble.com/shots/2248785-Web-Wireframes-UX-Flow/attachments/420198) réalisés en petits groupes peuvent vous donner une bonne approximation de la structure souhaitée. Il s'agit d'un élément important dans la mesure où il va être matérialisé par les interfaces de navigation qui sont une contrainte importante au niveau du design.

*Exercice: phase de recherche pour le site de l'ESA Saint Luc: publics cibles, proto personas, job stories, adjectifs, design brief*

## 2. Couleurs

Ici, il vous faudra faire preuve de mesure. Dans la plupart des cas, une couleur principale (déclinée) et une couleur d'accent (déclinée également) ainsi qu'une gamme de gris (basés sur votre couleur principale) pour les couleurs neutres suffiront largement. Certaines applications ou sites ont des palettes de couleurs plus étendues mais il est préférable de rester le plus simple possible.

Commencer par choisir une couleur principale en rapport avec votre branding ou qui vous plait. Pour le choix de la couleur complémentaire, des outils peuvent vous aider, comme [Adobe Color CC](https://color.adobe.com/create/color-wheel/) ou [Coolors](https://coolors.co/). Pensez également à aller faire un tour sur [Dribbble](https://dribbble.com/colors/3116EF) et à utiliser l'outil de recherche par couleur pour immédiatement avoir un grand choix de couleurs complémentaires.

Une fois que vous avez deux (maximum trois) couleurs complémentaires, vous pouvez utiliser votre application de design favorite et [des techniques reposant sur des layers](https://www.smashingmagazine.com/2017/07/advanced-color-palettes-photoshop-sketch-affinity-designer/) pour démultiplier vos options tout en restant dans la gamme. Il vous reste ensuite à déterminer une gamme de gris contenant votre couleur principale et vous voilà paré.

Une autre méthode efficace pour cérer une palette de de couleurs harmonieuse consiste à partir de photos de paysage / de nature. Adobe Color CC possède une fonction qui vous y aidera.

Un dernier conseil, [évitez le noir pur dans vos palettes](https://ianstormtaylor.com/design-tip-never-use-black/). Afin dêtre dans la gamme partez plutôt de votre couleur de base et saturez-là pour obtenir une couleur proche du noir mais contenant votre couleur de base.

*Exercice: créer une palette de couleurs simple*

## 3. Typographie

Comme le dit fort justement Oliver Reichenstein, [le texte compose 95% d'un site web ou d'une application](https://ia.net/topics/the-web-is-all-about-typography-period). La typographie est donc une étape importante dans la conception de tout produit digital. Comme nous l'avons vu plus haut, nous disposons désormais d'une grande variété de polices avec `@font-face` et les services de distribution de fontes tels que [Google Fonts](https://fonts.google.com/) ou [Typekit](https://typekit.com/).

Se pose donc la question du choix des fonts à utiliser pour un projet donné. Comment faire un choix pertinent?

### Choisir une ou plusieurs polices

Pour commencer, il est important de poser des limites. Les fichiers de polices sont des ressources externes et charger une police, une graisse ou un style supplémanetaire ajoutera au poinds de vos pages. En général on travaillera donc avec une ou deux polices maximum et un nombre limité de variantes en terme de graisses et de styles.

*Exercice: Google Font et poids des fichiers de police*

Votre premier choix devra sans doute être la police que vous utiliserez pour votre corps de texte. Il vous faut une police solide et de lisible qui permettra aux autres éléments textuels importants (titres, calls to action) de ressortir. Préférez des polices avec une x-height élevée et peu de fioritures. Soyez également attentif à ce que la police choisie possède plusieurs graisses et variantes (au moins bold et italique). Les polices avec plusieurs graisses sont intéressantes de par la variété potentielle qu'elles proposent.

Si vous vous posez des questions, regardez simplement dans quel but ou contexte la police que vous considérez a été dévelopée, explorez son histoire. Des services tels que Typekit ou Google fonts vous donnerons des reseignements précieux. Ces services possèdent également des spécimens qui vous permettrons de mieux appréhender les caractéristiques des divers fontes proposées. Allez également faire un petit tour du côté des sites tels que [Typewolf](https://www.typewolf.com/), [Fonts in Use](https://fontsinuse.com/) ou [Dribbble](https://dribbble.com/).

Un exercice difficile en typographie consiste à trouver plusieurs polices qui vont fonctionner ensemble dans un design. Une fois votre police de coprs de texte choisie, vous avez plusieurs options:

- **Superfamilies**: certaines polices forment une famille de polices et sont designées comme telles. Elles contiennent souvent des polices différentes (serif et sans-serif par exemple), utilisables à différentes tailles (caption, display, etc.) ou ayant différentes approches / kernings (Normal, Condensed, Extended). En voici quelques exemples sur Typekit: Calluna et Calluna Sans, Freight Text et Freight Sans, etc.
- **Designer / Fondrie identique**: voici un raccourci par rapport au point suivant. En général, des polices même différentes au premier regard on pas mal de caractéristiques communes si elles sont designées par la même personne ou la même fondrie. Pensez donc à aller voir de ce côté lorsque vous cherche un accord entre deux polices.
- **Caractéristiques communes**: cherchez des polices qui sont suffisemment différentes que pour êtres distinguées l'une de l'aure facilement mais qui ont des caractéristiques communes (formes des lettres, x-height, etc.) ou qui ont été développées dans un même contexte ou selon un conceopt similaire.
- **Outils**: des outils et services tels que Google Fonts ou Typekit vous proposent des pistes intéressantes pour le font pairing. N'hésitez pas non plus à inspecter des sites que vous appréciez au niveau typographique.

*Exercice: Voici [quelques](http://femmebot.github.io/google-type/) [exemples](http://hellohappy.org/beautiful-web-type/) de typographies réussies avec Google fonts. Analysons-les.*

Une fois vos polices choisies, l'étape suivante consiste à mettre en place une échelle typographique et un rythme vertical. Pour ce qui est de l'échelle typographique, vous pouvez-vous appuyer sur "[Modular Scale](https://www.modularscale.com/)" un outil développé par [Tim Brown](http://tbrown.org/). Pour ce qui est du rythme vertical (nous y reviendrons), le plus facile est de prendre un échelle à laquelle vous allez vous tenir pour ce qui est de l'interligne et de tous les espaces verticaux. Les échelles les plus populaires sont les échelles [de cinq](https://guides.area17.com/design-techniques/#baseline-grid), de six ou de [huit](https://themefoundation.com/vertical-rhythm-responsive-typography/).

Personellement, [je ne souscris pas forcément à une grille stricte](http://jasonsantamaria.com/articles/baseline-grids-on-the-web) (baseline grid) difficile à maintenir sur un médium aussi fluide que le web . Par contre, je suis attentif à avoir un rythme vertical aussi cohérent que possible en essayant que tous les espacements verticaux ainsi que les hauteurs de lignes soient des multiples de l'échelle de base.

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

*Exercice: chercher 5 compositions typographiques sur Dribble et expliquer quels sont les outils utilisés*

*Exercice: utiliser la typographie et Google fonts pour designer les divers éléments d'un blogpost et des paroles d'un track de hip-hop, d'abord dans Figma et puis dans le code*

## 4. Media: Images, Icônes, Video et Sons

Outre le texte, images, illustrations, icônes et autres média plus interactifs tels que les sons ou les videos font aujourd'hui partie intégrante d'une experience web. Ces media sont des fichiers externes appellés par les fichiers HTML, CSS ou JS.

*Exercice: voir les assets dans une page web via l'onglet Network des developer tools*

### Icônes

Après être passé par diverses transitions (images, icon fonts, etc.) les icones utilisées aujourd'hui sont dans un format vectoriel appellé SVG (Scalable Vector Graphics).

Les fichiers SVG sont des fichiers textes qui ressemblent à du HTML et peuvent être liés comme une image et se comporter comme telle ou bien être intégrés au document, ce qui offre les avantages d'être manipulable directment par JS ou CSS, ce qui permet de leur appliquer des transitions ou des animations.

Généralement, ces fichiers vectoriel sont exportés à partir de Figma, Sketch ou Illustrator et optimisés. Ils sont ensuite intégrés aux pages / vues.

*Exercice: exemple de fichier SVG*

*Exercice: faire une transition avec une icone dans un lien*

### Images et illustrations

Images ou illustrations sur le web peuvent être soit des contenus (chargées depuis la page HTML) soit décoratives (chargées depuis CSS ou JS). Dans tous les cas, ce sont des assets lourds à charger, il faut donc les optimiser au mieux, en terme de format (choisir le format le moins lourd en regard de la nature de l'image) comme en terme de poids (optimisation).

*Exercice: comparer fichier optimisés et non-optimisés*

#### Images de contenus (HTML)

Les imgages de contenus peuvent être dans divers formats comme vu plus haut. Les images comme éléments de contenus peuvent être fluides (layout) mais également responsives (performance) pour charger un fichier différent suivants les résolutions ou les tailles d'écran.

Pour rendre une image fluide au niveau du layout, il suffit de spécifier que sa largeur maximum est 100% de son container parent. Il faut pour cela que ses dimensions soient plus importantes que la largeur maximale de son parent.

```css
/* image fluide */
.o-fluidimage {
  max-width: 100%;
  vertical-align: middle;
}
```

Si vous souhaitez des hauteur et largeurs variables sans distordre l'image, vous pouver utiliser la propriété `object-fit`, [dont Jen Simmons propose une démo](https://labs.jensimmons.com/2016/examples/object-fit.html), comme suit:

```css
/* image fluide */
.o-fitimage {
  width: 100%;
  height: 100%:
  object-fit: cover;
}
```

Si CSS peut règler les choses sur le plan de la mise en page, il est contre prodcutif de charger une grande image si la page ou vue est affichée sur un petit écran comme celui d'un smartphone. Grâces aux [images responsives](https://www.smashingmagazine.com/2014/05/responsive-images-done-right-guide-picture-srcset/) et à `srcset`, `sizes`] et `<picture>`, le bavigateur fait une grande partie du travail pour vous.

Uitliser `srcset` et `sizes` si vous souhaiter servir une image identique mais à des tailles différentes suivant la résolution et la taille d'écran.

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

Si vous souhaiter charger une iamge différente (cadrage, orientation, etc) suivant les tailles d'écran, il vous faudra utiliser l'élement `<picture>`.

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

*Exercice: responsive image et Network panel dans les outils de dévelopement*

### Images de background

Les images sont également utilisées comme élements de background des divers éléments (boites) qui composent une page ou une vue. Ces images de background peuvent avoir différentes caractéristiques définies par CSS (répétées ou pas, positionnées, superposées, mises à l'échelle, etc.), ce qui en fait des composants importants de n'importe quel design.

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

*Exercice: réaliser une banner avec des images de background dans Figma et en code*

### Effets: filtres et masques

Les dégradés, les filtres, les masques et les blend modes sont également très utilisés pour ajouter des effets aux designs web.

Commençons par [les dégradés](https://developer.mozilla.org/fr/docs/Web/CSS/Utilisation_de_d%C3%A9grad%C3%A9s_CSS) qui peuvent être créés très silmplement en CSS, qu'ils soient radiaux ou linéaires.

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

Les proprités `background-blend-mode` et `mix-blend-mode` permettent de modifier vos images de façon importante, comme vous le feriez avec des calques dans une application graphique. `background-blend-mode` se charge faire un blend mode entre deux backgrounds, tandis que `mix-blend-mode` est utilisé pour gérer un blend mode entre un élement et un autre.

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

Clipping et masking puvent également aider à apporter un peu de variété à vos images. Ces deux principes se ressemblent en ce qu'ils servent tous les deux à cacher certaines parties d'un élement. Le support au niveau des navigateurs n'est pas identique mais [voici une page de test par Yoksel](https://codepen.io/yoksel/full/fsdbu/) pour vérifier par vous mêmes.

- masques: sont des images. Avec `mask-mode: luminance;` les parties noires du masque sont cachés, les parties blanches sont visibles. Avec `mask-mode: alpha;` les parties opaques du masque sont visibles et les parties transparentes cachées.
- clips: sont des formes. ce qui est à l'intérieur de la forme est visible

```css
/* appliqué à une <img> */
.masked {
  mask-image: url(../img/masks-scribbles.svg);
  -webkit-mask-image: url(../img/masks-scribbles.svg);
  mask-repeat: no-repeat;
  -webkit-mask-repeat: no-repeat;

}
```

```css
/* appliqué à une <img> (ne fontionne qu'avec un svg interne pour Safari, Chrome et Opera) */
.clipped-svg {
  clip-path: url(../img/clip.svg#myClip);
  -webkit-clip-path: url(../img/clip.svg#myClip);
}
```

```css
/* appliqué à une <img> */
.clipped-polygon {
  clip-path: polygon(20% 0%, 0% 20%, 30% 50%, 0% 80%, 20% 100%, 50% 70%, 80% 100%, 100% 80%, 70% 50%, 100% 20%, 80% 0%, 50% 30%);
  -webkit-clip-path: polygon(20% 0%, 0% 20%, 30% 50%, 0% 80%, 20% 100%, 50% 70%, 80% 100%, 100% 80%, 70% 50%, 100% 20%, 80% 0%, 50% 30%);
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

*Exercice: expérimenter avec filtres, blend modes, clipping et masques dans Figma et en code*

### Videos

Nous avons vu comment intégrer des videos dans vos documents HTML5. Ces videos peuvent être des éléments de contenu mais peuvent également être [utilisées de façon créative](https://www.nurturedigital.com/) [comme éléments de layout](https://www.kikk.be/2017/) sous forme de petites boucles simples. Les vidéos HTML5 offrent l'avantage d'être bien plus contrôlables via des attributs et une API video scriptable en JavaScript.

Par contre, les services tels que Youtube et Vimeo encodent et en servent automatiquement les videos en différentes résolutions et formats suivant le navigateur et la machine utilisées. Ils utilisent également des CDN qui améliorent encore les performances en faisant en corte que leserveur qui vous transmet la vidéo se trouve géographiquement le plus près possible de vous.

Les videos HTML5 comme les videos servies via une `<iframe>` par des services tels que Youtube et Viemo peuvent facilement être rendues fluides et s'adapter à des layout responsive.

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

*Exercice: expériementer avec des videos*

## 5. Layout: Grilles et outils CSS

En design, les grilles sont un outil essentiel. Elles vous permettent de structurer vos contenus et de créer des mises en page complexes et structurées dont les élements sont connectés les uns au autres par une structure sous-jascente.

  > Nothing could be more useful to reach our intention than the Grid. The grid represents the basic structure of our graphic design, it helps to organize the content, it provides consistency, it gives an orderly look and it projects a level of intellectual elegance that we like to express.

  > Massimo Vignelli. The Vignelli Canon

### Rythme horizontal et colonnes

En venant du print et de ses canevas fixes, la question se pose naturellement, comment créer une grille alors que le canevas global change constamment?

La réponse est la même que pour le reste: vos grilles doivent être fluides. La technique la plus utilisée est de garder des gutters fixes, tandis que la largeur et le nombre de colonnes change. Là où un design sur petits écrans utilisera une grille de 2 ou 3 colonnes maximum, un design sur un grand écran peut utiliser 8, 10, 12 ou 16 colonnes par exemple.

*Exercice: reconstruire la grille du [New York Times](nytimes.com)*

*Exercice: reconstruire la grille de [Steele Brand Co](https://dribbble.com/shots/2899485-Steele-Brand-Co/attachments/600278)*

Il existe deux grandes méthodes pour créer ces grilles:

- **Grilles content out**: grilles designées à partir des contenus et des contraintes du projet (publicités, unités typographiques, longueur de lignes, etc.)
- **Grilles canvas in**: partir de vos différents breakpoints et designer plusieurs grilles.

Ces grilles peuvent être de différents types:

- **Grilles symétriques**: toutes les colonnes sont de même taille. Vous avez la possibilité de combiner deux grilles pour plus de variété (une grille de 10 et une grille de 12 par exemple)
- **Grilles asymétriques**: certaines colonnes sont de différentes tailles, à nouveau en se basant sur les contraintes du projet ou certaines éléments (menu latéral, compound grids)

Les grilles les plus courantes sur le web sont des grilles symétriques, souvent de 12 colonnes car 12 offre l'avantage d'être divisible par 2, 3 ou 4.

Si un nombre de colonnes pair comme 8, 10, 12 ou 18 apporte un grand équilibre et une grade symétrie, ce genre de grilles peut parfois être ennuyeux. Les grilles ayant un nombre de colonnes impair 5, 7, 9 sont légèrement plus difficile à maîtriser mais apportent un dynamisme intéressant.

En parlant de dynamisme, n'oubliez pas que vous pouvez avoir des grilles sans gutter ou encore laisser des colonnes vides dans vos designs.

- Grilles fluides simples (5, 7, 10, 12, etc)
- Grilles fluides proportionnelles

*Exercice: design d'une grille responsive symétrique pour trois tailles d'écran*

*Exercice: design d'une grille responsive asymétrique pour trois tailles d'écran*

### Rythme vertical et grilles typographiques

Le rythme vertical d'une page est important. En print, cela se traduit souvent par une baseline grid ou grille typograohique stricte. Sur le web, une telle grille stricte est peu pratique pour les raisons suivantes:

- ces grilles sont techniquement fragiles et difficile à implémenter avec succès
- certains éléments ne respectent pas ces grilles et ont parfoi des ratio standards (images, videos, etc)
- ces grilles sont faites à l'origine pour les grandes pages de spread dans les magazines, etc. Il n'y a jamais autant d'espace sur le web.

Plutôt que de faire tout correspondre à une baseline grid stricte, l'idée est plutôt de créer un rythme vertical en ayant une échelle stricte pour tous les espacements verticaux. Certains adoptent une grille de 10, d'autres une grille de 8 ou de 6. Encore une fois, tout dépend de vos contraintes et de votre typographie.

*Exercice: rythme vertical et typographie pour trois cartes côte à côte*

### Outils CSS au niveau du layout

Au niveau du code, disposer de véritables outils de layout pour le web est assez récent. Après avoir été obligés d'employer diverses méthodes plus ou moins orthodoxes (tableaux et gif transparents, floats, inline-block, etc.) CSS dispose désormais de deux outils de layout dignes de ce nom: Flexbox et Grid.

- **Flexbox**: gère une seule dimension (verticale ou horizontale), fonctionne à partir des caractéristiques des contenus pour gérer leurs répartition dans un container.
- **Grid**: gère deux dimensions (verticale et horizontale), fonctionne à partir des caractéristiques d'une grille dans laquelle les contenus sont placés.

Ces deux outils de layout font en outre appel au [module de Box Alignment](https://www.w3.org/TR/css-align-3/). Vous retrouverez donc des propriétés d'alignement communes à Grid et à Flexbox.

#### Flexbox

Flexbox est appliqué gâce à la propriété display. Une fois la propriété `display: flex;` ou `display: inline-flex;` déclarée sur un élement, celui-ci devient un **flex-container** est ses enfants directs des **flex-items**. Comme dit plus haut, Flexbox permet de gérer les choses dans une dimension principale (verticale ou horizontale). C'est ce que l'on appelle le "main-axis" qui est spécifié via la propriété `flex-direction` et permet de gérer l'alignement principal des flex-items. Une fois le "main-axis" précisé, un "cross axis" perpendiculaire permet de gérer des propriétés d'alignement plus secondaires des flex-items.

Voici les propriétés les plus importantes au niveau du flex-container. Ces propriétés ont des valeurs par défaut mais, lorsque vous commencez, il est conseillé de les spécifier toutes explicitement.

- `flex-direction: [row | row-reverse | column | column-reverse];`: établi la direction du "main axis" (et donc aussi celle du "cross axis"). La valeur `row` spécifie un axe horizontal gauche droite pour les documents en mode `ltr` et un axe horiontal droite gauche pour les documents en mode `rtl`
- `justify-content: [flex-start | flex-end | center | space-between | space-around | space-evenly];`: gestion de l'alignement des flex-items et de la distribution de l'espace sur le main axis. `flex-start` et `flex-end` dépendent du mode de document `ltr` ou `rtl`.
- `align-items: [flex-start | flex-end | center | baseline | stretch];` gestion de l'alignement des flex-items et de la distribution de l'espace sur le cross axis
- `flex-wrap: [wrap | nowrap];`: les flex-items sont autorisés à passer sur une autre ligne ou pas.

Voici les propriétés les plus importantes au niveau des flex-items. Ces propriétés ont des valeurs par défaut. Lorsque vous commencez, il est conseillé de spécifier `flex` et ses trois valeurs explicitement.

- `flex-basis` détermine les dimensions d'un flex-item avant que l'espace vide dans le flex-container soit distribué. Peut être soit une valeur (px, rem, em, %, etc.) soit `auto` (dans ce cas la valeur spécifiée pour `width` ou `height` est prise en compte). La valeur par défaut est `auto`.
- `flex-grow`: détermine si un flex-item peut grandir au delà de ses dimensions de base si nécessaire. A comme valeur `0` ou un nombre entier qui représente la proportion avec laquelle les flex-items vont grandir si ils sont plus petits que leur flex-container après l'application de `flex-basis`. Plus le nombre entier est grand, plus la proprotion est importante. La valeur par défaut est `0`.
- `flex-shrink`: détermine si un flex-item peur rétrécir en deça de ses dimensions de base si nécessaire. A comme valeur `0` ou un nombre entier positif qui représente la proportion avec laquelle les flex-items vont rétrécir si ils sont plus grands que leur flex-container après l'application de `flex-basis`. Plus le nombre entier est grand, plus la proportion est importante. La veleur par défaut est `1`.
- `order [integer]`: détermine l'ordre d'affichage des flex-items dans un flex-container indépendemment de leur ordre dans le code source. La valeur est spécifiée sous la forme d'un nombre entier positif ou négatif.
- `flex: [flex-grow | flex-shrink | flex-basis]`: propriété courte permettant de gérer à la fois `flex-grow`, `flex-shrink` et `flex-basis`. Il vaut mieux utiliser cette propriété courte plutôt que les propriétés longues pour des raisons de compatibilté entre navigateurs.

La propriété `margin` avec une valeur de `auto` est intéressante pour les `flex-items`, elle permet d'allouer tout l'espace disponible dans le flex-container à cette marge et ainsi de "pousser" un ou plusieurs flex-items vers l'extrémité opposée du main axis. L'aricle "[Flexbox’s Best-Kept Secret](https://hackernoon.com/flexbox-s-best-kept-secret-bd3d892826b6)" explique le phénomène en détail.

CSS tricks possède un bon article "[A complete guide to flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)" résumant l'ensemble des propriétés et valeurs liées à Flexbox. [Flexbox Froggy](http://flexboxfroggy.com/) adopte une approche plus ludique.

**Exemple: interface de navigation horizontale (expérimenter avec les différentes propriétés et valeurs)**

```html
<ul class="mainnav">
  <li class="mainnav__item"><a class="mainnav__link" href="#">Home</a></li>
  <li class="mainnav__item"><a class="mainnav__link" href="#">About</a></li>
  <li class="mainnav__item"><a class="mainnav__link" href="#">Work</a></li>
  <li class="mainnav__item  mainnav__item--contact"><a class="mainnav__link" href="#">Contact</a></li>
</ul>
```

```css
.mainnav
{
  list-style: none;
  margin: 0;
  padding: 0;

  display: flex;
  flex-direction: row;
  justify-content: flex-end;
  align-items: center;
  flex-wrap: nowrap;

  background-color: #ccc;
}

.mainnav__item
{
  flex: 0 1 auto;
}

.mainnav__item--contact
{
  margin-left: auto;
}

.mainnav__link
{
  display: block;
  padding: 1rem;
  background-color: #dfdfdf;
}

.mainnav__link:hover
{
  background-color: #eee;
}
```

#### Grid

CSS grid permet de créer des grilles en deux dimensions et de positionner des élements à l'aide de ces grilles. CSS grid est appliqué à l'aide de la proprité display. Une fois `display: grid;` ou `display: inline-grid;` appliqué à un élément, celui-ci devient un **grid-container** et ses enfants directs des **grid-items**.

Grid est une spécification relativement complexe, nous allons ici en voir les propriétés principales. Pour un aperçu plus complet, je ne peux que vous recommander "[Grid by example](https://gridbyexample.com/examples/)" par Rachel Andrew et [un guide très bien fait disponible en français sur Mozilla Developer Network](https://developer.mozilla.org/fr/docs/Web/CSS/CSS_Grid_Layout/Les_concepts_de_base). Voir également "[A Complete Guide to Grid](https://css-tricks.com/snippets/css/complete-guide-grid/)" sur CSS Tricks pomur un bon résumé.

Voici les propriétés principales au niveau du **grid-container**:

- `grid-template-columns`: défini les dimensions des colonnes de la grille. Peut être une valeur (fr,%,px,rem,em, etc.) ou `auto`. Si ces valeurs sont répétées il est intéressant d'utiliser la notation `repeat`. La valeur `minmax([valeur-min], [valeur-max])` est également très utile pour spécifier une valeur minimale et maximale pour les dimensions des colonnes. Lorsque `minmax` est utilisé avec `repeat` comme dans `grid-template-columns: repeat(3, 1fr);`, les valeurs `auto-fill` ou `auto-fit` peuvent être utilisées en lieu et place du nombre de répétitions souhaitées pour laisser le browser faire les calculs.
- `grid-template-rows`: défini les dimensions des rangées de la grille. Peut être une valeur (fr,%,px,rem,em, etc.) ou `auto`. Si ces valeurs sont répétées il est intéressant d'utiliser la notation `repeat`. La valeur `minmax([valeur-min], [valeur-max])` est également très utile pour spécifier une valeur minimale et maximale pour les dimensions des colonnes. Lorsque `minmax` est utilisé avec `repeat`, il est également possible d'utiliser `auto-fill` ou `auto-fit`.
- `justify-content: [start | end | center | stretch (default)]`: permet d'aligner les grid-items par rapport à l'axe des rangées.
- `align-items: [start | end | center | stretch (default)]`: permet d'aligner les grid-items par rapport à l'axe des colonnes.
- `grid-column-gap`, `grid-row-gap`, `grid-gap`: permettent de spécifier les espaces entre les colonnes et les rangées de la grille ou les deux à la fois. Peut être une valeur (%,px,rem,em, etc.).
- `grid-templates-areas`: permet de définir des zones de grilles nommées de façon visuelle. les valeurs sont soit des chînes de caractères, soit un "." qui permet de laisser la zone visée vide de tout contenu.

Voici les propriétés principales au niveau des **grid-items**:

- `grid-column-start`, `grid-column-end`, `grid-column`, `grid-row-start`, `grid-row-end`, `grid-row`: permettent de placer les grid-items dans les colonnes de la grilles. Peuvent prendre comme valeur des nombres correspondant à des grid lines ou des noms de grid lines nommées. Le mot-clé `span` peut être utilisé avec un nombre ou un nom de grid line pour faire en sorte que des grid-items occupent plusieurs "cases" de la grille. Une valeur de `auto` est la valeur par défaut et correspond à un placement automatique des grid-items. `grid-column` et `grid-row` sont des propriétés courtes permattant de gérer les deux à la fois avec les notations `column-start / column-end` ou `row-start / row-end`
- `grid-area`: permet de placer des grid-items dans des zones de la grille nommées à l'aide de `grid-template-areas`. Cette propriété peut également servir de notation ultra condensée pour spécifier `row-start / column-start / row-end / column-end`
- `justify-self`: permet d'aligner les grid-item le long de l'axe des rangées.
- `align-self`: permet d'aligner les grid-item le long de l'axe des colonnes.

##### Placement explicite et implicite des élements dans la grille

Si le placement des éléments dans la grille n'est pas spécifié explicitement avec `grid-column`, `grid-row`, `grid-area`, etc. les éléments vont simplement se placer dans les cellules de la grille dans l'odre spécifié par le code source du document.

La valeur `dense` de la propriété `grid-auto-flow` oblige le navigateur à optimiser le placement automatique / implicite des éléments pour remplir au mieux toutes les cellules de la grille. Cela peut causer une modification de l'ordre d'affichage des éléments par rapport au code source du document.

##### Grilles explicites et implicites

Des notions importantes à comprendre sont celles de grilles explicites et implicites. Lorsque vous définissez une grille à l'aide de `grid-template-columns` et `grid-template-rows`, si le nombre d'éléments qui doivent être placés dans la grille est plus important que le nombre de cellules définies dans la grille, de nouvelles cellules vont automatiquement être créés.

Par défaut, elles seront créées comme des rangées, avec une dimension de `auto`. Vous pouvez spécifier les dimensions des colonnes ou des rangées créées implicitement à l'aide des propriétés `grid-auto-rows` et `grid-auto-columns` qui sont l'équivalent pour les grilles implicites des propriétés `grid-template-columns` et `grid-template-rows` pour les grilles explicites.

Vous pouvez également utiliser `grid-auto-flow: [row (default) | columns | dense | row dense | column dense]`. Si vous spécifiez une valeur de `columns`, des colonnes implicites seront créées plutôt que des rangées.  Le mot-clé `dense` oblige le navigateur à optimiser le placement automatique / implicite des éléments pour remplir au mieux toutes les cellules de la grille. Cela peut modifier l'ordre dans lequel les éléments sont affichés par rapport à leur ordre dans le code source du document.

**Exemple: grilles fluide simple - expérimenter avec les différentes propriétés et valeurs**

```html
<div class="grid">
  <div class="grid__item">grid item</div>
  <div class="grid__item">grid item</div>
  <div class="grid__item">grid item</div>
  <div class="grid__item">grid item</div>
  <div class="grid__item">grid item</div>
  <div class="grid__item">grid item</div>
  <div class="grid__item">grid item</div>
</div>
```

```css
.grid
{
  display: grid;
  /* grid-template columns: 1fr 1fr 1fr 1fr; */
  grid-template-columns: repeat(4, 1fr);
  grid-template-rows: auto;
  grid-gap: 20px;
}

.grid__item
{
  background-color: teal;
}
```

**Exemple: grille fluide responsive avec minmax et auto-fit - expériementer avec les différentes propriétés et valeurs**

```html
<div class="grid">
  <div class="grid__item">grid item</div>
  <div class="grid__item">grid item</div>
  <div class="grid__item">grid item</div>
  <div class="grid__item">grid item</div>
  <div class="grid__item">grid item</div>
  <div class="grid__item">grid item</div>
  <div class="grid__item">grid item</div>
</div>
```

```css
.grid
{
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  grid-template-rows: auto;
  grid-gap: 20px;
}

.grid__item
{
  background-color: teal;
}
```

**Exemple: grille responsive avec des zones nommées à l'aide de template areas**

```html
<div class="page">
  <header class="pageheader">header</header>
  <div class="content-secondary">secondary content</div>
  <main class="content-main">main content</main>
  <footer class="pagefooter">footer</footer>
</div>
```

```css
.page
{
  box-sizing: border-box;
  margin: 0 auto;
  padding: 0 20px;
  max-width: 1140px;

  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: auto;
  grid-template-areas: "header"
                       "content"
                       "sidebar"
                       "footer";
}

@media all and (min-width: 760px)
{
  .page
  {
    grid-template-columns: 300px 20px 1fr;
    grid-template-rows: auto;
    grid-template-areas: "header header header"
                         "sidebar . content"
                         "footer footer footer";
  }
}

.pageheader
{
  grid-area: header;
  background-color: silver;
}

.content-secondary
{
  grid-area: sidebar;
  background-color: teal;
}

.content-main
{
  grid-area: content;
  background-color: olive;
}

.pagefooter
{
  grid-area: footer;
  background-color: purple;
}
```

**Exemple: grille responsive avec elements placés automatiquement et un élément placé explicitement (avec span)**

```html
<ul class="grid">
  <li class="grid__item"><p>grid item</p></li>
  <li class="grid__item"><p>grid item</p></li>
  <li class="grid__item  grid__item--highlight"><p>grid item</p></li>
  <li class="grid__item"><p>grid item</p></li>
  <li class="grid__item"><p>grid item</p></li>
  <li class="grid__item"><p>grid item</p></li>
  <li class="grid__item"><p>grid item</p></li>
  <li class="grid__item"><p>grid item</p></li>
</ul>
```

```css
.grid
{
  list-style: none;
  margin: 0;
  padding: 0;

  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  grid-template-rows: auto;
  grid-gap: 2rem;
}

.grid__item
{
  background-color: teal;
}

.grid__item--highlight
{
  background-color: red;
  grid-row: 1 / 2;
  grid-column: 1 / 2;
}

@media all and (min-width: 440px)
{
  .grid__item--highlight
  {
    grid-row: 1 / 3;
    grid-column: 1 / 3;
  }
}
```

## 6. Transitions et Animations

Le web actuel repose également sur les transitions et les animations. Celles-ci vont des plus simples aux plus complexes et emmetent en jeux différentes technologies.

### Transitions CSS

Les transtions CSS sont sans doute ce qu'il à de plus simple à comprendre. Prenons un simple bouton qui comporte un changement d'état au survol de la souris. Si nous n'avons pas de transition, le passage entre les deux états se fait immédiatement.

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

Les transitions CSS sont faciles à mettre en oeuvre et à maniouler via JavaScript. Elles permettent de réaliser une certaine palette d'effets mais elles ont également leurs limitations:

- les transtions se font toujours d'un état A vers un état B, sans étapes intermédiaires. Pour contrôler plus finement les étapes, il faut se tourner vers les animations CSS.
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

### Déclenchement au scroll

Avec l'aide Javascript, les transitions et animations CSS peuvent facilement être [déclenchées via le scroll](http://dogstudio.be).

`intersectionObserver` permet facilement de détecter si un ou plusieurs élements sont affichés dans le viewport du navigateur pour déclencher des animations lorsque c'est le cas via quelques changements de classes CSS. Voici [une petite démonstration](https://github.com/jeromecoupe/onscroll_css_animations) rapide.

*Exercice: décortiquer le script et voir comment CSS et JS interagissent*

## Animations Javascript

Web animation API offre les mêmes possibilités que les animations CSS offre bien plus de contrôle. Un bon support dans les divers navigateurs et la présence d'un polyfill en fait le choix par défaut si vous avez besoin d'interactivité, d'effets poussé ou de séquences d'animations chainées les unes aux autres. Bref, si vous avez besoin de quelque chose de plus riche que ce qu'offrent des animations déclaratives en CSS, cette technologie native deviendra intéressante lorsque le support des navigateurs augmentera.

Il est également possible d'utiliser requestAnimationFrame. Cette méthode vous permet de faire à peu près n'importe quoi mais vous devez tout créer vous-même, ce qui rend cette approche beacuoup plus complexe et vous oblige à gérer vous-même les problèmes de performance éventuels.

Ajourd'hui, la librairies JavaScript la plus utilisée pour ls animations complexes en JavaScript est [GSAP de Greensock](https://greensock.com/gsap), qui vous permet d'utiliser une timeline pour contrôler finement toutes vos animations, leur séquencage et leur déroulement.

*Exercice: animations et transitrions dans Figma et dans le code*

## 7. Design web: documents de delivery

Afin de présenter les designs web dans tous leurs aspects, [le plus efficace est de le faire à l’aide de prototypes interactifs](https://www.webstoemp.com/blog/to-hell-with-abstract-prescriptive-deliverables/), plutôt que d’utiliser des documents et méthodes plus statiques qui posent problème à de nombreux niveaux.

### Problèmes des documents statiques / uniques

Classiquement, les designs à l’aide de [wireframes](https://dribbble.com/shots/1893359-Exelerate-Wireframes/attachments/322535) statiques qui se transforment finalement en [chartes graphiques statiques détaillées](https://dribbble.com/shots/1874207-Exelerate-Product-view/attachments/317155) réalisées sur Sketch , Figma ou Photoshop. Cette manière de travailler provient du print mais n’est pas adaptée au design web pour diverses raisons.

#### Non prise en compte des spécificités du medium

Ces documents ne sont pas à même de matérialiser efficacement les spécificités du medium Internet que sont l’interactivité (survol des boutons, menus déroulant, accordéons, slideshows, animations, etc.), l’adaptation aux diverses tailles d’écran et résolutions (desktops, tablettes, mobiles, écrans haute résolution, etc.) et l'adaptation aux capacités du navigateur ou du terminal utilisé.

#### Représentation irréaliste du produit fini

De tels documents donnent une fausse image du produit fini. On habitue ainsi le client à voir une version “irréaliste” de son futur site.

La résolution des documents imprimés est plus élevée qu’un affichage sur écran, les pages sont présentées dans leur entièreté alors que -dans un navigateur- seule une petite portion en sera visible à la fois, les polices n’ont pas du tout le même rendu à l’écran.

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

Plutôt que de fournir au client des “mockups” sur Sketch, Figma ou Photoshop dans lesquels les moindres éléments des pages sont designés, il est plus facile et plus rapide d’explorer diverses pistes graphiques à l’aide de ce que Dan Mall appelle des "[elements collages](http://v3.danielmall.com/articles/rif-element-collages/)".

De tels elements collages ou [moodboards](https://thomasbyttebier.be/blog/mood-boards-in-a-content-first-design-process) peuvent être produits relativement rapidement pour réaliser quelques itérations autour de concepts intéressants et d'éléments centraux du site / de l’application. Présenter les choses sous forme d'une longue page web permet aussi d'utiliser des videos ou un peu de JavaScript pour présenter des concepts plus interactifs ou dynamiques.

Sketch, Figma ou Framer sont encore présents dans le processus, mais la philosophie change.

Il ne s'agit plus de produire des designs finalisés mais de pouvoir rapidement tester et valider des idées pour ensuite pouvoir travailler de façon itérative et collaborative.

### Designers hybrides

> [the design process] is about designing, prototyping and making. When you separate those, I think the final result suffers."
> Jonathan Ive, March, 2012

Cette phrase de Jonathan Ive pourrait sans problème être appliquée au web d’aujourd’hui, dans lequel le design, la création de prototypes et la réalisation technique sont de plus en plus intimement liés.

#### Les designers web doivent ils coder?

Pas forcément, mais cela aide beaucoup et cela permet de gagner du temps. Au minimum, designers et dévelopeurs doivent collaborer étroitement et avoir une bonne connaissance des modes de travail et défis recontrés par les uns et les autres est primordial.

Le travail des designers web à grandement évolué: nous devons maintenant créer des systèmes modulaires et flexibles et plus des interfaces fixes dans photoshop. Le nombre d’inconnues et d’élements entrant en ligne de compte dans un site Internet ne cesse d’augmenter.

Cela requiert des changements dans les process et workflow utilisés mais aussi une plus grande collaboration et un dialogue plus étroit entre les différents intervenants

> You must also address the very human issue of communication. Earlier and more frequent collaboration among team members and the client must become the rule in your workflow, not the exception. Content, design, and development team members must review and collaborate regularly at every stage in the creation process until the site is live. We can’t ‘throw it over the wall’ anymore— at least, not if we want our sites to be excellent. There are simply too many moving parts now. Go forth and collaborate.

> Drew Clemens - Smashing Magazine
