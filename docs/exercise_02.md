---
title: Extended Functionality
description: Excercise 02
tags: 
    - easy
    - exercise
---


## Extended Functionality  

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

