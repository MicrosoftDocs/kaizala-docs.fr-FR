# <a name="webhook-response-schema-for-registered-events"></a>Schéma de réponse webhook pour les événements inscrits

Si un webhook est inscrit, Kaizala renvoie une réponse webHook pour chaque événement sur l'objectId enregistré, filtré pour les événements inscrits. Vous trouverez ci-dessous les détails du schéma de différentes réponses de webhook pour différents événements.

## <a name="response-body"></a>Corps de la réponse
| Paramètre | Type | Description |
| :---: | :---: | :--- |
| objectId | Chaîne | Identificateur représentant l'objet dans lequel le webhook a été créé. Pour ObjectType = Group, l'identificateur de son groupe, pour ObjectType = action, son actionId, pour ObjectType = ActionPackage, son action-Package-ID |
| objectType | Chaîne | Énumération: «Group»/«action»/«ActionPackage» |
| Évènement | Chaîne | Événement Registered qui a été appelé |
| eventId | Chaîne | Identificateur représentant l'événement |
| données | Objet JSON | Objet représentant des données spécifiques à cet événement. Paramètres définis ci-dessous pour chacun des événements pris en charge. |
| contexte | Chaîne | Renvoie la valeur qui a été définie lors de l'inscription d'un webhook sous le paramètre «callbackContext»|
| fromUser | Chaîne | Numéro de téléphone de l'expéditeur |
| fromUserId | Chaîne | UserId de l'expéditeur |
| fromUserName | Chaîne | Nom enregistré de l'expéditeur avec Kaizala |
| fromUserProfilePic | url | Profil de l'expéditeur pic |

Le paramètre «Data» varie en fonction de l'événement webHook. Vous pouvez trouver le schéma de chaque événement ci-dessous.

### <a name="data-for-event-textmessagecreated"></a>données de l'événement «TextMessageCreated»
| Paramètre | Type | Description |
| :---: | :---: | :--- |
| text | Chaîne | Message texte envoyé |

#### <a name="sample-webhook-response-for-textmessagecreated"></a>Exemple de réponse webHook pour «TextMessageCreated»
```javascript
{
  "objectId": "8c2050-9be8-45d6-97f5-bb7013930027",
  "objectType": "Group",
  "eventType": "TextMessageCreated",
  "eventId": "55ed01-02b5-491e-8e7e-484726da976b",
  "data": {
    "text": "Test Message"
  },
  "context": "Any data which is required to be returned in callback",
  "fromUser": "+91xxxxxxxx",
  "fromUserId": "72e91-f3-4e7b-84eb-4e228406fb9b",
  "fromUserName": "Robin Richard",
  "fromUserProfilePic": "https://mobileonlyapps.blob.core.windows.net/72e29591-4e7b-84eb-4e228406fb9b/c34afc0d53614ae29285d08e6409e416.jpg"
}
```

### <a name="data-for-event-attachmentcreated"></a>données de l'événement «AttachmentCreated»
| Paramètre | Type | Description |
| :---: | :---: | :--- |
| panne | Tableau | Chaque élément contient mediaUrl et mediaFileName|
| mediaUrl | url | URL de l'image |
| mediaFileName | Chaîne | Filename |
| actionType | String | Valeur enum: 'image' |
| caption | Chaîne | légende associée à l'image |

#### <a name="sample-webhook-response-for-attachmentcreated"></a>Exemple de réponse webHook pour «AttachmentCreated»
```javascript
{
  "objectId": "8c291050-9be8-45d6-97f5-bb7013930027",
  "objectType": "Group",
  "eventType": "AttachmentCreated",
  "eventId": "59e2e9f9-9b10-4b67-8bc5-3f85a04f2d91",
  "data": {
    "media": [
      {
        "mediaUrl": "https://cdn.inc-000.kms.osi.office.net/att/0ad142c52b30d797addebadb620c19bf6f018299ed4acdce5760e45e2e4bc4ae.jpg?sv=2015-12-11&amp;sr=b&amp;sig=Thbp46wdgoqbDaAF06v2Y2ijzny0jx2fBDo1EZab%2BNY%3D&amp;st=2018-03-22T10:22:21Z&amp;se=2292-01-05T11:22:21Z&amp;sp=r",
        "mediaFileName": "IMG_18-03-22_165220084_1.jpg"
      }
    ],
    "actionType": "Image",
    "caption": "Testing."
  },
 "context": "Any data which is required to be returned in callback",
  "fromUser": "+91xxxxxxxx",
  "fromUserId": "72e91-f3-4e7b-84eb-4e228406fb9b",
  "fromUserName": "Robin Richard",
  "fromUserProfilePic": "https://mobileonlyapps.blob.core.windows.net/72e29591-4e7b-84eb-4e228406fb9b/c34afc0d53614ae29285d08e6409e416.jpg"
}
```
### <a name="data-for-event-announcement"></a>données de l'événement'annonce'
| Paramètre | Type | Description |
| :---: | :---: | :--- |
| title | Chaîne | Titre de l'action d'annonce |
| text | Chaîne | Corps du message de l'action d'annonce |
| panne | Tableau | Chaque élément contient mediaUrl et mediaFileName|
| mediaUrl | url | URL de l'image |
| mediaFileName | Chaîne | Filename |


#### <a name="sample-webhook-response-for-announcement"></a>Exemple de réponse webHook pour «Announcement»
```javascript
{
  "objectId": "8c291050-9be8-45d6-97f5-bb7013930027",
  "objectType": "Group",
  "eventType": "Announcement",
  "eventId": "3e49b367-acf6-48a7-a675-6bf4d372a070",
  "data": {
    "text": "Caption :Testing.",
    "title": "Sent by Robin Richard",
    "media": [
      {
        "url": "https://cdn.inc-000.kms.osi.office.net/contenthost/beb2cfef8732c6cc3b54652c1f6f99d64f529fd9be3d409e2966552639fb791f.jpeg",
        "fileName": "e3c145f1-5e6f-4ee9-bd83-49ec3a1c2550.jpeg"
      }
    ]
  },
 "context": "Any data which is required to be returned in callback",
  "fromUser": "+91xxxxxxxx",
  "fromUserId": "72e91-f3-4e7b-84eb-4e228406fb9b",
  "fromUserName": "Robin Richard",
  "fromUserProfilePic": "https://mobileonlyapps.blob.core.windows.net/72e29591-4e7b-84eb-4e228406fb9b/c34afc0d53614ae29285d08e6409e416.jpg"
}
```

### <a name="data-for-event-jobcreated"></a>données de l'événement «JobCreated»
| Paramètre | Type | Description |
| :---: | :---: | :--- |
| title | Chaîne | Titre de l'action d'annonce |
| text | Chaîne | Corps du message de l'action d'annonce |
| actionId | Id | Identificateur de cette instance particulière de l'action de travail |
| dueDate | Date | Date d'expiration de la tâche |
| assignedTo | Tableau de chaînes | Tableau de numéros de téléphone |


#### <a name="sample-webhook-response-for-jobcreated"></a>Exemple de réponse webHook pour «JobCreated»
```javascript
{
  "objectId": "8c2950-9be8-45d6-97f5-bb7013930027",
  "objectType": "Group",
  "eventType": "JobCreated",
  "eventId": "3e49b367-acf6-48a7-a675-6bf4d372a070",
  "data": {
    "assignedTo": [
      "+919740797266"
    ],
    "title": "Test Job",
    "dueDate": "2018-03-22T18:29:59Z",
    "actionId": "aeb012-31a0-477a-a131-8a1e2791b36e",
    "groupId": "8c291050-9be8-6-97f5-bb7013930027"
  },
 "context": "Any data which is required to be returned in callback",
  "fromUser": "+91xxxxxxxx",
  "fromUserId": "72e91-f3-4e7b-84eb-4e228406fb9b",
  "fromUserName": "Robin Richard",
  "fromUserProfilePic": "https://mobileonlyapps.blob.core.windows.net/72e29591-4e7b-84eb-4e228406fb9b/c34afc0d53614ae29285d08e6409e416.jpg"
}
```

### <a name="data-for-event-jobresponse"></a>données de l'événement «JobResponse»
| Paramètre | Type | Description |
| :---: | :---: | :--- |
| title | Chaîne | Titre de l'action d'annonce |
| text | Chaîne | Corps du message de l'action d'annonce |
| actionId | Id | Identificateur de cette instance particulière de l'action de travail |
| groupId | Chaîne | Identificateur de groupe |
| responseId | Chaîne | GUID permettant d'identifier cette réponse |
| responseDetails | Tableau de chaînes | Tableau d'objets Response |
| utilisateur | Chaîne | Numéro de téléphone du destinataire |
| assigneeName | Chaîne | Nom du cessionnaire |
| assigneeProfilePic | url | URL du profil de l'intervenant pic |
| isCompleted | Booléen | Le travail est-il terminé? |




#### <a name="sample-webhook-response-for-jobresponse"></a>Exemple de réponse webHook pour «JobResponse»
```javascript
{
  "objectId": "8c2950-9be8-45d6-97f5-bb7013930027",
  "objectType": "Group",
  "eventType": "JobResponse",
  "eventId": "3e49b367-acf6-48a7-a675-6bf4d372a070",
  "data": {
    "actionId": "2ce34820-3d67-4807-9a1d-7cf099c2e7ae",
    "groupId": "8c291050-9be8-45d6-97f5-bb7013930027",
    "responseId": "80a883ec-e6c7-4dc8-979d-d268bbeeee8b",
    "responseDetails": {
      "response": {
        "assignee": "++91xxxxxxxx",
        "assigneeName": "Robin Richard",
        "assigneeProfilePic": "https://mobileonlyapps.blob.core.windows.net/72e29591-f391-4e7b-84eb-4e228406fb9b/c34afc0d536285d08e6409e416.jpg",
        "isCompleted": true
      }
    }
  },
  "context": "Any data which is required to be returned in callback",
  "fromUser": "+91xxxxxxxx",
  "fromUserId": "72e91-f3-4e7b-84eb-4e228406fb9b",
  "fromUserName": "Robin Richard",
  "fromUserProfilePic": "https://mobileonlyapps.blob.core.windows.net/72e29591-4e7b-84eb-4e228406fb9b/c34afc0d53614ae29285d08e6409e416.jpg"
}
```

### <a name="data-for-event-actioncreated--surveycreated"></a>données pour l'événement «ActionCreated»/«SurveyCreated»
| Paramètre | Type | Description |
| :---: | :---: | :--- |
| actionId | Id | Identificateur de cette instance particulière de l'action de travail |
| groupId | Chaîne | Identificateur de groupe |
| responseId | Chaîne | GUID permettant d'identifier cette réponse |
| questions | Tableau de chaînes | Tableau d'objets |
| répondeur | Chaîne | Numéro de téléphone du répondeur |
| responderName | Chaîne | Nom du répondeur |
| responderProfilePic | url | URL du profil du répondeur pic |
| isAnonymous | Booléen | La réponse de l'enquête a-t-elle été soumise de manière anonyme? |
| isUpdateResponse | Booléen | La réponse a-t-elle été mise à jour par un répondeur, car la réponse a été envoyée plus tôt |


#### <a name="schema-details-for-responsewithquestions-object"></a>Détails du schéma pour l'objet «responseWithQuestions»
| Paramètre | Type | Description |
| :---: | :---: | :--- |
| title | String | Titre de la question |
| type | String | QuestionType |
| options | Tableau | Liste d'options (paire clé-valeur) applicable aux questions à choix multiples |
| isInvisible | Booléen | Est la question cachée de l'interface utilisateur |



#### <a name="sample-webhook-response-for-actioncreated--surveycreated"></a>Exemple de réponse webHook pour «ActionCreated»/«SurveyCreated»
```javascript
{
  "objectId": "8c2950-9be8-45d6-97f5-bb7013930027",
  "objectType": "Group",
  "eventType": "ActionCreated",
  "eventId": "3e49b367-acf6-48a7-a675-6bf4d372a070",
  "data": {
   "actionId": "920f9802-62dafb-9bc2-8d3ba5c43609",
    "groupId": "8c291050-9be8-4d6-97f5-bb7013930027",
    "responseId": "420e9ef0-2a6d-405-a2bf-2688648ce79a",
    "isUpdateResponse": false,
    "responder": "+91xxxxxxxxx",
    "responderName": "Robin Richard",
    "responderProfilePic": "https://mobileonlyapps.blob.core.windows.net/72e29591-f391-4e7b-84eb-4e228406fb9b/c34afc0d53614ae29285d08e6409e416.jpg",
    "isAnonymous": false,
    "responseDetails": {
      "responseWithQuestions": [
        {
          "title": "1",
          "type": "Text",
          "options": [],
          "answer": "1"
        },
        {
          "title": "2",
          "type": "AttachmentList",
          "options": [],
          "answer": [
            {
              "mediaUrl": "https://cdn.inc-000.kms.osi.office.net/att/9841be297131449fba1123ec8545ab30fa72c2017555ba4bcd4ac18d5f7850b4.jpg?sv=2015-12-11&amp;sr=b&amp;sig=Egd4wDmAfGrIoklLj70SrV7D3QtwtMEWQx673U%3D&amp;st=2018-03-23T09:26:24Z&amp;se=2292-01-06T10:26:24Z&amp;sp=r",
              "mediaFileName": "IMG_18-03-23_155619990_1.jpg"
            }
          ]
        },
        {
          "isInvisible": true,
          "title": "ResponseTime",
          "type": "DateTime",
          "options": [],
          "answer": 1521800782956
        }
      ]
    }
  },
  "context": "Any data which is required to be returned in callback",
  "fromUser": "+91xxxxxxxx",
  "fromUserId": "72e91-f3-4e7b-84eb-4e228406fb9b",
  "fromUserName": "Robin Richard",
  "fromUserProfilePic": "https://mobileonlyapps.blob.core.windows.net/72e29591-4e7b-84eb-4e228406fb9b/c34afc0d53614ae29285d08e6409e416.jpg"
}
```



### <a name="data-for-event-surveyresponse-actionresponse"></a>données pour l'événement «SurveyResponse»/«ActionResponse»
| Paramètre | Type | Description |
| :---: | :---: | :--- |
| actionId | Id | Identificateur de cette instance particulière de l'action de travail |
| groupId | Chaîne | Identificateur de groupe |
| responseId | Chaîne | GUID permettant d'identifier cette réponse |
| responseDetails | Tableau de chaînes | Tableau d'objets «responseWithQuestions» |
| répondeur | Chaîne | Numéro de téléphone du répondeur |
| responderName | Chaîne | Nom du répondeur |
| responderProfilePic | url | URL du profil du répondeur pic |
| isAnonymous | Booléen | La réponse de l'enquête a-t-elle été soumise de manière anonyme? |
| isUpdateResponse | Booléen | La réponse a-t-elle été mise à jour par un répondeur, car la réponse a été envoyée plus tôt |


#### <a name="schema-details-for-responsewithquestions-object"></a>Détails du schéma pour l'objet «responseWithQuestions»
| Paramètre | Type | Description |
| :---: | :---: | :--- |
| title | String | Titre de la question |
| type | String | QuestionType |
| options | Tableau | Liste des options applicables aux questions à choix multiples |
| répondre | Tableau d'objets JSON | Réponses |
| isInvisible | Booléen | Est la question cachée de l'interface utilisateur |



#### <a name="sample-webhook-response-for-surveyresponse-actionresponse"></a>Exemple de réponse webHook pour «SurveyResponse» «ActionResponse»
```javascript
{
  "objectId": "8c2950-9be8-45d6-97f5-bb7013930027",
  "objectType": "Group",
  "eventType": "SurveyResponse",
  "eventId": "3e49b367-acf6-48a7-a675-6bf4d372a070",
  "data": {
   "actionId": "920f9802-62dafb-9bc2-8d3ba5c43609",
    "groupId": "8c291050-9be8-4d6-97f5-bb7013930027",
    "responseId": "420e9ef0-2a6d-405-a2bf-2688648ce79a",
    "isUpdateResponse": false,
    "responder": "+91xxxxxxxxx",
    "responderName": "Robin Richard",
    "responderProfilePic": "https://mobileonlyapps.blob.core.windows.net/72e29591-f391-4e7b-84eb-4e228406fb9b/c34afc0d53614ae29285d08e6409e416.jpg",
    "isAnonymous": false,
    "responseDetails": {
      "responseWithQuestions": [
        {
          "title": "1",
          "type": "Text",
          "options": [],
          "answer": "1"
        },
        {
          "title": "2",
          "type": "AttachmentList",
          "options": [],
          "answer": [
            {
              "mediaUrl": "https://cdn.inc-000.kms.osi.office.net/att/9841be297131449fba1123ec8545ab30fa72c2017555ba4bcd4ac18d5f7850b4.jpg?sv=2015-12-11&amp;sr=b&amp;sig=Egd4wDmAfGrIoklLj70SrV7D3QtwtMEWQx673U%3D&amp;st=2018-03-23T09:26:24Z&amp;se=2292-01-06T10:26:24Z&amp;sp=r",
              "mediaFileName": "IMG_18-03-23_155619990_1.jpg"
            }
          ]
        },
        {
          "isInvisible": true,
          "title": "ResponseTime",
          "type": "DateTime",
          "options": [],
          "answer": 1521800782956
        }
      ]
    }
  },
  "context": "Any data which is required to be returned in callback",
  "fromUser": "+91xxxxxxxx",
  "fromUserId": "72e91-f3-4e7b-84eb-4e228406fb9b",
  "fromUserName": "Robin Richard",
  "fromUserProfilePic": "https://mobileonlyapps.blob.core.windows.net/72e29591-4e7b-84eb-4e228406fb9b/c34afc0d53614ae29285d08e6409e416.jpg"
}
```


### <a name="data-for-event-memberadded--memberremoved"></a>données pour l'événement «MemberAdded»/«MemberRemoved»
| Paramètre | Type | Description |
| :---: | :---: | :--- |
| membre | Chaîne | Numéro de téléphone du membre ajouté |
| NomMembre | Chaîne | Nom du membre ajouté |
| type | String | Rôle d'appartenance du membre ajouté |
| memberProfilePic | url | URL du profil de l'intervenant pic |





#### <a name="sample-webhook-response-for-memberadded-memberremoved"></a>Exemple de réponse webHook pour «MemberAdded»/«MemberRemoved»
```javascript
{
  "objectId": "8c2950-9be8-45d6-97f5-bb7013930027",
  "objectType": "Group",
  "eventType": "JobResponse",
  "eventId": "3e49b367-acf6-48a7-a675-6bf4d372a070",
  "data": {
    "member": "+91xxxxxxxx",
    "memberName": "Jan Decker",
    "memberProfilePic": "https://mobileonlyapps.blob.core.windows.net/polymer-7ebb8d90e1324b5cbd61d1e10a30ada7/bbac582a4364860679d40fda7c6b.jpg",
    "type": "Member"
  },
  "context": "Any data which is required to be returned in callback",
  "fromUser": "+91xxxxxxxx",
  "fromUserId": "72e91-f3-4e7b-84eb-4e228406fb9b",
  "fromUserName": "Robin Richard",
  "fromUserProfilePic": "https://mobileonlyapps.blob.core.windows.net/72e29591-4e7b-84eb-4e228406fb9b/c34afc0d53614ae29285d08e6409e416.jpg"
}
```

