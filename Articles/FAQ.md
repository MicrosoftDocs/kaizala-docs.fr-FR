# <a name="frequently-asked-questions"></a>Forum aux Questions : 

## <a name="kaizala-rest-based-apis"></a>API REST Kaizala

**1. comment commencer à utiliser Kaizala APIs ?**</br></br>
Pour commencer à utiliser les API de REST de Kaizala, vous devez
 
-   Première [définir Kaizala connecteur et de générer un jeton actualiser](https://docs.microsoft.com/en-in/kaizala/connectors/setup).
-   Vous devez ensuite [Générer un jeton d’accès](https://docs.microsoft.com/en-in/kaizala/connectors/tokens)
-   puis [commencer à utiliser les API](https://docs.microsoft.com/en-in/kaizala/connectors/api)

<br/>

**2. comment générer par programme des jetons d’actualisation ?**</br></br>
  Il existe deux types d’actualiser le jeton.
  - Jeton de l’utilisateur
  - Émission de jeton de groupe
  
  **Jeton de l’utilisateur** peuvent être générées à l’aide de la page de détails de connecteurs (a) dans le portail de gestion Kaizala, (b) à l’aide API (GeneratePin et LoginWithPinAndApplicationId api (détails dans la collection postman shared [ici](https://app.getpostman.com/run-collection/f68a8abec784cc00b0b9#?env%5BKaizala-APIs-environment%5D=W3siZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlciIsInZhbHVlIjoiKzkxOTkxMDg3MDAwNSIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJhY2Nlc3MtdG9rZW4iLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LWdyb3VwLWlkIiwidmFsdWUiOiIiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlci0yIiwidmFsdWUiOiIrOTExMTk5OTk5OTk5IiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImFwaS1yb290IiwidmFsdWUiOiJodHRwczovL2FwaS5rYWl6YS5sYSIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJhcHBsaWNhdGlvbi1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImFwcGxpY2F0aW9uLXNlY3JldCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImVuZHBvaW50LXVybCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InJlZnJlc2gtdG9rZW4iLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LXB1YmxpYy1ncm91cC1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InRlc3Qtc3ViLWdyb3VwLWlkIiwidmFsdWUiOiIiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlci0zIiwidmFsdWUiOiIrOTExMDk5OTk5OTkiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoidGVzdC1hY3Rpb24taWQiLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LXN1cnZleS1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InRlc3Qtd2ViaG9vay1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifV0=) ) oAuth Kaizala (c). <br/>
  **Jeton de groupe** peuvent être générées à l’aide de la page de détails de connecteurs dans le portail de gestion Kaizala.

En savoir plus sur les [jetons](https://docs.microsoft.com/en-in/kaizala/connectors/tokens)
<br/><br/>

**3. comment vous assurer que l’expiration de la connexion entre Kaizala et mon système/application ne s’arrête pas refreshToken**</br></br>
 En règle générale actualiser le jeton expire au bout de 365 jours. Pour permettre à des systèmes tiers 3e maintenir la connexion même lorsque refreshToken va expirer, envoie Kaizala qu'appelle de nouveau actualiser jeton avec chaque jeton d’accès par rapport à 90 % de la validité de l’actualisation jeton a été atteint. Par conséquent, le système doit être en mesure de lire cette refreshToken et utilisez ce refreshToken pour accessTokens suivantes. [En savoir plus](https://docs.microsoft.com/en-in/kaizala/connectors/tokens)

**4. comment créer un groupe à l’aide des API ?**</br></br>
  Kaizala permet de créer des groupes et sous-groupes à l’aide des API. En savoir plus pour [créer un groupe](https://docs.microsoft.com/en-in/kaizala/connectors/groups). 
  >Remarque : Si vous utilisez le jeton utilisateur au niveau de l’actualisation, nouveau groupe sera créé. Mais si le jeton au niveau du groupe est utilisé pour créer un groupe, un groupe secondaire pour le groupe concerné est créé.
<br/><br/>

**5. Comment puis-je envoyer un message via des API dans Kaizala ?**</br></br>
  Kaizala propose une API à l’aide de laquelle vous pouvez envoyer un message à n’importe quel groupe. Obtenir plus de détails [ici](https://docs.microsoft.com/en-gb/kaizala/connectors/messages).
<br/><br/>


**6. existe-t-il exemple disponible en ligne pour différentes fonctionnalités Kaizala comme API, Webhooks ?**</br></br>
  Vous pouvez trouver l’exemple de code en c# [ici](https://github.com/MicrosoftDocs/kaizala-docs/blob/master/Articles/Samples/Getting%20started%20with%20Kaizala%20REST%20APIs%20-%20C%23%20sample%20(shared).docx)

**7. Comment puis-je obtenir les numéros de téléphone de tous les membres/abonnés dans un groupe ?**</br></br>
  Kaizala expose des API pour obtenir les détails de tous les membres d’un groupe. Obtenir plus de détails [ici](https://docs.microsoft.com/en-gb/kaizala/connectors/members) pour obtenir plus d’informations du membre du groupe, vous devez installer les connecteurs Kaizala. [En savoir plus](https://github.com/MicrosoftDocs/kaizala-docs/blob/master/Articles/connectors/README.md) 
<br/><br/>


**8. comment nous pouvons pour ajouter un membre à un groupe par le biais de Kaizala APIs ?**</br></br>
  Kaizala expose des API pour ajouter des membres dans un groupe. Obtenir plus de détails [ici](https://docs.microsoft.com/en-gb/kaizala/connectors/members).     Pour rendre un membre du groupe administrateur, consultez ci-dessous un exemple : 
````  
PUT {endpoint-url}/v1/groups/{groupId}/members/{memberId} 

Header: 
accessToken 

Body 
{"role":"Admin"} 
````

**9. est-il possible de créer un webhook qui peut informer sur la création d’un groupe ?**</br></br>
  Il n’est pas possible de créer un webhook pour obtenir des notifications sur la création de groupe, car tous les webhooks fonctionnent actuellement dans le contexte d’un groupe. Dans le contexte d’un groupe, vous pouvez créer webhooks pour obtenir des notifications sur les messages et les actions qui sont envoyé/reçu Ajout du membre et suppression, etc..  
<br/><br/>

**10. les connecteurs doivent-elles être ajoutés manuellement à chaque groupe ?**</br></br>
  Si le connecteur est créé à partir de l’administrateur du client, n’ont pas à ajouter le connecteur manuellement à chaque groupe. 
<br/><br/>


**11. Comment puis-je récupérer des réponses complètes de tous les participants dans une enquête ?**</br></br>
Pour obtenir toutes les réponses pour une enquête particulière dans un groupe, utilisez l’API suivant :
````
{{endpoint-url}}/v1/groups/{{group-id}}/actions/{{survey-id}}?getDetails=true 
 
Headers: 
accessToken : {{access-token}} 
```` 
<br/><br/>

**12. puis-je envoyer un message dans une conversation 1-1 dans Kaizala via des API ?**</br></br>  Toutes les API dans Kaizala fonctionnent dans le contexte d’un groupe. Ainsi, il n’est pas possible d’envoyer un message dans une conversation 1-1 à l’aide d’une API. Les fonctionnalités suivantes sont prises en charge :
-   Envoi du message à un abonné particulier dans un groupe public 
-   Création d’un groupe à l’utilisateur et l’envoi de message au groupe

<br/>
    
**13. est-il possible d’envoyer un message uniquement à un membre particulier dans un groupe ?**</br></br>
  Uniquement dans le cas d’un groupe public, il est possible d’envoyer un message à un abonné particulier. Dans un groupe normal, ce n’est pas possible. Veuillez consulter le lien suivant pour plus d’informations sur l’API associée : https://docs.microsoft.com/en-gb/kaizala/connectors/messages. <br/>
<br/><br/>

**14. est-il possible d’envoyer un message uniquement à un membre particulier dans un groupe ?**</br></br>
  Toutes les API dans Kaizala fonctionnent dans le contexte d’un groupe. Ainsi, il n’est pas possible d’envoyer une action dans une conversation 1-1 à l’aide d’une API.  
<br/><br/>

## <a name="kaizala-actions"></a>Actions Kaizala

**1. Comment puis-je commencer avec le développement d’Action personnalisée ? Y a-t-il une documentation disponible ?**</br></br>
  Développement d’Action personnalisée et la documentation associée est sous Aperçu avant impression et est couvert par un accord de confidentialité. Vous pouvez démarrer en lisant [ce](Actions/README.md). </br>
  Si vous avez des questions, vous pouvez [nous contacter](feedback.md).
<br/><br/>

**2. Comment puis-je obtenir le Kit de développement logiciel le plus récent Kaizala Action ?**</br></br>

  Vous pouvez trouver la dernière version du SDK de Action [ici]()
<br/><br/> 

 **3. Comment puis-je I test/debug une Action personnalisée sans avoir à télécharger un package de chaque fois ?**</br></br>

  Pour tester une Action personnalisée, en savoir plus sur le processus [d’étapes/ici](Actions/test.md) 
<br/><br/>


 **4. Quelles sont les directives Package Action suivre ?**</br></br>
En tant que développeur, vous devez respecter les instructions lors du développement personnalisé Package.Please Action retrouver [ici](Actions/validation.md). Kaizala Microsoft peut supprimer votre Action à partir de l’application, s’il en trouve toutes les incohérences.
<br/><br/>

**5. où puis-je accéder aux rapports correspondant à mes Actions personnalisées sur le portail de gestion Kaizala ?**</br></br>
 Portail de gestion Kaizala permet aux utilisateurs de créer des actions personnalisées, formulaires, des cartes de commentaires, etc.. Ces actions pouvant être mappées à vos groupes et envoyées à plusieurs reprises pour effectuer le suivi des mesures critiques. Sur le portail, ces données sont indiquées sous « Périodique des rapports enquête ». Fonctionnalité supplémentaire, le rapport regroupe les réponses à ces cartes au fil du temps et instances. 
<br/><br/>

**6. Comment puis-je charger le contenu externe dans ma page action ?**</br></br>
Vous pouvez charger le contenu externe dans l’action en création de listes autorisées l’URL qui contient les données. Vous trouverez des étapes de création de listes autorisées URL [ici](Actions/UrlWhitelisting.md).
<br/><br/>

## <a name="integration-with-microsoft-apps"></a>Intégration aux applications Microsoft

**1. Comment pouvons-nous créer un connecteur Kaizala dans PowerApps ?**</br></br>
  Microsoft Kaizala a été publié en tant que connecteur Microsoft Flow & PowerApps. En savoir plus [ici](https://support.office.com/en-us/article/Integrate-your-workflow-in-Kaizala-using-Microsoft-Flow-883343d0-6b16-4725-a23d-bc69fb264356)
<br/><br/>

**2. Comment puis-je ajouter et utiliser le complément Excel pour Kaizala ?**</br></br>

  Le complément Excel pour Kaizala permet de toutes les tables dans Excel pour être exposés en tant qu’une enquête sur Kaizala. Toutes les réponses à l’enquête seront automatiquement renseignés dans le tableau Excel. En savoir plus [ici](https://support.office.com/en-us/article/Kaizala-Office-Add-in-4cd01439-5da2-4a9f-b493-8f2e23e2fd91?ui=en-US&rs=en-US&ad=US) 

<br/><br/> 



