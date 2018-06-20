# <a name="load-external-urls-within-your-action"></a><span data-ttu-id="689f5-101">Charger des URL externes au sein de votre Action</span><span class="sxs-lookup"><span data-stu-id="689f5-101">Load external urls within your Action</span></span>

<span data-ttu-id="689f5-102">Kaizala permet aux développeurs Action charger URL https au sein d’une Action.</span><span class="sxs-lookup"><span data-stu-id="689f5-102">Kaizala enables Action developers to load https urls within an Action.</span></span> <span data-ttu-id="689f5-103">Dans les scénarios où Action développeur souhaite ouvrir une page Web, ils peuvent utiliser « externalUrls » pour charger des pages Web dans les vues IMMERSIFS.</span><span class="sxs-lookup"><span data-stu-id="689f5-103">In scenarios, where Action developer wants to open a webpage, they can use ‘externalUrls’ to load webpages within immersive views.</span></span>
<span data-ttu-id="689f5-104">Pour activer le chargement de page Web au sein d’une Action, développeur Action doit d’autorisation les URL et les ajouter dans le fichier Package.json pour l’Action.</span><span class="sxs-lookup"><span data-stu-id="689f5-104">In order to enable loading of webpage within an Action, Action developer needs to whitelist the urls and add them in the Package.json file for the Action.</span></span>

## <a name="whitelisting-external-url"></a><span data-ttu-id="689f5-105">Création de listes autorisées des URL externe</span><span class="sxs-lookup"><span data-stu-id="689f5-105">Whitelisting external URL</span></span>

<span data-ttu-id="689f5-106">Dans votre fichier 'Package.json' pour votre Action</span><span class="sxs-lookup"><span data-stu-id="689f5-106">In your ‘Package.json’ file for your Action</span></span>
* <span data-ttu-id="689f5-107">Ajoutez une nouvelle balise **'externalUrls'**.</span><span class="sxs-lookup"><span data-stu-id="689f5-107">Add a new tag **‘externalUrls’**.</span></span>
* <span data-ttu-id="689f5-108">Ajouter la liste d’URL que vous souhaitez à la liste d’autorisation dans cette balise.</span><span class="sxs-lookup"><span data-stu-id="689f5-108">Add list of URLs which you want to whitelist in this tag.</span></span> <span data-ttu-id="689f5-109">Vous trouverez la partie de l’exemple de code ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="689f5-109">Please find the part of the sample code below.</span></span> 
```
  "externalUrls": [
    { "url" : "https://www.example-url.com" },
    { "url" : "https://another-example-url.com" },
  ],
```
* <span data-ttu-id="689f5-110">Chaque url doit être une url complète valide.</span><span class="sxs-lookup"><span data-stu-id="689f5-110">Each url should be a valid complete url.</span></span>
* <span data-ttu-id="689f5-111">Chaque url doit être une url https.</span><span class="sxs-lookup"><span data-stu-id="689f5-111">Each url should be an https url.</span></span>

