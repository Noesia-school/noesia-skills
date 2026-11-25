# Relire un Dockerfile — partie 4.2

Dans le projet à examiner, invoquez `@docker-image-review`. Le skill compare le
Dockerfile aux besoins de l’application et propose un plan, sans modifier les
fichiers, construire l’image ni lancer de conteneur.

Pour vérifier un conseil, ouvrez les lignes citées. Par exemple, le dossier où
le Dockerfile copie l’interface est-il bien celui que le serveur utilise ?

**Si l’agent propose un `docker inspect` sans filtre, ne le lancez pas** :
le résultat peut contenir des secrets. Ne le copiez pas dans la conversation.
Cette revue statique n’est pas un audit de sécurité. À vous de décider ensuite
quels changements appliquer et, séparément, comment les tester.
