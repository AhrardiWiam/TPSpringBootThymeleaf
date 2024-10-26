# TP : Spring Boot et Thymeleaf - Application CRUD d'utilisateurs

Ce projet est un TP simple qui illustre l'utilisation de Spring Boot et Thymeleaf pour créer une application Web CRUD basique permettant de gérer des utilisateurs.

## Prérequis

- **Java** 1.8 ou supérieur
- **Maven**
- Un IDE comme **IntelliJ IDEA** ou **Eclipse**
- **MySQL** (ou un autre SGBD) et un client pour y accéder

## Installation et Configuration

1. **Cloner le projet :**

    ```bash
    git clone [url du repo]
    ```

2. **Configurer le fichier `application.properties` :**

   Remplacez les valeurs `spring.datasource.url`, `spring.datasource.username`, et `spring.datasource.password` par les informations de connexion à votre base de données MySQL.

   Vous pouvez modifier le port du serveur (`server.port`) si nécessaire.

3. **Créer la base de données :**

   Créez une base de données nommée `thymeleaf` dans votre instance MySQL.

4. **Lancer l'application :**

   Ouvrez un terminal dans le répertoire du projet et exécutez la commande suivante pour construire et lancer l'application :

    ```bash
    mvn spring-boot:run
    ```

## Fonctionnalités

L'application offre les fonctionnalités CRUD de base suivantes :

- **Ajouter un utilisateur :**
  - Accédez à l'URL `/signup` pour afficher le formulaire d'inscription.
  - Remplissez les champs obligatoires (nom et e-mail) et soumettez le formulaire.

- **Afficher la liste des utilisateurs :**
  - La page d'accueil de l'application (`/`) affiche la liste des utilisateurs enregistrés.

- **Modifier un utilisateur :**
  - Cliquez sur le lien "Edit" à côté d'un utilisateur pour afficher le formulaire de modification.
  - Modifiez les informations et soumettez le formulaire.

- **Supprimer un utilisateur :**
  - Cliquez sur le lien "Delete" à côté d'un utilisateur pour le supprimer de la base de données.

## Structure du projet

Le projet est organisé de manière classique pour les applications Spring Boot :

- **`pom.xml`** : Fichier de configuration Maven qui définit les dépendances du projet.
- **`src/main/java`** :
  - `ma.thymeleaf.dem.demothymeleaf` : Paquet principal contenant les classes de l'application.
  - `DemothymeleafApplication.java` : Classe d'entrée de l'application.
  - `UserController.java` : Contrôleur gérant les requêtes HTTP pour les utilisateurs.
  - `UserRepository.java` : Interface du référentiel d'utilisateurs, utilisant Spring Data JPA.
  - `User.java` : Entité représentant un utilisateur.
- **`src/main/resources`** :
  - `application.properties` : Fichier de configuration de l'application.
  - **`templates`** :
    - `add-user.html` : Template du formulaire d'ajout d'utilisateur.
    - `update-user.html` : Template du formulaire de modification d'utilisateur.
    - `index.html` : Template de la page d'accueil affichant la liste des utilisateurs.

## Demonstration 

-La page principale:

![image](https://github.com/user-attachments/assets/f491bd54-d88b-4f0f-a943-7a33f5b5317e)


-La page pour créer un user:

![image](https://github.com/user-attachments/assets/fa59a06e-d8aa-414d-8ef8-7dae7a161ec2)


-La liste des users ( apres avoir crées plusieurs users)

![image](https://github.com/user-attachments/assets/8512c9a1-5fff-4cf7-809e-bcbf6d1a568d)

## Conclusion

Ce TP vous a permis de découvrir les bases de Spring Boot et Thymeleaf pour développer une application Web CRUD simple.
