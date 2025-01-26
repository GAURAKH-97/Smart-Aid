# Chatbot Automation Script

This script sets up and runs an AI chatbot using the `Groq` API. The chatbot provides accurate and advanced responses, leveraging real-time information when needed. Below is a detailed explanation of the script components.

## Importing Libraries

The code begins by importing several necessary libraries:

- `Groq` from the `groq` library: This is likely a custom library used for interacting with a specific API or service.
- `load` and `dump` from the `json` library: These functions are used for reading and writing JSON files.
- `datetime` from the `datetime` module: This is used to get the current date and time.
- `dotenv_values` from the `dotenv` library: This function is used to load environment variables from a `.env` file.

## Setting Variables

The code retrieves environment variables from a `.env` file and assigns them to Python variables. These variables include:

- `Username`
- `Assistantname`
- `GroqAPIKey`

It also initializes a `Groq` client using the `GroqAPIKey` and prepares an empty list `messages` for storing chat messages.

## System Prompt for the Chatbot

A system prompt is defined for the chatbot. This prompt sets up the chatbot with specific behavior rules, such as:

- Not telling the time unless asked.
- Keeping responses concise.
- Replying in English only.
- Avoiding mentions of its training data.

## Loading or Creating Chat Log

The code attempts to load a chat log from a JSON file (`ChatLog.json`). If the file does not exist, it creates an empty JSON file for the chat log.

## Realtime Information Function

This function generates and returns a string containing the current date and time information, which can be used in chatbot responses.

## Answer Modifier Function

This function removes empty lines from the chatbot's answers to make them more concise and readable.

## ChatBot Function

The `ChatBot` function handles sending a query to the chatbot and returning the answer. It follows these steps:

1. Loads the current chat log.
2. Appends the user's query to the chat log.
3. Creates a chat completion request to the `Groq` client using the model `llama3-70b-8192`, including the system prompt, real-time information, and the chat log.
4. Collects the response from the chatbot and appends it to the chat log.
5. Saves the updated chat log to the JSON file.
6. Returns the modified answer without empty lines.

If an error occurs during this process, it resets the chat log and retries the query.

## Main Functionality

The main section of the code runs an infinite loop, continually prompting the user for input and printing the chatbot's response.
