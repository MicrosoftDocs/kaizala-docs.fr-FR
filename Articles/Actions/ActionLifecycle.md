# <a name="action-lifecycle"></a>Action de cycle de vie

Une Action peut prendre 5 états :

* **Brouillon** - Action est téléchargé avec succès. Il est visible uniquement par le créateur de l’Action et organisation Admin(s) sur le portail de gestion Kaizala. Il ne peut pas être ajouté aux groupes
* **Intermédiaire** - Action dans un état intermédiaire peuvent être testées (avant le déploiement) dans les groupes pour lesquels créateur d’Action est un administrateur. Il est visible uniquement par le créateur de l’Action et Organisation Admin(s) sur le portail de gestion Kaizala
* **Active** - après une version d’une Action est mis en place, il peut être activé. Dans un état actif, il est disponible pour tous les membres de l’Organisation pour l’ajouter dans leurs groupes respectifs sur le portail de gestion Kaizala
* Inactif peut être établie à **inactif/Inactive** - Action dans un état actif. Dans ce cas, concerné package Action n’est pas disponible à d’autres membres de l’organisation pour l’ajouter à leurs groupes respectifs. Application Kaizala, il peut toujours être utilisé par les utilisateurs dans les groupes dans laquelle cette Action a déjà été ajoutée
* **Suppression** - si une version d’une Action est explicitement supprimée ou remplacée par une autre version, elle est déplacée vers l’état de suppression. Sur les applications Kaizala, ces packages ne sera pas disponibles pour l’utilisateur à utiliser
