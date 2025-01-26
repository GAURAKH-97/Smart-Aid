# Text-to-Speech (TTS) Conversion with Audio Playback

## Overview

This Python script utilizes `edge_tts` and `pygame` libraries to convert text into speech (Text-to-Speech) and play the generated audio file. It includes functionality to handle long texts and provide additional responses when necessary.

## Setup

1. **Dependencies**:
   - Ensure you have Python installed on your system.
   - Install the required libraries using pip:
     ```bash
     pip install pygame asyncio edge-tts mtranslate-python dotenv
     ```

2. **Environment Variables**:
   - Create a `.env` file in the script's directory.
   - Add the following variables to your `.env` file:
     ```
     AssistantVoice=your_assistant_voice
     ```

3. **Audio Setup**:
   - The script saves the generated audio file (`speech.mp3`) in the `Data` directory.

## Usage

1. **Running the Script**:
   - Execute the script (`text_to_speech.py`):
     ```bash
     python text_to_speech.py
     ```

2. **Interaction**:
   - Enter the text when prompted (`Enter the text:`).
   - The script converts the text to speech and plays the audio using `pygame`.
   - Handles long texts by speaking only the first few sentences and providing additional responses for the remainder.

## Example Interactions

- **Text**: User enters a long text exceeding 250 characters.
  - **Response**: The script speaks the first two sentences and adds a random response indicating more information is available on the screen.

- **Text**: User enters a short text.
  - **Response**: The script directly converts and plays the text as speech using `pygame`.

## Notes

- Ensure your `.env` file is correctly configured with the `AssistantVoice` variable.
- Modify the script as needed to adjust voice settings, responses, or integrate with other services.
- The script uses `edge_tts` for text-to-speech conversion and `pygame` for audio playback.

