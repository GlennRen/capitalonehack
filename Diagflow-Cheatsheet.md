# [DialogFlow](https://console.dialogflow.com/api-client/) Cheatsheet

### Intents
1. You can create a new action for Google Assistant by creating a new intent.
2. Add your user expressions.
  * Will expand & create parameters/entities if needed. You can double click to manually add them.
3. Give your intent an action name (this is important).
4. Under actions you can rename parameters and set ones as required.
5. Click on 'Fulfillment' and click 'Use Webhook'.

### Fulfillment
1. Use the inline editor to edit your code.
2. Add an actionHandlers based on the action name of the previous intent.
3. View logs at the bottom of the page at 'View execution logs in the Firebase console'

ex.
```javascript
'college': () => {
        const firstName = parameters.firstName;
        const lastName = parameters.lastName; // null if optional
        console.log("firstName: " + firstName);
        const summiteer = findSummiteer(summiteers, firstName, lastName);
        if (summiteer) {
            sendResponse(firstName + " went to college at " + summiteer.college);
        }
        else {
            sendResponse("I don't know where " + firstName + " went to college.");
        }
    }
```

### Entities
* Will search for entities in your intent expressions

### Integrations
* Export to other accounts

### Other
* To try it on your phone you have to say "Talk to my test app."
* [Jared's Bot Presentation](https://docs.google.com/presentation/d/1UmXwFZiupKPNSRyhrszesUEMDR1ng0GBgBPfoHaKHog/edit#slide=id.g112d91e51c_0_62)
