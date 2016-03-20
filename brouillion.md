##### Construire une architecture micro - service

Back-end :
Symfony2 / Silex

Séparation des roles :
- Authentification
- Message
- Gestion des produits
- Paiement
- [...]

Communication entre WebService : 
- RestFull api (back => back)

Fron-end :
Framework js isomorphic :
- Angular
- Meteor
- React
- Backbone rendr
Framework php : 
- Symfony2

##### Gerer un projet

- ScrumDo (scrum + kanbran) pour gestion agile
- Poker planning
- Release managing
- Backlog + itération

##### Déployer un projet avec une intégration continu
- Platform.sh (best)

##### Structurer l'équipe

- Equipe TMA (Ou rotation)
- Equipe FRONT
- Equipe BACK
- Equipe chef de projet technique
- Equipe chef de projet fonctionel
- Architecte technique
- Ux / Ui designer

##### Veillez aux respect des bonnes pratique

Je pars du principe qu'il vaut mieux recadrer le dév à la source, 
plutot que d'attente la merge request ce qui fera perdre du temps à tout le monde

- Rappeler les règles du jeu avant chaque commit et responsabilité les développeur en leur demandant 
s'il ont bien réspecter ces règles afin d'avoir une réponse engageante de leur pars
- Vérifier à chaque commit (phpcs, phpmd, phpunit, behat, etc...)

##### Verifier avec des indicateur la stabilité de la plateforme

- Analyser les temps de réponses des urls dites clé (page accueil, etc...)
- Analyser la code de réponse (200, 404, 500) des urls dites clé (page accueil, etc...)

##### Gérer un deploiment éficace

- Vagrant en dev (généré avec ...)
- Capistrano en production

##### Optimiser les temps de réponse 

- Gerer le cache serveur (varnish, result cache mysql)
- Gerer le cache client (cdn, etc..)
- Gerer le cache applicatif (memcached, apc)

Une bonne stratégie de cache est basée sur ESI.
