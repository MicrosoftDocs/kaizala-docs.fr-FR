# <a name="office-365-compliance-framework-and-microsoft-kaizala"></a>Infrastructure de conformité Office 365 et Microsoft Kaizala

Document de l'infrastructure de conformité Office 365 décrit les niveaux de classification de conformité avec les contrôles requis pour différents services Microsoft Online. Microsoft Kaizala suit la même infrastructure de conformité pour gérer & exploiter le service, ainsi que pour gérer les données client. Actuellement, Microsoft Kaizala est certifié pour la catégorie de conformité A par l'équipe interne de conformité de Microsoft Office 365, qui est responsable de la gestion de cette infrastructure. Cela signifie essentiellement que Microsoft Kaizala a de fortes engagements en matière de confidentialité et de sécurité avec une promesse de-

* Aucune exploration des données client pour la publicité 
* Aucune divulgation volontaire aux services répressifs 

## <a name="employee-training"></a>Formation des employés

S'il y a une intervention humaine minime pour maintenir le service en cours d'exécution, tous les ingénieurs qui travaillent sur le produit doivent être soumis à la formation sur la sécurité et la confidentialité. Microsoft s'assure également que tous les employés certifient l'acceptation des responsabilités pour les besoins en matière de confidentialité. 

## <a name="kaizala-compliance-features-for-customers"></a>Fonctionnalités de conformité Kaizala pour les clients

Les services et les données Microsoft Kaizala sont hébergés sur des centres de données Microsoft Azure locaux pour les clients indiens. Tous les messages, pièces jointes et actions partagés sur les groupes Kaizala pour les numéros de téléphone mobile Indiens sont stockés uniquement dans les centres de données situés en Inde.  
Kaizala fournit également des fonctionnalités qui aident les clients à répondre à leurs besoins de conformité. Voici les principales fonctionnalités liées à la conformité actuellement disponibles dans le produit: 

**1. affichage et gestion de tous les utilisateurs Kaizala disposant d'un accès aux données**

Kaizala gère une liste d'utilisateurs Kaizala spécifique à une organisation (KUL), qui est comme un annuaire téléphonique pour tous ses utilisateurs Kaizala, pour ses administrateurs pour la gestion centrale. Tout utilisateur qui devient membre d'un groupe d'organisation dans Kaizala devient automatiquement membre de KUL. Cela signifie qu'il s'agit d'une liste de tous les utilisateurs Kaizala qui ont un accès potentiel aux données des organisations, c'est-à-dire tous les membres de ses groupes d'organisation. Les administrateurs peuvent associer des attributs personnalisés supplémentaires spécifiques à leur organisation, tels que Aadhar, l'emplacement, la désignation, etc., pour faciliter l'identification. Il est également possible de supprimer un utilisateur de KUL, qui révoque automatiquement les appartenances aux groupes de l'utilisateur.  

**2. supprimer un utilisateur de tous les groupes d'organisation** 

Le portail de gestion Kaizala offre des fonctionnalités avancées de gestion des utilisateurs et des groupes, ce qui permet aux administrateurs d'intégrer et de quitter plus facilement les employés et les partenaires. En recherchant le numéro de téléphone d'un utilisateur, le portail répertorie tous les groupes dont l'utilisateur est membre. L'administrateur peut choisir de supprimer un utilisateur d'une partie ou de la totalité des groupes en un seul accès. 

**3. effacer les données du périphérique client**

Lorsqu'un utilisateur quitte ou est supprimé d'un groupe d'organisations, Kaizala efface automatiquement tous les messages, les actions Kaizala et les pièces jointes du périphérique client. Il s'agit d'une fonctionnalité unique dans Kaizala qui permet aux organisations de contrôler les utilisateurs contre le vol des données de l'organisation et est particulièrement utile dans les scénarios d'arrêt des partenaires ou d'employés hostiles. Kaizala fournit également des API REST ouvertes et sécurisées pour gérer par programme ces scénarios dans les flux d'entreprise étendus à partir de systèmes externes. Nous continuerons à créer des fonctionnalités de sécurité et de conformité supplémentaires dans le produit en fonction des commentaires de nos clients.
