# Gemini Object Identifier

A web application that uses Google's Gemini Live API to identify objects in real-time through your webcam.

## Features

- Real-time object identification using Gemini 2.0 Flash Live
- WebSocket-based streaming for low latency
- Captures and sends 1 frame per second
- Clean, modern UI with identification history

## Setup

1. Get a Gemini API key from [Google AI Studio](https://aistudio.google.com/apikey)

2. Serve the HTML file using any local server:

   ```bash
   # Using Python 3
   python -m http.server 8000

   # Using Node.js (npx)
   npx serve .

   # Using PHP
   php -S localhost:8000
   ```

3. Open http://localhost:8000 in your browser

4. Enter your API key and click "Start Identifying"

5. Hold up objects to your camera!

## How It Works

1. Connects to Gemini Live API via WebSocket
2. Captures video frames from your webcam at 1 FPS
3. Encodes frames as base64 JPEG and sends to Gemini
4. Displays Gemini's real-time object identifications

## Requirements

- Modern browser with WebSocket and getUserMedia support
- Webcam access
- Gemini API key with Live API access

## Notes

- The Gemini Live API processes video at 1 frame per second
- Your API key is only used in the browser and sent directly to Google's API
- Camera access is required for the application to work
