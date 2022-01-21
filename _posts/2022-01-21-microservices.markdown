---
layout: post
title:  Les microservices
date:   2022-01-21 09:00:00 +0200
categories: technologie
author: Cédric Gérard
image: https://cdn.pixabay.com/photo/2018/12/01/09/53/network-3849202_1280.jpg
tags: dev technologie
---

Depuis quelques années, on entend beaucoup parler de microservices. Mais qui a-t-il réellement dernière cette dénomination ? Et surtout qu’est-ce que cela implique sur un projet ?

### Un effet de mode ?

Les microservices sont à la mode depuis quelques années. Ils ont été popularisés par des géants comme Netflix ou Amazon, pour ne citer qu’eux, qui communiquent beaucoup sur leurs solutions techniques. Comme souvent chaque communication ou projet open source lancée par ce genre de géant à tendance à créer un effet de mode qui est souvent repris dans les startups du moment.

Cela n’a pas manqué pour les microservices qui se sont vu présenter comme la solution ultime à tous les soucis des applications actuelles en terme de scalabilité, de couplage et de maintenabilité.

### Microservices, quésaco ?

Tout d’abord, que met-on derrière miroservice ? En fait, il ne s’agit pas d’une grande révolution par rapport à ce qu’on était capable de faire à l’époque. Il s’agit d’une variante des architectures orientées services (SOA – service-oriented architecture) avec comme particularité de découpé les services le plus finement possible. Avant cette approche, les solutions étaient déjà découpées afin de gérer la scalabilité de chaque partie spécifiquement. Le principe des microservices tient dans le terme « micro ». Ces derniers doivent être le plus petit possible et le plus simple possible. La conséquence est qu’on se retrouve vite avec un grand nombre de services à déployer et maintenir.

Dans les faits, pas de révolution, il s’agit d’une approche architecturale différente de ce qu’on faisait auparavant. Cette approche a été rendue possible avec deux évolutions techniques majeurs au niveau infrastructure et déploiement. La première, c’est le développement du cloud et des services d’hébergements. La deuxième est la conteneurisation des applications. Comme je vous l’ai expliqué au paragraphe précédent, avec les microservices on se retrouve à déployer beaucoup d’unité et on doit être capable de gérer les déploiements de chaque service indépendamment. Docker et les plateformes cloud comme AWS, Azur et Google Cloud ont ouvert la voie avec des outils permettant de répondre à ces besoins.

Quand on parle de beaucoup de services, il faut voir ce découpage comme le plus petit possible d’un point de vue technique et le plus proche possible du métier. En gros, on se retrouve avec au minimum un service par fonctionnalité. Bien souvent, les contraintes techniques ou les dépendances externes amènent à avoir plusieurs services pour une seule fonctionnalité. Au final, notre application peut compter plusieurs dizaines de services dans les cas simples et plusieurs centaines pour un gros projet. Cela demande d’avoir une plateforme de déploiement qui tient la route et un monitoring au top.

Il reste une dernière problématique qui est la communication entre ces services. Dans la plupart des cas, les services ne sont pas tous au même niveau. Vous allez, par exemple, avoir une API comme point d’entrée ou une application en front. Et les appels vont déclencher tout un enchaînement d’actions dans vos services pour aboutir au résultat attendu. Il y a une grosse partie d’échange entre ces derniers qui apporte un autre niveau de complexité. En effet, votre application ne doit pas planter si un service et hors d’usage. Vous devez être capable de tracer les échanges et reproduire les actions afin d'éviter les pertes de données et pouvoir comprendre les comportements en production. Pour cela, on utilise des "message brocker" (Kafka, RabbitMQ, etc.) pour gérer les échanges et la synchronisation des services. Cette partie est souvent celle qui est négligée et encore plus souvent sous-estimée, mais c’est pourtant la plus critique. Il faut bien comprendre que votre brocker va acheminer une importante quantité de messages. Avoir plusieurs millions de messages par jours n’est pas rare sur une application de taille normale.

### La solution ultime ?

Pour être honnête, je n’ai jamais vu un système conçu sur la base de microservice bien conçu. J’ai à chaque fois, sois eu un surcoût monstrueux en maintenance à cause de mauvais choix techniques ou un découpage raté qui aboutit plutôt à des macroservices. Dans le dernier cas, on se retrouve avec la complexité des microservice et la lourdeur d’une application monolithique. C’est certainement ça qui a fait la mauvaise réputation des systèmes distribués à une époque pas si lointaine.

Au final est-ce que le coût des microservices en vaut la peine. Je dirai que dans 95 % des cas, non. Il faut comprendre que les microservice répondent principalement à des problématiques de scalabilité par une optimisation des déploiements. La capacité de scaler unitairement et dynamiquement chaque service est un besoin assez rare qu’on retrouve chez les géants du numérique. Les besoins de Netflix ou Facebook sont à des années-lumière de ce qu’on peut retrouver dans les projets communs même s'ils paraissent énormes.

Le problème des microservices et qu’ils nécessitent dès le début une infrastructure lourde, qu’ils ajoutent un surcoût non négligeable sur les aspects synchronisation entre services et qu’ils sollicites beaucoup plus la couche réseau. 

Au-delà de la scalabilité on vente les microservices pour résoudre des problèmes de couplage dans une application. Je suis personnellement en désaccord avec cette affirmation. Dans les faits, les microservice s’intéressent au découpage d’une application et offrent des opportunités au niveau du déploiement d’une solution, ils ne changent pas grand-chose côté code. Vous pouvez avoir autant de couplage entre de services distribués que dans un monolithe. Et à l’inverse avoir un monolithe qui ne souffre d’aucun problème de couplage et qui d’ailleurs pourrait être découpé facilement par la suite si besoin. Il faut aussi avoir en tête que même si les microservice permettent une gestion plus fine des déploiements ils coûte aussi beaucoup plus cher niveau infrastructure.

### Ma vision des microservices

Si d’aventure vous voulez quand même vous lancer voici les conseils que je pourrais donner suite à mes retours d’expériences:

- Découper votre application en services en fonction de vos contextes métier et le plus finement possible. Un service ne doit avoir qu’une seule responsabilité

- Créer un service pour encapsuler chaque dépendance externe

- Vos services doivent exposer des contrats clairs tant concernant les API que les messages qui passent par votre brocker. Il est nécessaire de définir ces contrats dès le début (c’est un moyen d’éviter les couplages implicites)

- Penser que dans les microservices on privilégie la remplaçabilité à l’évolutivité. J’entends par là que, contrairement à un monolithe, on ne va pas forcément modifier une service existant pour changer son comportement, mais plutôt coder un nouveau service qui le remplacera à terme. Ainsi, il n’y a pas de risque de casser l’existant et le rollback est facile à automatiser via l’orchestrateur de services. Vous comprendrez que cette technique n’est faisable que si vos interfaces de services sont contractualisées et ce n’est rentable que si vos services sont « micro ». Je peux illustrer ce point avec un service de cartographie. Vous avez un service existant qui se base sur GoogleMap. Vous décidez pour de changer pour le service HereMap. Vous ne faites pas de modification dans le service existant. Vous allez implémenter un nouveau service qui utilise HereMap et qui va implémenter le même contrat que l'ancien. Ensuite, vous remplacerez l'ancien service au déploiement

- Concernant vos messages, ils doivent être le plus précis possible. Par exemple, si vous avez un service qui gère vos clients. Lors d’une mise à jour de l’e-mail, il ne faut pas envoyer un message de mise à jour avec comme payload tout le client. Une bonne pratique serait d’envoyer un message avec uniquement l’information de ce qui a été changée

- Conteneuriser vos services dès le début

En conclusion, pour un nouveau projet, je n’opterai pas pour les microservices dès le début. Je commencerai par un monolithe en m’appuyant sur des pratiques comme les DDD, BDD ainsi que sur l’architecture hexagonale pour éviter le couplage et définir les contextes métiers de mon application. Avec cette approche, il est toujours possible de sortir un contexte dans son propre service plus tard pour répondre à un problème particulier de déploiement ou de scalabilité unitaire. Il est très rare d’atteindre les limites d’une application monolithique même sur un gros service. La plupart du temps, c’est l’état du code qui est la cause des limitations et non la typologie de la solution.

