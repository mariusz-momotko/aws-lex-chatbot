# aws-lex-chatbot
Materials (presentation, code, data) for the "Introduction to Build AI Chatbots using AWS LEX" meetup.
There are three main folders:
* lambda - includes lambda functions which are used for validation and fulfilment actions in the OrderTicket bot.
* lex - includes definition of the OrderTicket bot and slot types.
* docs - includes the presentation given at the meetup in PDF format.

In order to test the OrderTicket bot you need:
1. Create and then import the code of the following lambda functions:
  - OrderTickerValidation
  - OrderTicketFulfillment

2. Optionally, create tests (i.e. create a given test, name it and copy-pase its content) for those lambda functions:
  - TestFulfilmentText - testing textual form of the final message
  - TestFulfillmentVoice - 
  
