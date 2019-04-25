## <a name="kas-client"></a>Client KAS

Le kit de développement logiciel client KAS fournit un pont entre l'interface native de l'application Kaizala (objective-C pour iOS, Java pour Android) et le code JavaScript de votre action Kaizala.

Les API KASClient largement répandues sont divisées en deux catégories:
1.  **API de formulaire**: la carte de conversation de chaque action est associée à un objet de formulaire. Un formulaire définit le comportement de l'action. Pour créer une instance d'action, vous devez initialiser un objet Form, y placer les informations nécessaires, puis l'envoyer en tant que demande à la conversation correspondante. Les participants à la conversation peuvent répondre au formulaire ou consulter le récapitulatif agrégé de toutes les réponses. Ces API ont été créées pour traiter tous les éléments liés aux formulaires. En fonction de différents flux, ceux-ci peuvent être sous-catégorisés:
    *   **API de flux de création**: le fait de cliquer sur l'icône de l'action dans la palette lance son flux de création. À l'aide de ces API, vous pouvez initialiser un objet Form, le manipuler et l'envoyer en tant que requête.
    *   **API de flux de réponse**: le recours au bouton répondre d'une carte d'action lance son flux de réponse. À l'aide de ces API, vous pouvez obtenir l'objet de formulaire associé, toutes les réponses précédentes et envoyer une nouvelle réponse.
    *   **API de flux de résumé**: le recours au bouton Résumé d'une carte d'action lance son flux de synthèse. À l'aide de ces API, vous pouvez obtenir l'objet de formulaire associé, toutes les réponses agrégées par les participants, et choisir de fermer le formulaire afin que les réponses supplémentaires ne soient pas autorisées.
    
2.  **API d'application**: il s'agit d'API qui peuvent être utilisées pour interagir avec l'interface native du client Kaizala et récupérer les informations nécessaires. Cela inclut les API génériques, comme afficher le sélecteur de contacts, le sélecteur d'images, l'emplacement actuel de l'appareil, les paramètres régionaux de l'application, etc. Ces API peuvent être utilisées dans n'importe quel flux mentionné ci-dessus.

Vous pouvez télécharger le fichier JavaScript KASClient actuel à partir de [cet emplacement](https://manage.kaiza.la/MiniApps/DownloadSDK) .

## <a name="api-reference"></a>Référence de l'API

*   [API de flux de création de formulaire](generated/modules/kasclient.form.md#creation)
*   [API de flux de réponse de formulaire](generated/modules/kasclient.form.md#response)
*   [API de flux de synthèse de formulaire](generated/modules/kasclient.form.md#summary)
*   [API d'application](generated/modules/kasclient.app.md)

## <a name="object-reference"></a>Référence d'objet

Les références de tous les objets du kit de développement logiciel (SDK) sont disponibles [ici](objects.md).
