---
title: /REACTION
description: Article de référence de l’API réactions de requête sur n’importe quelle Action envoyé dans un groupe
topic: Reference
author: nitinjms
ms.openlocfilehash: a0c86aac9dd70e4c72e177f64c6e2dcaeeb8b41c
ms.sourcegitcommit: 9ac64dcb3ef72a84589483e45ae8e528aaa5aa4c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/18/2018
ms.locfileid: "20457303"
---
# <a name="reaction"></a>/REACTION
Point de terminaison API pour interroger les données réactions sur n’importe quelle Action envoyée dans un groupe.

## <a name="post-reaction"></a>/Reaction POST

    POST {endpoint-url}/v1/groups/{groupId}/reaction

### <a name="request-parameters"></a>Paramètres de la demande

| | Paramètre | Type | Facultatif ? | Description |
| :---: | :---: | :---: | :---  | :--- |
| Paramètre de chemin d’accès d’URL | groupId | String | Non | GUID représentant le groupId de la ressource groupe spécifique |
| En-tête HTTP | accessToken | String | Non | Reçu à partir de la fin de l’authentification par jeton d’accès |
| En-tête HTTP | Content-Type | String | Non | valeur : application/json |

### <a name="request-body"></a>Corps de la requête

| Paramètre | Type | Facultatif ? | Description |
| :---: | :---: | :--- | :--- |
| referenceId | String | Non | GUID représentant l’id de référence d’entité qui représente une Action |
| sourceGroupId | String | Non | GUID du groupe dans lequel l’Action a été envoyée. En cas de groupes est d’un autre groupe de celle-ci peut différer de 'groupId' fourni dans l’url de paramètre de chemin d’accès|
| reactionType | String | Non | Valeur enum : « Like'/ ' commentaire »|
| comment | String | Non | Texte de commentaire est obligatoire uniquement pour reactionType « Comment ». Pour « Like », il doit être ignoré |

#### <a name="sample-json-request"></a>Exemple de demande JSON

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
| reactionId | String | GUID représentant l’id de l’entité réaction après l’exécution réussie de la demande |

#### <a name="sample-json-response"></a>Exemple de réponse JSON

```javascript
{
    "reactionId": "71df-d53a-43cc-9b73-80dcc22502ab"
}
```
## <a name="get-reaction-summary-at-action-level"></a>OBTENIR /reaction résumé au niveau de l’Action

    GET {endpoint-url}/v1/groups/{groupId}/reaction/{referenceId}/summary?sourceGroupId={sourceGroupId}


### <a name="request-parameters"></a>Paramètres de la demande

|  | Paramètre | Type | Facultatif ? | Description |
| :---: | :---: | :---: | :---: | :--- |
| Paramètre de chemin d’accès d’URL | groupId | String | Non | GUID représentant le groupId de la ressource groupe spécifique |
| Paramètre de chemin d’accès d’URL | referenceId | String | Non | GUID représentant l’id de référence d’entité qui représente une Action |
| Paramètre de chemin d’accès d’URL | sourceGroupId | String | Non | GUID du groupe dans lequel l’Action a été envoyée. |
| En-tête HTTP | accessToken | String | Non | Reçu à partir de la fin de l’authentification par jeton d’accès |

### <a name="response-body"></a>Corps de la réponse

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| Résumé | Tableau JSON | Tableau de JSON objets chaque résumé réactions représentant une action envoyé dans un groupe |

### <a name="response-body-summary-object"></a>Objet synthèse de corps de réponse

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| referenceId | String | GUID représentant l’id de référence d’entité qui représente une Action |
| reactionsCountMap | Objet JSON | Objet JSON contenant un nombre j’aime et des commentaires pour cette referenceId |


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

## <a name="get-reaction-summary-at-group-level"></a>OBTENIR /reaction résumé au niveau de groupe

    GET {endpoint-url}/v1/groups/{groupId}/reaction/summary?sourceGroupId={sourceGroupId}&cursor={timeStamp}


### <a name="request-parameters"></a>Paramètres de la demande

|  | Paramètre | Type | Facultatif ? | Description |
| :---: | :---: | :---: | :---: | :--- |
| Paramètre de chemin d’accès d’URL | groupId | String | Non | GUID représentant le groupId de la ressource groupe spécifique |
| Paramètre de chemin d’accès d’URL | sourceGroupId | String | Non | GUID du groupe dans lequel l’Action a été envoyée. |
| Paramètre de chemin d’accès d’URL | curseur | Horodatage | Non | Horodatage à partir de laquelle le résumé doit être calculée. La valeur 0 par défaut |
| En-tête HTTP | accessToken | String | Non | Reçu à partir de la fin de l’authentification par jeton d’accès |

### <a name="response-body"></a>Corps de la réponse

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| curseur | Horodatage | Horodatage jusqu'à laquelle résumé a été calculé. L’ensemble suivant de reactionSummary peut être générée à l’aide de cette valeur de curseur |
| Résumé | Tableau JSON | Tableau de JSON objets chaque résumé réactions représentant une action envoyé dans un groupe |

#### <a name="response-body-summary-object"></a>Objet synthèse de corps de réponse

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| referenceId | String | GUID représentant l’id de référence d’entité qui représente une Action |
| reactionsCountMap | Objet JSON | Objet JSON contenant un nombre j’aime et des commentaires pour cette referenceId |


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

## <a name="get-reaction-details-for-a-action"></a>OBTENIR plus d’informations /reaction pour une Action

    GET {endpoint-url}/v1/groups/{groupId}/reaction/{referenceId}?sourceGroupId={sourceGroupId}&reactionType={reactionType}&cursor={timeStamp}


### <a name="request-parameters"></a>Paramètres de la demande

|  | Paramètre | Type | Facultatif ? | Description |
| :---: | :---: | :---: | :---: | :--- |
| Paramètre de chemin d’accès d’URL | groupId | String | Non | GUID représentant le groupId de la ressource groupe spécifique |
| Paramètre de chemin d’accès d’URL | sourceGroupId | String | Non | GUID du groupe dans lequel l’Action a été envoyée. |
| Paramètre de chemin d’accès d’URL | referenceId | String | Non | GUID représentant l’id de référence d’entité qui représente une Action |
| Paramètre de chemin d’accès d’URL | reactionType | String | Non | Valeur enum : « Like'/ ' commentaire »|
| Paramètre de chemin d’accès d’URL | curseur | TimeStamp | Non | Horodatage à partir de laquelle le résumé doit être calculée. La valeur 0 par défaut |
| En-tête HTTP | accessToken | String | Non | Reçu à partir de la fin de l’authentification par jeton d’accès |

### <a name="response-body"></a>Corps de la réponse

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| curseur | TimeStamp | Horodatage jusqu'à laquelle reactionDetail a été fournie. L’ensemble suivant de reactionDetails peut être générée à l’aide de cette valeur de curseur |
| reactionDetails | Tableau JSON | Tableau de JSON objets chaque détail réactions représentant une action envoyé dans un groupe |

#### <a name="response-body-summary-object"></a>Objet synthèse de corps de réponse

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| reactionId | String | GUID représentant l’id de la réaction créée sur referenceId représentant une Action |
| userId | Objet JSON | Nom d’utilisateur de l’utilisateur qui a créé la réaction d’une Action |
| heure de dernière modification | Timestamp | Horodatage auquel réaction a été créé ou mis à jour |


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