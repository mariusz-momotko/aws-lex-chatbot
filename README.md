# aws-lex-chatbot
Materials (presentation, code, data) for the "Introduction to Build AI Chatbots using AWS LEX" meetup.
There are three main folders:
* lambda - includes lambda functions which are used for validation and fulfilment actions in the OrderTicket bot.
* lex - includes definition of the OrderTicket bot and slot types.
* docs - includes the presentation given at the meetup in PDF format.
---
In order to test the OrderTicket bot you need:

0. Choose the region you will do all installations. Preferrably it is US. East, N. Virginia. 

1. Create and then import the code of the following lambda functions:
  - OrderTickerValidation
  - OrderTicketFulfillment

2. Optionally, create tests (i.e. create a given test, name it and copy-pase its content) for those lambda functions:
  - TestValidationBasic - testing basic / positive use case to process slots
  - TestValidationSame - testing an exceptional case when fromStation and toStation slots values are the same
  - TestValidationEmpty - testing if validation rules work properly when some slots are empty
  - TestFulfilmentText - testing textual form of the final bot message
  - TestFulfillmentVoice - testing voice enabled form of the final bot message
  
3. Create and then import the OrderTicker bot. The required SKMSlotType should be imported as well.

4. Assign lambda functions to relevant parts of the OrderTicket bot definition:
  -  Bot, Lambda initialization and validation - set "Initialization and validation code hook" option and select OrderTickerValidation function (latest version).
  - Bot, Fulfillment - set "AWS Lambda function" option and select OrderTicketFulfillment function (latest version).
  Save the bot!
  
 5. Build the bot. Now you can test it.
 ---
  
