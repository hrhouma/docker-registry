# Tutoriel de base sur la mise en place et l'utilisation d'un Docker Registry privé. 
Ce guide couvre l'installation d'un Registry local, la poussée (push) et la récupération (pull) d'images Docker.

### Prérequis
- Docker installé sur votre machine. Vous pouvez télécharger Docker à partir du site officiel [docker.com](https://www.docker.com/products/docker-desktop).

### Étape 1: Lancer un Docker Registry local

1. **Démarrer le Registry**: Lancez un container Docker Registry en exécutant la commande suivante dans votre terminal :
   ```
   docker run -d -p 5000:5000 --name registry registry:2
   ```
   Cette commande télécharge l'image `registry:2` si elle n'est pas déjà présente localement, et démarre un container nommé `registry` qui écoute sur le port `5000`.

### Étape 2: Pousser une image dans votre Registry

1. **Tagger une image Docker**: Avant de pousser une image dans votre Registry local, vous devez la tagger avec l'adresse de votre Registry. Par exemple, pour tagger une image `monapp:latest` :
   ```
   docker tag monapp:latest localhost:5000/monapp:latest
   ```
   Remplacez `monapp:latest` par le nom et le tag de votre image.

2. **Pousser l'image dans le Registry**: Maintenant, poussez l'image taggée vers votre Registry local :
   ```
   docker push localhost:5000/monapp:latest
   ```

### Étape 3: Récupérer (Pull) une image depuis votre Registry

1. **Récupérer l'image**: Pour récupérer une image depuis votre Registry local, utilisez la commande suivante :
   ```
   docker pull localhost:5000/monapp:latest
   ```
   Assurez-vous que l'image que vous souhaitez récupérer a été préalablement poussée dans votre Registry local.

### Étape 4: Supprimer le Registry local (Optionnel)

1. **Arrêter le container Registry**: Si vous souhaitez arrêter votre Registry local, exécutez la commande suivante :
   ```
   docker container stop registry
   ```

2. **Supprimer le container Registry**: Pour supprimer le container après l'avoir arrêté, utilisez :
   ```
   docker container rm registry
   ```

### Conseils supplémentaires

- **Sécurité**: Par défaut, votre Registry communique en HTTP, ce qui n'est pas sécurisé. Pour une utilisation en production, envisagez de configurer une communication HTTPS avec des certificats SSL/TLS.
- **Stockage**: Par défaut, les données du Registry sont stockées dans le système de fichiers du container. Pour une utilisation en production, il est recommandé de configurer un stockage externe, comme un volume Docker, pour la persistance des données.
- **Nettoyage**: Avec le temps, votre Registry peut accumuler beaucoup d'images non utilisées. Docker fournit des outils et des stratégies pour nettoyer votre Registry et gérer l'espace disque.

Ce tutoriel fournit une introduction de base à Docker Registry. Pour des configurations plus avancées et des options de déploiement, veuillez consulter la documentation officielle de Docker Registry.
