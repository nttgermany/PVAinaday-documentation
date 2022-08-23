---
title: Integration Options
description: Excercise 03
tags: 
    - easy
    - exercise
---


## Integration Options    

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
