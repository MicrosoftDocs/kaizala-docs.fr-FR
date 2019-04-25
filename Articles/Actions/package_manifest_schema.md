`````
{
    "$schema": "http://json-schema.org/draft-04/schema#",
    "type": "object",
    "properties": {
        "schemaVersion": {
            "type": "number",
            "description": "The version of the manifest schema this manifest is using. The corresponding schema version is 1."
        },
        "id": {
            "type": "string",
            "description": "A unique identifier for this Action. The id must use reverse domain name notation.",
            "maxLength": 64
        },
        "version": {
            "type": "string",
            "description": "The version of this Action. Changes to the Action should cause a version change. This version string must follow the semver standard."
        },
        "displayName": {
            "type": "string",
            "description": "Display name for the Action. This name will be used when your Action shows up in Kaizala's Discover tab and Action palette.",
            "maxLength": 64
        },
        "description": {
            "type": "string",
            "description": "Description for the Action. This description will be used when your Action shows up in Kaizala's Discover tab.",
            "maxLength": 128
        },
        "providerName": {
            "type": "string",
            "description": "Display name for the developer/publisher. This name will be used when your Action shows up in Kaizala's Discover tab and Action palette.",
            "maxLength": 64
        },
        "icon": {
            "type": "string",
            "description": "File name of the Action's icon sized 36*36. Each icon image file must be a transparent PNG, with a white or light-colored background.",
            "maxLength": 64
        },
        "appModel": {
            "type": "string",
            "description": "File name of the Action's app model. Refer to the app Model JSON schema and ensure compliance.",
            "maxLength": 64
        },
        "externalUrls": {
            "type": "object",
            "properties": {
                "url": {
                    "type": "string",
                    "description": "The url which needs to be whitelisted for showing external content. All of these URLs must conform to https protocol."
                }
            },
            "required": [
                "url"
            ]
        },
        "ActionStoreSchema": {
            "type": "string",
            "description": "File name of the action store schema file. This key is added only while using custom operators in chatcardview json. By default, the contents of this new file is an empty json object: {}"
        },
        "views": {
            "type": "object",
            "properties": {
                "ChatCanvasCardView": {
                    "type": "object",
                    "properties": {
                        "labelRespondToForm": {
                            "type": "string",
                            "description": "The call-to-action string asking for an end user to respond to the Action. eg/Default: Respond to Survey",
                            "maxLength": 32
                        },
                        "labelResponded": {
                            "type": "string",
                            "description": "String to show when a user has responded to a specific instance of the Kaizala Action. eg/Default: You have responded.",
                            "maxLength": 32
                        },
                        "labelUpdateResponse": {
                            "type": "string",
                            "description": "The call-to-action string asking for an end user to update their response to the Action. eg/Default: Update My Response",
                            "maxLength": 32
                        },
                        "labelAnotherResponse": {
                            "type": "string",
                            "description": "The call-to-action string asking for an end user to add another response to the Action. eg/Default: Add Another Response",
                            "maxLength": 32
                        },
                        "labelExpiryMsg": {
                            "type": "string",
                            "description": "String to show when a specific instance of the Kaizala Action has expired. eg/Default: Survey Closed",
                            "maxLength": 32
                        },
                        "showExpiry": {
                            "type": "boolean",
                            "description": "When set to true, the card on the chat canvas will display the expiry date and time.",
                            "default": true
                        },
                        "showResponseCount": {
                            "type": "boolean",
                            "description": "When set to true, the card on the chat canvas will display the response count.",
                            "default": true
                        },
                        "showHeader": {
                            "type": "boolean",
                            "description": "When set to true, the card on the chat canvas will display the header.",
                            "default": true
                        },
                        "showFooter": {
                            "type": "boolean",
                            "description": "When set to true, the card on the chat canvas will display the footer.",
                            "default": true
                        },
                        "isResponseEditable": {
                            "type": "boolean",
                            "description": "When set to true, responses to the Kaizala Action by a user are subsequently editable later.",
                            "default": true
                        }
                    }
                },
                "CreationView": {
                    "type": "object",
                    "properties": {
                        "labelHeader": {
                            "type": "string",
                            "description": "String to show in the header for the immersive view.",
                            "maxLength": 32
                        },
                        "sourceLocation": {
                            "type": "string",
                            "description": "Filename for the immersive view to show when the Action is invoked from the palette and a new instance is created.",
                            "maxLength": 32
                        },
                        "showNativeToolbar": {
                            "type": "boolean",
                            "description": "When set to true, the immersive view has the native toolbar visible.",
                            "default": true
                        },
                        "backDialogVisibility": {
                            "type": "boolean",
                            "description": "When set to true, the immersive view has the back button visible.",
                            "default": true
                        },
                        "backDialogTitle": {
                            "type": "string",
                            "description": "Title of the alert shown when the back button is pressed in the immersive view's native toolbar.",
                            "maxLength": 16
                        },
                        "backDialogDescription": {
                            "type": "string",
                            "description": "Description of the alert shown when the back button is pressed in the immersive view's native toolbar.",
                            "maxLength": 32
                        }
                    },
                    "required": [
                        "sourceLocation"
                    ]
                },
                "ResponseView": {
                    "type": "object",
                    "properties": {
                        "labelHeader": {
                            "type": "string",
                            "description": "String to show in the header for the immersive view.",
                            "maxLength": 32
                        },
                        "sourceLocation": {
                            "type": "string",
                            "description": "Filename for the immersive view to show when the Action is invoked from the palette and a new instance is created.",
                            "maxLength": 32
                        },
                        "showNativeToolbar": {
                            "type": "boolean",
                            "description": "When set to true, the immersive view has the native toolbar visible.",
                            "default": true
                        },
                        "backDialogVisibility": {
                            "type": "boolean",
                            "description": "When set to true, the immersive view has the back button visible.",
                            "default": true
                        },
                        "backDialogTitle": {
                            "type": "string",
                            "description": "Title of the alert shown when the back button is pressed in the immersive view's native toolbar.",
                            "maxLength": 16
                        },
                        "backDialogDescription": {
                            "type": "string",
                            "description": "Description of the alert shown when the back button is pressed in the immersive view's native toolbar.",
                            "maxLength": 32
                        }
                    },
                    "required": [
                        "sourceLocation"
                    ]
                },
                "ResponseResultsView": {
                    "type": "object",
                    "properties": {
                        "labelHeader": {
                            "type": "string",
                            "description": "String to show in the header for the immersive view.",
                            "maxLength": 32
                        },
                        "sourceLocation": {
                            "type": "string",
                            "description": "Filename for the immersive view to show when the Action is invoked from the palette and a new instance is created.",
                            "maxLength": 32
                        },
                        "showNativeToolbar": {
                            "type": "boolean",
                            "description": "When set to true, the immersive view has the native toolbar visible.",
                            "default": true
                        },
                        "backDialogVisibility": {
                            "type": "boolean",
                            "description": "When set to true, the immersive view has the back button visible.",
                            "default": true
                        },
                        "backDialogTitle": {
                            "type": "string",
                            "description": "Title of the alert shown when the back button is pressed in the immersive view's native toolbar.",
                            "maxLength": 16
                        },
                        "backDialogDescription": {
                            "type": "string",
                            "description": "Description of the alert shown when the back button is pressed in the immersive view's native toolbar.",
                            "maxLength": 32
                        }
                    },
                    "required": [
                        "sourceLocation"
                    ]
                }
            },
            "required": [
                "CreationView",
                "ResponseView",
                "ResponseResultsView"
            ]
        }
    },
    "required": [
        "schemaVersion",
        "id",
        "version",
        "displayName",
        "description",
        "providerName",
        "icon",
        "appModel"
    ]
}
`````
