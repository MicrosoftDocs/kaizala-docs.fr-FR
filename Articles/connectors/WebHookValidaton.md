# <a name="callback-url-validation"></a>Validation de l'URL de rappel

Pour vérifier que votre point de terminaison de service webhook est authentique et que nous travaillons, nous allons vérifier votre URL de rappel avant de créer un abonnement.
Pour la vérification, nous vous enverrons un jeton de validation dont vous avez besoin pour nous envoyer vos commentaires dans un délai de 5 secondes. Un aperçu de l'ensemble du processus:

1.  Demandez à Kaizala d'enregistrer votre webhook à l'aide de [post/Webhook](webHooks.md). 
2.  Kaizala génère un jeton de validation et envoie une requête GET à votre webhook avec un paramètre de requête «validationToken».
3.  Votre service est supposé renvoyer le jeton de validation (reçu dans la demande) dans le corps de la réponse en tant que texte brut
4.  Si nous recevons la réponse dans un délai de 5 secondes et que le jeton de validation reçu correspond à celui envoyé à l'étape 2, le webhook sera enregistré, sinon il sera rejeté. 
