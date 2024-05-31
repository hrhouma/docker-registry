# C'est quoi un Docker Registry 
Un Docker Registry est un service permettant de stocker et distribuer des images Docker. Voici quelques utilisations principales d'un Docker Registry :

1. **Stockage des images Docker** : Il permet de centraliser toutes les images Docker utilisées par une organisation. Cela facilite la gestion, le partage et la distribution des images entre les différents environnements de développement, test et production.

2. **Distribution des images** : Le Docker Registry facilite le déploiement d'images Docker sur différents serveurs et environnements. Les développeurs peuvent tirer (pull) les images du registre pour les utiliser localement ou les déployer dans des environnements de production.

3. **Versioning des images** : Les registres Docker permettent de versionner les images. Ainsi, il est possible de revenir à une version antérieure d'une image si une mise à jour pose des problèmes.

4. **Sécurité et contrôle d'accès** : Les Docker Registries peuvent être configurés pour gérer les accès et sécuriser les images. Par exemple, Docker Hub permet de créer des registres privés où seules les personnes autorisées peuvent accéder aux images.

5. **Intégration avec CI/CD** : Les Docker Registries sont souvent intégrés dans des pipelines CI/CD (intégration continue et déploiement continu), permettant d'automatiser le processus de construction, de test et de déploiement des images Docker.

### Exemples de Docker Registries

- **Docker Hub** : Le service de registre public officiel de Docker. Il propose des registres publics et privés.
- **Azure Container Registry (ACR)** : Un service de registre Docker fourni par Microsoft Azure.
- **Amazon Elastic Container Registry (ECR)** : Un service de registre Docker fourni par AWS.
- **GitLab Container Registry** : Un registre intégré à GitLab permettant de stocker les images Docker associées aux projets GitLab.

En résumé, un Docker Registry est essentiel pour la gestion efficace des images Docker, offrant des fonctionnalités de stockage, de versioning, de sécurité et d'intégration avec des processus de déploiement automatisés.
