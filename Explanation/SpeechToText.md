# Speech Recognition and Translation Script

## Overview

This Python script integrates Selenium WebDriver with a custom HTML page for speech recognition and translation capabilities. It uses Chrome WebDriver to interact with a locally hosted HTML file where users can speak, and their speech is recognized and optionally translated based on configuration.

## Setup

1. **Dependencies**:
   - Ensure you have Python installed on your system.
   - Install the required libraries using pip:
     ```bash
     pip install selenium webdriver-manager mtranslate-python dotenv
     ```

2. **Environment Variables**:
   - Create a `.env` file in the script's directory.
   - Add the following variables to your `.env` file:
     ```
     InputLanguage=your_input_language_code
     ```

3. **HTML Setup**:
   - The script generates a custom HTML (`Voice.html`) for speech recognition and saves it in the `Data` directory.

4. **Chrome WebDriver**:
   - The script uses Selenium with Chrome WebDriver. Ensure you have Chrome installed.
   - WebDriver is managed using `webdriver-manager` to automatically download and manage the ChromeDriver.

## Usage

1. **Running the Script**:
   - Execute the script (`speech_recognition.py`):
     ```bash
     python speech_recognition.py
     ```

2. **Interaction**:
   - The script launches a headless Chrome browser session and opens the speech recognition interface.
   - Clicking on "Start Recognition" allows users to speak, and their speech is recognized and displayed.
   - Clicking on "Stop Recognition" ends the recognition session and prints the recognized text after optionally modifying or translating it based on configuration.

## Example Interactions

- **Query**: User speaks "What is the weather today?"
  - **Response**: Recognizes the speech, modifies the query to "What is the weather today?", and prints the modified query.

- **Query**: User speaks in a language other than English.
  - **Response**: Recognizes the speech, translates it to English, modifies the translated query, and prints the modified query.

## Notes

- The script uses Selenium WebDriver to automate interactions with the speech recognition HTML page.
- Ensure your `.env` file is correctly configured with the `InputLanguage` variable.
- Modify the HTML (`Voice.html`) or script behavior as needed for specific applications or requirements.

