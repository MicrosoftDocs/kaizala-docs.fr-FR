# <a name="security-for-end-users"></a>Sécurité pour les utilisateurs finaux
## <a name="client-data-protection"></a>Protection des données client

Tous les stockages les données sur android, iOS et Windows Clients sont effectuées sur les stockages internes qui fournissent des Sandbox de l’Application, qui isole votre application data et code l’exécution à partir d’autres applications. L’utilisateur posséder les autorisations pour restreindre l’accès aux fonctionnalités du système et des données utilisateur sont utilisées uniquement. Kaizala suit toutes les normes de plateforme pour restreindre l’accès aux ressources de clients en fonction des autorisations autorisées. Aucun stockage externe qui permet le monde accès en lecture et écriture, n’est utilisé. MODE_WORLD_READABLE ou MODE_WORLD_WRITEABLE ne sont pas activées. 

## <a name="authentication-and-authorization"></a>Authentification et autorisation

Application mobile Microsoft Kaizala authentifie les utilisateurs de périphériques à l’aide de numéro de téléphone et une fois le mot de passe unique pour l’expérience de l’intégration et plus facile d’inscription.  

Pour des raisons de sécurité, Kaizala s’applique également plusieurs stratégies de sécurité pour limiter un numéro de téléphone à un périphérique à une heure et le nombre de demandes unique dans une journée.  

Accès à toutes les données client telles que des messages, des documents, des médias, etc. est limité et les utilisateurs finaux pertinents, membres du groupe Administrateurs de l’organisation. 

L’authentification multifacteur pour les utilisateurs de l’application Kaizala peut être activée par le biais de stratégies de groupe. Un administrateur de groupe ou le locataire peut-être imposer la connexion du compte Office 365 (DAS) supplémentaires pour être en mesure d’ouvrir un groupe Kaizala. Cela signifie qu’un utilisateur doit se connecter avec un compte DAS lié dans une application mobile Kaizala, en outre au numéro de téléphone & unique. Jusqu'à ce que l’utilisateur se connecte avec DAS lié compte, les messages dans le groupe ne sont pas visible par l’utilisateur pour le groupe configuré. 

Portail de gestion Kaizala utilise l’authentification des services Azure Active Directory pour sécuriser l’accès et la gestion des données d’organisation. Ce service est utilisé par des millions de clients dans le monde pour l’hébergement de leurs données métiers en toute sécurité dans Office 365. 

Dans Kaizala, contrôle total de gestion de groupe et les appartenances est limité aux seules groupe et les administrateurs d’organisation respectifs. 

## <a name="kaizala-group-policies"></a>Stratégies de groupe Kaizala

Kaizala permet aux administrateurs de client et de groupe contrôler le flux de données et le comportement à l’intérieur d’un seul ou tous les groupes de l’organisation. Voici les différentes stratégies de groupe qui peuvent être configurés par le client et du groupe Administrateurs pour améliorer la sécurité des données : 

  
- Limiter les messages, les pièces jointes et les Actions Kaizala de transfert à partir du groupe actuel ou de ses groupes d’organisation 
- Restreindre la copie du contenu des messages, les pièces jointes et les Actions Kaizala 
- Restreindre le partage de contenu des messages, les pièces jointes et les Actions Kaizala 
- Activer l’authentification multifacteur pour les membres par le biais de DAS telle que l’utilisateur doit se connecter avec son compte DAS pour afficher les messages dans le groupe d’organisation. 
- Activer Microsoft Intune des stratégies avancées, par exemple le code confidentiel après la durée d’inactivité. À moins que l’utilisateur activé Intune, le groupe ne peut pas être ouvert par l’utilisateur. 

## <a name="mobile-application-management-with-microsoft-intune"></a>Gestion des applications mobiles avec Microsoft Intune

Pour la gestion avancée des applications, l’application mobile Kaizala peut être en conteneur à l’aide de Microsoft Intune. Microsoft Kaizala est en mode natif intégré avec Intune SDK et fournit des première prise en charge des stratégies spécifiques avancées Intune répertoriées ci-dessous :
    - Nécessitent un accès PIN sur application mobile pour la sécurité du client améliorée 
    - Bloc gérées applications de s’exécuter sur jailbroken ou périphériques racine 
    - Restreindre couper, copier, Coller avec les autres • applications gérées application Restrict pour transférer des données vers / à partir d’autres applications gérées 
    - Capture d’écran de bloquer ou de partage d’écran 
    - Appliquer la version du système d’exploitation android minimale 
    - Restreindre le contenu web à afficher dans le navigateur géré
    - Intervalle d’en mode hors connexion avant des données sont effacées. 

Les stratégies Intune peuvent être facilement gérées de manière centralisée via le portail Intune, comme indiqué ci-dessous :  

![Intune.PNG](Images/Intune.png)



