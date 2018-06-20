# <a name="callback-url-validation"></a>Validation des URL de rappel

Pour vérifier que votre point de terminaison de service webhook est authentique et qu’elle fonctionne nous allons maintenant vérifier votre URL de rappel avant de créer l’abonnement.
Pour la vérification, nous vous enverrons un jeton de validation dont vous aurez besoin pour nous envoyer dans les 5 secondes. Examinez l’ensemble du processus :

1.  Demander Kaizala pour inscrire votre webhook à l’aide de [POST /Webhook](webHooks.md). 
2.  Kaizala génère un jeton de validation et envoyer une demande GET à votre webhook avec un paramètre de requête « validationToken ».
3.  Votre service est censé pour retourner le jeton de validation (reçu dans la demande) dans le corps de réponse comme un texte brut
4.  Si nous recevoir la réponse dans les 5 secondes et la validation jeton reçu correspond à celui envoyé à l’étape 2, que webhook sera enregistré avec succès, sinon il sera rejeté. 
