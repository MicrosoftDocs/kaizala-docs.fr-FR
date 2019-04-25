---
title: /actions
description: Article de référence pour l'API permettant d'obtenir la liste des actions dans un groupe
topic: Reference
author: nitinjms
ms.openlocfilehash: 717b91d38ed43c85c3511de84538bb357e799f9b
ms.sourcegitcommit: 973f754fdb7c93381f808632f47fe66a46cc069e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/24/2019
ms.locfileid: "33190719"
---
# <a name="get-list-of-actions-in-a-group"></a>Obtenir la liste des actions dans un groupe
## <a name="get-actions"></a>OBTENIR/actions

    GET {endpoint-url}/v1/groups/{groupId}/actions?actionType={action_Type}

### <a name="request-parameters"></a>Paramètres de la demande

|  | Paramètre | Type | Module? | Description |
| :---: | :---: | :---: | :---: | :--- |
| Paramètre de chemin d'URL | groupId | Chaîne | Non | GUID représentant l'ID de ressource de la ressource de groupe spécifique |
| En-tête HTTP | accessToken | Chaîne | Non | Jeton d'accès reçu depuis le point de terminaison auth |
| Paramètre de requête d'URL | actionType | Chaîne | Non | Type d'action à récupérer |
| Paramètre de requête d'URL | fromDate | Date/heure (époque) | Oui | Heure à partir de laquelle les actions doivent être récupérées |
| Paramètre de requête d'URL | count | number | Oui | Nombre d'actions individuelles à renvoyer; Valeur par défaut = 30 |

### <a name="response-body"></a>Corps de la réponse

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| actions | Tableau d'objets JSON | Tableau d'objets action |
| hasMore | booléen | Si le nombre maximal d'actions par réponse est atteint, cette variable sera définie sur true. |

Structure JSON pour chaque action individuelle dans les actions de tableau []:

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| ID | Chaîne | ID pour le message |
| actionType | String | Type d'action retourné |
| actionBody | Tableau d'objets JSON propre au ActionType | Tableau avec des objets spécifiques au ActionType |
| expéditeur | Chaîne | Numéro de téléphone de l'utilisateur qui a envoyé l'action au groupe |
| sentAt | DateTime
 | Heure à laquelle l'action a été publiée dans le groupe |

####  <a name="actionbody-object-structure-for-imagepicture-attachment"></a>structure d'objet actionBody pour la pièce jointe image/image:

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| imageURL | Chaîne | Chaîne de l'URL de l'image |

##### <a name="sample-json-response"></a>Exemple de réponse JSON:

```javascript
{
  "actions": [
    {
      "referenceId": "8a93c6cc-8499-44b0-aa54-016648100080",
      "actionType": "Image",
      "sender": "+9196500000",
      "creationTime": 1481180806,
      "actionBody": {
        "imageUrl": "https://kaizala.blob.core.windows.net/polymer/9540ca6cd6f0753314d6e.jpg"
      }
    }
]
}
```

####  <a name="actionbody-object-structure-for-the-action-share-location"></a>structure d'objet actionBody pour l'action «emplacement de partage»:

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| latitude | Double | Coordonnées latitude de l'emplacement |
| longitude | Double | Coordonnées de longitude de l'emplacement |

##### <a name="sample-json-response"></a>Exemple de réponse JSON:

```javascript
{
  "actions": [
    {
      "referenceId": "3ba9f6b6-e968-44f2-a83a-acc03a3d18d3",
      "actionType": "ShareLocation",
      "sender": "+919900000",
      "creationTime": 1481180922,
      "actionBody": {
        "latitude": 17.429725,
        "longitude": 78.3408851
      }
    }
  ]
}
```

#### <a name="actionbody-object-structure-for-the-action-photo-with-location"></a>structure d'objet actionBody pour l'action «photo avec emplacement»:

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| imageURL | Chaîne | Chaîne de l'URL de l'image |
| latitude | Double | Coordonnées latitude de l'emplacement |
| longitude | Double | Coordonnées de longitude de l'emplacement |

##### <a name="sample-json-response"></a>Exemple de réponse JSON:

```javascript
{
  "actions": [
    {
      "referenceId": "3ba9f6b6-e968-44f2-a83a-acc03a3d18d3",
      "actionType": "ShareLocation",
      "sender": "+919900000",
      "creationTime": 1481180922,
      "actionBody": {
        "imageUrl": "https://kaizala.blob.core.windows.net/polymer/9540ca6cd6f0753314d6e.jpg",
        "latitude": 17.429725,
        "longitude": 78.3408851
      }
    }
  ]
}
```

####  <a name="actionbody-object-structure-for-the-action-job"></a>structure d'objet actionBody pour l'action «Job»:

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| actionId | Chaîne | GUID représentant l'instance d'action spécifique |
| title | Chaîne | Titre du travail |
| assigneeCount | Numérique | Nombre de personnes affectées |
| responseCount | Numérique | Nombre d'utilisateurs ayant marqué le travail comme terminé |
| isCompleted | Booléen | True lorsque tous les utilisateurs ont effectué le travail |

##### <a name="sample-json-response"></a>Exemple de réponse JSON:

```javascript
{
  "actions": [
    {
      "referenceId": "3214841c-eaa2-4bf3-a583-acc69d9279c4",
      "actionType": "Job",
      "sender": "+919910005",
      "creationTime": 1481179788,
      "actionBody": {
        "actionId": "f260dc09-f1f3-4305-84f6-6edbedb82fb7",
        "title": "Test",
        "assigneeCount": 1,
        "responseCount": 0,
        "isCompleted": false
      }
    }
  ]
}
```
####  <a name="actionbody-object-structure-for-the-action-poll"></a>structure d'objet actionBody pour l'action «Poll»:

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| actionId | Chaîne | GUID représentant l'instance d'action spécifique |
| relative | Chaîne | Question de sondage |
| isSenderOnly | Booléen | True lorsque le résumé de l'interRogation est visible uniquement par l'expéditeur |
| expiryDate | DateTime
 | Date et heure de l'expiration du sondage |
| Choix | Tableau JSON | Liste d'objets JSON avec le composant suivant <ol><li>titre-texte d'option</li><li>image de l'option image</li></ol> |

##### <a name="sample-json-response"></a>Exemple de réponse JSON:

```javascript
{
    "actions": [
        {
            "referenceId": "d4753fdc-13fe-4162-a48f-5bf071bfd380",
            "actionType": "Poll",
            "sender": "+918585010248",
            "sentAt": "2017-12-20T08:33:51Z",
            "actionBody": {
                "actionId": "27c7dbcf-48bb-4523-8273-d53a3da2343b",
                "question": "Do you find Kaizala extensibility easy to use?",
                "isSenderOnly": false,
                "expiryDate": "2017-12-20T18:33:51Z",
                "choices": [
                    {
                        "title": "Yes",
                        "image": "https://cdn.kascore.osi.office.net/75e8e7b63d2a4c10cdc30208aa27f1c2987d868a0e764fc742a94f6549d8bdb2.png?sv=2015-12-11&sr=b&sig=4iqswjFVYyqGqyKg6cdMdUQmiAez8sV951UScUmLzLk%3D&st=2017-05-17T07%3A04%3A41Z&se=2291-03-02T08%3A04%3A41Z&sp=r"
                    },
                    {
                        "title": "No"
                    },
                    {
                        "title": "Not at all"
                    }
                ]
            }
        }
  ]
}
```
####  <a name="actionbody-object-structure-for-the-action-lets-meet"></a>structure d'objet actionBody pour l'action «je suis en réunion»:

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| actionId | Chaîne | GUID représentant l'instance d'action spécifique |
| title | String | Titre de la demande de réunion |
| isSenderOnly | Booléen | True lorsque le résumé de l'interRogation est visible uniquement par l'expéditeur |
| duration | Entier | Durée de la réunion (en minutes) |
| réunion | Chaîne | Calendrier défini pour la réunion |
| startingTime | DateTime
 | Date et heure de l'expiration du sondage |
| Positionnement | Objet JSON | Données de localisation avec le composant suivant <ol><li>Système</li><li>Ouest</li><li>name</li></ol> |

##### <a name="sample-json-response"></a>Exemple de réponse JSON:

```javascript
{
    "actions": [
        {
            "referenceId": "32d1e5ad-36ff-4237-a49c-4be95a10cd12",
            "actionType": "LetsMeet",
            "sender": "+918585010248",
            "sentAt": "2017-12-20T08:55:04Z",
            "actionBody": {
                "actionId": "3c80f0f1-2b2f-460a-b760-ec10adb7dbb1",
                "title": "lets catch up?",
                "startingTime": "2018-01-01T00:00:00Z",
                "agenda": "no agenda",
                "duration": 30,
                "isSenderOnly": false,
                "place": {
                    "latitude": 15,
                    "longitude": 96,
                    "name": "MS Building 3"
                }
            }
        }
  ]
}
```


####  <a name="actionbody-object-structure-for-the-action-survey"></a>structure d'objet actionBody pour l'action «Survey»:

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| actionId | Chaîne | GUID représentant l'instance d'action spécifique |
| title | String | Titre de l'enquête |
| responseCount | Numérique | Nombre de personnes ayant répondu à l'enquête |
| expiryDate | DateTime
 | Date et heure de l'expiration de l'enquête |

##### <a name="sample-json-response"></a>Exemple de réponse JSON:

```javascript
{
  "actions": [
    {
      "referenceId": "88a93ddd-0349d-4d18-86ee-c0f8484728db",
      "actionType": "Survey",
      "sender": "+91960000",
      "creationTime": 1480931759,
      "actionBody": {
        "actionId": "8106b2bb-236c-4952-a554-2baadcbd49a0",
        "title": "Sample Survey",
        "responseCount": 1
      }
    }
]
}
```

Ensuite: vous pouvez récupérer des informations supplémentaires sur chaque instance d'action avec l'actionId correspondant. [API pour la récupération des détails d'instance d'action](actionDetails.md)
