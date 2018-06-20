# <a name="customer-ticketing-solution-on-kaizala"></a>Solution de création de tickets sur Kaizala de client
![](Images/Customer%20ticketing%20solution.PNG)
<br>
<br> Dans ce cas, nous vous explorez comment obtenir un client prend en charge le système de gestion de ticket sur Kaizala. Au lieu d’envoyer des messages texte plusieurs pour attribuer une mise à jour sur le statut du ticket, nous aurions pu simplement une carte riche qui fournit l’état de ticket. Et, lorsqu’il existe un changement d’état, la carte peut être mis à jour pour refléter l’état le plus récent.
<br><br>Pour ce faire, vous trouverez ci-dessous les étapes qui seraient nécessaires :
<br>1. créer une carte de carte de conversation personnalisée en fonction des propriétés définies
<br>2. appeler une API pour envoyer la carte (scénario où ticket est déclenché)
<br>3. appeler une API pour mettre à jour de la carte (scénario où le statut du ticket change)
## <a name="building-card-with-custom-chat-card-view"></a>Carte de construction avec affichage de carte de messagerie instantanée
[Kaizala permet d’étendre côté client à l’aide d’actions personnalisées / cartes. Documentation Microsoft pour le développement d’une action personnalisée qui se trouvent [ici](https://github.com/MicrosoftDocs/kaizala-docs/blob/master/Articles/Actions/develop.md).]
<br><br>Pour créer une carte de carte de messagerie instantanée, nous vous devrez définir la sourceLocation de l’affichage de carte de zone de conversation dans package.json. Contrairement à la réponse un affichage Création ou résultats / affichage de synthèse qui sont html / JS en, la carte de conversation prend un schéma déclaratif [plus d’informations [ici](https://github.com/MicrosoftDocs/kaizala-docs/blob/master/Articles/Actions/ChatCanvasCardView.md)].
### <a name="packagejson"></a>package.json
{  <br>« id » : « com.gls.xyz.care », <br>« Version » : 1, <br>« displayName » : « Service clientèle », <br>« providerName » : « Test-GLS », <br>« icône » : « AppIcon.png », <br>« version » : « 1 » <br>« minorVersion » : « 1 » <br>« appModel » : « AppModel.json », <br>« description » : « Package pour l’envoi de ticket client [test] », <br>« compose » : { <br>« isLocalised » : false <br>« isPinned » : false <br>},  <br>« affichages » : { <br>« ChatCanvasCardView » : { <br>« sourceLocation » : « ChatCardView.json », <br>« showReceipts » : true <br>« showLikes » : false <br>« showComments » : false <br>« showExpiry » : false <br>« showFooter » : true <br>« showHeader » : false <br>« showFooter » : false <br>« isResponseEditable » : false <br>}
<br> }
<br>}
### <a name="chatcardviewjson"></a>ChatCardView.json
La carte de conversation ici comporte quatre champs : 1 codée en dur « XYZ clientèle » et les autres 3 champs chargées à partir des propriétés : nom de client, ticketnumber et ticketstatus.
<br>{
<br> « Version » : 2, <br>« schéma » : {
<br> « type » : « conteneur »,
<br> « initialHeight » : 300,
<br> « présentation » : « vertical »
<br> « enfants » : [
<br> {  <br>« type » : « texte », <br>« paddingLeft » : 10, <br>« paddingRight » : 10,
<br> « paddingTop » : 10,
<br> « paddingBottom » : 10,
<br> « chaîne » : « XYZ clientèle »,
<br> « fontSize » : 18,
<br> « fontStyle » : « gras »
<br> « textColor » : « #ffffff »,
<br> « backgroundColor » : « #fcb72d »,
<br> « textAlignment » : « centre »,
<br> « maxNumberOfLines » : 1,
<br> « marginBottom » : 10
<br> },
<br> {
<br> « type » : « texte »,
<br> « paddingLeft » : 10,
<br> « paddingRight » : 10,
<br> « string":"${Form.properties[customername].value} »
<br> « fontSize » : 18,
<br> « fontStyle » : « normal »,
<br> « textColor » : « #000000 »
<br> « backgroundColor » : « #ffffff »,
<br> « textAlignment » : « left »,
<br> « maxNumberOfLines » : 5,
<br> « marginBottom » : 10
<br> },
<br> {
<br> « type » : « texte »,
<br> « paddingLeft » : 10,
<br> « paddingRight » : 10,
<br> « string":"${Form.properties[ticketnumber].value} »
<br> « fontSize » : 18,
<br> « fontStyle » : « normal »,
<br> « textColor » : « #000000 »
<br> « backgroundColor » : « #ffffff »,
<br> « textAlignment » : « left »,
<br> « maxNumberOfLines » : 2,
<br> « marginBottom » : 10
<br> },
<br> {
<br> « type » : « texte »,
<br> « paddingLeft » : 10,
<br> « paddingRight » : 10,
<br> « string":"${Form.properties[ticketstatus].value} »
<br> « fontSize » : 18,
<br> « fontStyle » : « normal »,
<br> « textColor » : « #000000 »
<br> « backgroundColor » : « #ffffff »,
<br> « textAlignment » : « left »,
<br> « maxNumberOfLines » : 2,
<br> « marginBottom » : 10
<br> }
<br> ]
<br> }
<br>}
### <a name="appmodeljson"></a>AppModel.json
Créez simplement un AppModel avec le titre et un tableau vide de questions.
<br> {
<br> « title » : « XYZ service clientèle »,
<br> « questions » :]
<br>}
## <a name="sending-ticket-from-api"></a>Envoi de ticket à partir d’API
Pour envoyer le ticket via l’API, nous vous pourriez utiliser le point de terminaison actions comme indiqué ci-dessous. Notez la baie abonnés, car nous devons envoyer ce ciblé pour l’abonné spécifique (pour plus d’informations, vous pouvez vous reporter le billet de blog [notifications SMS déplacer Kaizala](https://kaizala007.wordpress.com/2018/02/07/kaizala-subscriber-message/)).
<br>L’exécution de cette API permet d’obtenir les referenceId actionId. Mettre en cache cette actionId car nous sera nécessaire à l’étape suivante. Dans le sous exemple, nous avons défini le nom client, les propriétés ticketnumber et ticketstatus sur « Nom : John Thomas », de « TICKET #: 907050", « Actif : état » respectivement.

| Méthode  |      Publier    |
|----------|-------------|
|**URL**|/ v1/groupes {{-url de terminaison}} / {{test-group-id}} / actions|
|**Corps de la demande**|{<br>ID:"com.GLS.xyz.Care »,<br>les abonnés : [« {{abonné-mobile-nombre}} »],<br>sendToAllSubscribers:false,<br>actionBody : {<br>propriétés : [<br>{<br>nom : nom « client »,<br>valeur : « nom : John Thomas »,<br>type : « Texte »<br>},<br>{<br>nom : « ticketnumber »,<br>valeur : « TICKET #: 907050″,<br>type : « Texte »<br>},<br>{<br>nom : « ticketstatus »,<br>valeur : « état : ACTIVE »,<br>type : « Texte »<br>}<br>]<br>}<br>}|
## <a name="updating-the-ticket-status-using-api"></a>Mise à jour le statut du ticket à l’aide des API
Comme le statut du ticket change, nous en aurais besoin mettre à jour le statut de la carte qui a été envoyé. Pour que nous utilisaient les actions / <<-id d’action >> / point de terminaison de propriétés. Dans le sous exemple, nous doit être mise à jour le statut du ticket résolu. Notez qu’actionId est l’ID de l’action envoyée à l’étape précédente.

| Méthode  |      PPUT    |
|----------|-------------|
|**URL**|{{-url de terminaison}} / v1/groupes / {{test-group-id}} /actions/ {{actionId}}|
|**Corps de la demande**|{<br>{<br>« version » : -1,<br>« MettreÀJourPropriétés » :<br>[<br>{<br>« name » : « ticketstatus »,<br>« type » : « Texte »,<br>« valeur » : « état : résolu »<br>}<br>]<br>}|

## <a name="screenshots-of-the-demo"></a>Captures d’écran de la démo
### <a name="ticket-sent-from-api"></a>Ticket envoyé à partir de l’API
![](Images/Ticket%20sent%20from%20API.PNG)
### <a name="ticket-after-updating-the-status-from-api"></a>Ticket après la mise à jour de l’état de l’API
![](Images/Ticket%20after%20updating%20the%20status%20from%20API.PNG)
<br>Partage du package à partir d' [ici](https://drive.google.com/file/d/1gQb1CpYVd8SLnOOH4PCZWPsUeYhdWehB/view), au cas où vous voulez lui attribuer une capture. (n’oubliez pas de modifier l’id de package avant le téléchargement à Kaizala pour éviter les conflits)

















