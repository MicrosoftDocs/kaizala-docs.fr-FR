# <a name="kaizala-actions"></a>Actions Kaizala

## <a name="overview"></a>Vue d'ensemble
Actions Kaizala sont base « unités de travail » qui permettent aux utilisateurs d’obtenir leur travail dans un contexte à l’intérieur de Kaizala conversationnel. Certaines de ces Actions comme tâche, enquête, sondage, etc. sont expédié out-de-the-box. Ces Actions peuvent être découverts au sein de l’application Kaizala et peuvent être appelées dans une conversation à partir de la Palette de l’Action. [En savoir plus](https://support.office.com/en-us/article/Kaizala-Actions-1EACC59A-DD14-43E9-B6B0-3C78773D5496).

Bien que les besoins de chaque organisation varient et ils nécessiterait fonctionnalités seraient très différentes de besoins de toute autre organisation. Par conséquent, Kaizala permet le développement d’Actions personnalisées Kaizala qui peuvent être effectuées par des développeurs tiers 3e. Ces Actions personnalisées peuvent être déployées sur un groupe, mappé au sein d’un contexte d’organisation.</br>

Toutes les Actions qui sont publiées sur un ensemble d’utilisateurs peuvent être appelées par leur Action avait été ajoutée à tous les groupes. 

> **Remarque :** Actions personnalisées peuvent uniquement être ajoutées aux groupes de l’organisation.

> **Remarque :** [Portail de gestion Kaizala](https://manage.kaiza.la) est la passerelle pour tout développement, test et publication de nouvelles Actions Kaizala.

## <a name="understanding-kaizala-action"></a>Présentation Kaizala Action

Une Action Kaizala contient actuellement quatre différentes vues qui peuvent être définis comme indiqué ci-dessous :

* **Mode Création** lorsqu’une Action est appelée à partir de la palette
* Une **vue de carte** qui apparaît sur la zone de conversation lorsqu’une instance de l’Action est envoyé
* Une **vue répondeur** pour répondre à l’Action Kaizala
* Un **affichage de synthèse** pour afficher les réponses agrégées

Par exemple, dans Out-of-Box(OOB) Kaizala enquête Action :

| Vue | Exemple de vue dans Action d’enquête prêtes à l’emploi |
|------|----------------------------------|
| Mode Création| ![](../images/CreationView.png)|
| Affichage de carte |![](../images/Chatcard.png) |
| Vue répondeur |![](../images/ResponseView.png) |
| Affichage de synthèse |![](../images/SummaryView.png) |

Dans Actions personnalisées, vous pouvez créer des affichages personnalisés qui correspondent aux au-dessus de vues.

## <a name="create-a-new-kaizala-action"></a>Créer une nouvelle Action Kaizala
Vous pouvez créer de nouvelles Actions Kaizala qui tirent parti de réseau de personnes de Kaizala et les fonctionnalités mobiles pour créer des expériences de la manière suivante :

* **Concevoir** une nouvelle Action Kaizala via le portail de gestion Kaizala - vous pouvez créer une Action personnalisée de Kaizala par le biais de l’interface du Concepteur d’Action en s’appuyant sur les modèles d’Action existantes. [En savoir plus](https://support.office.com/en-us/article/Kaizala-Actions-1eacc59a-dd14-43e9-b6b0-3c78773d5496?ui=en-US&rs=en-US&ad=US)
* **Développer** une nouvelle Action Kaizala - vous pouvez créer des Actions Kaizala nouveau complexes qui fournissent des fonctionnalités personnalisées à l’aide de technologies web tels que HTML, CSS et JavaScript. Suivez les liens ci-dessous pour en savoir plus sur les différentes étapes du développement d’une Action Kaizala.
    *   [Anatomie d’un package de l’Action Kaizala](anatomy.md)
    *   [Mise en route](get_started.md)
    *   [Développer](develop.md)
    *   [Publier](publish.md)

Toutes les Actions Kaizala doivent respecter les [instructions](validation.md) pour pouvoir être publiés sur les clients Kaizala.

## <a name="build-your-first-kaizala-action"></a>Créer votre première Action Kaizala

Vous pouvez essayer de création de votre première Action Kaizala en suivant notre simple [didacticiel](tutorial.md)

## <a name="download-sample-action-packages"></a>Téléchargez des exemples de Packages de Action

*  [Exemples d’Actions](https://manage.kaiza.la/MiniApps/DownloadSDK)
