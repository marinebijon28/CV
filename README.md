#### Composition d'une page HTML

###         doctype
<!DOCTYPE html>
En HTML, le doctype est le préambule requis en haut de tous les documents. Son seul but est d’empêcher un navigateur de passer en soi-disant "quirks mode" lors du rendu d’un document ; c’est-à-dire que le doctype garantit que le navigateur fait de son mieux pour suivre les spécifications pertinentes, plutôt que d’utiliser un mode de rendu différent incompatible avec certaines spécifications. 

# Mode quirks et mode standard
Par le passé, les pages web étaient souvent écrites sous deux versions : une destinée à Netscape Navigator et l'autre à Microsoft Internet Explorer. Lorsque les standards du Web sont apparus avec le W3C, les navigateurs ne pouvaient pas simplement commencer à les utiliser car leur mise en place rendrait inutilisable la plupart des sites web existant. Les navigateurs ont alors introduit deux modes afin de traiter les sites respectants les standards des autres sites historiques.

Il existe aujourd'hui trois modes utilisés par les moteurs de rendu des navigateurs web : le mode quirks, le mode quasi-standard et le mode standard total. En mode quirks, le moteur de mise en page émule le comportement non-standard de Navigator 4 et d'Internet Explorer 5. Ce mode permet de prendre en charge les sites web rédigés avant l'adoption généralisée des standards web. En mode standard total, le comportement du navigateur est entièrement (aux bugs près) celui décrit par les spécifications HTML et CSS. En mode quasi-standard, très peu de déviations sont implémentées.

Comment les navigateurs déterminent le mode à utiliser ?
Pour les documents HTML, les navigateurs utilisent le DOCTYPE présent au début du document afin de déterminer si celui-ci doit être géré avec le mode quirks ou avec l'un des modes standards. Si vous souhaitez qu'une page utilise le mode standard total, son DOCTYPE devra correspondre à celui utilisé dans cet exemple : <!DOCTYPE html>

Le DOCTYPE illustré dans cet exemple, <!DOCTYPE html>, est le plus simple possible et correspond à la recommandation HTML5. Les versions précédentes des standards HTML recommandaient d'autres variantes. Toutefois, l'ensemble des navigateurs actuels utiliseront le mode standard total avec ce DOCTYPE (y compris IE6). Il n'est pas justifié de choisir un DOCTYPE plus compliqué ; le faire risquerait de déclencher l'utilisation du mode quasi-standard ou du mode quirks.

Assurez-vous que le DOCTYPE soit présent au tout début du document HTML. Tout ce qui précède le DOCTYPE (un commentaire ou une déclaration XML) déclenchera le mode quirks pour Internet Explorer 9 et les versions antérieures.

En HTML5, le seul but du DOCTYPE est d'activer le mode standard total. Les anciennes versions du standard HTML donnaient une sémantique plus riche au DOCTYPE mais aucun navigateur n'a utilisé le DOCTYPE pour autre chose que pour choisir entre le mode quirks et l'un des modes standards.

Vous pouvez également consulter cet article avec plus de détails sur la façon dont les navigateurs choisissent entre les différents modes.

# XHTML
Si la page est servie comme XHTML avec le type MIME application/xhtml+xml dans l'en-tête HTTP Content-Type, il n'est pas nécessaire d'utiliser de DOCTYPE afin d'activer le mode standard, car de tels documents utiliseront toujours le mode standard total. On notera toutefois que servir les pages avec un type application/xhtml+xml entraînera l'affichage d'une boîte de téléchargement d'un fichier au format inconnu sous Internet Explorer 8 car IE9 est la première version d'Internet Explorer à prendre en charge XHTML.

Si on sert un contenu semblable à du XHTML mais avec le type MIME text/html, le navigateur l'interprètera comme du HTML et il faudra alors ajouter le DOCTYPE afin d'utiliser un mode standard.

Comment connaître le mode utilisé ?
Sous Firefox, vous pouvez utiliser le menu contextuel : "Informations sur la page" et le champ "Mode de rendu" de l'onglet Général..

Sous Internet Explorer, appuyez sur la touche F12 et utilisez le champ Document Mode.



###             html
<html lang="fr">
</html>
L’élément de racine du document HTML représente la racine d’un document HTML ou XHTML. Tout autre élément du document doit être un descendant de cet élément.

# Attribut :
- xmlns : Définit l’espace de noms XML du document. La valeur par défaut est "http://www.w3.org/1999/xhtml". Cet attribut est obligatoire dans un document XML et optionnel dans un document de type text/html.

# Notes : 
Puisque l’élément html <html> est le premier élément dans un document, autre que les commentaires, il est désigné comme l’élément racine du document. Bien que cette balise soit implicite, ou non requise dans un document HTML, il est requis dans un document XHTML (à la fois pour la balise ouvrante et pour la balise fermante).

# Accessibilité :
L’utilisation d’un attribut lang valide (au sens de l’IETF = Internet Engineering Task Force) pour l’élément HTML permettra aux lecteurs d’écran de déterminer la langue à utiliser pour l’énonciation. La balise de langage utilisée doit correspondre à celle utilisée pour la majorité du contenu de la page. Sans attribut, les lecteurs d’écran utiliseront la langue paramétrée par le système d’exploitation, ce qui pourra entraîner des défauts de pronociations.

Ajouter un attribut lang valide au sein de l’élément HTML permet également de s’assurer que les métadonnées importantes contenue dans l’élément <head>, telle que le titre de la page (<title>) sont énoncées correctement.  




###         head
<head>
</head>
L’élément HTML <head> fournit des informations générales (métadonnées) sur le document, incluant son titre et des liens ou des définitions vers des scripts et feuilles de style.

# Note : 
L’élément <head> contient principalement des données destinées au traitement automatisé et pas nécessairement lisibles par des humains. Pour afficher des informations lisibles pour les utilisateurs dans des en-têtes ou titre, voir l’élément <header>




###         title
<title>Curriculum Vitae de Marine Bijon – Retrouvez mes compétences</title>
L’élément <title> définit le titre du document (qui est affiché dans la barre de titre du navigateur ou dans l’onglet de la page). Cet élément ne peut contenir que du texte, les balises qu’il contiendrait seraient ignorées.

# Référencement (SEO)
Le titre d’une page fait partie des éléments principaux qui sont scannés lors de l’indexation d’une page. C’est aussi le texte qui est affiché parmi les résultats du moteur de recherche, de façon proéminente et donc visible par les utilisateurs qui trouvent votre site grâce à un moteur de recherche.

Aussi, mieux vaudra avoir des titres descriptifs plutôt que des titres trop courts ou vagues.

# Quelques observations :
- On pourra éviter des titres sur un ou deux mots.
- La longueur affichée pour les titres dans les résultats d’un moteur de recherche se situe entre 55 et 60 caractères. Si le titre est plus long, on veillera à ce que les concepts majeurs apparaissent avant cette longueur.
- Attention aux entités (les chevrons HTML pourront être affichés différemment entre les navigateurs).
- Le titre soit être intelligible et pas une simple concaténation de mots-clés.
- Le titre devra être unique pour un même site

# Accessibilité
Il est important de fournir une valeur pour l’attribut title qui décrit le but de la page de façon claire et concise.

Les personnes utilisant des outils d’assistance peuvent utiliser le titre de la page afin de déterminer rapidement ce qu’elle contient. Ainsi, il ne peut pas être nécessaire de naviguer « dans » la page, ce qui peut prendre du temps et être source de confusion si, ce faisant, on doit déterminer le but de la page.

Mettre à jour la valeur de title afin de refléter un changement d’état important (un problème de validation d’un formulaire par exemple) peut également s’avérer utile :

<title>2 erreurs sur votre commande - Restaurant chinois Maison bleue - Commande en ligne</title>




##  link
L'élément HTML <link /> définit la relation entre le document courant et une ressource externe. Cet élément peut être utilisé pour définir un lien vers une feuille de style, vers les icônes utilisées en barre de titre ou comme icône d'application sur les appareils mobiles.

Pour lier une feuille de style externe, on inclut un élément <link> de la forme suivante à l'intérieur de l'élément <head> :

<link href="main.css" rel="stylesheet" />
Dans cet exemple, on indique le chemin vers la feuille de style grâce à l'attribut href, l'attribut rel possède une valeur stylesheet qui indique que c'est une feuille de style. rel signifie relationship qui correspond donc à la relation entre la ressource et le document courant. Il existe de nombreux types de liens possibles.

Certains types sont assez fréquents. Ainsi, pour l'icône présentant le site dans l'onglet, on trouvera :

<link rel="icon" href="favicon.ico" />
Il existe différents types de relations pour préciser les icônes et qui permettent notamment de cibler certaines plateformes mobiles :

<link rel="apple-touch-icon-precomposed" sizes="114x114"
      href="apple-icon-114.png" type="image/png" />
L'attribut sizes indique la taille de l'icône tandis que l'attribut type contient le type MIME de la ressource qui est liée. Ces attributs permettent alors au navigateur de sélectionner la ressource la plus adéquate.

On peut également fournir l'attribut media afin d'utiliser telle ou telle ressource lorsqu'une requête média est vérifiée. Ainsi, on pourra utiliser ce qui suit afin d'avoir une feuille de style utilisée à l'impression et une autre dédiée au mobile :

<link href="print.css" rel="stylesheet" media="print" />
<link href="mobile.css" rel="stylesheet" media="screen and (max-width: 600px)" />
Certaines fonctionnalités relatives à la sécurité sont également disponibles avec certains attributs de <link />. Dans cet exemple :

# lien extérieur sécurité
<link rel="preload" href="myFont.woff2" as="font"
      type="font/woff2" crossorigin="anonymous" />
L'attribut rel vaut preload et indique que le navigateur doit précharger la ressource (voir Le préchargement du contenu avec rel="preload" pour plus de détails), l'attribut as indique la classe de contenu qui est récupéré et l'attribut crossorigin indique si la ressource doit être récupérée avec une requête CORS.

# Quelques notes d'utilisation :
- Un élément <link> element peut être placé dans un élément <head> ou <body> selon la valeur de la relation. C'est cependant une bonne pratique que de placer l'ensemble des éléments <link> dans l'élément <head>.
- Lorsque <link> est utilisé pour la favicon d'un site et que celui-ci utilise les règles CSP afin d'améliorer la sécurité, les règles s'appliquent également aux icônes. Aussi, si la favicon ne charge pas, veuillez vérifier que la directive img-src de l'en-tête Content-Security-Policy ne bloque pas le chargement de l'image.
- Les spécifications HTML et XHTML définissent des gestionnaires d'évènements pour l'élément <link> mais leur utilisation reste incertaine.
- Pour XHTML 1.0, les éléments vides tels que <link> devaient utiliser une barre oblique de fin : <link />.
- WebTV prend en charge la valeur next pour l'attribut rel afin de précharger la page suivante pour une série de documents.

## Attributs
Cet élément inclut les attributs universels.

# as
Cet attribut est uniquement utilisé lorsque rel="preload" ou rel="prefetch" est utilisé pour l'élément <link>. L'attribut indique le type de contenu chargé par l'élément <link> et permet au navigateur de déterminer la priorité du contenu, d'identifier les utilisations de la ressource plus bas dans le document, d'appliquer la bonne politique de sécurité des contenus et de définir le bon en-tête de requête Accept.

# crossorigin
Cet attribut à valeur contrainte indique si le CORS doit être utilisé lorsque la ressource liée est récupérée. Les images avec CORS activé peuvent être réutilisée dans un élément <canvas> sans qu'il soit corrompu. Les valeurs autorisées sont :

- "anonymous" : une requête cross-origine est effectuée (avec l'en-tête HTTP Origin). Mais aucune information d'identification n'est envoyée (aucun cookie, aucun certificat X.509, aucune authentification simple via HTTP). Si le serveur ne fournit pas d'informations au site d'origine (c'est-à-dire sans utiliser l'en-tête HTTP Access-Control-Allow-Origin, l'image sera corrompue et son utilisation sera restreinte.
- "use-credentials" : une requête cross-origine est effectuée (avec l'en-tête HTTP Origin) avec des informations d'authentification qui sont envoyées (un cookie, un certification et une authentification HTTP simple sont envoyés). Si le serveur ne fournit pas d'information d'authentification au site d'origine via l'en-tête Access-Control-Allow-Credentials (en-US), l'image sera corrompue et son utilisation sera restreinte.
- Lorsque l'attribut est absent, la ressource est récupérée sans requête CORS (c'est-à-dire sans envoyer l'en-tête Origin) ce qui empêche de l'utiliser dans les éléments qui ne doivent pas être corrompus tels que <canvas>. Si la valeur est invalide, elle est synonyme de anonymous. Pour plus d'informations, consulter l'article sur le contrôle d'origine HTTP (CORS).

# disabled
Cet attribut est uniquement utilisable avec les liens avec rel="stylesheet". L'attribut booléen disabled indique si la feuille de style référencée devrait être chargée et appliquée au document. Si l'attribut disabled est indiqué dans le document HTML lors de son chargement, la feuille de style ne sera pas chargé au chargement de la page. La feuille de style sera uniquement chargée à la demande si (et lorsque) l'attribut disabled est retiré ou passé à falsevia un script.

Toutefois, une fois que la feuille de style a été chargée, toute modification à l'attribut disabled n'aura aucun impact, sa valeur ne sera pas liée à la propriété StyleSheet.disabled. Modifier cet attribut ne fait qu'activer/désactiver la capacité de charger et d'appliquer la feuille de style au document.

Cette propriété est à distinguer de la propriété disabled de l'interface StyleSheet : lorsqu'on utilise celle-ci, la feuille de style est retirée de document.styleSheets et elle n'est pas rechargée automatiquement lorsqu'on la repasse à false.

# href
Cet attribut définit l'URL de la ressource liée. L'URL utilisée peut être absolue ou relative.

# hreflang
Cet attribut, purement indicatif, définit la langue de la ressource liée. La valeur doit être une balise de langue BCP47 valide. Cet attribut doit uniquement être utilisé si l'attribut href est présent.

# auto
Aucune préférence n'est indiquée. Le navigateur peut utiliser une heuristique qui lui est propre afin de décider de la priorité de la ressource.

# media
Cet attribut indique le média auquel s'applique la ressource liée. Sa valeur doit être une requête média. Cet attribut est principalement utilisé pour permettre à l'agent utilisateur de sélectionner la meilleure feuille de style en fonction de l'appareil de l'utilisateur.

# Note :

- En HTML4, la valeur de cet attribut était une liste de descripteurs de médias (des types ou des groupes de média) séparés par des espaces, par exemple print screen aural braille. HTML5 étend cet attribut à l'ensemble des requêtes média qui forment un surensemble des valeurs autorisées en HTML 4.
- Les navigateurs qui ne prennent pas en charge les requêtes média CSS3 ne reconnaîtront pas nécessairement les liens adéquats et il faut donc toujours fournir des liens de recours.

# rel
Cet attribut indique la relation qui existe entre le document et la ressource liée. Cet attribut doit être une liste de types de lien, séparés par des espaces. La plupart du temps, cet attribut est utilisé pour caractériser un lien vers une feuille de style et il vaut alors stylesheet quand l'attribut href reçoit l'URL de la feuille de style à charger. WebTV supporte également la valeur next qui permet de précharger la page suivante d'une série de pages.

# sizes
Cet attribut définit les dimensions des icônes pour le média contenu dans la ressource. Cet attribut doit uniquement être présent lorsque rel contient le type de lien icon. Il peut prendre l'une des valeurs suivantes :

- any : l'icône peut être redimensionnée à volonté car elle utilise un format vectoriel (par exemple image/svg+xml).
- une liste de tailles, séparées par des espaces, dont chacune est de la forme <largeur en pixels>x<hauteur en pixels> ou <largeur en pixels>X<hauteur en pixels>. Pour chacune de ces dimensions, il doit exister une image correspondante dans la ressource.

# Note :
- La plupart des format d'icône permettent simplement de stocker une seule icône, c'est pour cela que, la plupart du temps, sizes ne contient qu'un seul élément.
- Safari sur iOS ne prend pas en charge cet attribut mais utilise des types de lien non-standards pour définir l'icône utilisé dans la barre du site ou pour le lancer : apple-touch-icon et apple-touch-startup-icon.

# title
L'attribut title possède un sens spécifique pour l'élément <link>. Utilisé pour un lien <link rel="stylesheet">, l'attribut title définit une feuille de style alternative ou une feuille de style préférée. S'il est mal utilisé, la feuille de style pourra être ignorée.

# type
Cet attribut est utilisé pour définir le type de contenu auquel le lien fait référence. La valeur de cet attribut doit être un type MIME tel que text/html ou text/css, etc. Le plus souvent, cet attribut est utilsé pour définir le type de feuille de style utilisé et la valeur la plus fréquente est text/css qui indique le format d'une feuille de style en cascade (Cascading Style Sheet pour CSS). Cet attribut est également utilisé pour les liens avec rel="preload" afin de vérifier la prise en charge du format de fichier (si le navigateur ne prend pas en charge ce fichier, il n'est pas téléchargé).

## Attributs dépréciés, obsolètes ou non-standard
# charset
Cet attribut définit l'encodage de la ressource lié. La valeur de cet attribut est une liste de jeux de caractères (tels que définis dans la RFC RFC 2045) séparés par des espaces ou des virgules. La valeur par défaut de cet attribut est iso-8859-1.

# Note : 
cet attribut est obsolète et ne doit pas être utilisé. Pour obtenir l'effet escompté, on utilisera l'en-tête HTTP Content-Type pour la ressource liée.

## Exemples
# Associer une feuille de style
Pour associer une feuille de style à la page courante, on utilisera la syntaxe suivante :

<link href="style.css" rel="stylesheet" />

# Fournir des feuilles de style alternatives
Pour un document, on peut indiquer plusieurs feuilles de style alternatives.

L'utilisateur pourra choisir parmi ces feuilles de style via le menu « Affichage > Style de la page ». Ainsi, un utilisateur pourra voir différentes versions d'une même page.

<link href="default.css" rel="stylesheet" title="Mise en forme par défaut">
<link href="joli.css" rel="alternate stylesheet" title="Joli">
<link href="simple.css" rel="alternate stylesheet" title="Simple">

# Évènements déclenchés au chargement d'une feuille de style
Il est possible de déterminer si une feuille de style a été chargée en écoutant l'évènement load. De la même façon, un évènement error indiquera qu'une erreur a eu lieu lors du traitement de la feuille de style:

<script>
  function sheetLoaded() {
    // faire quelque chose, sachant
    // que la feuille a été chargéee
  }

  function sheetError() {
    console.log("Erreur lors du chargement de la feuille de style !");
  }
</script>

<link rel="stylesheet" href="mafeuilledestyle.css"
  onload="sheetLoaded()"
  onerror="sheetError()">

# Note : 
L'évènement load est déclenché une fois que la feuille de style et que le contenu associé ont été chargés et analysés et immédiatement avant que la mise en forme soit appliquée au contenu.

# Exemples avec preload
De nombreux exemples avec <link rel="preload"> peuvent être lus sur Précharger des ressources grâce à rel="preload".

# Notes :
- Un élément <link> peut être utilisé à l'intérieur d'un élément <head> ou bien dans le corps du document (<body>) si le type de lien le permet (body-ok). On peut par exemple utiliser <link rel="stylesheet"> car ce type de lien est autorisé au sein de l'élément <body>.
- HTML 3.2 définit uniquement les attributs href, rel, rev et title pour l'élément <link>.
- HTML 2 définit les attributs href, methods, rel, rev, title et urn pour l'élément <link>. Les attributs methods et urn ont ensuite été retirés des spécifications.
- Les spécifications HTML et XHTML définissent toutes deux des gestionnaires d'évènements pour l'élément <link>.
- En XHTML 1.0, il est nécessaire qu'un élément <link> ait une barre oblique avant le chevron fermant.
