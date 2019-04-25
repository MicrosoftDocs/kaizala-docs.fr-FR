---
title: /Actions_post
description: Article de référence pour l'API de publication d'une action sur un groupe Kaizala
topic: Reference
author: nitinjms
ms.openlocfilehash: 5ca7c92f76a0e0e18025dda2526b53515a003e90
ms.sourcegitcommit: 973f754fdb7c93381f808632f47fe66a46cc069e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/24/2019
ms.locfileid: "33190741"
---
# <a name="post-a-action-in-a-group"></a>Publier une action dans un groupe
## <a name="post-actions"></a>POST/actions

    POST {endpoint-url}/groups/{groupId}/actions

### <a name="request-parameters"></a>Paramètres de la demande

|  | Paramètre | Type | Module? | Description |
| :---: | :---: | :---: | :---: | :--- |
| Paramètre de chemin d'URL | groupId | String | Non | Identificateur de groupe |
| En-tête HTTP | accessToken | String | Non | Jeton d'accès reçu depuis le point de terminaison auth |
| En-tête HTTP | Content-Type | String | Non | valeur: application/JSON |

### <a name="request-body"></a>Corps de la demande

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| id | String | ID du package d'action Kaizala. L'un des actionType ou l'ID doit être spécifié |
| actionType | String | Enum «Survey»/«Job». L'un des actionType ou l'ID doit être spécifié |
| actionBody | Objet JSON | Objet représentant les données nécessaires pour l'action correspondante. Paramètres définis ci-dessous pour chacune des actions prises en charge. |


#### <a name="actionbody-for-an-announcement-action"></a>actionBody pour une action d'annonce

| Paramètre | Type | Module? | Description |
| :---: | :---: | :---: | :--- |
| title | String | Non | Titre de l'annonce |
| MediaResources | Chaîne [] | Oui | Tableau des ressources multimédias |
| Message | String | Non | Corps du message |

#### <a name="sample-json-request-for-an-announcement-action"></a>Exemple de demande JSON pour une action d'annonce

```javascript
{
  "actionType" : "Announcement",
  "actionBody" : 
  {
    "Message":"Announcement from API Message text",
    "Title" : "Title text", 
    "MediaResources" : 
    [
      "eyJUaHVtYm5haWwiOiIvOWovNEFBUVNrWkpSZ0FCQVFFQVlBQmdBQUQvMndCREFJVmNaSFZrVTRWMWJIV1dqb1dleVAvWnlMZTN5UC8vLy9MLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8yd0JEQVk2V2xzaXZ5UC9aMmYvLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vL3dBQVJDQUNTQVFRREFTSUFBaEVCQXhFQi84UUFId0FBQVFVQkFRRUJBUUVBQUFBQUFBQUFBQUVDQXdRRkJnY0lDUW9MLzhRQXRSQUFBZ0VEQXdJRUF3VUZCQVFBQUFGOUFRSURBQVFSQlJJaE1VRUdFMUZoQnlKeEZES0JrYUVJSTBLeHdSVlMwZkFrTTJKeWdna0tGaGNZR1JvbEppY29LU28wTlRZM09EazZRMFJGUmtkSVNV","eyJUaHVtYm5haWwiOiIvOWovNEFBUVNrWkpSZ0FCQVFFQVlBQmdBQUQvMndCREFJVmNaSFZrVTRWMWJIV1dqb1dleVAvWnlMZTN5UC8vLy9MLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8yd0JEQVk2V2xzaXZ5UC9aMmYvLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vL3dBQVJDQUNTQVFRREFTSUFBaEVCQXhFQi84UUFId0FBQVFVQkFRRUJBUUVBQUFBQUFBQUFBQUVDQXdRRkJnY0lDUW9MLzhRQXRSQUFBZ0VE"
    ]
  }
}

```

#### <a name="actionbody-for-a-job-action"></a>actionBody pour une action de travail

| Paramètre | Type | Module? | Description |
| :---: | :---: | :---: | :--- |
| title | String | Non | Titre du travail |
| assignedTo | Chaîne [] | Non | Titre du travail |
| dueDate | long | Oui | Valeur par défaut: 24 heures. Nombre d'heures avant laquelle le travail doit être effectué |

##### <a name="sample-json-request-for-a-job-action"></a>Exemple de demande JSON pour une action de travail

```javascript
{
    actionType:"Job",
    actionBody: {
        title : "test job",
        assignedTo : ["+911111111111", "+911111111112"],
        dueDate : 10
    }
}

```

#### <a name="actionbody-for-a-poll-action"></a>actionBody pour une action de sondage

| Paramètre | Type | Module? | Description |
| :---: | :---: | :---: | :--- |
| relative | String | Non | Question de sondage |
| Choix | Tableau JSON | Non | Options disponibles pour le sondage. Chaque choix comporte le composant suivant: <ol><li>title (obligatoire & dans le format de chaîne) </li><li>image (facultatif)</li></ol> |
| expiryInHours | Entier | Oui | Valeur par défaut: 720. Nombre d'heures pendant lesquelles une interrogation gven a expiré. |

##### <a name="sample-json-request-for-a-poll-action"></a>Exemple de requête JSON pour une action de sondage

```javascript
{actionType:"Poll", actionBody:{question:"Do you find Kaizala extensibility easy to use?", 
    choices:
        [
        {title:"Yes",image:"eyJUaHVtYm5haWwiOiIvOWovNEFBUVNrWkpSZ0FCQVFFQVlBQmdBQUQvMndCREFJVmNaSFZrVTRWMWJIV1dqb1dleVAvWnlMZTN5UC8vLy9MLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8yd0JEQVk2V2xzaXZ5UC9aMmYvLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vLy8vL3dBQVJDQUNTQVFRREFTSUFBaEVCQXhFQi84UUFId0FBQVFVQkFRRUJBUUVBQUFBQUFBQUFBQUVDQXdRRkJnY0lDUW9MLzhRQXRSQUFBZ0VEQXdJRUF3VUZCQVFBQUFGOUFRSURBQVFSQlJJaE1VRUdFMUZoQnlKeEZES0JrYUVJSTBLeHdSVlMwZkFrTTJKeWdna0tGaGNZR1JvbEppY29LU28wTlRZM09EazZRMFJGUmtkSVNVcFRWRlZXVjFoWldtTmtaV1puYUdscWMzUjFkbmQ0ZVhxRGhJV0doNGlKaXBLVGxKV1dsNWlabXFLanBLV21wNmlwcXJLenRMVzJ0N2k1dXNMRHhNWEd4OGpKeXRMVDFOWFcxOWpaMnVIaTQrVGw1dWZvNmVyeDh2UDA5ZmIzK1BuNi84UUFId0VBQXdFQkFRRUJBUUVCQVFBQUFBQUFBQUVDQXdRRkJnY0lDUW9MLzhRQXRSRUFBZ0VDQkFRREJBY0ZCQVFBQVFKM0FBRUNBeEVFQlNFeEJoSkJVUWRoY1JNaU1vRUlGRUtSb2JIQkNTTXpVdkFWWW5MUkNoWWtOT0VsOFJjWUdSb21KeWdwS2pVMk56ZzVPa05FUlVaSFNFbEtVMVJWVmxkWVdWcGpaR1ZtWjJocGFuTjBkWFozZUhsNmdvT0VoWWFIaUltS2twT1VsWmFYbUptYW9xT2twYWFucUttcXNyTzB0YmEzdUxtNndzUEV4Y2JIeU1uSzB0UFUxZGJYMk5uYTR1UGs1ZWJuNk9ucTh2UDA5ZmIzK1BuNi85b0FEQU1CQUFJUkF4RUFQd0N4UlJSUUFVVVVVQUZGRkZBQlJSUlFBVVVVVUFGRkZGQUJSUlJRQVVVVVVBRkZGRkFCUlJSUUFVVVVVQUZGRkZBQlJSUlFBVVVVVUFGRkZGQUJSUlJRQVVVVVVBRkZGRkFCUlJSUUFVVVVsQUMwVW1hTTByZ0xSU1pvelJjQmFLVE5HYUxnTFJTWm96UmNCYUtUTkdhTGdMUlNab3pSY0JhS1ROR2FMb0JhS0tLWUJSUlJRQVVVVVVBRkZGRkFCUlJSUUFVVVVVQUZGRkZBQlJSUlFBVVVVVUFGSWVsTFNIcFNld0MwVVVVd0NpaWs3MEFMUlNZb3hTMUFXaWt4UmlqVUJhS1RGR0tOUUZvcE1VWW8xQVdrUFNqRkJIRkR2WUJhS1RGR0tOUUZvcE1VWW8xQVdpa3hSaWpVQmFLVEZHS05RRm9wQlMwd0NpaWlnQW9vb29BS0tLS0FDaWlpZ0FwRDBwYVE5S1QyQVdpaWltQVVuZWxwTzlJQmFLS0tZQlJSUlFBVVVVVUFGRkZGQUJTSHBTMGg2VW5zQXRGRkZNQW9vb29BS0tLS0FDaWlpZ0JPOUxTZDZXa2dDaWlpbUFVVVVVQUZGRkZBQlJSUlFBVVVVVUFKaWpGTFJTc2dFeFJpbHBPOUZrQVlveFMwVVdRQ1lveFMwVVdRQ1lveFMwVVdRQ1lveFMwVVdRQ1lveFMwVVdRQlJSUlRBS0tLS0FDaWlpZ0Fvb29vQVR2UzBuZWxwSUFvb29wZ0ZGRkZBQlJSUlFBVVVVVUFGRkZGQUJSUlJRQVVuZWxwTzlMc0F0RkZGTUFvb29vQUtLS0tBQ2lpaWdBb29vb0FLS0tLQUNpaWlnQW9vb29BS0tLS0FFNzB0SjNwYVNBS0tLS1lCUlJSUUFVVVVVQUZGRkZBQlJSUlFBVVVVVUFGSjNwYVR2U0FXaWlpbUFVVVVVQUZGRkZBQlJSUlFBVVVVVUFGRkZGQUJSUlJRQVVVVVVBRkZGRkFDZDZXazcwdEpBRkZGRk1Bb29vb0FLS0tLQUNpaWlnQW9vb29BS0tLS0FDa3BhS0FFeFJpbG9wV1FDWW94UzBVV1FDWW94UzBVV1FDWW94UzBVV1FDWW94UzBVV1FDWW94UzBVV1FDWW94UzBVV1FDWW94UzBVV1FDWW94UzBVV1FDVXRGRk1Bb29vb0FLS0tLQUNpaWlnQW9vb29BS0tLS0FDaWlpZ0Fvb29vQUtLS0tBQ2lpaWdBb29vb0FLS0tLQUNpaWlnQW9vb29BS0tLS0FDaWlpZ0Fvb29vQUtLS0tBQ2lpaWdBb29vb0FLS0tLQUNpaWlnQW9vb29BS0tLS0FDaWlpZ0Fvb29vQUtLS0tBQ2lpaWdBb29vb0FLS0tLQUNpaWlnQW9vb29BS0tLS0FDaWlpZ0Fvb29vQUtLS0tBQ2lpaWdELzlrPSIsIkFjdGlvblR5cGUiOjMsIkZpbGVzIjpbeyJJZCI6ImU1Y2YyMWJmLWQ3OGItNGY4Yi1iYjY3LTM2NTJlNDk1ZDEyZSIsIk5hbWUiOiJ0ZXN0LnBuZyIsIlNpemUiOjQsIlVybCI6Imh0dHBzOi8vY2RuLmthc2NvcmUub3NpLm9mZmljZS5uZXQvNzVlOGU3YjYzZDJhNGMxMGNkYzMwMjA4YWEyN2YxYzI5ODdkODY4YTBlNzY0ZmM3NDJhOTRmNjU0OWQ4YmRiMi5wbmc/c3Y9MjAxNS0xMi0xMSZzcj1iJnNpZz00aXFzd2pGVll5cUdxeUtnNmNkTWRVUW1pQWV6OHNWOTUxVVNjVW1MekxrJTNEJnN0PTIwMTctMDUtMTdUMDclM0EwNCUzQTQxWiZzZT0yMjkxLTAzLTAyVDA4JTNBMDQlM0E0MVomc3A9ciJ9XX0="},
        {title:"No"},
        {title:"Not at all"}
        ],
    expiryInHours:10}}
```
#### <a name="actionbody-for-a-lets-meet-action"></a>actionBody pour une action de réunion

| Paramètre | Type | Module? | Description |
| :---: | :---: | :---: | :--- |
| title | String | Non | Titre de la demande de réunion  |
| startingTime | DateTime
 | Non | Heure de début de la réunion |
| DurationInMins | Entier | Non | Valeur par défaut: 30 minutes. Nombre de minutes pendant lesquelles une réunion est effectuée |
| positionnement | Objet JSON | Oui | Emplacement de la réunion. Contient 3 composants: Latitude, longitude, nom  |
| réunion | Chaîne | Oui | Ordre du jour de la réunion/Description de la réunion |
| isSenderOnly | Bool | Oui | Pour autoriser uniquement l'expéditeur à consulter le résumé de la réunion. Valeur par défaut: false |

##### <a name="sample-json-request-for-a-lets-meet-action"></a>Exemple de demande JSON pour une action de réunion

```javascript
{actionType:"LetsMeet", actionBody:{title:"lets catch up?", startingTime:"2018-01-01T00:00:00Z", duration:45, place:{"latitude":15.0,"longitude":96.0,"name":"MS Building 3"}, agenda:"no agenda", isSenderOnly:false}}

```

#### <a name="actionbody-for-a-survey-action-or-action-package-instanceid-"></a>actionBody pour une action d'enquête ou une instance de package d'action (ID):

| Paramètre | Type | Module? | Description |
| :---: | :---: | :---: | :--- |
| title | String | Non | Titre du travail |
| dueDate | long | Oui | Valeur par défaut: 24 heures. Nombre d'heures avant laquelle le travail doit être effectué |
| isAnonymous | Bool | Oui | Pour autoriser les réponses d'enquête anonymes. Valeur par défaut: false |
| isSenderOnly | Bool | Oui | Pour autoriser uniquement l'expéditeur à afficher le résumé de l'enquête. Valeur par défaut: false |
| acceptMultipleResponses | Bool | Oui | Pour autoriser plusieurs réponses du même répondeur. Valeur par défaut: false |
| questions | object[] | Non | Chaque élément de l'objet [] est décrit ci-dessous en tant qu'objet question. |
| properties | object[] | Non | Chaque élément de l'objet [] est décrit ci-dessous en tant qu'objet Property. Valide uniquement pour la création d'une instance de package d'action |

##### <a name="structure-for-question-object"></a>Structure de l'objet question

| Paramètre | Type | Module? | Description |
| :---: | :---: | :---: | :--- |
| title | String | Non | Titre de la question |
| type | String | Non | Type de la question. Énumération: SingleOption/multiOption/Text/Image/Numeric/date/location/AttachmentList |
| isInvisible | Bool | Oui | Valeur par défaut: false. Pour contrôler la visibilité de la question |
| options | object[] | Oui | Obligatoire pour SingleOption et le type de question multiOption. chaque élément de l'objet [] est décrit ci-dessous comme objet option |

###### <a name="structure-for-option-object"></a>Structure de l'objet option

| Paramètre | Type | Module? | Description |
| :---: | :---: | :---: | :--- |
| title | Chaîne | Non | Titre de l'option |

###### <a name="structure-for-property-object"></a>Structure de l'objet Property

| Paramètre | Type | Module? | Description |
| :---: | :---: | :---: | :--- |
| name | Chaîne | Non | Nom de la propriété |
| type | Chaîne | Non | Type de la propriété. Énumération: Text, Numeric, location, DateTime, StringList, Attachment, StringSet, AttachmentList |
| value | Chaîne | Non | Valeur de la propriété |

##### <a name="sample-json-request-for-a-survey-action"></a>Exemple de demande JSON pour une action d'enquête

```javascript
{
  actionType: "Survey",
  actionBody: {
    isAnonymous:false,
    isSenderOnly:false,
    acceptMultipleResponses:true,
    dueDate:10,
    title: "A test survey!!",
    questions: [
        {
            title: "a test question written here",
            type: "Text"
        },
        {
            title: "Single select question",
            type: "SingleOption",
            options: [{title:"Opt1"},{title:"Opt2"}]
        },
        {
            title: "Multi select question",
            type: "MultiOption",
            options: [{title:"MOpt1"},{title:"MOpt2"},{title:"MOpt3"}]
        },
        {
            title: "Numeric question",
            type: "Numeric"
        },
        {
            title: "Location question",
            type: "Location"
        },
        {
            title: "DateTime question",
            type: "DateTime"
        },
        {
            title: "Image question",
            type: "Image"
        }
        ]
  }
}
```

##### <a name="response-body"></a>Corps de la réponse

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| ID | Chaîne | Identificateur de demande |
| actionId | Chaîne | Identificateur d'action |

```javascript
{
    "referenceId": "79f43f77-d586-4e9a-b8b8-103e0ac5b782",
    "actionId": "232e7003-22a1-4a28-bb36-9176e704e10c"
}
```
