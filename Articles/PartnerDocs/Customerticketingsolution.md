# <a name="customer-ticketing-solution-on-kaizala"></a>Solution de ticket de client sur Kaizala
![](Images/Customer%20ticketing%20solution.PNG)
<br>
<br> Nous allons nous pencher sur la façon d'obtenir un système de gestion des tickets de support client sur Kaizala. Au lieu d'envoyer plusieurs messages texte pour donner une mise à jour à l'état du ticket, nous aurions pu simplement disposer d'une carte enrichie qui fournit l'état du ticket. En cas de modification de l'État, la carte peut être mise à jour pour refléter le dernier statut.
<br><br>Pour ce faire, vous trouverez ci-dessous les étapes nécessaires:
<br>1. créer une carte avec une carte de conversation personnalisée basée sur les propriétés définies
<br>2. appeler une API pour envoyer la carte (scénario où le ticket est généré)
<br>3. appeler une API pour mettre à jour la carte (scénario dans lequel l'état du ticket change)
## <a name="building-card-with-custom-chat-card-view"></a>Carte de construction avec affichage de carte de conversation personnalisée
[Kaizala permet d'étendre les fonctionnalités côté client à l'aide d'actions/cartes personnalisées. La documentation Microsoft pour le développement d'une action personnalisée peut être trouvée [ici](https://github.com/MicrosoftDocs/kaizala-docs/blob/master/Articles/Actions/develop.md).]
<br><br>Pour créer une carte avec une carte de conversation personnalisée, nous devons définir le sourceLocation de la vue de la carte de canevas de conversation dans package. JSON. Contrairement à la vue de réponse, la vue de création ou la vue de résultats/résumés, qui sont basées sur html/JS, la carte de conversation prend un schéma déclaratif [en savoir plus [ici](https://github.com/MicrosoftDocs/kaizala-docs/blob/master/Articles/Actions/ChatCanvasCardView.md)].
### <a name="packagejson"></a>Package. JSON
{  <br>"ID": "com. GLS. xyz. Care", <br>«schemaVersion»: 1, <br>"displayName": "support technique", <br>"providerName": "GLS-test", <br>"Icon": "apPicon. png", <br>"version": "1", <br>"minorVersion": "1", <br>"appModel": "AppModel. JSON", <br>"Description": "package pour l'envoi de ticket client [test]", <br>«numérotation»: { <br>«isLocalised»: false, <br>«isPinned»: false <br>},  <br>«Vues»: { <br>«ChatCanvasCardView»: { <br>"sourceLocation": "ChatCardView. JSON", <br>«showReceipts»: true, <br>«showLikes»: false, <br>«showcomments,»: false, <br>«showExpiry»: false, <br>«showFooter»: true, <br>«showHeader»: false, <br>«showFooter»: false, <br>«isResponseEditable»: false <br>}
<br> }
<br>}
### <a name="chatcardviewjson"></a>ChatCardView. JSON
La carte de conversation comporte quatre champs: un codé en dur pour «service clientèle XYZ» et les 3 autres champs provenant de propriétés: CustomerName, ticketnumber et ticketstatus.
<br>{
<br> «schemaVersion»: 2, <br>«schéma»: {
<br> «type»: «conteneur»,
<br> «initialHeight»: 300,
<br> "mise en page": "vertical",
<br> «enfants»: [
<br> {  <br>"type": "Text", <br>«paddingLeft»: 10, <br>«paddingRight»: 10,
<br> «paddingTop»: 10,
<br> «paddingBottom»: 10,
<br> "chaîne": "service clientèle XYZ",
<br> "FontSize": 18,
<br> "fontStyle": "BOLD",
<br> «textColor»: «#ffffff»,
<br> "backgroundColor": "#fcb72d",
<br> "textAlignment": "Center",
<br> «maxNumberOfLines»: 1,
<br> «marginBottom»: 10
<br> },
<br> {
<br> "type": "Text",
<br> «paddingLeft»: 10,
<br> «paddingRight»: 10,
<br> "chaîne": "$ {Form. Properties [CustomerName]. Value}",
<br> "FontSize": 18,
<br> «fontStyle»: «Regular»,
<br> «textColor»: «#000000»,
<br> "backgroundColor": "#ffffff",
<br> "textAlignment": "left",
<br> «maxNumberOfLines»: 5,
<br> «marginBottom»: 10
<br> },
<br> {
<br> "type": "Text",
<br> «paddingLeft»: 10,
<br> «paddingRight»: 10,
<br> "chaîne": "$ {Form. Properties [ticketnumber]. Value}",
<br> "FontSize": 18,
<br> «fontStyle»: «Regular»,
<br> «textColor»: «#000000»,
<br> "backgroundColor": "#ffffff",
<br> "textAlignment": "left",
<br> «maxNumberOfLines»: 2,
<br> «marginBottom»: 10
<br> },
<br> {
<br> "type": "Text",
<br> «paddingLeft»: 10,
<br> «paddingRight»: 10,
<br> "chaîne": "$ {Form. Properties [ticketstatus]. Value}",
<br> "FontSize": 18,
<br> «fontStyle»: «Regular»,
<br> «textColor»: «#000000»,
<br> "backgroundColor": "#ffffff",
<br> "textAlignment": "left",
<br> «maxNumberOfLines»: 2,
<br> «marginBottom»: 10
<br> }
<br> ]
<br> }
<br>}
### <a name="appmodeljson"></a>AppModel. JSON
Créez simplement un AppModel avec le titre et le tableau des questions vides.
<br> {
<br> "title": "support client XYZ",
<br> «questions»: []
<br>}
## <a name="sending-ticket-from-api"></a>Envoi d'un ticket à partir de l'API
Pour envoyer le ticket via l'API, nous utiliserons le point de terminaison actions comme indiqué ci-dessous. Notez le tableau des abonnés, étant donné que nous devons envoyer cet abonnement à un abonné particulier (pour plus d'informations, vous pouvez consulter la rubrique post [Move SMS notifications to Kaizala](https://kaizala007.wordpress.com/2018/02/07/kaizala-subscriber-message/)).
<br>L'exécution de cette API vous donnera le ID et l'actionId. Mettez en cache cet actionId, comme nous l'aurez besoin à l'étape suivante. Dans l'exemple ci-dessous, nous avons défini les propriétés CustomerName, ticketnumber et ticketstatus sur «NAME: John Thomas», «TICKET #: 907050», «État: actif», respectivement.

| Méthode  |      POST    |
|----------|-------------|
|**URL**|{{Endpoint-URL}}/v1/Groups/{{test-Group-ID}}/actions|
|**Corps de la demande**|{<br>ID: "com. GLS. xyz. Care",<br>abonnés: ["{{Subscriber-mobile-Number}}"],<br>sendToAllSubscribers: false,<br>actionBody: {<br>Propriétés: [<br>{<br>nom: «CustomerName»,<br>valeur: "NAME: John Thomas",<br>type: "texte"<br>},<br>{<br>nom: «ticketnumber»,<br>valeur: "TICKET #: 907050",<br>type: "texte"<br>},<br>{<br>nom: «ticketstatus»,<br>valeur: "État: actif",<br>type: "texte"<br>}<br>]<br>}<br>}|
## <a name="updating-the-ticket-status-using-api"></a>Mise à jour de l'état du ticket à l'aide de l'API
Lorsque l'état du ticket change, nous aurions besoin de mettre à jour l'état de la carte qui a été envoyée. Pour cela, nous utiliserons le point de terminaison actions/<<action-id>>/Properties. Dans l'exemple ci-dessous, nous allons mettre à jour l'état du ticket sur résolu. Notez que l'actionId est l'ID de l'action envoyée à l'étape précédente.

| Méthode  |      PPUT    |
|----------|-------------|
|**URL**|{{Endpoint-URL}}/v1/groups/{{test-group-id}}/actions/{{actionId}}|
|**Corps de la demande**|{<br>{<br>"version":-1,<br>«updateProperties»:<br>[<br>{<br>"nom": "ticketstatus",<br>"type": "Text",<br>«valeur»: «État: résolu»<br>}<br>]<br>}|

## <a name="screenshots-of-the-demo"></a>Captures d'écran de la démonstration
### <a name="ticket-sent-from-api"></a>Ticket envoyé par l'API
![](Images/Ticket%20sent%20from%20API.PNG)
### <a name="ticket-after-updating-the-status-from-api"></a>Ticket après la mise à jour de l'État à partir de l'API
![](Images/Ticket%20after%20updating%20the%20status%20from%20API.PNG)
<br>Partage du package [ici](https://drive.google.com/file/d/1gQb1CpYVd8SLnOOH4PCZWPsUeYhdWehB/view), au cas où vous souhaiteriez lui donner une photo. (n'oubliez pas de modifier l'ID de package avant de le télécharger vers Kaizala pour éviter les conflits)

















