# Guide d'utilisation

D'abord, je n'ai pas lu le fichier README avant de commencer le développement. Je ne l'ai lu qu'au moment de rendre l'exercice.  
Cependant, tout ce qui est demandé est faisable pour moi. J'ai réalisé que le temps qui me reste avant l'entretien technique demain est insuffisant pour entammer de nouveau une phase de dev.

L'instruction que j'ai reçue par e-mail est la suivante :

Comme convenu, voici le test que nos experts techniques ont mis en place pour les échanges techniques.

Il faut créer un module pour afficher une liste de produits qui peuvent être modifiés (en fonction de si l’utilisateur est admin ou non).

Le but est de faire le plus possible en fonction de vos compréhensions/compétences, et évidemment du temps que vous aurez à y accorder.

L’objectif est de pouvoir avoir une vision de votre réflexion et analyse.

https://alten.arcabox.net/invitations/?share=29d6d77126b857151b56&dl=0

Quand vous l’aurez terminé, vous pourrez l’ajouter à un GitHub et m’envoyer le lien ?

## 1. Lancer les deux applications : [Front-end](#front-end) et [Back-end](#back-end)

Ce projet comporte deux applications :
- **Back-end** : `shop-sapp` (Spring Boot)
- **Front-end** : Angular  

### Étapes pour démarrer les applications :  

1. Placez-vous à la racine du projet `product-trial-master`.  
2. Exécutez la commande suivante pour démarrer les applications (back et front) via Docker :

```sh
docker-compose up --build
```
Si tout se passe bien :

- Le back-end sera accessible sur
  
          http://localhost:8083

    - Le front-end sera accessible sur
    
           http://localhost:4200

### 2. Identifiants de connexion

L'application Angular est protégée par une page de connexion.

Deux utilisateurs sont créés au lancement de l'application, avec des rôles distincts :

Nom d'utilisateur	Mot de passe	Rôle

user	                12	        USER

admin	               123	        ADMIN


### 3. Points clés

   - L'utilisateur avec le rôle USER ne peut ni ajouter, ni modifier, ni supprimer un produit.

   - Seul l'ADMIN a ces permissions.

   - 10 produits sont insérées automatiquement au démarrage de l'application Spring Boot, dans une base de données en mémoire H2.

   - Quelques tests unitaires ont été ajoutés pour démontrer la faisabilité.
   
   - A la racine du projet product-trial-master existe le fichier User-db.postman_collection pour tester les API REST
