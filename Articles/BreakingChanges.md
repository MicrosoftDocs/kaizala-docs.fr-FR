# <a name="breaking-changes-communication"></a>Communication avec interruption des modifications

S'abonner au [développeur Kaizala Connectez-vous](https://join.kaiza.la/g/jwoUnTyHR_Kgrd_GuDDc1w) à partir de votre application mobile pour recevoir la communication avec des modifications critiques dans la plateforme de développement Kaizala.

<!---

## Deprecating Mobile Number data from Kaizala APIs & Webhooks
||Details|
|--|--|
|**Impact Area**| APIs & Webhooks |
|**Impact Summary**|Kaizala APIs & Webhooks will stop returning Mobile Number as part of reponse. It will return Kaizala userIDs, which can be used to identify unique users. List of APIs & Webhook impacted:<br> <ol><li></li>|
|**Requires Action**|3rd party developers should make necessary changes to avoid break in their solutions. During the time period between 'Date of communication' & 'Date of Impact', Kaizala APIs will return both Mobile numbers and User IDs|
|**Date of Communication**| 18-04-2018 |
|**Date of Impact**| 15-05-2018|

-->

## <a name="managed-public-groups-can-only-be-created-using-tenant-level-user-token-in-create-group-api"></a>Les groupes publics gérés peuvent uniquement être créés à l'aide du jeton d'utilisateur au niveau du client dans l'API «créer un groupe»

||Détails|
|--|--|
|**Zone d'impact**| API |
|**Synthèse des impacts**| Un groupe public antérieur a été autorisé à être créé sans être mappé à une organisation. Désormais, les groupes publics gérés peuvent être créés via «[créer un groupe](https://docs.microsoft.com/en-us/kaizala/connectors/groups#groups)», uniquement lorsque le jeton de l'utilisateur au niveau du client est utilisé dans l'API. En [](connectors/UserToken.md) savoir plus pour le processus de génération du jeton d'utilisateur |
|**Date de communication**|06-06-2018|
|**Date de l'impact**|22-06-2018|

## <a name="validation-of-registered-callbackurl-when-webhook-is-created"></a>Validation des callBackUrl enregistrées lors de la création du webhook

||Détails|
|--|--|
|**Zone d'impact**| Webhooks |
|**Synthèse des impacts**| À l'avance, lors de la création du webhook ([post/webhook](https://docs.microsoft.com/en-us/kaizala/connectors/webhooks#webhook)), les callBackUrl inscrits seront validés. Une fois la validation réussie, un webhook est créé. |
|**Action requise**| Les abonnements de webhook plus anciens continueront de fonctionner au-delà de la date d'impact. Les nouvelles demandes d'abonnement webhook vous obligent à vous assurer que votre service suit le processus mentionné [ici](connectors/WebHookValidaton.md) . |
|**Date de communication**|09-05-2018|
|**Date de l'impact**|15-06-2018|

<!---

## Webhook subscription will be cancelled, if 10 consecutive failures are received

||Details|
|--|--|
|**Impact Area**| Webhooks |
|**Impact Summary**| Subscription of WebHooks would be suspended, if Kaizala server doesn't receive success for 10 consecutive attempts. Developer will get communication regarding the same on Kaizala Developer Connect. Click here to join [Kaizala Developer Connect]()|
|**Required Action**||
|**Date of Communication**| 18-04-2018 |
|**Date of Impact**| 01-06-2018 |
-->


