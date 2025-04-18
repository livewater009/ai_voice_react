# AI Voice convertor In react

This is a React application that allows users to engage in voice-based conversations with AI personalities. Users can create their own distinct AI personality and experience real-time, interactive conversations with AI.

- Voice-based conversations with AI
- Customizable AI personality prompt
- Real-time, interactive communication
- Responsive and user-friendly interface
- Compatible with various devices and screen sizes
  <br><br>

## Prerequisites

Ensure that you have the following prerequisites installed and set up on your system:

1. **Node.js**: The application is built using Node.js, so you need to have it installed on your machine. You can download the latest version of Node.js from the [official website](https://nodejs.org/).

2. **Amazon AWS Polly API Key**: The voice output feature of the application utilizes Amazon AWS Polly, a text-to-speech service. To use AWS Polly, sign up for an AWS account, and follow the steps to create an IAM user with the required permissions. Once you have your IAM user, set up your AWS credentials in the `.env` file of the application. You can refer to the [official AWS Polly documentation](https://docs.aws.amazon.com/polly/latest/dg/get-started-quick.html) for more information.

3. **OpenAI API Key**: The application requires an OpenAI API key for AI integration (Chat-GPT and Whisper Transcription). Sign up for an OpenAI account and obtain an API key from the [OpenAI Developer Dashboard](https://beta.openai.com/signup/). Once you have your API key, set it up in the `.env` file of the application.

## Getting Started

```bash
# Clone repository
git clone https://github.com/darrylschaefer/voice-ai-react

# Change directory
cd voice-ai-react

# Install dependencies
npm install

# Add API keys to .env in root folder
AMAZON_AWS_POLLY_ACCESS_KEY=
AMAZON_AWS_POLLY_SECRET_KEY=
OPENAI_API_KEY=

# Build app
npm run build

# Start app
npm start

# Open client
Start your internet browser, and type in the address: http://localhost:3000
```

## Getting Started with the Application

1. **Configure API keys:** Make sure your API keys are properly set up in the application.

2. **Set your prompt <i>(optional)</i>:** Open the prompt dialog box to modify the default prompt.

3. **Initiate a session:** Type your message in the text input and press enter, or click the microphone icon to send a voice message.

4. **Understand the three phases:**

   - **User Input Phase:** The microphone is ready, it will capture your voice input to send it to the AI for processing once you begin talking.

   - **AI Processing phase:** Your recording is being handled by the APIs.

   - **AI Playing phase:** The generated response is played back to you.

5. **Engage with the AI:** By default, the application will automatically cycle through the phases. Be ready to respond to AI when it's your turn.

6. **Control the pace (optional):** If you need more time to respond, disable Automatic Detection and manually put the application into standby mode by clicking the microphone button when it's your turn.

7. **Speak in complete sentences:** For better transcription and understanding, use complete sentences when engaging with the AI.

## Options Menu

Find the options menu below the console with these available features:

- **Abandon Session**: Reset the session
- **Voices**: Change the AWS Polly voice
- **Personality Type**: The type of personality that the interviewer will have.
- **Automatic Detection**: Sets recording mode to standby after AI finishes playing their audio prompt. If you turn this off, you will have to click the Microphone button after the AI has spoken in order to set the Mic to standby and begin a recording.
- **Voice Threshold**: This slider sets the minimum volume level needed to trigger a recording from standby mode. Adjust based on background noise & experiment for best results.
- **Mic Pause Timer**: This slider sets the delay after a recording dips below the Volume Threshold that will trigger an automatic completion of the user recording.

## Microphone Statuses:

1. **Orange Border**: _Standby mode_ - awaiting voice to surpass the Voice Threshold and initiate recording.
2. **Red Border**: _Recording in progress_ - triggered by exceeding Voice Threshold, and will stop when volume falls below the threshold for the Mic Pause Timer duration.
3. **Grey Border**: _Inactive_ - AI is currently processing the conversation.
4. **White Border**: _Inactive_ - no session in progress.
