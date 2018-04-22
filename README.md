# breakfast-bot
Demo files for Amazon Lex showing challenges with Natural Language Understanding

# Important
This bot is designed to show a not very good bot that was used as part of a presentation demo on the limitations of natural language understanding. 

It lacks proper purpose and has deliberately haphard utterances. It is not hooked up to any fulfilments.

IT SHOULD NOT BE USED FOR THE BASIS OF ANY REAL BOT.

# Setup

### Prerequisites for Bot
* AWS Account https://docs.aws.amazon.com/AmazonSimpleDB/latest/DeveloperGuide/AboutAWSAccounts.html

### Steps
Follow the steps for importing a bot at https://docs.aws.amazon.com/lex/latest/dg/import-export.html, the first bot shown in the presentation is this one:
https://github.com/virtualgill/breakfast-bot/blob/master/BREAKFAST-BOT/BOTS/BreakfastBot_LEX_Initial.zip

----

### Prerequisites for Tests
* Postman installed - https://www.getpostman.com
* Import https://github.com/virtualgill/breakfast-bot/blob/master/BREAKFAST-BOT/TEST/TESTS_BreakfastBot.postman_collection.json into Postman. Instructions are here https://www.getpostman.com/docs/v6/postman/collections/data_formats
* Create an IAM user in your AWS Account with access to Lex https://docs.aws.amazon.com/IAM/latest/UserGuide/id_users_create.html#id_users_create_console
* Set up environment variables in Postman and add in your user's access and secret keys https://www.getpostman.com/docs/v6/postman/environments_and_globals/manage_environments. Be aware that you will need to change the resource name if you create you bot anywhere but us-east-1.
~~~~
resource_name:https://runtime.lex.us-east-1.amazonaws.com
access_key:<<INSERT KEY HERE>>
secret_key:<<INSERT SECRET KEY HERE>>
bot_name:BreakfastBot
bot_alias_name:demo
~~~~

### Steps
* Ensure you have Published a version of your Bot with a bot alias matching the one in your environment variables (here shown as 'demo'.
* Run your collection https://www.getpostman.com/docs/v6/postman/collection_runs/starting_a_collection_run
* Remember when you make a change to your bot you will need to re-publish.

