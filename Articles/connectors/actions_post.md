---
title: / Actions_post
description: Article de référence de l’API de publier des actions sur un groupe Kaizala
topic: Reference
author: nitinjms
ms.openlocfilehash: 015a60bbef7be7108cc0edc10e81cc1f8b5636e2
ms.sourcegitcommit: 3a6a13cc885faf1bbc9ee8498f5183f414395aac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/20/2018
ms.locfileid: "19905129"
---
# <a name="post-a-action-in-a-group"></a>Publier une Action dans un groupe
### <a name="post-actions"></a>/Actions POST

    POST {endpoint-url}/groups/{groupId}/actions

##### <a name="request-parameters"></a>Paramètres de la demande

|  | Paramètre | Type | Facultatif ? | Description |
| :---: | :---: | :---: | :---: | :--- |
| Paramètre de chemin d’accès d’URL | groupId | Chaîne | Non | Identificateur de groupe |
| En-tête HTTP | accessToken | Chaîne | Non | Reçu à partir de la fin de l’authentification par jeton d’accès |
| En-tête HTTP | Content-Type | Chaîne | Non | valeur : application/json |

##### <a name="request-body"></a>Corps de la requête

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| id | Chaîne | ID du package Kaizala Action. ActionType ou Id doit être spécifiée |
| actionType | String | Enum « Enquête » / « Du travail ». ActionType ou Id doit être spécifiée |
| actionBody | Objet JSON | Objet représentant les données nécessaires pour l’Action respectif. Paramètres définis ci-dessous pour chacune des Actions prises en charge. |


###### <a name="actionbody-for-an-announcement-action"></a>actionBody pour une Action d’annonce

| Paramètre | Type | Facultatif ? | Description |
| :---: | :---: | :---: | :--- |
| title | Chaîne | Non | Titre de l’annonce |
| MediaResources | String] | Oui | Tableau des ressources multimédia |
| Message | Chaîne | Non | Corps du message |

###### <a name="sample-json-request-for-an-announcement-action"></a>Exemple de demande JSON pour une Action d’annonce

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

###### <a name="actionbody-for-a-job-action"></a>actionBody pour une Action de tâche

| Paramètre | Type | Facultatif ? | Description |
| :---: | :---: | :---: | :--- |
| title | Chaîne | Non | Titre de la tâche |
| assignedTo | String] | Non | Titre de la tâche |
| dueDate | long | Oui | Par défaut : 24 heures. Nombre d’heures avant laquelle le travail doit être terminé |

###### <a name="sample-json-request-for-a-job-action"></a>Exemple de demande JSON pour une Action de tâche

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

###### <a name="actionbody-for-a-poll-action"></a>actionBody pour une Action de sondage

| Paramètre | Type | Facultatif ? | Description |
| :---: | :---: | :---: | :--- |
| question | Chaîne | Non | Question du sondage |
| Choices | Tableau JSON | Non | Options disponibles pour l’interrogation. Chaque choix ont ci-dessous composant : <ol><li>titre (obligatoire & sous forme de chaîne) </li><li>image (facultatif)</li></ol> |
| expiryInHours | Entier | Oui | Par défaut : 720. Nombre d’heures dans laquelle un sondage gven expire |

###### <a name="sample-json-request-for-a-poll-action"></a>Exemple de demande JSON pour une Action de sondage

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
###### <a name="actionbody-for-a-lets-meet-action"></a>actionBody pour une Action répondent aux jetons

| Paramètre | Type | Facultatif ? | Description |
| :---: | :---: | :---: | :--- |
| title | Chaîne | Non | Titre de la demande de réunion  |
| startingTime | Date/heure | Non | Heure de début de la réunion |
| DurationInMins | Entier | Non | Valeur par défaut : 30 minutes. Nombre de minutes pour laquelle une réunion est effectuée |
| place | Objet JSON | Oui | Emplacement de la réunion. Contient les 3 composants : latitude, longitude, nom  |
| ordre du jour | Chaîne | Oui | L’ordre du jour de la réunion / Description de la réunion |
| isSenderOnly | Bool | Oui | Pour autoriser uniquement l’expéditeur afficher les rendez-vous résumé. Par défaut : false |

###### <a name="sample-json-request-for-a-lets-meet-action"></a>Exemple de demande JSON pour un rendez-vous Action

```javascript
{actionType:"LetsMeet", actionBody:{title:"lets catch up?", startingTime:"2018-01-01T00:00:00Z", duration:45, place:{"latitude":15.0,"longitude":96.0,"name":"MS Building 3"}, agenda:"no agenda", isSenderOnly:false}}

```

###### <a name="actionbody-for-a-survey-action-or-action-package-instanceid-"></a>actionBody pour un instance(id) de package enquête Action ou Action :

| Paramètre | Type | Facultatif ? | Description |
| :---: | :---: | :---: | :--- |
| title | Chaîne | Non | Titre de la tâche |
| dueDate | long | Oui | Par défaut : 24 heures. Nombre d’heures avant laquelle le travail doit être terminé |
| é anonyme | Bool | Oui | Pour autoriser les réponses de l’enquête anonyme. Par défaut : false |
| isSenderOnly | Bool | Oui | Pour autoriser uniquement l’expéditeur afficher le résumé enquête. Par défaut : false |
| acceptMultipleResponses | Bool | Oui | Pour autoriser plusieurs réponses à partir de la même répondeur. Par défaut : false |
| questions | object[] | Non | Chaque élément d’object [] est décrit ci-dessous en tant qu’objet Question |
| properties | object[] | Non | Chaque élément d’object [] est décrit ci-dessous en tant qu’objet Property. Valide uniquement pour la création d’Instance de Package de l’Action |

###### <a name="structure-for-question-object"></a>Structure de l’objet Question

| Paramètre | Type | Facultatif ? | Description |
| :---: | :---: | :---: | :--- |
| title | Chaîne | Non | Titre de la question |
| type | Chaîne | Non | Type de la question. Enum : SingleOption/MultiOption/texte/Image/numérique/Date/emplacement/AttachmentList |
| isInvisible | Bool | Oui | Par défaut : false. Pour contrôler la visibilité de la question |
| options | object[] | Oui | Obligatoire pour le type de question SingleOption et MultiOption. chaque élément d’object [] est décrit ci-dessous en tant qu’Option, objet |

###### <a name="structure-for-option-object"></a>Structure d’Option, objet

| Paramètre | Type | Facultatif ? | Description |
| :---: | :---: | :---: | :--- |
| title | Chaîne | Non | Titre de l’Option |

###### <a name="structure-for-property-object"></a>Structure de l’objet Property

| Paramètre | Type | Facultatif ? | Description |
| :---: | :---: | :---: | :--- |
| name | Chaîne | Non | Nom de la propriété |
| type | Chaîne | Non | Type de la propriété. Enum : Texte, numérique, emplacement, DateTime, StringList, pièce jointe, StringSet, AttachmentList |
| value | Chaîne | Non | Valeur de la propriété |

###### <a name="sample-json-request-for-a-survey-action"></a>Exemple de demande JSON pour une Action de l’enquête

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

###### <a name="response-body"></a>Corps de la réponse

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| referenceId | Chaîne | Identificateur de demande |
| actionId | Chaîne | Identificateur d’action |

```javascript
{
    "referenceId": "79f43f77-d586-4e9a-b8b8-103e0ac5b782",
    "actionId": "232e7003-22a1-4a28-bb36-9176e704e10c"
}
```
