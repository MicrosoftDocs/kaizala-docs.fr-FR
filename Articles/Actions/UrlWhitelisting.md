# <a name="load-external-urls-within-your-action"></a><span data-ttu-id="13b40-101">Charger les URL externes dans votre action</span><span class="sxs-lookup"><span data-stu-id="13b40-101">Load external urls within your Action</span></span>

<span data-ttu-id="13b40-102">Kaizala permet aux développeurs d'actions de charger les URL HTTPS au sein d'une action.</span><span class="sxs-lookup"><span data-stu-id="13b40-102">Kaizala enables Action developers to load https urls within an Action.</span></span> <span data-ttu-id="13b40-103">Dans les scénarios où les développeurs d'actions veulent ouvrir une page Web, ils peuvent utiliser «externalUrls» pour charger des pages Web au sein d'affichages immersifs.</span><span class="sxs-lookup"><span data-stu-id="13b40-103">In scenarios, where Action developer wants to open a webpage, they can use ‘externalUrls’ to load webpages within immersive views.</span></span>
<span data-ttu-id="13b40-104">Pour activer le chargement de la page Web au sein d'une action, le développeur d'actions doit utiliser les URL de la liste blanche et les ajouter dans le fichier Package. JSON pour l'action.</span><span class="sxs-lookup"><span data-stu-id="13b40-104">In order to enable loading of webpage within an Action, Action developer needs to whitelist the urls and add them in the Package.json file for the Action.</span></span>

## <a name="whitelisting-external-url"></a><span data-ttu-id="13b40-105">URL externe de liste d'adresses</span><span class="sxs-lookup"><span data-stu-id="13b40-105">Whitelisting external URL</span></span>

<span data-ttu-id="13b40-106">Dans le fichier «Package. JSON» pour votre action</span><span class="sxs-lookup"><span data-stu-id="13b40-106">In your ‘Package.json’ file for your Action</span></span>
* <span data-ttu-id="13b40-107">Ajoutez une nouvelle balise **«externalUrls»**.</span><span class="sxs-lookup"><span data-stu-id="13b40-107">Add a new tag **‘externalUrls’**.</span></span>
* <span data-ttu-id="13b40-108">Ajoutez la liste des URL que vous souhaitez autoriser dans cette balise.</span><span class="sxs-lookup"><span data-stu-id="13b40-108">Add list of URLs which you want to whitelist in this tag.</span></span> <span data-ttu-id="13b40-109">Recherchez la partie de l'exemple de code ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="13b40-109">Please find the part of the sample code below.</span></span> 
```
  "externalUrls": [
    { "url" : "https://www.example-url.com" },
    { "url" : "https://another-example-url.com" },
  ],
```
* <span data-ttu-id="13b40-110">Chaque URL doit être une URL complète valide.</span><span class="sxs-lookup"><span data-stu-id="13b40-110">Each url should be a valid complete url.</span></span>
* <span data-ttu-id="13b40-111">Chaque URL doit être une URL HTTPS.</span><span class="sxs-lookup"><span data-stu-id="13b40-111">Each url should be an https url.</span></span>

