# <a name="frequently-asked-questions"></a>Forum aux questions: 

## <a name="kaizala-rest-based-apis"></a>API REST basées sur Kaizala

**1. Comment puis-je commencer à utiliser les API Kaizala?**</br></br>
Pour commencer à utiliser l'API basée sur REST de Kaizala, vous devez
 
-   ConFigurez d'abord le [connecteur Kaizala et générez un jeton d'actualisation](https://docs.microsoft.com/en-in/kaizala/connectors/setup).
-   Vous devez ensuite [générer un jeton d'accès](https://docs.microsoft.com/en-in/kaizala/connectors/tokens) .
-   puis [commencez à utiliser les API](https://docs.microsoft.com/en-in/kaizala/connectors/api)

<br/>

**2. Comment générer des jetons d'actualisation par programmation?**</br></br>
  Il existe deux types de jeton d'actualisation.
  - Jeton de l'utilisateur
  - Jeton de groupe
  
  Le **jeton utilisateur** peut être généré à l'aide de la page de détails des connecteurs (a) dans le portail de gestion Kaizala, (b) à l'aide de l'API (GeneratePin et API LoginWithPinAndApplicationId (détails dans la collection Postic Shared [ici](https://app.getpostman.com/run-collection/f68a8abec784cc00b0b9#?env%5BKaizala-APIs-environment%5D=W3siZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlciIsInZhbHVlIjoiKzkxOTkxMDg3MDAwNSIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJhY2Nlc3MtdG9rZW4iLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LWdyb3VwLWlkIiwidmFsdWUiOiIiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlci0yIiwidmFsdWUiOiIrOTExMTk5OTk5OTk5IiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImFwaS1yb290IiwidmFsdWUiOiJodHRwczovL2FwaS5rYWl6YS5sYSIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJhcHBsaWNhdGlvbi1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImFwcGxpY2F0aW9uLXNlY3JldCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6ImVuZHBvaW50LXVybCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InJlZnJlc2gtdG9rZW4iLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LXB1YmxpYy1ncm91cC1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InRlc3Qtc3ViLWdyb3VwLWlkIiwidmFsdWUiOiIiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoibW9iaWxlLW51bWJlci0zIiwidmFsdWUiOiIrOTExMDk5OTk5OTkiLCJ0eXBlIjoidGV4dCJ9LHsiZW5hYmxlZCI6dHJ1ZSwia2V5IjoidGVzdC1hY3Rpb24taWQiLCJ2YWx1ZSI6IiIsInR5cGUiOiJ0ZXh0In0seyJlbmFibGVkIjp0cnVlLCJrZXkiOiJ0ZXN0LXN1cnZleS1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifSx7ImVuYWJsZWQiOnRydWUsImtleSI6InRlc3Qtd2ViaG9vay1pZCIsInZhbHVlIjoiIiwidHlwZSI6InRleHQifV0=) ) (c) Kaizala OAuth. <br/>
  Le **jeton de groupe** peut être généré à l'aide de la page de détails des connecteurs dans le portail de gestion Kaizala.

En savoir plus sur les [jetons](https://docs.microsoft.com/en-in/kaizala/connectors/tokens)
<br/><br/>

**3. Comment s'assurer que l'expiration de refreshToken n'arrête pas la connexion entre Kaizala et mon système/application**</br></br>
 Généralement, le jeton d'actualisation expire après 365 jours. Afin de permettre aux systèmes tiers de maintenir la connexion même si refreshToken est sur le niveau de l'expiration, Kaizala envoie un nouveau jeton d'actualisation avec chaque appel de jeton d'accès depuis 90% de la validité du jeton d'actualisation est atteint. Ainsi, le système doit être en mesure de lire ce refreshToken et d'utiliser cet refreshToken pour les futures accessTokens. [En savoir plus](https://docs.microsoft.com/en-in/kaizala/connectors/tokens)

**4. Comment puis-je créer un groupe à l'aide de l'API?**</br></br>
  Kaizala permet la création de groupes & sous-groupes à l'aide d'API. Pour en savoir plus, [créez un groupe](https://docs.microsoft.com/en-in/kaizala/connectors/groups). 
  >Remarque: Si vous utilisez un jeton d'actualisation au niveau de l'utilisateur, le nouveau groupe sera créé. Toutefois, si le jeton de niveau de groupe est utilisé pour créer un groupe, un sous-groupe du groupe concerné est créé.
<br/><br/>

**5. Comment puis-je envoyer un message via des API dans Kaizala?**</br></br>
  Kaizala expose une API qui vous permet d'envoyer un message à n'importe quel groupe. Pour plus d' [](https://docs.microsoft.com/en-gb/kaizala/connectors/messages)informations, accédez à.
<br/><br/>


**6. existe-t-il des exemples disponibles en ligne pour différentes fonctionnalités Kaizala, telles que les API, les webhooks?**</br></br>
  Vous trouverez l'exemple de code en C# [ici](https://github.com/MicrosoftDocs/kaizala-docs/blob/master/Articles/Samples/Getting%20started%20with%20Kaizala%20REST%20APIs%20-%20C%23%20sample%20(shared).docx)

**7. Comment puis-je obtenir les numéros de téléphone de tous les membres/abonnés d'un groupe?**</br></br>
  Kaizala expose des API pour obtenir les détails de tous les membres d'un groupe. Pour obtenir plus d'informations [ici](https://docs.microsoft.com/en-gb/kaizala/connectors/members) , pour obtenir des détails sur les membres du groupe, vous devez configurer les connecteurs Kaizala. [En savoir plus](https://github.com/MicrosoftDocs/kaizala-docs/blob/master/Articles/connectors/README.md) 
<br/><br/>


**8. Comment pouvons-nous ajouter un membre à un groupe via les API Kaizala?**</br></br>
  Kaizala expose des API pour ajouter des membres dans un groupe. Pour plus d' [](https://docs.microsoft.com/en-gb/kaizala/connectors/members)informations, accédez à.     Pour faire d'un membre du groupe un administrateur, voir l'exemple ci-dessous: 
````  
PUT {endpoint-url}/v1/groups/{groupId}/members/{memberId} 

Header: 
accessToken 

Body 
{"role":"Admin"} 
````

**9. est-il possible de créer un webhook qui peut vous avertir lors de la création d'un groupe?**</br></br>
  Il n'est pas possible de créer un webhook pour obtenir des notifications sur les créations de groupe car tous les webhooks fonctionnent actuellement dans le contexte d'un groupe. Dans le cadre d'un groupe, vous pouvez créer des webhooks pour obtenir des notifications sur les messages/actions envoyés/reçus, l'ajout et la suppression de membres, etc.  
<br/><br/>

**10. les connecteurs doivent-ils être ajoutés manuellement à chaque groupe?**</br></br>
  Si le connecteur est créé à partir de l'administrateur client, il n'est pas nécessaire d'ajouter manuellement le connecteur à chaque groupe. 
<br/><br/>


**11. Comment puis-je extraire les réponses complètes de tous les participants à une enquête?**</br></br>
Utilisez l'API suivante pour obtenir toutes les réponses pour une enquête particulière dans un groupe:
````
{{endpoint-url}}/v1/groups/{{group-id}}/actions/{{survey-id}}?getDetails=true 
 
Headers: 
accessToken : {{access-token}} 
```` 
<br/><br/>

**12. puis-je envoyer un message dans une conversation 1-1 dans Kaizala via des API?**</br></br>  Toutes les API dans Kaizala fonctionnent dans le contexte d'un groupe. Par conséquent, il n'est pas possible d'envoyer un message dans une conversation de 1-1 à l'aide d'une API. Les fonctionnalités suivantes sont prises en charge:
-   Envoi d'un message à un abonné particulier dans un groupe public 
-   Création d'un groupe avec l'utilisateur et envoi d'un message au groupe

<br/>
    
**13. est-il possible d'envoyer un message uniquement à un membre particulier d'un groupe?**</br></br>
  Dans le cas d'un groupe public, il est possible d'envoyer un message à un abonné particulier. Dans un groupe normal, cela n'est pas possible. Pour plus d'informations sur l'API associée, consultez le lien suivant: https://docs.microsoft.com/en-gb/kaizala/connectors/messages. <br/>
<br/><br/>

**14. est-il possible d'envoyer un message uniquement à un membre particulier d'un groupe?**</br></br>
  Toutes les API dans Kaizala fonctionnent dans le contexte d'un groupe. Par conséquent, il n'est pas possible d'envoyer une action dans une conversation 1-1 à l'aide d'une API.  
<br/><br/>

## <a name="kaizala-actions"></a>Actions Kaizala

**1. Comment puis-je commencer à utiliser le développement d'actions personnalisées? Existe-t-il des documents disponibles?**</br></br>
  Le développement d'actions personnalisées et la documentation associée sont en mode Aperçu et sont couverts par l'accord de confidentialité. Vous pouvez commencer par [le](Actions/README.md)lire. </br>
  Si vous avez des requêtes, vous pouvez [nous contacter](feedback.md).
<br/><br/>

**2. Comment puis-je obtenir le dernier Kit de développement d'actions Kaizala?**</br></br>

  Vous trouverez le dernier SDK action [ici]()
<br/><br/> 

 **3. Comment puis-je tester/déboguer une action personnalisée sans avoir à télécharger un package à chaque fois?**</br></br>

  Pour tester une action personnalisée, en savoir plus sur les étapes/processus [ici](Actions/test.md) 
<br/><br/>


 **4. Quelles sont les instructions que le package d'action doit suivre?**</br></br>
En tant que développeur, vous devez respecter les instructions lors du développement d'un package d'actions personnalisées. veuillez les trouver [ici](Actions/validation.md). Microsoft Kaizala peut supprimer votre action de l'application, si elle trouve des incohérences.
<br/><br/>

**5. où puis-je accéder aux rapports correspondant à mes actions personnalisées sur le portail de gestion Kaizala?**</br></br>
 Le portail de gestion Kaizala permet aux utilisateurs de créer des actions personnalisées, des formulaires, des fiches de rétroaction, etc. Ces actions peuvent ensuite être mappées à vos groupes et envoyées à plusieurs reprises pour suivre les mesures stratégiques critiques. Sur le portail, ces données sont reportées sous «rapports récurrents de l'enquête». En tant que fonctionnalité supplémentaire, le rapport agrège les réponses à ces cartes dans le temps et entre les instances. 
<br/><br/>

**6. Comment puis-je charger du contenu externe dans ma page d'action?**</br></br>
Vous pouvez charger du contenu externe dans votre action en faisant une liste d'adresses, qui contient les données. Vous trouverez [ci-dessous](Actions/UrlWhitelisting.md)les étapes à suivre pour la liste d'adresses autorisées.
<br/><br/>

## <a name="integration-with-microsoft-apps"></a>Intégration aux applications Microsoft

**1. Comment pouvons-nous créer un connecteur Kaizala dans les PowerApp?**</br></br>
  Microsoft Kaizala a été publié en tant que connecteur sur les PowerApp de Microsoft Flow &. En savoir plus [ici](https://support.office.com/en-us/article/Integrate-your-workflow-in-Kaizala-using-Microsoft-Flow-883343d0-6b16-4725-a23d-bc69fb264356)
<br/><br/>

**2. Comment puis-je ajouter et utiliser le complément Excel pour Kaizala?**</br></br>

  Le complément Excel pour Kaizala permet d'exposer n'importe quelle table dans Excel sous la forme d'une enquête sur Kaizala. Toutes les réponses à l'enquête seront automatiquement renseignées dans le tableau Excel. En savoir plus [ici](https://support.office.com/en-us/article/Kaizala-Office-Add-in-4cd01439-5da2-4a9f-b493-8f2e23e2fd91?ui=en-US&rs=en-US&ad=US) 

<br/><br/> 



