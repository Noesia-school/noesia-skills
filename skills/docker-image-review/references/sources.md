# Références techniques

Documentation officielle consultée le 5 octobre 2026. Revenir à ces pages si un
point précis peut changer la recommandation. Les exemples ne constituent pas
une autorisation d’exécuter des commandes ni de manipuler des secrets.

- [Bonnes pratiques de construction d’une image](https://docs.docker.com/build/building/best-practices/) :
  séparer construction et exécution, choisir une base adaptée, limiter les
  dépendances et gérer les mises à jour des images fixées par empreinte.
- [Contexte de construction et `.dockerignore`](https://docs.docker.com/build/concepts/context/#dockerignore-files) :
  déterminer quels fichiers sont accessibles au constructeur et comment les
  exclusions peuvent varier selon le Dockerfile.
- [Référence du Dockerfile](https://docs.docker.com/reference/dockerfile/) :
  utilisateur, démarrage, signaux d’arrêt, ports et limites des sondes de santé.
- [Secrets nécessaires à la construction](https://docs.docker.com/build/building/secrets/) :
  utiliser un montage temporaire si nécessaire ; ne pas placer de secret dans
  `ARG`, `ENV` ou une couche de l’image.

Les consignes du skill sont originales ; aucun texte tiers n’est redistribué.
L’étude détaillée des sources, des licences envisagées et des essais reste dans
le dépôt pédagogique. Elle n’est pas nécessaire pour utiliser le skill.
