---
ms.openlocfilehash: de0df75d7a62fda9ea6ff5625fbef94774069cfd
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28727718"
---
## <a name="kas-client"></a>KAS Client

SDK de Client KAS fournit un pont entre l’interface de l’application Kaizala native (Objective-C pour iOS, Java pour Android) et javascript de l’Action de votre Kaizala.

KASClient APIs sont divisées en deux catégories :
1.  **API de formulaire**: carte de conversation de chaque Action associée à un objet form. Un formulaire définit le comportement de l’Action. Pour créer une instance d’Action que vous avez besoin d’initialisation d’un objet form, insérer les informations nécessaires, puis l’envoyer en tant que demande à la conversation respectif. Participants à la conversation peuvent répondre à l’écran ou afficher le résumé agrégé de toutes les réponses. Ces API ont été créés pour faire face à tout ce qui concerne les formulaires. En fonction de différents flux, qui peuvent plus être sous-fonctionnalités classés dans :
    *   **Flux de création API**: fait d’appuyer sur l’icône de l’Action dans la palette lance le flux de sa création. À l’aide de ces API, vous pouvez initialiser un objet form, manipuler et envoyer en tant que demande.
    *   **Flux de réponse API**: fait d’appuyer sur le bouton répondre d’une carte Action lance le flux de réponse. À l’aide de ces API, vous pouvez obtenir l’objet de formulaire, toutes les réponses précédentes et soumettre une nouvelle réponse.
    *   **Résumé des API de flux**: fait d’appuyer sur le bouton de synthèse d’une carte Action lance le flux de synthèse. À l’aide de ces API, vous pouvez obtenir l’objet de formulaire, toutes les réponses agrégées par les participants et choisissez Fermer le formulaire afin que les autres réponses ne sont pas autorisés.
    
2.  **API d’application**: il s’agit des API qui peut servir à interagir avec l’interface native du client Kaizala et récupérer les informations nécessaires. Cela inclut des API génériques, comme afficher le sélecteur de contact, sélecteur d’images, emplacement actuel de l’unité get, aux paramètres régionaux de l’application, etc.. Ces API peuvent être utilisées dans un des flux mentionnés ci-dessus.

Vous pouvez télécharger le fichier KASClient Javascript actuel à partir [d’ici](https://manage.kaiza.la/MiniApps/DownloadSDK)

## <a name="api-reference"></a>Référence API

*   [Flux de création de formulaire API](generated/modules/kasclient.form.md#creation)
*   [Formulaire de flux de réponse API](generated/modules/kasclient.form.md#response)
*   [API de flux de résumé de formulaire](generated/modules/kasclient.form.md#summary)
*   [API d’application](generated/modules/kasclient.app.md)

## <a name="object-reference"></a>Référence d’objet

Les références de tous les objets dans le SDK sont disponibles [ici](objects.md).
