# <a name="data-residency-and-go-local-support-in-microsoft-kaizala"></a>Prise en charge des données et de l’accès local dans Microsoft Kaizala

Actuellement, Microsoft Kaizala offre une prise en charge des données régionales par les centres de données en Europe (UE), Asie-Pacifique (APAC), aux États-Unis (É.U.) et en Inde (en). Cela signifie que les clients Kaizala auront des données liées aux [groupes et conversations](https://support.office.com/article/organization-chats-and-groups-in-kaizala-c8a7855c-d232-4914-811c-f6708734dcc3) de l’organisation, telles que les messages, les pièces jointes et les actions Kaizala stockées dans le centre de données de leur région de facturation.

En plus de prendre en charge les objectifs de la résidence des données dans la région, les centres de données de service Kaizala facilitent également le basculement et la récupération d’urgence via les centres de données.

## <a name="global-datacenter-footprint-with-data-residency-support"></a>Encombrement global des centres de données avec prise en charge de la résidence des données

Actuellement, Kaizala possède huit centres de centres (principaux et de sauvegarde) dans trois régions et un pays:

- APAC (Asie-Pacifique à l’exception de l’Inde)-centres de centre de Singapour et Hong Kong
- EMEA (UE, MEA)-centres de centre de Dublin et Amsterdam
- AMER (Nord et Sud-Unis)-centres de redirection dans le Texas et l’Illinois
- Inde (Go-local)-centres de Chennai et Pune

En plus de fournir des services de calcul et de stockage, Kaizala fournit également une prise en charge des données de résidence, un basculement robuste et une prise en charge de la récupération d’urgence aux clients d’entreprise. De plus, ces unités d’étendue contribuent à améliorer les performances de connectivité et de messagerie pour les clients d’entreprise et les clients généraux. 

![Graphique illustrant la résidence des données et les frontières géographiques locales dans Kaizala](Images/data-residency-geo-boundaries.png)

## <a name="how-is-data-stored-in-kaizala"></a>Comment les données sont-elles stockées dans Kaizala

Kaizala stocke les données différemment en fonction des types de données des messages.

- **Conversations, j’aime et commentaires** : tous les messages, les aiment et les données de commentaire appartenant à un groupe d’organisation ou des conversations de l’organisation 1:1 sont stockés dans un service de conversation Office 365 et Azure Powered qui est régionalement lié aux clients, en fonction de leur pays de facturation.
- **Pièces jointes** : toutes les pièces jointes sont localisées en même temps que les messages de conversation dans la même limite de données.
- **Fiches d’action Kaizala** -toutes les données de la carte d’action Kaizala, qui incluent les données de métadonnées, de package d’action et de rapport de réponse, sont colocalisées avec le service de conversation dans la même limite de données.
- L' **appel** étant transitoire, les données d’appel Kaizala ne sont pas stockées dans les centres de données. Toutefois, les journaux d’appels suivent la même résidence des données que les conversations.

### <a name="example"></a>Exemple

Contoso a son pays de facturation Office 365 dans l’UE. Contoso s’est inscrit sur Kaizala en avril 2019 et toutes ses données de base, y compris les conversations, les pièces jointes et les cartes d’action seront stockées au repos exclusivement dans les unités de l’Union européenne (Dublin et Amsterdam).

## <a name="what-is-in-store-in-future"></a>Qu’est-ce que le stockage à venir?

- **Page d’intégration à l’emplacement des données** : pour les entreprises, l’emplacement des données pour les différentes charges de travail d’Office 365 est visible sous le portail d’administration d’Office 365 sous profil Home\Organizational. La possibilité d’intégrer Kaizala à la page d’emplacement des données sur le portail d’administration est à paraître. Regardez cette section pour les mises à jour.
- **Nouveaux centres** de développement: l’équipe Kaizala examine continuellement l’expansion en fonction de la meilleure expérience utilisateur pour les utilisateurs. Si vous avez un cas client, publiez vos questions dans notre [communauté TechNet](https://techcommunity.microsoft.com/t5/Microsoft-Kaizala/ct-p/MicrosoftKaizala).

## <a name="faqs"></a>FAQ

### <a name="what-does-it-mean-for-existing-enterprise-customers"></a>Qu’est-ce que cela signifie pour les clients d’entreprise existants?

Les clients existants en Inde ont déjà leur résidence de données en Inde. Toutefois, les données de tous les clients existants non-Inde continueront à rester dans l’emplacement du groupe (en fonction du code pays du créateur). Toutefois, après le 2019 avril, tous les nouveaux groupes d’organisation et les nouveaux messages de groupes d’organisation ou de conversations existants commencent à suivre la résidence des données en fonction de la région de facturation du client.

### <a name="what-does-it-mean-for-new-enterprise-customers"></a>Qu’est-ce que cela signifie pour les nouveaux clients d’entreprise?

La résidence des données s’applique automatiquement à tous les clients qui s’inscrivent sur Kaizala après le 2019 avril. De plus, la résidence des données sur les cartes d’action doit être applicable aux dernières versions des applications Android ou iOS.
 
### <a name="i-do-have-more-questions-who-do-i-reach-out-to"></a>J’ai plus de questions. Qui dois-je atteindre?

En cas de questions supplémentaires, contactez votre équipe de compte ou notre [communauté TechNet](https://techcommunity.microsoft.com/t5/Microsoft-Kaizala/ct-p/MicrosoftKaizala). En outre, vous pouvez écrire dans [Kaizalafeedback@microsoft.com](mailto:kaizalafeedback@microsoft.com).








