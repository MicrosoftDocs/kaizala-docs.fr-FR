# <a name="kaizala-actions"></a>Actions Kaizala

## <a name="overview"></a>Vue d'ensemble
Les actions Kaizala sont des «unités de travail» qui aident les utilisateurs à effectuer des tâches dans un contexte de conversation à l'intérieur de Kaizala. Certaines de ces actions, telles que Job, Survey, Poll, etc., sont fournies en tout ou partie. Ces actions peuvent être découvertes dans l'application Kaizala et peuvent être appelées dans un contexte de conversation à partir de la palette d'actions. 

Le [portail de gestion Kaizala](https://manage.kaiza.la) est la passerelle pour tout développement, test, approbation ou publication de nouvelles actions Kaizala.

La possibilité d'appeler ou de créer une nouvelle instance d'une action peut être étendue uniquement aux membres d'un groupe spécifique. La prise en charge de la publication sur les membres de tous les groupes mappés à une organisation via le portail de gestion Kaizala bientôt disponible.

Toutes les actions qui sont publiées sur un ensemble d'utilisateurs peuvent être appelées par elles sur n'importe quelle conversation à laquelle ils appartiennent. Cela inclut les conversations 1:1, les groupes privés ou les groupes mappés à une organisation.

Une action Kaizala contient actuellement quatre vues différentes pouvant être définies:

* Une vue de création lorsqu'une action est appelée à partir de la palette
* Affichage de carte qui apparaît dans la zone de conversation lors de l'envoi d'une instance de l'action
* Une vue de répondeur permettant aux utilisateurs de répondre à l'action Kaizala
* Affichage de synthèse pour afficher les réponses agrégées

Vous pouvez créer de nouvelles actions Kaizala qui exploitent le réseau des personnes de Kaizala et des fonctionnalités mobiles pour créer des expériences attrayantes de la manière suivante:

* **Concevoir une nouvelle action Kaizala via le portail de gestion Kaizala** : vous pouvez concevoir une action Kaizala personnalisée via l'interface du concepteur d'actions en utilisant les modèles d'action existants.
* **Développer un nouveau package d'actions Kaizala** : vous pouvez créer de nouvelles actions Kaizala complexes qui fournissent des fonctionnalités personnalisées à l'aide de technologies Web telles que HTML, CSS et JavaScript. Suivez les liens ci-dessous pour en savoir plus sur les différentes étapes du développement d'une action Kaizala.
    *   [Anatomie d'un package d'action Kaizala](anatomy.md)
    *   [Prise en main](get_started.md)
    *   [Développer](develop.md)
    *   [Test et déBogage](test.md)
    *   [Publish](publish.md)

Toutes les actions Kaizala doivent confirmer que les [stratégies de validation](validation.md) peuvent être publiées sur les clients Kaizala.

## <a name="build-your-first-kaizala-action"></a>Créer votre première action Kaizala

Vous pouvez essayer de créer votre première action Kaizala en suivant notre [didacticiel](tutorial.md) simple.

## <a name="download-sample-action-packages"></a>Télécharger des packages d'actions d'exemple

Vous pouvez télécharger des packages d'actions d'exemple à partir de [ici](https://manage.kaiza.la/MiniApps/DownloadSDK)
