# <a name="automating-business-process-using-kaizala-flow-connector"></a>Automatisation du processus d'entreprise à l'aide du connecteur de flux Kaizala
## <a name="introduction-to-microsoft-flow"></a>Présentation de Microsoft Flow
Microsoft Flow est un service qui vous permet de créer des flux de travail automatisés entre vos applications et vos services favoris pour synchroniser des fichiers, recevoir des notifications, collecter des données et bien plus encore. [courtoisie: [Flow](https://docs.microsoft.com/en-us/flow/getting-started)]. En d'autres termes, vous pouvez créer un organigramme qui exécuterait la logique en arrière-plan, c'est simple!
<br> Le flux extrait des services en tant que connecteurs servant de proxy/wrapper pour le service sous-jacent. Flow communique avec le (s) connecteur (s) et vous permet de transmettre la sortie d'un connecteur à un autre.  Cela vous permet de créer un flux qui s'intègre avec plusieurs services. Un connecteur peut avoir des déclencheurs et des actions. Les déclencheurs sont l'événement qui déclenchent un flux. Chaque flux commence par un déclencheur. Exemple de déclencheur: lors de la réception d'un message électronique. Les actions sont les fonctionnalités exposées par les services. Exemple d'action: envoyer un courrier électronique. Lorsque vous ajoutez un connecteur sur le flux, si le connecteur nécessite un compte sous-jacent pour accéder au service/fonctionnalité, vous devez l'authentifier/le configurer avant de pouvoir utiliser le connecteur. Ces informations sont enregistrées en tant que connexion.
<br> Si votre service n'est pas encore disponible en flux, vous pouvez créer un connecteur de flux personnalisé pour votre service!
## <a name="kaizala-flow-connector"></a>Connecteur de flux Kaizala
Kaizala est disponible sous forme de connecteur sur Microsoft Flow. Cela vous permet d'incorporer Kaizala dans votre flux de travail d'entreprise. Et, étant donné que le flux prend en charge 200 connecteurs +, ce qui présente une opportunité de créer des solutions Kaizala.
<br> Vous trouverez ci-dessous des captures d'écran illustrant la liste des déclencheurs et des actions actuellement disponibles dans le connecteur de flux Kaizala.
### <a name="actions"></a>Actions
![](Images/MailFlow_Actions.PNG)
### <a name="triggers"></a>Déclenche
![](Images/MailFlow_Triggers.PNG)
<br>
<br> Kaizala dispose de 2 modèles de flux publiés que vous pouvez utiliser comme point de départ:
<br> 1. [Ajouter un élément de liste SharePoint pour chaque réponse d'enquête Kaizala](https://us.flow.microsoft.com/en-us/galleries/public/templates/a71f0ac3e35a40728b3e9ee27bf9dbcd/add-a-sharepoint-list-item-for-every-kaizala-survey-response/)
<br> 2. [Envoyer une annonce sur Kaizala lorsque vous recevez un message électronique Outlook](https://us.flow.microsoft.com/en-us/galleries/public/templates/cb85f664dfb0421dbd937dd64618f791/send-an-announcement-on-kaizala-when-you-get-an-outlook-email/)
## <a name="example-scenario"></a>Exemple de scénario
Pour illustrer le connecteur de flux Kaizala, faites-nous part d'un scénario: «envoyez un message électronique au message texte reçu sur le groupe Kaizala».
### <a name="steps"></a>Étapes :
<br> 1. Accédez à [https://flow.microsoft.com](https://flow.microsoft.com/en-us/) et connectez-vous avec vos informations d'identification
<br> 2. cliquez sur «mes flux», puis cliquez sur «créer à partir d'un espace»![](Images/MailFlow_Search.PNG)
<br> 4. Donnez un nom à votre flux
<br> 5. dans la zone de recherche du connecteur, recherchez Kaizala
<br> 6. Sélectionnez le connecteur de flux Kaizala à partir du résultat de la recherche.
<br>  7. à partir des déclencheurs disponibles, sélectionnez «lors de l'envoi d'un message texte sur un groupe» (vous devrez vous authentifier auprès de Kaizala à ce stade avec votre numéro de téléphone mobile et le mot de passe à usage unique que vous recevrez).
<br>  8. Ajoutez maintenant une action pour envoyer le courrier électronique (j'ai choisi Outlook.com – envoyer une action de courrier électronique – vous devrez vous authentifier auprès de votre compte de messagerie)
<br> 9. Entrez une adresse de messagerie dans le champ à
<br>10. cliquez sur le champ objet, vous remarquerez qu'une fenêtre contextuelle s'affiche sur la droite qui vous donne une série de valeurs extraites du déclencheur ci-dessus.
<br>![](Images/MailFlow_4.PNG)
<br> 11. laissez le nom de l'expéditeur dans l'objet et le message, numéro de téléphone mobile dans le corps du message. Le flux se présente comme suit:
<br>
![](Images/MailFlow_5.PNG)
<br> 12. cliquez sur créer un flux
<br>  Poursuivez et testez le flux en envoyant un message texte sur le groupe que vous avez configuré.
### <a name="sample-screenshot-of-the-message-sent-on-the-group"></a>Exemple de capture d'écran du message envoyé au groupe:

![](Images/MailFlow_6.PNG)
### <a name="sample-screenshot-of-the-email-received"></a>Capture d'écran d'exemple du courrier électronique reçu:
![](Images/MailFlow_MailReceived.PNG)









