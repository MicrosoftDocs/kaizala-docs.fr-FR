---
title: /Reaction
description: Article de référence pour l'API permettant d'interroger les réactions sur n'importe quelle action envoyée dans un groupe
topic: Reference
author: nitinjms
ms.openlocfilehash: a0c86aac9dd70e4c72e177f64c6e2dcaeeb8b41c
ms.sourcegitcommit: 973f754fdb7c93381f808632f47fe66a46cc069e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/24/2019
ms.locfileid: "33191301"
---
# <a name="reaction"></a>/Reaction
Point de terminaison d'API pour les données de réactions de requête sur n'importe quelle action envoyée dans un groupe.

## <a name="post-reaction"></a>POST/reaction

    POST {endpoint-url}/v1/groups/{groupId}/reaction

### <a name="request-parameters"></a>Paramètres de la demande

| | Paramètre | Type | Module? | Description |
| :---: | :---: | :---: | :---  | :--- |
| Paramètre de chemin d'URL | groupId | Chaîne | Non | GUID représentant l'ID de ressource de la ressource de groupe spécifique |
| En-tête HTTP | accessToken | Chaîne | Non | Jeton d'accès reçu depuis le point de terminaison auth |
| En-tête HTTP | Content-Type | Chaîne | Non | valeur: application/JSON |

### <a name="request-body"></a>Corps de la demande

| Paramètre | Type | Module? | Description |
| :---: | :---: | :--- | :--- |
| ID | Chaîne | Non | GUID représentant l'ID de la référence d'entité représentant une action |
| sourceGroupId | Chaîne | Non | GUID du groupe dans lequel l'action a été envoyée. Dans le cas de groupes qui sont un sous-groupe d'un autre groupe, cela peut être différent de «groupId» fourni dans le paramètre de chemin d'URL|
| reactionType | Chaîne | Non | Valeur enum: 'like'/'commentaire'|
| comment | Chaîne | Non | Le texte du commentaire est obligatoire uniquement pour reactionType'commentaire'. Pour'like', ceci doit être ignoré |

#### <a name="sample-json-request"></a>Exemple de requête JSON

```javascript
{
    "comment":"Comment-3",
    "referenceId":"4a44e62f-5142-a980-c7a48e2d92a8",
    "sourceGroupId":"fc6f2802-4431-b82f-60985a515b58",
    "reactionType":"Comment"
}
```

### <a name="response-body"></a>Corps de la réponse

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| reactionId | Chaîne | GUID représentant l'ID de l'entité de réaction après exécution réussie de la demande |

#### <a name="sample-json-response"></a>Exemple de réponse JSON

```javascript
{
    "reactionId": "71df-d53a-43cc-9b73-80dcc22502ab"
}
```
## <a name="get-reaction-summary-at-action-level"></a>OBTENIR un résumé/reaction au niveau de l'action

    GET {endpoint-url}/v1/groups/{groupId}/reaction/{referenceId}/summary?sourceGroupId={sourceGroupId}


### <a name="request-parameters"></a>Paramètres de la demande

|  | Paramètre | Type | Module? | Description |
| :---: | :---: | :---: | :---: | :--- |
| Paramètre de chemin d'URL | groupId | Chaîne | Non | GUID représentant l'ID de ressource de la ressource de groupe spécifique |
| Paramètre de chemin d'URL | ID | Chaîne | Non | GUID représentant l'ID de la référence d'entité représentant une action |
| Paramètre de chemin d'URL | sourceGroupId | Chaîne | Non | GUID du groupe dans lequel l'action a été envoyée. |
| En-tête HTTP | accessToken | Chaîne | Non | Jeton d'accès reçu depuis le point de terminaison auth |

### <a name="response-body"></a>Corps de la réponse

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| résumé | Tableau JSON | Tableau d'objets JSON représentant chacun une synthèse des réactions sur une action envoyée dans un groupe |

### <a name="response-body-summary-object"></a>Objet de synthèse du corps de la réponse

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| ID | Chaîne | GUID représentant l'ID de la référence d'entité représentant une action |
| reactionsCountMap | Objet JSON | Objet JSON contenant le nombre d'objets et de commentaires pour ce ID |


### <a name="sample-json-response"></a>Exemple de réponse JSON

```javascript
{
    "summary": [
        {
            "referenceId": "4a44e62e-4b42-a980-c7a48e2d92a8",
            "reactionsCountMap": {
                "like": 1,
                "comment": 4
            }
        }
    ]
}
```

## <a name="get-reaction-summary-at-group-level"></a>OBTENIR un résumé/reaction au niveau du groupe

    GET {endpoint-url}/v1/groups/{groupId}/reaction/summary?sourceGroupId={sourceGroupId}&cursor={timeStamp}


### <a name="request-parameters"></a>Paramètres de la demande

|  | Paramètre | Type | Module? | Description |
| :---: | :---: | :---: | :---: | :--- |
| Paramètre de chemin d'URL | groupId | Chaîne | Non | GUID représentant l'ID de ressource de la ressource de groupe spécifique |
| Paramètre de chemin d'URL | sourceGroupId | Chaîne | Non | GUID du groupe dans lequel l'action a été envoyée. |
| Paramètre de chemin d'URL | curseur | Dates | Non | Horodatage à partir duquel le résumé doit être calculé. Valeur par défaut 0 |
| En-tête HTTP | accessToken | Chaîne | Non | Jeton d'accès reçu depuis le point de terminaison auth |

### <a name="response-body"></a>Corps de la réponse

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| curseur | Dates | timeStamp: le résumé qui a été calculé. Le prochain jeu de reactionSummary peut être généré à l'aide de cette valeur de curseur |
| résumé | Tableau JSON | Tableau d'objets JSON représentant chacun une synthèse des réactions sur une action envoyée dans un groupe |

#### <a name="response-body-summary-object"></a>Objet de synthèse du corps de la réponse

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| ID | Chaîne | GUID représentant l'ID de la référence d'entité représentant une action |
| reactionsCountMap | Objet JSON | Objet JSON contenant le nombre d'objets et de commentaires pour ce ID |


#### <a name="sample-json-response"></a>Exemple de réponse JSON

```javascript
{
    "cursor": 636674054802000000,
    "summary": [
        {
            "referenceId": "4a44-51be-4b42-a980-c7a48e2d92a8",
            "reactionsCountMap": {
                "like": 1,
                "comment": 4
            }
        },
        {
            "referenceId": "4a44-51be-4b420-c7a48e2d92a8",
            "reactionsCountMap": {
                "like": 10,
                "comment": 14
            }
        }
    ]
}
```

## <a name="get-reaction-details-for-a-action"></a>OBTENIR les détails de/reaction pour une action

    GET {endpoint-url}/v1/groups/{groupId}/reaction/{referenceId}?sourceGroupId={sourceGroupId}&reactionType={reactionType}&cursor={timeStamp}


### <a name="request-parameters"></a>Paramètres de la demande

|  | Paramètre | Type | Module? | Description |
| :---: | :---: | :---: | :---: | :--- |
| Paramètre de chemin d'URL | groupId | Chaîne | Non | GUID représentant l'ID de ressource de la ressource de groupe spécifique |
| Paramètre de chemin d'URL | sourceGroupId | Chaîne | Non | GUID du groupe dans lequel l'action a été envoyée. |
| Paramètre de chemin d'URL | ID | Chaîne | Non | GUID représentant l'ID de la référence d'entité représentant une action |
| Paramètre de chemin d'URL | reactionType | Chaîne | Non | Valeur enum: 'like'/'commentaire'|
| Paramètre de chemin d'URL | curseur | Dates | Non | Horodatage à partir duquel le résumé doit être calculé. Valeur par défaut 0 |
| En-tête HTTP | accessToken | Chaîne | Non | Jeton d'accès reçu depuis le point de terminaison auth |

### <a name="response-body"></a>Corps de la réponse

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| curseur | Dates | TimeStamp pour laquelle reactionDetail a été fourni. Le prochain jeu de reactionDetails peut être généré à l'aide de cette valeur de curseur |
| reactionDetails | Tableau JSON | Tableau d'objets JSON chacun représentant les réactions détaillées sur une action envoyée dans un groupe |

#### <a name="response-body-summary-object"></a>Objet de synthèse du corps de la réponse

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| reactionId | Chaîne | GUID représentant l'ID de la réaction créée sur ID représentant une action |
| userId | Objet JSON | UserId de l'utilisateur qui a créé la réaction sur une action |
| lastModifiedTime | Timestamp | Horodateur à partir duquel la réaction a été créée/mise à jour |


#### <a name="sample-json-response"></a>Exemple de réponse JSON

```javascript
{
    "cursor": 636674054802000000,
    "reactionDetails": [
        {
            "lastModifiedTime": 1529573303063,
            "reactionId": "4b2fb78b-b529-4fa1-acda-f670b491ebca",
            "userId": "72e29591-f391-4e7b-84eb-4e228406fb9b"
        },
        {
            "lastModifiedTime": 1529573313063,
            "reactionId": "4b2fb7529-4fa1-acda-f670b491ebca",
            "userId": "72e29591-f391-4eb-4e228406fb9b"
        }
    ]
}
```