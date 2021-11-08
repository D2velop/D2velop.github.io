---
layout: post
title:  Leadformance
date:   2020-11-09 09:00:00 +0200
categories: dev-life
author: Cédric Gérard
image: https://static4.pagesjaunes.fr/media/vignette/AAAJPDUUIK2W-73004.gif
tags: dev chronique
---

Me voici donc toujours au même endroit, mais officiellement employé de Leadformance. On pourrait croire que cela n’a pas changé grand-chose. Mais pour moi, c’était vraiment comme un nouveau job.

## Un seul patron

J’étais vraiment heureux de me débarrasser de ma société de services. J’avais le sentiment qu’elle ne m’apportait rien, si ce n’est des obligations en plus de l’investissement que je mettais chez Leadformance (LF).

Je devais rendre des comptes au CTO chez LF concernant les projets sur lesquels je travaillais. Et je devais rendre des comptes à mon manager chez Kaizen. Parfois, les deux étaient alignées et parfois non.

Je me suis senti beaucoup plus libre de ne plus avoir à gérer la société de services en plus de mon quotidien. Je n’avais plus cette sensation de ne pas trop être à ma place, parce que j’étais presta, chez mon client et ne pas être à ma place chez Kaizen parce que je n’avais pas de lien avec mon entreprise.

## Une boite agile

Là, j’étais enfin calé, je savais où j’allais et les règles étaient claires. Après mon passage en binôme sur l’API publique, j’avais rejoint une des équipes qui bossait sur la version 3 de BRIDGE, le produit développé par Leadformance. Cette équipe fonctionnait en SCRUM et je trouvais ça plutôt bien. Il y avait un bon rythme et nous avancions avec des release du produit toutes les semaines, le mardi. 

Il y avait un super équilibre entre l'équipe produit et les devs. Nous pouvions retravailler le code sans problème tout en mettant en place de nouvelles fonctionnalités. Il y avait une bonne démarche de qualité de code, compris par l’ensemble des parties prenantes des différents projets. Nous pouvions être en contact direct avec des clients. Ça a été mon cas, plusieurs fois concernant l’API publique. J’ai été en contact avec les entreprises qui montaient un projet d’intégration de notre API.

Il y avait peu d’intermédiaires entre la direction et les employés. Je pouvais facilement discuter avec le CEO qui était en vérité mon N+2, il n’y avait que mon CTO entre nous. J’adorais également le fait que les équipes ne soient pas cloisonnées. Il n'y avait pas les dev d’un côté, le service client de l’autre et impossible de se parler autrement que par un gestionnaire de tickets. On échangeait avec tout le monde facilement, ce qui nous permettait de bien comprendre les problématiques métiers des différents utilisateurs. Lorsqu’un bug était remonté, il n’y avait pas de bloqueur pour pairer avec l’auteur du ticket du bug (dev ou pas) pour bien comprendre le problème et proposer une solution qui tienne la route.

## Aspects techniques

Côté technique, c’était vraiment top. J’ai beaucoup appris en NodeJS et sur les architectures micro-services. J'ai vécu la gestion d’un SaaS en production avec une clientèle internationale, du BtoB avec des grands comptes et les exigences qui vont avec.

J’ai également beaucoup appris sur la qualité de code. C’était la première fois que j’avais une CI énorme qui permettait de suivre les TU, TI et E2E liés à une PR avec à la fin un rapport détaillé. On avait également un retour sur la couverture de code. Il y avait des règles simples, pour pouvoir "merger" sa branche, il fallait, avoir eu une revue de code par un dev, que tous les tests (TU,TI et E2E) passent. Et qu’on ai pas diminué la couverture de code. Cela sous-entendait, qu’on devait ajouter les tests correspondant au code de production ou qu’on ait pas supprimé de tests par "erreur".

Bref, j’ai découvert de vrais processus d’industrialisation du logiciel, avec une base de code conséquente, composé de plusieurs services, des différentes bases de données. Tout ça conteneurisé avec Docker et déployé dynamiquement chez AWS avec Kubernetes et Terraform. J’ai découvert la possibilité de "scaler" son infra en une ligne de commande, et même de la voir "scaler" dynamiquement en fonction de la charge.

C’était vraiment une expérience super enrichissante techniquement parlant.

## Aspects humains

J’ai également découvert une nouvelle forme de management. Les équipes étaient auto-organisées. On pouvait choisir notre mode de fonctionnement et nos outils. On pouvait tester de nouvelles manières de travailler tant que cela n’impactait pas d’autres équipes. Nous étions 25 développeurs repartis sur 4 équipes produits et sur 2 sites géographiques. Nous travaillions tous sur le même produit global avec une application Angular pour note back office. Cela fonctionnait bien, les équipes ne se marchaient pas dessus et nous pouvions être efficaces.

Il y avait des développeurs qui étaient les lead dev de la boite, même s'ils n’en avaient pas le rôle officiellement. Ces derniers avaient la vision la plus large du produit, ils étaient parmi les plus expérimentés et étaient à la base des choix techniques et architecturaux de la version 3 de BRIDGE. Même si deux d’entre eux n’étaient pas motivés pour mon intégration, je n’ai pas eu de problème à mon entrée sur la V3. Il y avait peut-être un manque de confiance, mais je dois dire qu’à cette époque, je n’étais pas très sûr de moi non plus. Il y a avait tellement de concepts à maîtriser et de règles pour garantir la qualité de code que chaque ligne de code me demandait beaucoup d’effort. Je sais aujourd’hui que c’est mon manque de maîtrise technique concernant les bonnes pratiques qui me mettait en difficulté.

J’ai beaucoup travaillé avec les développeurs les plus juniors de LF. J’ai même eu à encadrer des stagiaires et des alternants. C’est quelque chose que j’ai beaucoup aimé. J’ai, à ces occasions, pris conscience du chemin que j’avais parcouru depuis mes débuts. De tout ce qui me paraissait évident, mais qui ne l’était pas pour un junior. Cela a été une révélation et ça m’a redonné du courage pour continuer à m’améliorer.

Vers la fin de mon contrat, j’en étais même arrivé à être considéré comme le lead dev de mon équipe. Il n’y avait rien d’officiel, mais la confiance que l’équipe plaçait en moi était super gratifiante.

J’ai également pris part à une vague de recrutement en participant aux entretiens des candidats. C’est une période que j’ai particulièrement appréciée. C’est super intéressant de pouvoir échanger avec d’éventuels futurs collègues. On doit s’assurer que la personne s’intégrera bien dans l’équipe, sur le plan humain et technique, mais aussi qu’elle partage nos valeurs et pratiques. Je trouve que c’est un exercice qui montre clairement que tu apprécies ou pas ton entreprise. La façon dont tu la présentes à un candidat en dit long. C’est aussi un bon moyen de faire le point sur ta situation, les questions des candidats étant souvent des déclencheurs pour se poser les bonnes questions.

## Qualité de vie

Je ne l’ai évoqué que très peu pour mes autres jobs, mais la qualité de vie est un aspect indispensable pour un bon poste. C’est ça qui nous permet de tenir sur la durée et du supporter les difficultés. Si la qualité de vie n’est pas au rendez-vous alors au premier problème, tout peut partir à la dérive.

Il n’y a pas de recette absolue pour permettre de définir ce qui nous offre une bonne qualité de vie. Cela appartient à chacun. Les seuls points communs, ce sont les ingrédients. À chacun de faire son propre mélange ensuite.

Voici un diagramme qui représente les critères qui sont importants à mes yeux (aujourd’hui sur la courbe bleue) pour garantir ma qualité de vie et ce que je ressentais dans mon travail (à LF ou même avant en orange). Je précise qu’il s’agit de ma perception et que ce n’est pas nécessairement la même réalité pour tout le monde à l’époque.

![qualite de vie](/assets/posts/leadformance/graph_qualite_vie.jpg){: .post_img .post_img_lg}

À l’époque où j’étais à Leadformance, je n’aurais pas été capable de faire cette introspection. Il m’a fallu prendre du recul et vivre d’autres choses pour pouvoir le faire.

Ce dont je suis sûr aujourd’hui, c’est que, si vous n’êtes pas aligné avec au moins vos trois principaux points, vous ne pouvez pas être épanouie au travail. Ça ne veut pas dire que c’est la catastrophe et que vous êtes mal. Simplement, vous aurez toujours une impression de manque, une frustration qui vous empêchera de profiter pleinement de victoire et qui rendra les défaites plus lourdes. Bien évidemment cet impact est plus fort avec la distance entre vos attentes et ce que vous vivez.

J’avais cette petite frustration à ce moment-là, que j’évacuais en râlant beaucoup 😣 et à voir mes collègues de l’époque, je ne devais pas être le seul à avoir quelque chose qui démange.

## Une histoire de rachat

Leadformance était une startup qui avait été racheté depuis quelques années sans que cela ne change quoi que ce soit, en tout cas pour le côté métier. Mais lorsque je suis arrivé, le groupe s’est beaucoup réorganisé, la petite startup Chambérienne a été intégrée plus activement dans les affaires du groupe.

J’ai donc vécu la transformation d’une entreprise qui se fait rachetée et qui passe de la dynamique d’une petite PME de 60 personnes à celle d’un groupe de plusieurs milliers de salariés.

Je vous raconte ça dans un prochain post.