# <a name="load-external-urls-within-your-action"></a>Charger les URL externes dans votre action

Kaizala permet aux développeurs d'actions de charger les URL HTTPS au sein d'une action. Dans les scénarios où les développeurs d'actions veulent ouvrir une page Web, ils peuvent utiliser «externalUrls» pour charger des pages Web au sein d'affichages immersifs.
Pour activer le chargement de la page Web au sein d'une action, le développeur d'actions doit utiliser les URL de la liste blanche et les ajouter dans le fichier Package. JSON pour l'action.

## <a name="whitelisting-external-url"></a>URL externe de liste d'adresses

Dans le fichier «Package. JSON» pour votre action
* Ajoutez une nouvelle balise **«externalUrls»**.
* Ajoutez la liste des URL que vous souhaitez autoriser dans cette balise. Recherchez la partie de l'exemple de code ci-dessous. 
```
  "externalUrls": [
    { "url" : "https://www.example-url.com" },
    { "url" : "https://another-example-url.com" },
  ],
```
* Chaque URL doit être une URL complète valide.
* Chaque URL doit être une URL HTTPS.

