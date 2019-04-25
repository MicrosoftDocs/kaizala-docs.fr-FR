---
title: /webhooks
description: Article de référence pour l'API permettant de gérer les abonnements Kaizala
topic: Reference
author: nitinjms
ms.openlocfilehash: a2cdb74284f6980644366cf3b61740ea46389512
ms.sourcegitcommit: 973f754fdb7c93381f808632f47fe66a46cc069e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/24/2019
ms.locfileid: "33190731"
---
# <a name="apis-to-register--manage-webhooks"></a>API pour inscrire & gérer les webhooks
## <a name="webhook"></a>/webhook
Point de terminaison de l'API pour gérer les abonnements aux événements dans Kaizala.

Les webHooks sont un modèle HTTP léger qui fournit un modèle d'éditeur/d'abonné simple pour le câblage des API Web et des services SaaS. Lorsqu'un événement se produit dans Kaizala, une notification est envoyée sous la forme d'une demande HTTP POST aux abonnés inscrits. La requête POST contient des informations sur l'événement, ce qui permet au destinataire d'agir en conséquence.


À l'aide des webHooks, vous pouvez vous abonner à différents événements qui se produisent dans un contexte de groupe de conversation dans Kaizala.

### <a name="post-webhook"></a>POST/webhook

    POST {endpoint-url}/v1/webhook

Pour vérifier que votre point de terminaison de service webhook est authentique et que nous travaillons, nous allons vérifier votre URL de rappel avant de créer un abonnement. Pour la vérification, nous vous enverrons un jeton de validation dont vous avez besoin pour nous envoyer vos commentaires dans un délai de 5 secondes. [En savoir plus](WebHookValidaton.md)

#### <a name="request-parameters"></a>Paramètres de la demande

|  | Paramètre | Type | Module? | Description |
| :---: | :---: | :---: | :---: | :--- |
| En-tête HTTP | accessToken | String | Non | Jeton d'accès reçu depuis le point de terminaison auth || En-tête HTTP | Content-Type | String | Non | «application/JSON» |

#### <a name="request-body"></a>Corps de la demande

|  Paramètre | Type | Module? | Description |
| :---: | :---: | :---: | :--- |
| objectId | String | Non | Identificateur représentant l'objet dans lequel le contexte des webhooks doit être créé. Pour ObjectType = Group, l'identificateur de son groupe, pour ObjectType = action, son actionId, pour ObjectType = ActionPackage, son action-Package-ID |
| objectType | String | Non | Énumération: «Group»/«action»/«ActionPackage» |
| eventTypes | Tableau | Non | Tableau des différents types d'événements dont vous avez besoin pour abonner le webhook. Les événements pris en charge sont: «ActionCreated», «ActionResponse», «SurveyCreated», «JobCreated», «SurveyResponse», «JobResponse», «TextMessageCreated», «AttachmentCreated», «Announcement», «MemberAdded», «MemberRemoved», «GroupAdded», «GroupRemoved», «» |
| callBackUrl | String | Non | URL HTTPs à laquelle les événements abonnés doivent être notifiés |
| callBackToken | Chaîne | Oui | Paramètre facultatif que vous pouvez définir qui sera envoyé dans l'en-tête HTTP'KZ-callback-Token'avec chaque rappel effectué par le webHook |
| callBackContext | Chaîne | Oui | Paramètre facultatif que vous pouvez définir qui sera envoyé dans la charge utile JSON en tant que «Context» avec chaque rappel effectué par le webHook |
| validité | Chaîne | Oui | La validité du webHook est active au format d'époque. La valeur par défaut est 2 ans |


#### <a name="response-body"></a>Corps de la réponse
| Paramètre | Type | Description |
| :---: | :---: | :--- |
| webhookId | Chaîne | Identificateur représentant le webHook créé |

#### <a name="request-body---subscribe-to-all-events-at-group-level"></a>Corps de la demande: s'abonner à tous les événements au niveau du groupe

```javascript
{  
   "objectId":"74943849802190eaea3810",
   "objectType":"Group",
   "eventTypes":[
      "ActionCreated",
      "ActionResponse",
      "SurveyCreated",
      "JobCreated",
      "SurveyResponse",
      "JobResponse",
      "TextMessageCreated",
      "AttachmentCreated",
      "Announcement",
      "MemberAdded",
      "MemberRemoved",
      "GroupAdded",
      "GroupRemoved"
   ],
   "callBackUrl":"https://requestb.in/123",
   "callBackToken":"tokenToBeVerifiedByCallback",
   "callBackContext":"Any data which is required to be returned in callback"
}

```


Vous pouvez trouver le schéma de réponse webhook pour les événements inscrits dans Kaizala [**ici**](EventSchema.md).

> **Remarque:** Kaizala garantit au moins une fois la remise de la réponse webhook. Cela peut se produire, dans certains cas, que Kaizala peut envoyer une réponse webhook en double pour le même événement.

### <a name="get-webhook"></a>Obtenir/webhook

    OBTENIR {Endpoint-URL}/v1/webhook

#### <a name="request-parameters"></a>Paramètres de la demande


|  | Paramètre | Type | Module? | Description |
| :---: | :---: | :---: | :---: | :--- |
| En-tête HTTP | accessToken | String | Non | Jeton d'accès reçu depuis le point de terminaison auth |
| Paramètre de requête | objectId | String | Non | Identificateur représentant l'objet dans lequel le contexte des webhooks doit être créé. Pour ObjectType = Group, l'identificateur de son groupe, pour ObjectType = action, son actionId, pour ObjectType = ActionPackage, son action-Package-ID |
| Paramètre de requête | objectType | String | Non | Énumération: «Group»/«action»/«ActionPackage» |

#### <a name="response-body"></a>Corps de la réponse

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| webhooks | Tableau d'objets JSON | Tableau de webhooks abonnés sur objectId |

#####  <a name="json-structure-for-each-individual-webhook-in-the-array-webhooks"></a>Structure JSON pour chaque webhook individuel dans le groupe webhooks []:

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| id | String | Identificateur de webhook |
| objectId | Chaîne | Identificateur d'objet |
| objectType | String | Énumération: «Group»/«action»/«ActionPackage» |
| events | Chaîne [] | Liste d'événements avec chaque valeur «ActionCreated», «ActionResponse», «SurveyCreated», «JobCreated», «SurveyResponse», «JobResponse», «TextMessageCreated», «AttachmentCreated», «Announcement», «MemberAdded», «MemberRemoved», «GroupAdded», «», « GroupRemoved» |
| callBackUrl | Chaîne | URL de rappel à laquelle les événements abonnés doivent être notifiés |
| callBackToken | Chaîne | Paramètre qui sera envoyé dans l'en-tête HTTP'KZ-callback-Token'avec chaque rappel effectué par le webHook |
| callBackContext | Chaîne | Paramètre envoyé dans la charge utile JSON comme «Context» avec chaque rappel effectué par le webHook |
| validité | Chaîne | La validité du webHook est active au format d'époque. |
| Active | Booléen | True si l'état du webhook est actif |

##### <a name="sample-json-response"></a>Exemple de réponse JSON

```javascript
{
    "webhooks": [
        {
            "id": "dac6fccf-f2e9-4abc-94d7-793037e99da7",
            "objectId": "b21405d1-4b10-4c46-bfa9-8338592f3782",
            "objectType": "Group",
            "events": [
                "ActionCreated",
                "ActionResponse",
                "SurveyCreated",
                "JobCreated",
                "SurveyResponse",
                "JobResponse",
                "TextMessageCreated",
                "AttachmentCreated",
                "Announcement",
                "MemberAdded",
                "MemberRemoved",
                "GroupAdded",
                "GroupRemoved"
            ],
            "filters": [],
            "callbackUrl": "https://requestb.in/12786un1",
            "callbackToken": "tokenToBeVerifiedByCallback",
            "ts": 1505491564677,
            "validity": 1568605416677
            "active": true
        }
    ]
}
```

### <a name="delete-webhook"></a>Supprimer/webhook

    DELETE {Endpoint-URL}/v1/webhook

#### <a name="request-parameters"></a>Paramètres de la demande
|  | Paramètre | Type | Module? | Description |
| :---: | :---: | :---: | :---: | :--- |
| En-tête HTTP | accessToken | String | Non | Jeton d'accès reçu depuis le point de terminaison auth |
| Paramètre Path | webhookId | String | Non | Identificateur de webhook |

### <a name="put-webhook"></a>PUT/webhook

    PUT {endpoint-url}/v1/webhook/{webhookId}

Tout paramètre du webhook peut être mis à jour. Le corps de la demande peut contenir un ou plusieurs paramètres, selon les besoins.

#### <a name="request-parameters"></a>Paramètres de la demande

|  | Paramètre | Type | Module? | Description |
| :---: | :---: | :---: | :---: | :--- |
| En-tête HTTP | accessToken | String | Non | Jeton d'accès reçu depuis le point de terminaison auth |
| Paramètre Path | webhookId | String | Non | Identificateur de webhook |

#### <a name="request-body"></a>Corps de la demande

|  Paramètre | Type | Module? | Description |
| :---: | :---: | :---: | :--- |
| objectId | Chaîne | Oui | Identificateur représentant l'objet dans lequel le contexte des webhooks doit être créé. Pour ObjectType = Group, l'identificateur de son groupe, pour ObjectType = action, son actionId, pour ObjectType = ActionPackage, son action-Package-ID |
| objectType | Chaîne | Oui | Énumération: «Group»/«action»/«ActionPackage» |
| eventTypes | Tableau | Oui | Tableau des différents types d'événements dont vous avez besoin pour abonner le webhook. Les événements pris en charge sont: «ActionCreated», «ActionResponse», «SurveyCreated», «JobCreated», «SurveyResponse», «JobResponse», «TextMessageCreated», «AttachmentCreated», «Announcement», «MemberAdded», «MemberRemoved», «GroupAdded», «GroupRemoved», «» |
| callBackUrl | Chaîne | Oui | URL HTTPs à laquelle les événements abonnés doivent être notifiés |
| callBackToken | Chaîne | Oui | Paramètre facultatif que vous pouvez définir qui sera envoyé dans l'en-tête HTTP'KZ-callback-Token'avec chaque rappel effectué par le webHook |
| callBackContext | Chaîne | Oui | Paramètre facultatif que vous pouvez définir qui sera envoyé dans la charge utile JSON en tant que «Context» avec chaque rappel effectué par le webHook |
| validité | Chaîne | Oui | La validité du webHook est active au format d'époque. La valeur par défaut est 2 ans |
| Actif | Booléen | Oui | Définir l'état du webhook sur actif si la valeur est true |


#### <a name="sample-request-body"></a>Exemple de corps de requête

````javascript
    { 
       "objectId":"74943849802190eaea3810",
       "objectType":"Group",
       "eventTypes":[
          "ActionCreated",
          "ActionResponse",
          "SurveyCreated",
          "JobCreated",
          "SurveyResponse",
          "JobResponse",
          "TextMessageCreated",
          "AttachmentCreated",
          "Announcement",
          "MemberAdded",
          "MemberRemoved",
          "GroupAdded",
          "GroupRemoved"
       ],
       "callBackUrl":"https://requestb.in/123",
       "callBackToken":"tokenToBeVerifiedByCallback",
      "Active": "true" 
    } 

````

## <a name="auto-disable-of-webhooks"></a>DésActivation automatique des webhooks

Pour améliorer la fiabilité de nos webhooks, nous avons récemment ajouté la nouvelle tentative et la logique de désActivation. L'URL/le point de terminaison de rappel enregistré avec un webhook, s'il n'est pas accessible ou ne répond pas avec un code d'État autre que 2xx (> = 3xx), notre service tentera de l'atteindre/le retenter de 6 fois de manière exponentielle dans un délai de 2 jours. 

En cas de défaillance continue pendant 2 jours, le webhook correspondant est désactivé et le propriétaire doit le mettre à jour avec l'API put/webhook avant de commencer à fonctionner à nouveau. Par exemple,

    
    PUT {endpoint-url}/v1/webhook/{subscriptionId}

### <a name="request-body"></a>Corps de la demande:
````javascript
{ 
  "Active": "true" 
} 
````
