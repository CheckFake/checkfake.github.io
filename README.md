# OnlyTrue
OnlyTrue est composé d'une API et d'une extension navigateur qui vous permet d'interroger l'API et d'afficher les informations de manière lisible et synthétique.

OnlyTrue vise à vous proposer des informations complémentaires aux articles d'informations que vous lisez sur internet en vous fournissant un niveau de confiance sur le contenu que vous avez devant les yeux.

Nous croyons qu'il n'existe rien de tel qu'une information purement vraie ou fausse, ainsi OnlyTrue ne juge pas la véracité d'une information ou non mais fournit une estimation de sa fiabilité.

## Niveau de fiabilité
Le niveau de fiabilité d'une information est déterminé selon une méthode inspirée du comportement humain lors de la recherche d'informations complémentaires :

- Lorsque vous cliquez sur l'extension, nous transmettons l'URL de la page que vous consultez à l'API
- L'API extrait plusieurs informations, comme le titre de l'article, sa date de publication ainsi que son contenu.
- Nous extrayons ensuite les noms communs et les noms propres du contenu de l'article et nous conservons uniquement ceux qui sont présents plusieurs fois dans le texte
- Nous réalisons une requête sur un moteur de recherche avec le titre de votre article
- Nous extrayons les noms communs et les noms propres des articles fournis par le moteur de recherche et nous les comparons avec les noms extraits dans l'article que vous lisez
- S'il y a suffisament de mots en commun, l'article fourni par le moteur de recherche est considéré comme "intéressant"
- Plus il y a d'articles "intéressants" parmi ceux que nous retourne le moteur de recherche, plus le niveau de confiance dans l'article que vous lisez sera élevé.

## Données conservées
Nous conservons les données suivantes dans notre base de données:

- URL de l'article soumis à l'API
- Nom de domaine de l'article (extrait de l'URL)
- Score attribué au contenu de l'article
- Version de la méthode de calcul ayant servi au calcul du score
- Nombre d'articles ayant servi à l'attribution du score de contenu
- Date de soumission de l'article
- Date de dernière modification
- URL, titre et score attribué aux articles "intéressants" liés à votre article

Nous ne stockons aucune donnée permettant de vous identifier directement.
