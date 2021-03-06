FORMAT: 1A
HOST: http://dahi.ai/

# Dahi.ai

# Bot

## How to Create Bot ?

1. Click Bots in the left menu.
2. Click Add New Bot button in the opening page
3. Type a Bot Name for the bot and select Language as Turkish.
4. After the steps above are done click done button. 

## How to Use Bot ?

1. After the bot, entities and categories were created, for using the bot, click Bots in the left
menu.
2. Select the bot you want to use.
3. Click Talk Your Bot button at the right bottom of the screen.
4. In the opening section, type a sentence making the bot enter into any specific category and
(If you want) including any parameters caught by the bot.
5. If any lacking parameters, type the parameters by following the question of the bot.
6. After all parameters were taken, the bot will show the determined result. 

# Entity

## What’s Entity ?

Entity is a set of words the bot can recognize. 

## How to Create Entity ?

1. Click Entities in the left menu.
2. Click add button in the opening page.
3. Type an Entity Name for the entity.
4. Select Entity Type as array.
5. In Define Value section, type what you want to add into the entity(Enter).
6. After the word was added, type synonym of the word into synonyms section.
7. After all required words were added, click save button. 

# Category

## What’s Category ?

Category is a section in which for any determined context, the parameters that needs to be given to
the bot and the answer given by the bot are determined while talking with the bot.

## How to Create Category ?

1. Click Bot Detail in the left menu.
2. Click Categories below Bot Detail.
3. Click add button in the opening page.
4. Type a Category Name for the category.
5. In the Define Rule section, type the sentence required to make the bot enter the flow of the
category while talking with the bot(Enter).
6. Click the words that have to be selected to make bot enter the category in Defined Rules.
7. In Defined Rules section, set the number, appearing when cursor is at the rightmost of the
section, as number of words you’ve chosen in the previous step.
8. To add a parameter to the category, type the parameter name into the Define Parameter
section(Enter).
9. Select the parameter Type.
10. If Parameter Type is integer, enter a number, if it is date, enter a date using the format such
as (12.02.2015), if it is time, enter a time using the format such as (08:00), if it is phone, enter
a phone number using the format such as 05XX XXX XX XX(For more detailed information
about Type, click here).
11. If the parameter Type is array, then enter the entity, from which the parameters will be
taken, into the Entity in the Define Parameters section.
12. If the parameters have not been given to the bot, determine the question asked by the bot
to take parameters from user.
13. After all parameters were given to the bot, type the answer into the Message section in the
Action section. If you want, you can use the parameters in Message.
14. If you want to use any operation, select one of the Method’s ďeloǁ Operation and enter the
required parameters.
15. If you want to use the answer returned from the operation in the Message, use the answer
as {return}.
16. If any parameter were not given, click the Quick Answers tab next to Parameters tab.
17. In Define Quick Answers section, determine the answer given by the bot when entered into
the flow(Enter).
18. After the required parameters were given and Message was created or Quick Answer was
created, click the save button. 

# Actions

## What is Action ?

Procedures carried out at the end of Category stream.

## What are the actions ?

No Forward, Forward and Text Forward.

## No Forward

The action came at the end of the determined flow. We have 2 types of output in this action. These message and confirm. Message types with plain text prompts, we can print the values of the parameters obtained in the flow we wanted. We can ignore the user to confirm the type approval process before the end of the stream.

## How to use No Forward Action ?

1. Open Category detail screen.
2. Click "No Forward" tab on Action Panel.
3. Select Message type in options. There are two options. Message and Confirm
4. Write your customize output message.

## Forward

Flow end, the parameters obtained in stream transmitted with parameters selected category, it allows to continue to another stream.

## How to use No Forward Action ?

1. Open Category detail screen.
2. Click "Forward" tab on Action Panel.
3. Do Double-Click on value opposite the parameter name.
4. The parameters obtained in flow edit parameters to be passed by value. This form is used {parameter_name} or only text.

## Text Forward

At the end of the stream output (this output may also include parameters obtained in flow) if there is match allows you to start streaming again.

## How to use Text Forward Action ?

1. Open Category detail screen.
2. Click "Text Forward" tab on Action Panel.
3. Write your customize output message. If you want you can also use the parameter values obtained in stream. like {parameter_name}

## What is Operation ?

The third party transactions are made at the end of the flow. There are two operation methods. These callServiceWithRaw and callServiceWithGet.
callServiceWithRaw mean, to be sent in raw type of post parameters.
callServiceWithGet mean, calling the get method of service.

## How to use Operation ?

1. Open Category detail screen.
2. Select the method name.
3. Edit the parameter's value on right side. (activate with a double click) 

# Integrations

## How to integrate Dahi.ai bot to Facebook Messenger ?

1. Create new web application on developers.facebook.com
2. Create Facebook Page for bot interface.
3. Add Messenger Product to your new web application.
4. On messenger product, create new token (chosee right facebook page for token).
5. Copy bot End-Point url on bot setting (dahi.ai) and paste webhooks setup callback url.
6. Copy generated token and paste webhooks setup and check all properties checkboxes.
7. Copy generated token and paste also Page Access Token area on dahi.ai bot settings page.
8. Done


## API [/category/sendMessage]

### Send Message [POST]

You may send messsage, your own bot.

+ Request (application/json)

        {
            "recipientId": "984941DA1767E119E6184E6E56E566E0",
            "token": "57ed2268e4b081dd2c1bd8a7",
            "message": { "text":"hello" ,"type":"text" }
        }

+ Response 200 (application/json)

    + Headers

            Location: /category/sendMessage

    + Body

            {"result":{"text":"hi how are you ?"}}
