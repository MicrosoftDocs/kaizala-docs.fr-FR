# <a name="breaking-changes-communication"></a>Annulation de communication des modifications

S’abonner à [Se connecter pour les développeurs de Kaizala](https://join.kaiza.la/g/jwoUnTyHR_Kgrd_GuDDc1w) à partir de votre application mobile pour recevoir les dernières modifications communication dans la plateforme de développement Kaizala.

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

## <a name="managed-public-groups-can-only-be-created-using-tenant-level-user-token-in-create-group-api"></a>Des groupes publics gérés ne peuvent être créés à l’aide du jeton de l’utilisateur au niveau du client dans « créer un groupe' API

||Détails|
|--|--|
|**Zone d’impact**| API |
|**Résumé de l’impact**| Groupe Public antérieur a été autorisée à être créée sans qu’il est mappée à une organisation. Désormais, groupes publics gérés peuvent être créés par le biais de «[créer le groupe](https://docs.microsoft.com/en-us/kaizala/connectors/groups#groups)», uniquement lorsque le jeton de l’utilisateur au niveau du client est utilisé dans l’API. Lecture [ici](connectors/UserToken.md) plus pour le processus à générer le jeton de l’utilisateur |
|**Date de Communication**|06-06-2018|
|**Date de l’Impact**|22-06-2018|

## <a name="validation-of-registered-callbackurl-when-webhook-is-created"></a>Validation de callBackUrl inscrit lorsque webhook est créé.

||Détails|
|--|--|
|**Zone d’impact**| Webhooks |
|**Résumé de l’impact**| Si vous continuez, lors de la création de Webhook ([POST /webhook](https://docs.microsoft.com/en-us/kaizala/connectors/webhooks#webhook)), callBackUrl enregistré est validé. Après une validation réussie, un webhook serait créée |
|**Action requise**| Ancienne Webhook abonnements continueront de fonctionner au-delà de la Date de l’Impact. Nouvelles demandes d’abonnement Webhook nécessite que vous vérifiez votre service suit le processus mentionné [ici](connectors/WebHookValidaton.md) |
|**Date de Communication**|09-05-2018|
|**Date de l’Impact**|15-06-2018|

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


