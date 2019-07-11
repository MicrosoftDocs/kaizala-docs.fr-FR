# <a name="office-365-compliance-framework-and-microsoft-kaizala"></a>Infrastructure de conformité Office 365 et Microsoft Kaizala

Actuellement, Microsoft Kaizala est certifié pour le niveau de conformité C par l’équipe interne de conformité de Microsoft Office 365, qui est responsable de la gestion de [cette infrastructure](https://download.microsoft.com/download/B/2/7/B27B3EF3-8849-4C18-8BA4-5AD755728620/Compliance%20Framework_customer%20guidance.pdf). Cela signifie que Microsoft Kaizala a des engagements de confidentialité et de sécurité de premier plan et qu’il est vérifié avec les normes et les termes internationaux et régionaux, notamment:

- ISO 27001
- ISO 27018
- Clauses de modèle UE (CMUE)
- FERPA
- Accord de partenariat professionnel HIPAA
- SSAE 16 rapports SOC 1 & SOC 2

## <a name="employee-training"></a>Formation des employés

S’il y a une intervention humaine minime pour maintenir le service en cours d’exécution, tous les ingénieurs qui travaillent sur le produit doivent être soumis à la formation sur la sécurité et la confidentialité. Microsoft s’assure également que tous les employés certifient l’acceptation des responsabilités pour les besoins en matière de confidentialité. 

## <a name="kaizala-compliance-features-for-customers"></a>Fonctionnalités de conformité Kaizala pour les clients

Microsoft Kaizala offre une prise en charge des [données régionales](dataresidency.md) dans les centres de données en Europe (UE), Asie-Pacifique (APAC), aux États-Unis (é.u.) et en Inde (en). Cela signifie que les clients Kaizala auront des données liées aux [groupes et conversations](https://support.office.com/article/organization-chats-and-groups-in-kaizala-c8a7855c-d232-4914-811c-f6708734dcc3) de l’organisation, telles que les messages, les pièces jointes et les actions Kaizala stockées dans le centre de données de leur région de facturation.

Voici les principales fonctionnalités liées à la conformité actuellement disponibles dans le produit. 

**1. affichage et gestion de tous les utilisateurs Kaizala disposant d’un accès aux données**

Kaizala gère un annuaire d' [ouverture](https://docs.microsoft.com/office365/kaizala/set-up-directory) spécifique de l’organisation (OD), qui est comme un annuaire téléphonique pour tous ses utilisateurs Kaizala, pour ses administrateurs pour la gestion centrale. Tout utilisateur qui devient membre d’un groupe d’organisation dans Kaizala devient automatiquement membre de OD. Cela signifie qu’il s’agit d’une liste de tous les utilisateurs Kaizala qui ont un accès potentiel aux données des organisations (c’est-à-dire, tous les membres de ses groupes d’organisation). Les administrateurs peuvent associer des attributs personnalisés supplémentaires spécifiques à leur organisation, tels que les Aadhar non, l’emplacement et la désignation, pour faciliter l’identification. Il est également possible de supprimer un utilisateur de OD, qui révoque automatiquement les appartenances aux groupes de l’utilisateur.

**2. supprimer un utilisateur de tous les groupes d’organisation** 

Le portail de gestion Kaizala offre des fonctionnalités avancées de gestion des utilisateurs et des groupes, ce qui permet aux administrateurs d’intégrer et de quitter plus facilement les employés et les partenaires. En recherchant le numéro de téléphone d’un utilisateur, le portail répertorie tous les groupes dont l’utilisateur est membre. Un administrateur peut choisir de supprimer un utilisateur d’une partie ou de la totalité des groupes en même temps. 

**3. effacer les données du périphérique client**

Lorsqu’un utilisateur quitte ou est supprimé d’un groupe d’organisations, Kaizala efface automatiquement tous les messages, les actions Kaizala et les pièces jointes du périphérique client. Il s’agit d’une fonctionnalité unique dans Kaizala, qui permet aux organisations de contrôler les utilisateurs contre le vol des données de l’organisation et est particulièrement utile dans les scénarios d’arrêt des partenaires ou d’employés hostiles. Kaizala fournit également des API REST ouvertes et sécurisées pour gérer par programme ces scénarios dans les flux d’entreprise étendus à partir de systèmes externes. Nous continuerons à créer des fonctionnalités de sécurité et de conformité supplémentaires dans le produit en fonction des commentaires de nos clients.
