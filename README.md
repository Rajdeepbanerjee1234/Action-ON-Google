# Action-ON-Google


'use strict';
const {dialogflow} = require('actions-on-google'); 
const functions = require('firebase-functions'); 
 
const app = dialogflow({debug : true});

app.intent('colour',(conv , {color}) =>{
         var lucky_no;
  lucky_no= color.length*5;
  conv.ask("Your lucky no. is "+lucky_no);
  
});

exports.dialogflowFirebaseFulfillment = functions.https.onRequest(app);

