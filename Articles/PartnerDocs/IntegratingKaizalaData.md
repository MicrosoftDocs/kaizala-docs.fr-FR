## <a name="integrating-kaizala-data-to-your-existing-dashboards"></a>Intégration de données Kaizala à vos tableaux de bord existant

Créer un rapport personnalisé ou connectez vos données Kaizala vos tableaux de bord existant à l’aide de Kaizala APIs. 
<br>En tant qu’une organisation tierce partie - vous souhaitez connecter des données Kaizala à votre tableau de bord existant, puis vous pouvez le faire à l’aide des manières suivantes :
<br>1. obtenir des données de Kaizala par le biais de Power BI-Content Pack et créer un rapport personnalisé sur PowerBI
<br>2 accéder aux données de Kaizala par le biais de connecteurs et passe au tableau de bord existant dans le format qu’il comprend. Vous pouvez accéder à l’aide de Kaizala Connecters de données :  
<br>a[API](https://docs.microsoft.com/en-us/kaizala/connectors/api) - Kaizala connecteurs permettent 3ème partie aux développeurs Kaizala intégrer leurs processus d’entreprise en fournissant des appels d’API en fonction de la capacité à exécuter un ensemble d’actions curated dans Kaizala à l’aide de REST. L’étendue de l’API est pour les systèmes externes pour le point de terminaison d’appel et effectuer des actions sur la demande. Autrement dit, il s’agit d’un modèle de collecte – où les points de terminaison individuels doivent être appelée pour effectuer des actions spécifiques à l’aide de l’API Kaizala. 
<br>b.[webhooks](https://docs.microsoft.com/en-us/kaizala/connectors/webhooks) - PUSH du modèle où plateforme Kaizala peut déclencher des actions peuvent être configurés à l’aide de webhooks.  
<br> Connecteurs Kaizala activer 3e développeurs tiers d’intégrer Kaizala leurs processus d’entreprise en fournissant des appels d’API en fonction de la capacité à exécuter un ensemble d’actions curated dans Kaizala à l’aide de REST. L’étendue de l’API est pour les systèmes externes pour le point de terminaison d’appel et effectuer des actions sur la demande. Autrement dit, il s’agit d’un modèle de collecte – où les points de terminaison individuels doivent être appelée pour effectuer des actions spécifiques à l’aide Kaizala [API](https://docs.microsoft.com/en-us/kaizala/connectors/api). Le modèle PUSH où plateforme Kaizala peut déclencher des actions permettre être configuré à l’aide de [webhooks](https://docs.microsoft.com/en-us/kaizala/connectors/webhooks). 
![](Images/GetImage.png)
### <a name="integration-using-webhooks"></a>Intégration à l’aide de Webhooks : 
<br>Il s’agit d’un mécanisme de diffusion en fonction. Une fois que Webhook est enregistré sur une action particulière, chaque fois que l’utilisateur envoie les données sur cette action sur Application Kaizala - Kaizala Server envoie une notification d’événement (message HTTP POST) avec la charge utile de réponse (au Format JSON) au point de terminaison URL configuré. Une fois les données sont informées sur le point de terminaison clients, logique pour l’analyse de la charge utile de réponse doit déclencher et insérer des données dans les tableaux respectifs dans le stockage (base de données ou sharepoint...) et visualisations peuvent être construites par l’interrogation de données à partir du stockage. Tirer parti est que toute organisation peuvent y accéder Kaizala données les tableaux de bord personnalisés sans interrompre leur flux de travail existant. 
### <a name="lets-drill-down-in-to-the-above-process-and-see-it-in-detail"></a>Permet d’atteindre la procédure ci-dessus et le voir en détail : 
#### <a name="how-to-register-a-webhook-on-endpoint"></a>Explique comment inscrire un webhook sur le point de terminaison ? 
<br> Une fois que vous configurez un point de terminaison URL sur laquelle vous souhaitez notifier les événements Kaizala, vous pouvez vous abonner à une notification sur le groupe ou d’une action particulière. Vous pouvez utiliser les clients 3ème partie API Rest comme Postman / Client reste avancé, etc. pour vous inscrire pour un webhook. Signature de l’inscription d’un webhook sur une Action particulière est donné ci-dessous :![](Images/GetImage_2.png)
<br>Accédez à [Kaizala API Documentation !](https://docs.microsoft.com/en-us/kaizala/connectors/api) sur la![](Images/GetImage%20_1.png)
<br>Effectuez la procédure pour obtenir le AccessToken et inscrire un wekbhook. 
 
<br>Comme vous avez maintenant inscrit un webhook, Kaizala server conserver sera avertissant les événements sur l’URL enregistré chaque fois qu’événement se produit. Réponse à un événement qui se trouve dans le ci-dessous au format JSON : 
 
<br> Exemple de réponse événement au format JSON :
<br> {   
<br> « objectId":"com.microsoft.kaizala.OrderFormDemo »,
<br> « objectType » : « ActionPackage »,
<br> « eventType » : « ActionResponse »,
<br> « eventId » : « 75609730-f5d2-4f07-XXXX-ccca96dd9e76 »,
<br>« données » : {   
<br> « actionId » : « eb40446b-3dc7-4e8e-XXXX-44ccc5ae760c »,
<br> « actionPackageId":"com.microsoft.kaizala.OrderFormDemo »,
<br> « packageId":"com.microsoft.kaizala.OrderFormDemo »,
<br> « groupId » : « af461a3c-49cf-47cf-XXXX-83b5d348318d »,
<br> « responseId » : « 75609730-f5d2-4f07-XXXX-ccca96dd9e76 »,
<br> « isUpdateResponse » : false
<br> « répondeur » : « +911234567890 »,
<br> « responderName » : « FooName »,
<br> « responderProfilePic » : « «,
<br> é « anonyme » : false
<br> « responseDetails » : {   
<br> « responseWithQuestions » : [   
<br> {   
<br>« title » : « Prise détaillant »,
<br>« type » : « SingleOption »,
<br> « options » : [   
<br>{   
<br> « title » : « ABC Traders »
<br>},
<br> {   
<br>« title » : « Distributeurs BCD »
<br>},
<br>{   
<br>« title » : « Gros EFG »
<br>}
<br>],
<br> « réponse » : [   
<br>« ABC Traders »
<br>]
<br> },
<br> {   
<br> « title » : « Riz 1KG »
<br> « type » : « Numérique »
<br>« options » : [   
<br> ],
<br> « répondre à » :1.0
<br>},
<br> {   
<br>« title » : « 5KG de riz »
<br> « type » : « Numérique »
<br>« options » : [   
<br>],
<br> « répondre à » :2.0
<br> },
<br> {   
<br> « title » : « Mixte jus 250ml »,
<br> « type » : « Numérique »
<br> « options » : [   
<br> ],
<br> « répondre à » :4.0
<br> },
<br> {   
<br> « title » : « Emplacement »,
<br> « type » : « Emplacement »,
<br>« options » : [   
 
<br> ],
<br> « réponse » : {   
<br> :99.1234567 « lt »,
<br>:88.1234567 « lg »,
<br> « n » : « FooAddress »
<br>}
<br>}
<br> ]
<br> }
<br> },
<br> « context » : « toutes les données qui doit être renvoyé dans le rappel.Données webhook en cours peuvent être affichées par l’actualisation :[: https://requestb.in/12786un1?inspect!](https://requestb.in/12786un1?inspect)
<br> « fromUser » : « +911234567890 »,
<br> « fromUserName » : « FooName »,
<br>« fromUserProfilePic » : « »
<br> }
<br> **Sur l’inscrit Point de terminaison** - comportant une logique métier pour analyser la réponse à un événement et insérer des données dans les tables de stockage respectif. Comme données sont désormais disponibles à votre fin, interroger les données du stockage et afficher des visualisations sur vos tableaux de bord existant. Avec cette approche - vous pouvez créer les visualisations de données Kaizala dans les tableaux de bord existant. Dans cette approche vous obtiendra les données averties en temps réel à l’aide du point de fin Webhook.  
#### <a name="how-to-pull-data-using-kaizala-apis"></a>Comment extraire des données à l’aide de l’API Kaizala ? 
Si vous souhaitez extraire des données à partir de Kaizala dans des intervalles réguliers et mettre à jour les données dans le tableau de bord - vous pouvez appeler Kaizala API d’à l’aide de connecteurs et extrait les données pour le Package Action requise, mettre à jour des données pour le stockage et actualiser le tableau de bord. 
<br><br>
**Pour interroger les réponses d’un Package Action**- vous pouvez voir la signature des API et la réponse en accédant à la collection Postman mentionnée ci-dessus et accédez à l’API de requête de contenu--> réponses d’action extraction d’un groupe et la remplacer par votre groupe, action Détails du package <br>
![](Images/GetImage_3.png)
