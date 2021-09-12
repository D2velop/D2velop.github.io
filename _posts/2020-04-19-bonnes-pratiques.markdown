---
layout: post
title:  "Bonne pratique"
date:   2020-04-19 20:00:00 +0200
categories: dev pratique
author: Cédric Gérard
---

Avant de commencer à parler de bonnes pratiques, je voulais vous poser quelques questions. Vous êtes-vous déjà demandé, en tant que développeur, si votre code était bon ? Je veux dire par là, est-ce que vous êtes satisfait du code que vous produisez ?

Beaucoup d’entre nous se contentent de faire du code qui « marche » sans se soucier de ce que ce code deviendra à l’avenir. Même si du point de vue d’une entreprise du code qui « marche », c’est suffisant, ça ne l’est pourtant pas du point de vue d’un développeur professionnel.

En réalité faire du code qui se contente de fonctionner ce n’est pas le plus compliqué. C’est même à la portée de n’importe qui avec les ressources que l’on trouve en ligne de nos jours. En revanche produire du code de qualité professionnelle, c’est une autre histoire.

On peut faire un parallèle avec le monde de l’artisanat. Tout le monde peut bricoler chez soi, avec plus ou moins de compétences. Mais si vous regardez un artisan qualifier à l’œuvre, vous prendrez tout de suite la mesure de la distance qui vous sépare en termes de maîtrise et d’assurance. Il en va de même pour les développeurs.

### Qu’est-ce que du bon code ?

Bien évidemment la qualité du code est une notion assez subjective, pour autant il existe des critères qui forment le minimum commun pour du code de qualité. 
Voici quatre critères qui caractérisent du bon code quel que soit votre niveau en programmation.

#### 1.	Facile à lire

Le premier point est certainement le plus connu, mais aussi le plus vague. En effet du code de qualité est du code facile à lire. Cela peut paraître évident, mais ce n’est pas aussi facile qu’on l’imagine. D’autant que dans le cadre d’un projet professionnel le code doit être aussi facile à lire pour celui qui l’écrit que pour ceux qui passeront après. Écrire un code facile à lire pour les autres est loin d’être évident si on n’est pas au fait des bonnes pratiques de développement et des standards des technologies utilisées.

Pour avoir un code lisible, il faut donner de l’importance à la présentation. Un code bien présenté est aéré et facilite la visualisation des blocs, des fonctions et des structures de données. De la même manière, les noms de variables, des fonctions et des classes doivent être intelligibles et faire sens dans le programme.

J’aime à penser que, plus que d’être lisible, un bon code est agréable à lire.

#### 2.	Organisation logique et évidente

Lorsque l’on rentre dans un code déjà écrit on reconnaît un code propre et de qualité à la facilité avec laquelle on peut trouver ce que l’on cherche. Il est important d’avoir une organisation claire de son code en allant au plus simple.

Tout le monde n’a pas la même vision de la simplicité. En effet, quelque chose de simple pour un développeur expérimenté ne le sera peut-être pas pour un développeur débutant. Un code peut paraître illogique s’il se base sur un patron de conception qu’on ne connaît pas encore. Encore une fois, il est important de bien connaître les bonnes pratiques de développement et de connaître les recommandations aux langages et aux Framework qu’on utilise.

Cependant, il existe quelques préceptes simples à respecter en toutes circonstances. 

•	Faire le plus simple possible

Que cela concerne l’organisation du projet et le code directement, il est important de faire le plus simple possible. La complexité d’un projet va croître avec le temps, c’est inéluctable, il est donc important de limiter ce phénomène en n’ajoutant pas de complexité inutile. De fait, un code simple et plus lisible et maintenable.

•	Avoir une vision métier plutôt qu’une vision technique

Une chose est certaine du code ne sert à rien s’il n’est pas au service d’une tâche particulière. La vraie valeur de votre code source est dans les problèmes qu’il résout et pas seulement dans son implémentation. Quand on ouvre votre projet dans un IDE, on doit pouvoir s’aventurer dans le code facilement dès lors qu’on comprend les aspects métier.

•	Séparer le métier du reste

Un langage est un outil tout comme un Framework. Il vous faut souvent écrire du code pour gérer la configuration technique d’une application ou pour le lancement du Framework que vous utilisez. Il est important que le code technique et le code métier soient dissociés. D’une part, cela facilite la lisibilité et d’autre part cela favorise la maintenabilité et la testabilité de l’application. Imaginer que vous réalisiez une application en Angular et que demain vous souhaitez passer sur une application en React. Cette opération ne devrait pas être compliquée dans la mesure où cela ne touche qu’au code technique. Votre code métier ne devrait pas être impacté du tout.

#### 3.	Explicite

Il n’y a rien de plus énervant que de devoir aller à droite à gauche dans des documentations pour comprendre un algorithme ou à quoi sert telle ou telle fonction. Un bon code se suffit à lui-même et ne nécessite rien d’autre pour être compris. 

Dans la même veine que le deuxième point, vous devez écrire du code simple et efficace tout en étant le plus explicite possible dans vos intentions. Votre code ne doit jamais dépendre d’une source externe pour pouvoir être compris. Les documentations externes sont donc à éviter. Si vous devez communiquer des informations concernant vos choix techniques ou les hypothèses concernant un algorithme alors vous devez le faire directement dans le code à l’aide de commentaires.

Tout comme dans une application, il faut éviter de faire naviguer un relecteur dans votre code. Cela ne veut pas dire qu’il faut s’abstenir de découper son code en différents blocs, fonctions, classes, etc. Seulement cela doit être fait sans offuscation. Pour comprendre un bloc de code, il ne doit pas, il y avoir besoin de descendre dans l’implémentation de chaque fonction. L’en-tête de ces dernières doit être suffisant.

Un dernier point concernant la compréhension du code concerne les tests. En effet, il n’y a pas de meilleure documentation que les tests. Tout comme pour le code, il y existe des bonnes pratiques pour rédiger des tests correctement. Ces derniers sont un bon point d’entrée pour un nouveau venu sur l’application afin de comprendre le fonctionnement de votre code.

#### 4.	Robuste dans le temps

Comme rappeler en introduction le code ne se limite pas à une application qui fonctionne. Il faut l’entretenir en permanence afin qu’il résiste aux affres du temps, ou plus particulièrement aux ajouts successifs qui auront lieu tout au long de la vie du projet.

Aujourd’hui trop de développeur et d’entreprise ont tendance à penser qu’à partir du moment où le code est passé en production tout est fini. Mais c’est faux. En vrai, le code doit être entretenu tout comme une voiture pour continuer à bien fonctionner dans le temps et pour rester maintenable.

Il ne faut pas hésiter à itérer pour produire une solution. D’abord quelque chose de simple et directe qui répond au problème. Ensuite une solution plus sophistiquée qui mise sur les bonnes pratiques. Il ne faut pas hésiter à avoir recours au « refactoring » même des mois après quand on tombe sur du code qui nous pose des problèmes. C’est de cette façon qu’on entretient la base de code d’un projet. 

Le « refactoring » est un bon moyen pour conserver un code robuste et maintenable tout en conservant les connaissances sur la base de code. C’est aussi le meilleur moyen de contenir la complexité grandissante d’un projet avec le temps.

### Comment produire du bon code ?

Il n’y a pas de formule magique, la première chose à faire est d’adopter le bon état d’esprits. C’est-à-dire qu’il faut produire du code dont on soit fière et qu’on veut maintenir dans la durée. On ne doit pas être dans l’idée de se débarrasser de son code au plus vite en visant uniquement la livraison. Ensuite, il faut avoir en tête les quatre points évoqués précédemment à chaque nouvelle ligne de code.

Il faut également se dire qu’il est quasiment impossible de produire le meilleur code possible du premier coup. De fait, au lieu de ne vouloir écrire que du code parfait, il faut accepter que son premier jet ne soit pas le meilleur. C’est avec le temps et les reprises successives du code qu’on approche petit à petit de la perfection. Un code source, c’est un peu comme une œuvre d’art, pour celui qui l’écrit, il n’est jamais terminé. Afin d’avoir cette vision itérative, des pratiques comme le TDD sont aujourd’hui indispensables.

Il existe bon nombre d’indicateurs afin d’évaluer le code qu’on produit. Ils peuvent être utilisés a posteriori via des outils de qualité de code ou en live dans votre IDE. Vous pouvez aller regarder un outil comme SonarQube par exemple. Même s’il existe beaucoup de configuration par défaut et que certaines peuvent suffire dans bien des projets, il ne faut pas hésiter à configurer ces outils en fonction de vos standards de qualité.

Un dernier point important qu’il faut mettre en avant et c’est le travail d’équipe. Il n’existe pas, à mon avis, de meilleurs moyens pour produire du bon code que de travailler à plusieurs. Le pair programming permet de résoudre les questions autour de la lisibilité de votre code. Il permet également de prendre du recul sur le code et d’avoir un regard différent ce qu’on implémente. Cela offre également l’opportunité de communiquer en temps réel avec un autre développeur qui est aligné sur les mêmes objectifs. Une autre méthode permettant d’impliquer d’autres personnes sur ses réalisations est la revue de code. Mais elle ne permet d’avoir des retours que lorsqu’on décide de les demander. Cela peut arriver tard et causer pas mal de frustration si on se retrouve avec beaucoup de retour qui conduise à des changements. Elle reste néanmoins un bon complément pour aller chercher un regard extérieur et s’assurer de l’homogénéité des différentes contributions d’un projet.

Pour conclure, je dirai que pour produire du bon code, la meilleure arme d’un développeur, c’est sa capacité à se remettre en question. Il est important d’être capable de revenir sur ce qu’on a déjà fait et d’accepter les limites de chaque solution qu’on propose. C’est le premier pas vers l’amélioration continue.

Si vous souhaitez vous former aux bonnes pratiques de développement, je vous conseille de jeter un œil à notre offre d’accompagnement. Il y a un parcours pour les débutants qui souhaitent devenir développeur. Nous allons bientôt proposer une offre pour des développeurs qui souhaitent faire évoluer leurs compétences et aller vers toujours plus de code de qualité. Vous pouvez également aller faire un tour sur [artisandeveloppeur.fr](https://artisandeveloppeur.fr/). Benoit Gantaume propose un excellent podcast qui vous permettra de comprendre l’état d’esprit qu’il faut avoir pour produire du code durable.
