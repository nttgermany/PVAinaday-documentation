## Headline  

### Step 1
Create a new blank topic and navigate to it.

![Image title](screenshots/Clipboard10.jpg){align=right}  

### Step 2
Rename the topic to 'Filiale suchen'.


![Image title](screenshots/Clipboard13.jpg){align=right}  

### Step 3

Add some trigger phrases in the trigger section. Trigger phrases or similiar phrases will execute the conversation topic you are creating at the moment. The trigger automatically ignores spelling mistakes, grammar or other spellings of words.
Example topics for this exercise: 'Filiale suchen', 'Zeige mir Filialen in meiner Nähe'.

![Image title](screenshots/Clipboard17.jpg){align=right}  

### Step 4
Each new topic already contains a message. Fill in the message with 'Dazu benötige ich noch ein paar Informationen von Ihnen.'
This message is displayed immediately after the topic is triggered.

![Image title](screenshots/Clipboard19.jpg){align=right}  

### Step 5
Click on the 'plus' symbol below the message.

![Image title](screenshots/Clipboard20.jpg){align=right}  

### Step 6
Select 'Eine Frage stellen' to add a new node to your conversation.

![Image title](screenshots/Clipboard21.jpg){align=right}  

### Step 7
Type in the question 'Wie heißen Sie?'
The bot user's response can be checked against an entity. This validates the response. In this question we ask for a name. For example, a name cannot contain numbers. This is checked by the entity.


![Image title](screenshots/Clipboard23.jpg){align=right}  

### Step 8
The user's response is stored in a variable to be used in further conversation flow.  
Edit the variable via the edit-symbol.

![Image title](screenshots/Clipboard25.jpg){align=right}  

### Step 9
There are two types of variables in PVA: Topic and Bot variables
Bot variables can be retrieved from all topics. Topic variables remain within a topic, but can be passed as input variables to another topic if required.
In this case, we define the variable as bot variable to retrieve the user name in other topics without asking again.

![Image title](screenshots/Clipboard26.jpg){align=right}  

### Step 10
Rename the variable to 'UserName'.
Please note that the variable has automatically been given the prefix 'bot.' because we have defined it as bot variable.

![Image title](screenshots/Clipboard27.jpg){align=right}  

### Step 11
Click on the 'plus' symbol below the question.

![Image title](screenshots/Clipboard28.jpg){align=right}  

### Step 12
Select 'Eine Frage stellen' to add a new node to your conversation.

![Image title](screenshots/Clipboard29.jpg){align=right}  

### Step 13
Having stored the answer to the previous question in a variable, we can now output the value, for example as a salutation.

![Image title](screenshots/Clipboard30.jpg){align=right}  

### Step 14
Enter the next question of this topic: 'welches Bundesland liegt in Ihrer Nähe?'.

![Image title](screenshots/Clipboard31.jpg){align=right}  

### Step 15
We allow the user to answer the question with given answer options. The answer is to be checked against 'Multiple Choice Options'.
Below the selection of the entity you can add answer options. In this case we want to define our offices as answer options.
The user can only choose from these options, but their answer may contain spelling errors and will still be recognised.
Enter answer options: 'Hamburg', 'Hessen'


![Image title](screenshots/Clipboard33.jpg){align=right}  

### Step 16
The user's response is saved as a variable. This time we store the value in a topic variable because we only need this information within this topic and not in other topics.
Rename the variable to 'Bundesland'.

![Image title](screenshots/Clipboard34.jpg){align=right}  

### Step 17
By default, a condition is already inserted when you ask a multiple choice question. For each option of the question there is automatically a conversation path.
The condition evaluates the answer from the user which is stored in the topic variable 'Bundesland'.
Click on the 'plus' symbol below the condtion 'Bundesland = Hamburg'.
![Image title](screenshots/Clipboard35.jpg){align=right}  

### Step 18
Select 'Eine Nachricht anzeigen'.
Enter the address of your office in Hamburg, e.g.

'Die nächste Filiale in Ihrer Nähe ist:
Brooktorkai 2020457 Hamburg'

![Image title](screenshots/Clipboard36.jpg){align=right}  

### Step 19
Repeat the last steps for the second condition 'Bundesland = Hessen'.
Enter the address of your office in Hessen, e.g.

'Die nächste Filiale in Ihrer Nähe ist:
Horexstraße 761352 Bad Homburg'

![Image title](screenshots/Clipboard37.jpg){align=right} 

### Step 20
The bot user has received the response. Finally, we can close the topic.
Click on the plus-symbol and select 'Mit Befragung beenden'.
The conversation will be directed to a default topic which is called 'Ende der Unterhaltung'

![Image title](screenshots/Clipboard38.jpg){align=right} 

### Step 21
Click on the plus-symbol in the other condition, but don't select a node. Drag the circle symbol from the right-hand side to the 'Ende der Unterhaltung' node on the left-hand side and drop it there.

![Image title](screenshots/Clipboard39.jpg){align=right}  

### Step 22
Both pathes of the conversation end in the same step.

![Image title](screenshots/Clipboard40.jpg){align=right}  

### Step 23
Save your topic and test it on the Testbot window. Type in a trigger that you defined in the first steps.

![Image title](screenshots/Clipboard43.jpg){align=right}  

### Step 24
Next topic.
Create a new blank topic.
We want to give our customers the possibility to change their address in our address book.
![Image title](screenshots/Clipboard44.jpg){align=right}  

### Step 25
Rename the topic to 'Adressänderung'.

![Image title](screenshots/Clipboard45.jpg){align=right}  

### Step 26
Add some trigger phrases which the users can use to start this topic.

![Image title](screenshots/Clipboard46.jpg){align=right}  

### Step 27
Delete the step that was created automatically.

![Image title](screenshots/Clipboard47.jpg){align=right}  

### Step 28
Add a new step to ask a question 'Eine Frage stellen'.
![Image title](screenshots/Clipboard48.jpg){align=right}  

### Step 29
Enter the question 'Wie lautet die Postleitzahl Ihres neuen Wohnortes?'

![Image title](screenshots/Clipboard49.jpg){align=right}  


### Step 30
To validate the user's response, choose 'Postleitzahl' as entity. Please note that only ZIP codes in the US format are accepted. If your customers are located elsewhere, it is better to create a custom entity or use the entire user response.
![Image title](screenshots/Clipboard50.jpg){align=right}  

### Step 31
Save the user's response as topic variable and rename the variable to 'Postleitzahl'.

![Image title](screenshots/Clipboard51.jpg){align=right}  
### Step 32
Add a new question 'Wie heißt der Ort, in dem Sie wohnen?'.
Identify the entire response. You could use the entity 'City' instead, but again, only US cities are available.
Save the user's response as topic variable and rename the variable to 'Wohnort'.
![Image title](screenshots/Clipboard52.jpg){align=right}  

### Step 33
Add a new question 'In welchem Bundesland wohnen Sie?'.
Identify the entire response or use a custom entity. We will come back to this step when the topic is finished.

![Image title](screenshots/Clipboard58.jpg){align=right}  

### Step 34
Save the user's response as topic variable and rename the variable to 'Bundesland'.

![Image title](screenshots/Clipboard59.jpg){align=right}  

### Step 35
Add a new questions 'Bitte geben Sie mir noch Ihre E-Mail Adresse zur Identifizierung'.
Validate the response with the entity 'E-Mail'.

![Image title](screenshots/Clipboard60.jpg){align=right}  

### Step 36
Save the user's response as topic variable and rename the variable to 'E-Mail'.
![Image title](screenshots/Clipboard62.jpg){align=right}  

### Step 37

Allow the variable to retrieve a value from another topic. We will later connect this topic to another topic where the user's email address is already known.

![Image title](screenshots/Clipboard63.jpg){align=right}  

### Step 38
Add a new question and summarise all answers for final confirmation. Select the answers from the variables section.
![Image title](screenshots/Clipboard64.jpg){align=right}  

### Step 39
Identify the user's response as 'Boolean'. This entity allows the user to give answers like 'Yes', 'No', 'True', 'False'.
![Image title](screenshots/Clipboard65.jpg){align=right}  

### Step 40
Save the user's response as topic variable and rename it to 'BestätigungAdressänderung'.
![Image title](screenshots/Clipboard66.jpg){align=right}  

### Step 41
Add a new condition to evaluate the user's response.
![Image title](screenshots/Clipboard67.jpg){align=right}  

### Step 42
Select the variable 'BestätigungAdressänderung' that we defined in the previous steps.
![Image title](screenshots/Clipboard68.jpg){align=right}  

### Step 43
In the drop-down field you can see all the values that the variable can take. Select 'true'.
![Image title](screenshots/Clipboard69.jpg){align=right}  

### Step 44
When the user has confirmed the data, we have to transfer the data to our address book. The address book is outside the bot. To connect external data sources, we need a Power Automate Flow.
Select 'Handlungsaufforderung'.
![Image title](screenshots/Clipboard70.jpg){align=right}  

### Step 45
Select the flow 'Adressänderung' to change the user's address. The flow must be created in Power Automate first.
![Image title](screenshots/Clipboard71.jpg){align=right}  

### Step 46
A flow can have input parameters and output parameters.
We want to update our address book, so we need to pass the new address of the user to Power Automate.
![Image title](screenshots/Clipboard72.jpg){align=right}  

### Step 47
Map all Input Parameters of the flow with the variables of the bot. Power Automate parameters have a blue background, variables of the bot have a grey background.
![Image title](screenshots/Clipboard74.jpg){align=right}  

### Step 48
Let's come back to the question we have created earlier: 'In welchem Bundesland wohnen Sie?'
Since the German states are not part of an entity, we have used the entire user response. However, there is a risk of spelling errors here.
Now we want to create a custom entity prevent this from happening. 
Got to 'Entitäten'.
![Image title](screenshots/Clipboard78.jpg){align=right}  

### Step 49
Create a new entity.
![Image title](screenshots/Clipboard80.jpg){align=right}  

### Step 50
Select 'Geschlossene Liste' and name it 'Bundesländer'.
![Image title](screenshots/Clipboard81.jpg){align=right}  

### Step 51
Create a list with all states. 
![Image title](screenshots/Clipboard82.jpg){align=right}  

### Step 52
You can also define synonyms or abbreviations.
![Image title](screenshots/Clipboard83.jpg){align=right}  

### Step 53


![Image title](screenshots/Clipboard84.jpg){align=right}  

### Step 54
By default, the entity allows spelling errors and learns over time.
![Image title](screenshots/Clipboard85.jpg){align=right}  

### Step 55
Go back to 'Themen'.
![Image title](screenshots/Clipboard86.jpg){align=right}  

### Step 56
Open the topic 'Adressänderung'.
![Image title](screenshots/Clipboard87.jpg){align=right}  

### Step 57
Navigate to the question 'In welchem Bundesland wohnen Sie?' and change the identifier to the newl created entity 'Bundesländer'.
Test the topic in the Testbot window.
![Image title](screenshots/Clipboard88.jpg){align=right}  

### Step 58
Next topic.
Create a new blank topic.

![Image title](screenshots/Clipboard89.jpg){align=right}  

### Step 59
Rename the topic to 'Bestellung zurückgeben'.
![Image title](screenshots/Clipboard90.jpg){align=right}  

### Step 60
Add some trigger phrases.
![Image title](screenshots/Clipboard91.jpg){align=right} 

### Step 61
Edit the message that is automatically created and enter the text: 
'Schade, dass Sie sich gegen unser Produkt entschieden haben.'
![Image title](screenshots/Clipboard92.jpg){align=right}  

### Step 62
Add a new question.

![Image title](screenshots/Clipboard93.jpg){align=right}  

### Step 63
Set the question to 'Wie lautet die Bestellnummer?'.
You can now save the entire user response. Alternatively, you can create a custom entity that checks the order number for a specific structure. For example, length of the number.


![Image title](screenshots/Clipboard94.jpg){align=right}  

### Step 64
Store the user's response in a topic variable and rename it to 'Bestellnummer'.
![Image title](screenshots/Clipboard95.jpg){align=right}  

### Step 65

Add a new question 'Zur Identifizierung benötige ich noch Ihren Namen.'
Identify the user response as 'Name der Person'.

![Image title](screenshots/Clipboard96.jpg){align=right}  

### Step 66
Store the user's response in a topic variable and rename it to 'Nachname'.
![Image title](screenshots/Clipboard97.jpg){align=right}  

### Step 67
Add a new node 'Handlungsaufforderung' and select a Power Automate Flow to query the order. You have to create the Flow in Power Automate first.
![Image title](screenshots/Clipboard98.jpg){align=right}  

### Step 68

Pass the variables from your bot to your flow.

![Image title](screenshots/Clipboard99.jpg){align=right}  

### Step 69

Using the order number and the user name, the flow can find the order in your order system and gives us the details back.

Save the response from the flow in topic variables: 'Betrag', 'Postleitzahl', 'Email', 'StatusBestellungAbrufen'.

The last variable 'StatusBestellungAbrufen' is used to find out whether the flow successfully found the order or not.

![Image title](screenshots/Clipboard100.jpg){align=right}  

### Step 70
Add a condition below to evaluate the status.
![Image title](screenshots/Clipboard101.jpg){align=right}  

### Step 71
Select the status variable 'StatusBestellungAbrufen' and check wether the value is 'Bestellung gefunden'.
![Image title](screenshots/Clipboard102.jpg){align=right}  

### Step 72
Add a message below and enter 'Ich habe die Bestellung gefunden'.
![Image title](screenshots/Clipboard103.jpg){align=right}  

### Step 73
Add condition below. We want to evaluate the total amount of the order. If the amount is less than 2.000 €, we assume that the user can return the order by post. If the amount is greater than 2.000 €, the user has to take the order to an office.

![Image title](screenshots/Clipboard104.jpg){align=right}  

### Step 74
Select the amount 'Betrag' that we want to evaluate.

![Image title](screenshots/Clipboard105.jpg){align=right}  

### Step 75
Select 'ist kleiner oder gleich' and enter '2.000'.

![Image title](screenshots/Clipboard107.jpg){align=right}  

### Step 76
Add a message below.


![Image title](screenshots/Clipboard108.jpg){align=right}  

### Step 77
Enter: 
'Sie können Ihre Bestellung per Post an folgende Adresse zurücksenden:

Horexstraße 761352 Bad Homburg'

![Image title](screenshots/Clipboard109.jpg){align=right}  

### Step 78
We repeat the step for other conditions. If the amount is not less than or equal to 2.000 €.
Add a message.
![Image title](screenshots/Clipboard110.jpg){align=right}  

### Step 79
Enter:
"Sie können Ihre Bestellung in einer unserer Filialen zurückgeben."

![Image title](screenshots/Clipboard111.jpg){align=right}  

### Step 80
Add a question below: "Kennen Sie die nächstgelegene Filiale?"



![Image title](screenshots/Clipboard112.jpg){align=right}  

### Step 81

Identify the user's response as 'Boolean'.
Store the user's response as a topic variable and rename it to 'BestätigenFilialsuche'.

![Image title](screenshots/Clipboard113.jpg){align=right}  

### Step 82
Add a new condtion to evaluate the response.

![Image title](screenshots/Clipboard114.jpg){align=right}  

### Step 83
Create the path: If 'BestätigenFilialsuche' = 'True'


![Image title](screenshots/Clipboard115.jpg){align=right}  

### Step 84
In this case the user knows how to return and where to return the order.
The topic is finished.
We can end the topic with a default topic 'Mit Befragung beenden'.

![Image title](screenshots/Clipboard116.jpg){align=right}  

### Step 85

We return to the previous condition and define the path if the user does not know where the next office is.

![Image title](screenshots/Clipboard119.jpg){align=right}  

### Step 86
Add a new question with the output variable 'Postleitzahl' of the Power Automate flow.
Ask 'Wohnen Sie noch in' and add the variable.

![Image title](screenshots/Clipboard120.jpg){align=right}  

### Step 87
Store the user's response in a topic variable and rename it to 'Bestätigen Wohnort'.
![Image title](screenshots/Clipboard121.jpg){align=right}  

### Step 88
Add a condition to evaluation the response.
![Image title](screenshots/Clipboard122.jpg){align=right}  

### Step 89
If the user still lives in the same place, we can refer directly to the topic 'Filiale suchen'.
![Image title](screenshots/Clipboard123.jpg){align=right}  

### Step 90
If the user's address has changed, we must first ask for their new address. For this, we refer to the topic 'Adressänderung'.
![Image title](screenshots/Clipboard124.jpg){align=right}  

### Step 91
Here we can fill the previously defined input variables. We take the email address from the order.
![Image title](screenshots/Clipboard125.jpg){align=right}  

### Step 92
Finally we can refer to the topic 'Filiale suchen'.
![Image title](screenshots/Clipboard126.jpg){align=right}  

### Step 93

![Image title](screenshots/Clipboard127.jpg){align=right}  

### Step 94
We now want to look again at the path of the conversation in case the order was not found.
Scroll up to the condition in which the variable 'StatusBestellungAbrufen' is evaluated.
![Image title](screenshots/Clipboard128.jpg){align=right}  

### Step 95
Add a message to the path if the order was not found.
Enter the message and use topic variables in the text.
'Ich habe leider nichts gefunden zu Bestellnummer BESTELLNUMMER und Nachname NACHNAME'.
![Image title](screenshots/Clipboard129.jpg){align=right}  

### Step 96
Add a question below to ask if the user input is correct
'Sind die eingegebenen Daten korrekt?'
![Image title](screenshots/Clipboard130.jpg){align=right}  

### Step 97
Store the user's response as a topic variable and rename it to 'BestätigungDatenvalidierung'.
![Image title](screenshots/Clipboard131.jpg){align=right}  

### Step 98
Add a condition to evaluate the user's response
![Image title](screenshots/Clipboard132.jpg){align=right}  

### Step 99
If the user confirms, the input data is correct, but the order cannot be found. In this case the bot can not help the user. The conversation must be passed on to a person.

![Image title](screenshots/Clipboard133.jpg){align=right}  

### Step 100
Add a step below 'Unterhaltung beenden' and select 'An Agent übertragen'.
![Image title](screenshots/Clipboard134.jpg){align=right} 

### Step 101
You can pass some details of the conversation to the agent.

![Image title](screenshots/Clipboard135.jpg){align=right}  

### Step 102
Return to the previous condition and define the path if the user has entered incorrect data. We want to give the user the possibility to change the entered data again.
Click on the plus-symbol, but don't select a node. 
Drag the circle symbol to the beginning of the conversation and drop it there.
![Image title](screenshots/Clipboard136.jpg){align=right}  

### Step 103
Drag the circle symbol to the beginning of the conversation and drop it there.
![Image title](screenshots/Clipboard137.jpg){align=right}  

### Step 104
This way, the conversation starts again at the beginning and the user can set the variables again.
![Image title](screenshots/Clipboard139.jpg){align=right}  
