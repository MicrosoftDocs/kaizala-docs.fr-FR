## <a name="integrating-kaizala-data-to-your-existing-dashboards"></a>Intégration de données Kaizala à vos tableaux de bord existants

Créer un rapport personnalisé ou connecter vos données Kaizala à vos tableaux de bord existants à l'aide des API Kaizala. 
<br>En tant qu'organisation tierce, vous souhaitez connecter des données Kaizala à votre tableau de bord existant, puis vous pouvez le faire en procédant comme suit:
<br>1. obtenir des données Kaizala via Power BI-Content Pack et créer un rapport personnalisé sur PowerBI
<br>2. accéder aux données Kaizala via des connecteurs et passer à un tableau de bord existant au format qu'il comprend. Vous pouvez accéder aux données à l'aide de connexions Kaizala:  
<br>les connecteurs.[APIs](https://docs.microsoft.com/en-us/kaizala/connectors/api) -Kaizala permettent aux développeurs tiers d'intégrer Kaizala à leurs processus métier en offrant la possibilité d'effectuer un ensemble d'actions organisée dans Kaizala à l'aide d'appels d'API basés sur REST. L'étendue de l'API est destinée aux systèmes externes pour appeler le point de terminaison et effectuer des actions à la demande. Autrement dit, il s'agit d'un modèle d'extraction, où les points de terminaison individuels doivent être appelés pour effectuer des actions spécifiques à l'aide de l'API Kaizala. 
<br>b.[](https://docs.microsoft.com/en-us/kaizala/connectors/webhooks) webhooks: le modèle poussé dans lequel la plateforme Kaizala peut déclencher des actions peut être configuré à l'aide des webhooks.  
<br> Les connecteurs Kaizala permettent aux développeurs tiers d'intégrer Kaizala à leurs processus métier en leur permettant d'effectuer un ensemble d'actions organisée dans Kaizala à l'aide d'appels d'API basés sur REST. L'étendue de l'API est destinée aux systèmes externes pour appeler le point de terminaison et effectuer des actions à la demande. Autrement dit, il s'agit d'un modèle d'extraction, où les points de terminaison individuels doivent être appelés pour effectuer des actions spécifiques à l'aide des [API](https://docs.microsoft.com/en-us/kaizala/connectors/api)Kaizala. Le modèle poussé dans lequel la plateforme Kaizala peut déclencher des actions peut [](https://docs.microsoft.com/en-us/kaizala/connectors/webhooks)être configuré à l'aide des webhooks. 
![](Images/GetImage.png)
### <a name="integration-using-webhooks"></a>Intégration à l'aide des webhooks: 
<br>Il s'agit d'un mécanisme de type poussé. Une fois que le webhook est inscrit sur une action particulière, chaque fois que l'utilisateur envoie des données sur cette action sur le serveur Kaizala de l'application Kaizala envoie une notification d'événement (message HTTP POST) avec un temps de réponse (format JSON) au point de terminaison de l'URL configuré. Une fois que les données sont notifiées sur le point de terminaison des clients, la logique d'analyse de la charge utile de réponse doit déclencher et insérer des données dans les tables respectives du stockage (base de données ou SharePoint,..) et les visualisations peuvent être créées en interrogeant les données à partir du stockage. L'avantage est que toute organisation peut obtenir des données Kaizala dans leurs tableaux de bord personnalisés sans interrompre les flux de travail existants. 
### <a name="lets-drill-down-in-to-the-above-process-and-see-it-in-detail"></a>Permet d'accéder au processus ci-dessus et de le voir en détail: 
#### <a name="how-to-register-a-webhook-on-endpoint"></a>Comment enregistrer un webhook sur un point de terminaison? 
<br> Une fois que vous avez configuré un point de terminaison d'URL sur lequel vous souhaitez avertir les événements Kaizala, vous pouvez vous abonner pour une notification sur le groupe ou une action particulière. Vous pouvez utiliser les clients de l'API REST tiers, tels que le client REST ou le client Rest avancé, etc., pour s'abonner à un webhook. La signature de l'inscription d'un webhook sur une action particulière est indiquée ci-dessous:![](Images/GetImage_2.png)
<br>Accédez à [la documentation de l'API Kaizala!](https://docs.microsoft.com/en-us/kaizala/connectors/api) et cliquez sur le![](Images/GetImage%20_1.png)
<br>Suivez les étapes pour obtenir le AccessToken et enregistrer un wekbhook. 
 
<br>Étant donné que vous avez enregistré un webhook, le serveur Kaizala continuera à avertir les événements sur l'URL inscrite chaque fois que l'événement se produit. La réponse d'événement se trouve au format JSON ci-dessous: 
 
<br> Exemple de réponse d'événement dans JSON:
<br> {   
<br> "objectId": "com. Microsoft. kaizala. OrderFormDemo",
<br> "objectType": "ActionPackage",
<br> "eventType": "ActionResponse",
<br> "eventId": "75609730-f5d2-4f07-XXXX-ccca96dd9e76",
<br>«données»: {   
<br> "actionId": "eb40446b-3dc7-4e8e-XXXX-44ccc5ae760c",
<br> «actionPackageId»: «com. Microsoft. kaizala. OrderFormDemo»,
<br> «packageId»: «com. Microsoft. kaizala. OrderFormDemo»,
<br> "groupId": "af461a3c-49cf-47cf-XXXX-83b5d348318d",
<br> "responseId": "75609730-f5d2-4f07-XXXX-ccca96dd9e76",
<br> «isUpdateResponse»: false,
<br> «répondeur»: «+ 911234567890»,
<br> «responderName»: «FooName»,
<br> «responderProfilePic»: «»,
<br> «isAnonymous»: false,
<br> «responseDetails»: {   
<br> «responseWithQuestions»: [   
<br> {   
<br>«titre»: «sortie détaillant»,
<br>«type»: «SingleOption»,
<br> «Options»: [   
<br>{   
<br> «titre»: «ABC Traders»
<br>},
<br> {   
<br>«titre»: «distributeurs BCD»
<br>},
<br>{   
<br>«title»: «EFG grossiste»
<br>}
<br>],
<br> «réponse»: [   
<br>«ABC Traders»
<br>]
<br> },
<br> {   
<br> "title": "riz 1KG",
<br> "type": "Numeric",
<br>«Options»: [   
<br> ],
<br> «réponse»: 1.0
<br>},
<br> {   
<br>"title": "riz 5KG",
<br> "type": "Numeric",
<br>«Options»: [   
<br>],
<br> «réponse»: 2.0
<br> },
<br> {   
<br> "titre": "mélange de jus de fruits 250ml",
<br> "type": "Numeric",
<br> «Options»: [   
<br> ],
<br> «réponse»: 4.0
<br> },
<br> {   
<br> "title": "location",
<br> "type": "location",
<br>«Options»: [   
 
<br> ],
<br> «réponse»: {   
<br> "lt": 99.1234567,
<br>«LG»: 88.1234567,
<br> «n»: «FooAddress»
<br>}
<br>}
<br> ]
<br> }
<br> },
<br> «Context»: «toutes les données qui doivent être renvoyées dans le rappel.Les données de webhook actuelles peuvent être vues en actualisant:[: https://requestb.in/12786un1?inspect!](https://requestb.in/12786un1?inspect)
<br> "fromUser": "+ 911234567890",
<br> «fromUserName»: «FooName»,
<br>"fromUserProfilePic": ""
<br> }
<br> **Sur le point de terminaison enregistré** , la logique métier doit analyser la réponse de l'événement et insérer des données dans les tables de stockage respectives. À l'issue de la mise à disposition des données, interrogez les données à partir du stockage et affichez les visualisations sur vos tableaux de bord existants. Cette approche vous permet de créer des visualisations de données Kaizala sur des tableaux de bord existants. Dans cette approche, vous allez obtenir les données notifiées en temps réel à l'aide du point de terminaison de webhook.  
#### <a name="how-to-pull-data-using-kaizala-apis"></a>Comment extraire des données à l'aide de l'API Kaizala? 
Si vous souhaitez extraire des données de Kaizala à intervalles réguliers et mettre à jour des données dans le tableau de bord, vous pouvez alors appeler des API Kaizala à l'aide de connecteurs et extraire des données pour le package d'actions requis, mettre à jour les données dans le tableau de bord de stockage et d'actualisation. 
<br><br>
**Pour interroger les réponses d'un package d'action**: vous pouvez voir la signature de l'API et la réponse en accédant à la collection post-citée ci-dessus et accéder à l'API de requête de contenu--> FETCH action Response in a Group et remplacer par votre groupe, action Détails du package <br>
![](Images/GetImage_3.png)
