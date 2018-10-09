---
title: /webhooks
description: Article de référence de l’API gérer les abonnements Kaizala
topic: Reference
author: nitinjms
ms.openlocfilehash: 00cbca686e8948d61425f067356e8c7eadb1892c
ms.sourcegitcommit: 27dd3ded71b4a77258961a2fc93c1ec0d02f2980
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25450927"
---
# <a name="apis-to-register--manage-webhooks"></a>API pour inscrire et gérer des webhooks
## <a name="webhook"></a>/webhook
Prévoit d’API pour gérer les abonnements aux événements à l’intérieur de Kaizala.

WebHooks est un modèle HTTP léger fournit un modèle d’éditeur/abonné simple pour câblage ensemble SaaS et les API de Web services. Lorsqu’un événement se produit dans Kaizala, une notification est envoyée sous la forme d’une demande HTTP POST pour les abonnés. La demande POST contient des informations sur l’événement qui rend possible pour le récepteur d’agir en conséquence.


À l’aide de WebHooks, vous pouvez vous abonner à différents événements qui se produisent dans un contexte de groupe de conversation dans Kaizala.

### <a name="post-webhook"></a>VALIDER /webhook

    POST {endpoint-url}/v1/webhook

Pour vérifier que votre point de terminaison de service webhook est authentique et qu’elle fonctionne nous allons maintenant vérifier votre URL de rappel avant de créer l’abonnement. Pour la vérification, nous vous enverrons un jeton de validation dont vous aurez besoin pour nous envoyer dans les 5 secondes. [En savoir plus](WebHookValidaton.md)

#### <a name="request-parameters"></a>Paramètres de la demande

|  | Paramètre | Type | Facultatif ? | Description |
| :---: | :---: | :---: | :---: | :--- |
| En-tête HTTP | accessToken | String | Non | Reçu à partir de la fin de l’authentification par jeton d’accès || En-tête HTTP | Content-Type | String | Non | « application/json » |

#### <a name="request-body"></a>Corps de la demande

|  Paramètre | Type | Facultatif ? | Description |
| :---: | :---: | :---: | :--- |
| objectId | String | Non | Identificateur représentant l’objet dans le contexte dans lequel les webhooks doivent être créés. Pour l’argument typeobjet = groupe, l’identificateur de son groupe, pour ObjectType = Action, son actionId, pour ObjectType = ActionPackage, son id de package d’action |
| objectType | String | Non | Enum : « groupe » / « Action » / « ActionPackage » |
| eventTypes | Tableau | Non | Tableau de différents types d’événements, à que vous devez vous inscrire le webhook. Supported events are: "ActionCreated","ActionResponse","SurveyCreated","JobCreated","SurveyResponse","JobResponse","TextMessageCreated","AttachmentCreated","Announcement","MemberAdded","MemberRemoved","GroupAdded","GroupRemoved" |
| callBackUrl | String | Non | URL HTTPS vers lequel doivent être notifiés pour les événements auxquels vous êtes abonnés |
| callBackToken | String | Oui | Paramètre facultatif vous pouvez définir qui seront envoyées dans l’en-tête HTTP 'jeton de rappel kz' avec chaque rappel effectuée par le WebHook |
| callBackContext | String | Oui | Paramètre facultatif vous pouvez définir qui seront envoyées dans la charge utile JSON en tant que contexte avec chaque rappel un effectuées par le WebHook |
| validité | String | Oui | Validité pour le WebHook actif au format d’origine. Valeur par défaut est de 2 ans |


#### <a name="response-body"></a>Corps de la réponse
| Paramètre | Type | Description |
| :---: | :---: | :--- |
| webhookId | String | Identificateur représentant le webHook créé |

#### <a name="request-body---subscribe-to-all-events-at-group-level"></a>Corps - de requête s’abonner à tous les événements au niveau de groupe

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


Vous pouvez trouver le schéma de réponse webhook les événements inscrits dans Kaizala [**ici**](EventSchema.md).

### <a name="get-webhook"></a>Obtenir /webhook

    GET {endpoint-url}/v1/webhook

#### <a name="request-parameters"></a>Paramètres de la demande


|  | Paramètre | Type | Facultatif ? | Description |
| :---: | :---: | :---: | :---: | :--- |
| En-tête HTTP | accessToken | String | Non | Reçu à partir de la fin de l’authentification par jeton d’accès |
| Paramètre de requête | objectId | String | Non | Identificateur représentant l’objet dans le contexte dans lequel les webhooks doivent être créés. Pour l’argument typeobjet = groupe, l’identificateur de son groupe, pour ObjectType = Action, son actionId, pour ObjectType = ActionPackage, son id de package d’action |
| Paramètre de requête | objectType | String | Non | Enum : « groupe » / « Action » / « ActionPackage » |

#### <a name="response-body"></a>Corps de la réponse

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| webhooks | Tableau d’objets JSON | Tableau de webhooks souscrit sur objectId |

#####  <a name="json-structure-for-each-individual-webhook-in-the-array-webhooks"></a>Structure de JSON pour chaque webhook individuel dans le tableau webhooks [-] :

| Paramètre | Type | Description |
| :---: | :---: | :--- |
| id | String | Identificateur Webhook |
| objectId | String | Identificateur d’objet |
| objectType | String | Enum : « groupe » / « Action » / « ActionPackage » |
| events | String] | Liste des événements avec chaque valeur comme « ActionCreated », « ActionResponse », « SurveyCreated », « JobCreated », « SurveyResponse », « JobResponse », « TextMessageCreated », « AttachmentCreated », « Announcement », « MemberAdded », « MemberRemoved », « GroupAdded » » GroupRemoved » |
| callBackUrl | String | URL de rappel à laquelle doivent être notifiés pour les événements auxquels vous êtes abonnés |
| callBackToken | String | Paramètre qui sera envoyé dans l’en-tête HTTP 'jeton de rappel kz' avec chaque rappel effectuée par le WebHook |
| callBackContext | String | Paramètre envoyé dans la charge utile JSON en tant que contexte avec chaque rappel un effectuées par le WebHook |
| validité | String | Validité pour le WebHook actif au format d’origine. |
| Active | Boolean | Valeur True, si l’état de webhook est actif |

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

### <a name="delete-webhook"></a>Supprimer /webhook

    DELETE {endpoint-url}/v1/webhook

#### <a name="request-parameters"></a>Paramètres de la demande
|  | Paramètre | Type | Facultatif ? | Description |
| :---: | :---: | :---: | :---: | :--- |
| En-tête HTTP | accessToken | String | Non | Reçu à partir de la fin de l’authentification par jeton d’accès |
| Paramètre de chemin d’accès | webhookId | String | Non | Identificateur Webhook |

### <a name="put-webhook"></a>Placez /webhook

    PUT {endpoint-url}/v1/webhook/{webhookId}

N’importe quel paramètre pour la webhook peut être mis à jour. Corps de la requête peut contenir des paramètres 1 ou plus, selon vos besoins.

#### <a name="request-parameters"></a>Paramètres de la demande

|  | Paramètre | Type | Facultatif ? | Description |
| :---: | :---: | :---: | :---: | :--- |
| En-tête HTTP | accessToken | String | Non | Reçu à partir de la fin de l’authentification par jeton d’accès |
| Paramètre de chemin d’accès | webhookId | String | Non | Identificateur Webhook |

#### <a name="request-body"></a>Corps de la demande

|  Paramètre | Type | Facultatif ? | Description |
| :---: | :---: | :---: | :--- |
| objectId | String | Oui | Identificateur représentant l’objet dans le contexte dans lequel les webhooks doivent être créés. Pour l’argument typeobjet = groupe, l’identificateur de son groupe, pour ObjectType = Action, son actionId, pour ObjectType = ActionPackage, son id de package d’action |
| objectType | String | Oui | Enum : « groupe » / « Action » / « ActionPackage » |
| eventTypes | Tableau | Oui | Tableau de différents types d’événements, à que vous devez vous inscrire le webhook. Supported events are: "ActionCreated","ActionResponse","SurveyCreated","JobCreated","SurveyResponse","JobResponse","TextMessageCreated","AttachmentCreated","Announcement","MemberAdded","MemberRemoved","GroupAdded","GroupRemoved" |
| callBackUrl | String | Oui | URL HTTPS vers lequel doivent être notifiés pour les événements auxquels vous êtes abonnés |
| callBackToken | String | Oui | Paramètre facultatif vous pouvez définir qui seront envoyées dans l’en-tête HTTP 'jeton de rappel kz' avec chaque rappel effectuée par le WebHook |
| callBackContext | String | Oui | Paramètre facultatif vous pouvez définir qui seront envoyées dans la charge utile JSON en tant que contexte avec chaque rappel un effectuées par le WebHook |
| validité | String | Oui | Validité pour le WebHook actif au format d’origine. Valeur par défaut est de 2 ans |
| Actif | Booléen | Oui | Modifier l’état de webhook actif, si la valeur est true |


#### <a name="sample-request-body"></a>Corps de demande d’exemple

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

## <a name="auto-disable-of-webhooks"></a>Désactivation automatique de Webhooks

Pour améliorer la fiabilité de nos Webhooks, nous avons récemment ajouté la logique de désactivation et de réessayer. Le rappel Url/point de terminaison auprès d’un webhook, si elle est inaccessible ou ne répond pas avec un code d’état autre que 2xx (> = 3xx), puis notre Service essaiera de portée/réessayer il de 6 fois de manière exponentielle dans une plage de 2 jours. 

Si elle échoue encore pour 2 jours, puis le Webhook correspondant sera désactivé et le propriétaire doit mettre à jour avec l’API de /webhook Put avant le début de votre travail. Pour, par exemple

    
    PUT {endpoint-url}/v1/webhook/{subscriptionId}

### <a name="request-body"></a>Corps de la demande :
````javascript
{ 
  "Active": "true" 
} 
````
