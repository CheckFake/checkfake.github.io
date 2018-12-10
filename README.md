# CheckFake
CheckFake vise à vous proposer des informations complémentaires aux articles d'informations que vous lisez sur internet en vous fournissant un niveau de confiance sur le contenu que vous avez devant les yeux.

CheckFake est composé d'une API et d'une extension navigateur qui vous permet d'interroger l'API et d'afficher les informations de manière lisible et synthétique.

Nous croyons qu'il n'existe rien de tel qu'une information purement vraie ou fausse, ainsi CheckFake ne juge pas la véracité d'une information ou non mais fournit une estimation de sa fiabilité. Nous ne souhaitons pas par ailleurs que vous fassiez une confiance aveugle à CheckFake. Comme tout système, CheckFake n'est pas fiable à 100%. Le but de cette extension est de vous faire prendre conscience que toutes les informations que vous lisez sur internet ne sont pas fiables à 100% et de vous amener à avoir un regard critique sur le contenu des articles que vous parcourez.

Par ailleurs, et dans un souci de transparence, le code source décrivant les traitements effectués par CheckFake pour vous fournir ses résultats est disponible [sur GitHub](https://github.com/onlytrue-fnd)

## Téléchargement
CheckFake est disponible en tant qu'extension pour les navigateurs suivants :

<a href="https://addons.mozilla.org/en-US/firefox/addon/checkfake/"><img src="images/firefox_64x64.png" alt="logo firefox"></a>
<a href="https://chrome.google.com/webstore/detail/checkfake/jcfpgmcndlcelogjncjamiebkicpijpp"><img src="images/chrome_64x64.png" alt="logo chrome"></a>

## Usage
Pour connaître le niveau de fiabilité accordé par CheckFake à un article affiché dans votre navigateur, cliquez sur l'icône CheckFake présente à côté de la barre d'adresse de votre navigateur. Après un temps de chargement, les informations s'affichent.

## Limitations
* CheckFake n'est pour le moment supportée que pour des textes en **français**.

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
Nous conservons les informations suivantes dans notre base de données:

- URL de l'article soumis à l'API
- Nom de domaine de l'article (extrait de l'URL)
- Score attribué au contenu de l'article
- Version de la méthode de calcul ayant servi au calcul du score
- Nombre d'articles ayant servi à l'attribution du score de contenu
- Date de soumission de l'article
- Date de dernière modification
- URL, titre et score attribué aux articles "intéressants" liés à votre article

Nous ne stockons aucune donnée permettant de vous identifier directement.
