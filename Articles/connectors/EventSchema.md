# <a name="webhook-response-schema-for-registered-events"></a>Schéma de réponse Webhook pour les événements enregistrés

Si un webhook est inscrit, Kaizala renvoie une réponse webHook pour chaque événement sur objectId inscrit, filtré pour les événements enregistrés. Vous trouverez ci-dessous les détails du schéma de réponse webhook différentes pour différents événements.

## <a name="response-body"></a>Corps de réponse
| Paramètre | Type | Description |
| :---: | :---: | :--- |
| objectId | Chaîne | Identificateur représentant l’objet dans le contexte dans lequel le webhook a été créé. Pour l’argument typeobjet = groupe, l’identificateur de son groupe, pour ObjectType = Action, son actionId, pour ObjectType = ActionPackage, son id de package d’action |
| objectType | Chaîne | Enum : « groupe » / « Action » / « ActionPackage » |
| eventType | Chaîne | Événements enregistrés qui a été appelée. |
| eventId | Chaîne | Identificateur représentant l’événement |
| data | Objet JSON | Objet représentant les données spécifiques à l’événement. Paramètres définis ci-dessous pour chacun de l’événement pris en charge. |
| context | Chaîne | Renvoie la valeur qui a été définie lors de l’enregistrement d’un webhook sous paramètre 'callbackContext'|
| fromUser | Chaîne | Numéro de téléphone de l’expéditeur |
| fromUserId | Chaîne | UserId de l’expéditeur |
| fromUserName | Chaîne | Nom de l’expéditeur enregistré avec Kaizala |
| fromUserProfilePic | url | Pic de profil de l’expéditeur |

Le paramètre « données » serait varient en fonction de l’événement webHook. Vous pouvez trouver le schéma pour chaque événement ci-dessous.

### <a name="data-for-event-textmessagecreated"></a>données pour l’événement 'TextMessageCreated'
| Paramètre | Type | Description |
| :---: | :---: | :--- |
| text | String | Message texte qui a été envoyé. |

#### <a name="sample-webhook-response-for-textmessagecreated"></a>Exemple de réponse webHook pour 'TextMessageCreated'
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

### <a name="data-for-event-attachmentcreated"></a>données pour l’événement 'AttachmentCreated'
| Paramètre | Type | Description |
| :---: | :---: | :--- |
| multimédia | Tableau | Chaque élément contient mediaUrl et mediaFileName|
| mediaUrl | url | URL de l’image |
| mediaFileName | Chaîne | Nom de fichier |
| actionType | String | Valeur enum : « Image » |
| légende | Chaîne | légende attachée à l’image |

#### <a name="sample-webhook-response-for-attachmentcreated"></a>Exemple de réponse webHook pour 'AttachmentCreated'
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
### <a name="data-for-event-announcement"></a>données pour l’événement « Annonce »
| Paramètre | Type | Description |
| :---: | :---: | :--- |
| title | Chaîne | Titre de l’Action de l’annonce |
| text | String | Corps du message d’Action de l’annonce |
| multimédia | Tableau | Chaque élément contient mediaUrl et mediaFileName|
| mediaUrl | url | URL de l’image |
| mediaFileName | Chaîne | Nom de fichier |


#### <a name="sample-webhook-response-for-announcement"></a>Exemple de réponse webHook pour « Annonce »
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

### <a name="data-for-event-jobcreated"></a>données pour l’événement 'JobCreated'
| Paramètre | Type | Description |
| :---: | :---: | :--- |
| title | Chaîne | Titre de l’Action de l’annonce |
| text | String | Corps du message d’Action de l’annonce |
| actionId | ID | Identificateur pour cette instance particulière d’une Action de la tâche |
| dueDate | Date | Date par projet expire |
| assignedTo | Tableau de chaînes | Tableau des numéros de téléphone |


#### <a name="sample-webhook-response-for-jobcreated"></a>Exemple de réponse webHook pour 'JobCreated'
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

### <a name="data-for-event-jobresponse"></a>données pour l’événement 'JobResponse'
| Paramètre | Type | Description |
| :---: | :---: | :--- |
| title | Chaîne | Titre de l’Action de l’annonce |
| text | String | Corps du message d’Action de l’annonce |
| actionId | ID | Identificateur pour cette instance particulière d’une Action de la tâche |
| groupId | Chaîne | Identificateur de groupe |
| responseId | Chaîne | GUID de l’identification de réponse |
| responseDetails | Tableau de chaînes | Tableau d’objets de réponse |
| intervenant | Chaîne | Numéro de téléphone du destinataire. |
| assigneeName | Chaîne | Nom de la personne affectée |
| assigneeProfilePic | url | URL de pic de profil de la personne affectée au |
| isCompleted | Bool�en | La tâche est terminée ? |




#### <a name="sample-webhook-response-for-jobresponse"></a>Exemple de réponse webHook pour 'JobResponse'
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

### <a name="data-for-event-actioncreated--surveycreated"></a>données pour l’événement 'ActionCreated' / 'SurveyCreated'
| Paramètre | Type | Description |
| :---: | :---: | :--- |
| actionId | ID | Identificateur pour cette instance particulière d’une Action de la tâche |
| groupId | Chaîne | Identificateur de groupe |
| responseId | Chaîne | GUID de l’identification de réponse |
| questions | Tableau de chaînes | Tableau d’objets |
| répondeur | Chaîne | Numéro de téléphone du répondeur |
| responderName | Chaîne | Nom de l’auteur |
| responderProfilePic | url | URL de pic de profil du répondeur |
| é anonyme | Bool�en | Est la réponse d’enquête été présentée de manière anonyme |
| isUpdateResponse | Bool�en | A la réponse été mis à jour par le répondeur, étant donné que la réponse a été précédemment envoyée |


#### <a name="schema-details-for-responsewithquestions-object"></a>Détails du schéma pour l’objet 'responseWithQuestions'
| Paramètre | Type | Description |
| :---: | :---: | :--- |
| title | Chaîne | Titre de la question |
| type | Chaîne | QuestionType |
| options | Tableau | Liste d’options (paire clé-valeur) applicables aux questions choice multiple |
| isInvisible | Bool�en | La question est masquée dans l’interface utilisateur |



#### <a name="sample-webhook-response-for-actioncreated--surveycreated"></a>Exemple de réponse webHook pour 'ActionCreated' / 'SurveyCreated'
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



### <a name="data-for-event-surveyresponse-actionresponse"></a>données pour l’événement 'SurveyResponse' / 'ActionResponse'
| Paramètre | Type | Description |
| :---: | :---: | :--- |
| actionId | ID | Identificateur pour cette instance particulière d’une Action de la tâche |
| groupId | Chaîne | Identificateur de groupe |
| responseId | Chaîne | GUID de l’identification de réponse |
| responseDetails | Tableau de chaînes | Tableau d’objets 'responseWithQuestions' |
| répondeur | Chaîne | Numéro de téléphone du répondeur |
| responderName | Chaîne | Nom de l’auteur |
| responderProfilePic | url | URL de pic de profil du répondeur |
| é anonyme | Bool�en | Est la réponse d’enquête été présentée de manière anonyme |
| isUpdateResponse | Bool�en | A la réponse été mis à jour par le répondeur, étant donné que la réponse a été précédemment envoyée |


#### <a name="schema-details-for-responsewithquestions-object"></a>Détails du schéma pour l’objet 'responseWithQuestions'
| Paramètre | Type | Description |
| :---: | :---: | :--- |
| title | Chaîne | Titre de la question |
| type | Chaîne | QuestionType |
| options | Tableau | Liste d’options applicables aux questions choice multiple |
| answer | Tableau de l’objet Json | Réponses |
| isInvisible | Bool�en | La question est masquée dans l’interface utilisateur |



#### <a name="sample-webhook-response-for-surveyresponse-actionresponse"></a>Exemple de réponse webHook pour 'SurveyResponse' 'ActionResponse'
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


### <a name="data-for-event-memberadded--memberremoved"></a>données pour l’événement 'MemberAdded' / 'MemberRemoved'
| Paramètre | Type | Description |
| :---: | :---: | :--- |
| membre | Chaîne | Numéro de téléphone du membre ajouté |
| NomMembre | Chaîne | Nom du membre ajouté |
| type | Chaîne | L’appartenance au rôle du membre ajouté |
| memberProfilePic | url | URL de pic de profil de la personne affectée au |





#### <a name="sample-webhook-response-for-memberadded-memberremoved"></a>Exemple de réponse webHook pour 'MemberAdded' / 'MemberRemoved'
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

