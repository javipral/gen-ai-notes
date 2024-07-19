# Integrating with function calling

## Why Function Calling

- Ensures Consistent response format
- Adds the ability to use data from other sources of an application in a chat context

## Use cases

- Calling External Tools.
- Creating API or Database Queries.
- Creating Structured Data.

## Steps

1. Calling the Chat Completions API with a list of your functions and a user message.
2. Reading the model's response to perform an action ie execute a function or API Call.
3. Making another call to Chat Completions API with the response from your function to use that information to create a response to the user.
