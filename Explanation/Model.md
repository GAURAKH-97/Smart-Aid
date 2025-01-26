# Decision-Making Model (DMM) Script

## Overview

This Python script serves as a Decision-Making Model (DMM) designed to interpret user queries and route them to appropriate actions or responses based on predefined rules and categories.

## Setup

1. **Dependencies**:
   - Ensure you have Python installed on your system.
   - Install the required libraries using pip:
     ```bash
     pip install cohere rich python-dotenv
     ```

2. **Environment Variables**:
   - Create a `.env` file in the script's directory.
   - Add your API key for the Cohere API in the `.env` file:
     ```
     CohereAPIKey=your_cohere_api_key_here
     ```

## Usage

1. **Running the Script**:
   - Execute the script (`decision_making_model.py`):
     ```bash
     python decision_making_model.py
     ```

2. **Interaction**:
   - The script will continuously prompt for user input (`>>> `).
   - Enter your query or command and press Enter.
   - The script will categorize the query and generate an appropriate response based on predefined rules.

## Example Interactions

- **Query**: `how are you?`
  - **Response**: `general how are you?`

- **Query**: `open chrome and tell me about Mahatma Gandhi.`
  - **Response**: `open chrome, general tell me about Mahatma Gandhi.`

- **Query**: `what is today's date and remind me that I have a dancing performance on 5th Aug at 11pm.`
  - **Response**: `general what is today's date, reminder 11:00pm 5th Aug dancing performance`

## Notes

- The script uses the Cohere API for natural language processing.
- Ensure your `.env` file is correctly configured with your Cohere API key.
- The `ChatHistory` variable maintains context across interactions for improved response relevance.


