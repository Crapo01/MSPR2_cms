# CMS for MSPR

# DEPLOIEMENT D'UNE NOUVELLE INSTANCE REACT VITE:

Cloner le repo.

Aller à la racine du site cd MSPRFRONT

  npm install 

pour installer toutes les dependences

Configurer les Variables d’Environnement

📌 Créer un fichier .env dans le dossier racine et ajouter les variables nécessaires :

Ajoute tes variables d’environnement :

    VITE_SITE_KEY = 

📌 Mettre à jour scr/config/config.js et ajouter l’URL de base:

    //export const BASE_URL="http://localhost:8080";
    export const BASE_URL="https://msprback-cms-reworked.onrender.com";


### lancement de l'app+serveur applicatif

  Aller à la racine du site et lancer dans la console:  
  
    npm run dev 

### BUILD de l'app pour deploiement WEB

  Aller à la racine du site et lancer dans la console:
  
    npm run build

  le build est dans le dossier dist

### deploiement sur serveur WEB

  transferer l'ensemble du dossier dist via  filezilla dans le dossier HTDOCS du serveur web

# MSPR2 development steps

## DEPENDENCIES

    npm install react-router-dom
    npm install react-bootstrap bootstrap
    npm install axios
    npm install react-validation validator
    npm install formik --save

  ## Connect to API
  
  API concert end point:  
  api/concerts"

  API actus end point:  
  api/informations

  API pointeur end point:  
  api/pointeurs



## Security

added signup/login/logout

source:  
[react-jwt-auth](https://www.bezkoder.com/react-jwt-auth/)

users are registered with ROLE_NONE role automatically.

users can be upgraded by ROLE_ADMIN user to:

ROLE_VIEWER: read only access with limited informations  
ROLE_EDITOR: read/write/update/delete access for concert/info/pointeurs endpoints    
ROLE_ADMIN: read/write/update/delete access for users endpoint  

## reCAPTCHA implementation

[react recaptcha](https://shejanmahamud.medium.com/implement-google-recaptcha-in-react-app-a9b8e3dc26ed)  
[useref in class components](https://stackoverflow.com/questions/62499061/how-to-use-react-useref-in-class-component) 



### backend validation

[springboot recaptcha validation](https://www.pixeltrice.com/recaptcha-validation-in-registration-form-using-spring-boot-application/)

endpoint api/auth/verify

## PUSH NOTIFICATIONS

    
resource:

[send-push-from-spring-boot-backend-to-react](https://hpcodes.medium.com/send-messages-from-spring-boot-backend-to-reactjs-app-using-websocket-4120f6979c9b)

https://www.npmjs.com/package/react-stomp-hooks

added send message 

added delete message