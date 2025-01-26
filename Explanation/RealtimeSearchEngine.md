# Realtime Information Chatbot

## Overview

This Python script acts as a Realtime Information Chatbot utilizing the Groq API and Google Search to provide up-to-date answers and information based on user queries.

## Setup

1. **Dependencies**:
   - Ensure you have Python installed on your system.
   - Install the required libraries using pip:
     ```bash
     pip install groq googlesearch-python-dotenv
     ```

2. **Environment Variables**:
   - Create a `.env` file in the script's directory.
   - Add the following variables to your `.env` file:
     ```
     Username=your_username
     Assistantname=your_assistant_name
     GroqAPIKey=your_groq_api_key
     ```

3. **Data Storage**:
   - The script uses a `ChatLog.json` file in the `Data` directory to store chat history.

## Usage

1. **Running the Script**:
   - Execute the script (`realtime_chatbot.py`):
     ```bash
     python realtime_chatbot.py
     ```

2. **Interaction**:
   - Enter your query when prompted (`Enter your query:`).
   - The script will perform a Google search for the query and provide real-time information.
   - It uses the Groq API to generate responses in a conversational format with proper grammar and punctuation.

## Example Interactions

- **Query**: `What is the current time in New York?`
  - **Response**: Provides the current time with professional formatting.

- **Query**: `Tell me about recent developments in artificial intelligence.`
  - **Response**: Retrieves Google search results about recent AI developments.

## Notes

- The script leverages the Groq API for generating natural language responses.
- Ensure your `.env` file is correctly configured with your Groq API key and other variables.
- `ChatLog.json` stores conversation history to maintain context across interactions.

