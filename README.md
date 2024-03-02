# docker-registry
# Question : c'est quoi la différence entre Docker Registry et Votre espace sur Docker Hub ?
La différence principale entre un Docker Registry et votre espace sur Docker Hub réside dans leur utilisation et leur portée.

1. **Docker Registry**:
   - Un Docker Registry est un stockage et un système de distribution pour les images Docker. Il s'agit d'une application serveur qui vous permet de stocker et de distribuer des images Docker. Les registries peuvent être publics ou privés.
   - Vous pouvez héberger votre propre Docker Registry localement ou utiliser un service hébergé. Le but principal d'un Docker Registry est de partager des images au sein d'une organisation ou d'un projet, permettant ainsi une collaboration et une gestion des versions plus efficaces.
   - Docker Inc., l'entreprise derrière Docker, offre son propre Docker Registry public appelé Docker Hub, mais il existe d'autres options comme Quay.io, Google Container Registry (GCR), et Amazon Elastic Container Registry (ECR).

2. **Votre espace sur Docker Hub**:
   - Docker Hub est un service en ligne qui offre à la fois un Docker Registry public et des fonctionnalités de réseau social comme la possibilité de suivre des contributeurs et de noter des images. Votre espace sur Docker Hub est l'endroit où vous pouvez stocker vos propres images Docker, les rendre publiques ou privées, et où vous pouvez également trouver, télécharger et utiliser des images créées par d'autres utilisateurs et organisations.
   - Sur Docker Hub, vous disposez d'un compte utilisateur qui vous permet de gérer vos images, de collaborer avec d'autres, et de configurer des builds automatisés à partir de dépôts de code source.
   - Bien que Docker Hub soit le Docker Registry public le plus populaire, il sert également de plateforme pour la collaboration et le partage d'images au sein de la communauté Docker.

En résumé, un Docker Registry est un concept général pour un service de stockage et de distribution d'images Docker, tandis que votre espace sur Docker Hub est votre compte personnel ou organisationnel au sein du Docker Registry public de Docker Inc., offrant des fonctionnalités supplémentaires pour la collaboration et le partage d'images.
