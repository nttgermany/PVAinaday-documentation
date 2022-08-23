---
title: Exercise 01
description: Excercise 01
tags: 
    - easy
    - exercise
---


## Exercise 01  

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

