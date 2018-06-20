# <a name="load-external-urls-within-your-action"></a>Charger des URL externes au sein de votre Action

Kaizala permet aux développeurs Action charger URL https au sein d’une Action. Dans les scénarios où Action développeur souhaite ouvrir une page Web, ils peuvent utiliser « externalUrls » pour charger des pages Web dans les vues IMMERSIFS.
Pour activer le chargement de page Web au sein d’une Action, développeur Action doit d’autorisation les URL et les ajouter dans le fichier Package.json pour l’Action.

## <a name="whitelisting-external-url"></a>Création de listes autorisées des URL externe

Dans votre fichier 'Package.json' pour votre Action
* Ajoutez une nouvelle balise **'externalUrls'**.
* Ajouter la liste d’URL que vous souhaitez à la liste d’autorisation dans cette balise. Vous trouverez la partie de l’exemple de code ci-dessous. 
```
  "externalUrls": [
    { "url" : "https://www.example-url.com" },
    { "url" : "https://another-example-url.com" },
  ],
```
* Chaque url doit être une url complète valide.
* Chaque url doit être une url https.

