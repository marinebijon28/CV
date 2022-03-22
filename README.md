#### Composition d'une page HTML

### doctype
<!DOCTYPE html>
En HTML, le doctype est le préambule requis en haut de tous les documents. Son seul but est d’empêcher un navigateur de passer en soi-disant "quirks mode" lors du rendu d’un document ; c’est-à-dire que le doctype garantit que le navigateur fait de son mieux pour suivre les spécifications pertinentes, plutôt que d’utiliser un mode de rendu différent incompatible avec certaines spécifications. 

# Mode quirks et mode standard
Par le passé, les pages web étaient souvent écrites sous deux versions : une destinée à Netscape Navigator et l'autre à Microsoft Internet Explorer. Lorsque les standards du Web sont apparus avec le W3C, les navigateurs ne pouvaient pas simplement commencer à les utiliser car leur mise en place rendrait inutilisable la plupart des sites web existant. Les navigateurs ont alors introduit deux modes afin de traiter les sites respectants les standards des autres sites historiques.

Il existe aujourd'hui trois modes utilisés par les moteurs de rendu des navigateurs web : le mode quirks, le mode quasi-standard et le mode standard total. En mode quirks, le moteur de mise en page émule le comportement non-standard de Navigator 4 et d'Internet Explorer 5. Ce mode permet de prendre en charge les sites web rédigés avant l'adoption généralisée des standards web. En mode standard total, le comportement du navigateur est entièrement (aux bugs près) celui décrit par les spécifications HTML et CSS. En mode quasi-standard, très peu de déviations sont implémentées.

Comment les navigateurs déterminent le mode à utiliser ?
Pour les documents HTML, les navigateurs utilisent le DOCTYPE présent au début du document afin de déterminer si celui-ci doit être géré avec le mode quirks ou avec l'un des modes standards. Si vous souhaitez qu'une page utilise le mode standard total, son DOCTYPE devra correspondre à celui utilisé dans cet exemple :

<!DOCTYPE html>
<html lang="fr">
  <head>
    <meta charset=UTF-8>
    <title>Bonjour tout le monde !</title>
  </head>
  <body>
  </body>
</html>
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



###    html
<html lang="fr">
</html>
L’élément de racine du document HTML représente la racine d’un document HTML ou XHTML. Tout autre élément du document doit être un descendant de cet élément.

# Attribut :
- xmlns : Définit l’espace de noms XML du document. La valeur par défaut est "http://www.w3.org/1999/xhtml". Cet attribut est obligatoire dans un document XML et optionnel dans un document de type text/html.

# Notes : 
Puisque l’élément html <html> est le premier élément dans un document, autre que les commentaires, il est désigné comme l’élément racine du document. Bien que cette balise soit implicite, ou non requise dans un document HTML, il est requis dans un document XHTML (à la fois pour la balise ouvrante et pour la balise fermante).

# Accessibilité :
L’utilisation d’un attribut lang valide (au sens de l’IETF = Internet Engineering Task Force) pour l’élément HTML permettra aux lecteurs d’écran de déterminer la langue à utiliser pour l’énonciation. La balise de langage utilisée doit correspondre à celle utilisée pour la majorité du contenu de la page. Sans attribut, les lecteurs d’écran utiliseront la lange paramétrée par le système d’exploitation, ce qui pourra entraîner des défauts de pronociations.

Ajouter un attribut lang valide au sein de l’élément HTML permet également de s’assurer que les métadonnées importantes contenue dans l’élément <head>, telle que le titre de la page (<title>) sont énoncées correctement.  




###         head
<head>
</head>
L’élément HTML <head> fournit des informations générales (métadonnées) sur le document, incluant son titre et des liens ou des définitions vers des scripts et feuilles de style.

Note : L’élément <head> contient principalement des données destinées au traitement automatisé et pas nécessairement lisibles par des humains. Pour afficher des informations lisibles pour les utilisateurs dans des en-têtes ou titre, voir l’élément <header>




##  title
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

