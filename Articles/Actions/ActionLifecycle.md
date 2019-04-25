# <a name="action-lifecycle"></a>Cycle de vie des actions

Une action peut avoir 5 États:

* **Draft** -action est téléchargée avec succès. Il n'est visible que par le créateur d'actions et les administrateurs d'organisation sur le portail de gestion Kaizala. Il ne peut pas être ajouté à des groupes
* **Intermédiaire** -l'action dans l'état intermédiaire peut être testée (avant le déploiement) dans des groupes pour lesquels le créateur d'action est un administrateur. Il n'est visible que pour le créateur d'action et les administrateurs d'organisation sur le portail de gestion Kaizala
* **Actif** : après qu'une version d'une action est intermédiaire, elle peut être activée. Dans l'état actif, il est disponible pour tous les membres de l'Organisation pour l'ajouter à ses groupes sur le portail de gestion Kaizala
* **Inactive** -l'état actif peut être inactif. Dans cet État, le package d'action concerné n'est pas accessible aux autres membres de l'Organisation pour l'ajouter à leurs groupes. Sur l'application Kaizala, elle peut toujours être utilisée par les utilisateurs dans les groupes dans lesquels cette action est déjà ajoutée.
* **Supprimé** : si une version d'une action est explicitement supprimée ou remplacée par une autre version, elle passe à l'état supprimé. Dans les applications Kaizala, ces packages ne pourront pas être utilisés par l'utilisateur.
