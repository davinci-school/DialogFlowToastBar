# Toastaria

> This folder contains supporting materials for WUD workshop: How to build a chatbot in Google [dialogflowES](https://dialogflow.cloud.google.com/) system. Files contains intents separated by numbered 1,2,3 or all intents in complete_toastaria.zip file. The dialog tree view for better orientation is available [here](https://bit.ly/3pFs6lp). Each bubble represent one intent. Its hard to copy separate sentence thus the intents are provided in the section bellow. The structure of each intent is as follows. The (X) in the bracket refer to zip file of this intent.

> ### *Name of intent (X)*
> *User: Training phrase or phrases separated by |*

> *Bot: Responses*
## 
## This section contains the list of INTENTS


### *Welcome*
*User: Hi*

*Bot: Welcome to Toustaria. Would you like to see the menu or order a toast?*
### *Toast Menu*
*User: Can i see the menu | menu please | show me the menu | i wanna see menu*

*Bot: Would you like a meet toast or vegetarian?*

### *Meet Toast menu (1)*
*User: I want toast with meat | meat toast please | definitely meat meat | meat*

*Bot: Today we offer 3 options. Ham and cheese, chicken and tomatoes, and Italian mortadella toast. Would you like to order? just write name of selected toast*

### *Vegetarian Toast Menu (1)*
*User: vegetarian | without meat*

*Bot: Today we offer 2 options. Cheesy toast or goat cheese with beetroot. Would you like to order? Just write the name of selected toast.*

### *Order Ham And Cheese Toast(2)*
*User: I'd like ham and chees toast*

*Bot: You have ordered ham and cheese toast.*

### *Order Chicken and Tomatoes Toast(2)*
*User: I'd like chicken and tomatoes toast*

*Bot: You have ordered toast with chicken and tomatoes.*

### *Order Italian Mortadela Toast(2)*
*User: I'd like toast with mortadela*

*Bot: You have ordered toast with mortadela.*

### *Order Cheese Toast (2)*
*User: I'd like Cheesy toast*

*Bot: You have ordered a Cheesy toast.*

### *Order Goat Cheese With Beetroot Toast (2)*
*User: I'd like goat cheese toast with beetroot*

*Bot: You have ordered toast with goat cheese and beetroot.*

##

## ENTITIES
> Having an intent for each type of toast is not effective thus we will use ENTITY to extract the information about toast type. The structure of enity is first its name, then each item represent one entry with synonyms in the bracket

### *Toasts*
* *ham and cheese (cheese with ham)*
* *chicken and tomatoes (chicken with tomatoes)*
* *Italian mortadela (mortadela)*
* *cheesy toast (cheesy, toast with cheese, cheese)*
* *goat cheese with beetroot (cheese beetroot)*

## Intent using entities
> When using entity in the intent, we can ask user to provide this information. In action and parameters select checkbox of required parameter and enter prompt (last column).  This promt is shown to the user if the entity is required.  Another change is in the response. As we replace 5 intents for each toas just by one, we want to show the user which toast he selected. This is done by calling our entity with dollar sign $toasts 

### *Order toast (3)*
*User: I'd like Cheesy toast |  one Cheesy | order a toast| i wanna ham and cheese toast*

*Prompt: What toast do you want? Enter the toast name or check the menu?*

*Bot: You have ordered $toasts toast.*



