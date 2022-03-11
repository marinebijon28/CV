#### Composition d'une page HTML

# doctype
<!DOCTYPE html>
En HTML, le doctype est le préambule requis en haut de tous les documents. Son seul but est d’empêcher un navigateur de passer en soi-disant "quirks mode" lors du rendu d’un document ; c’est-à-dire que le doctype garantit que le navigateur fait de son mieux pour suivre les spécifications pertinentes, plutôt que d’utiliser un mode de rendu différent incompatible avec certaines spécifications. 




####    html
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


