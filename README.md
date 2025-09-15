# GPT-Realtime + WebRTC + Next.js 15 + Azure AI Foundry

This is a WebRTC-based Voice AI stream application using `OpenAI`'s `Realtime API` and `WebRTC`. Project contains `/api` route and UI components developed with `Next.js` and `shadcn/ui`. It supports real-time audio conversations implemented in [skrivov/openai-voice-webrtc-next](https://github.com/skrivov/openai-voice-webrtc-next) with the addition of a hook to abstract the WebRTC handling.

This repository has been customised to run against Azure AI Foundry (Azure OpenAI) deployments - configuration examples below show the endpoint, API key and realtime model deployment name needed to connect to an AI Foundry realtime model.

https://github.com/user-attachments/assets/ea9324af-5c18-48d2-b980-2b81baeea4c0

## Features

- **Next.js Framework**: Built with Next.js for server-side rendering and API routes.
- **Modern UI**: Animated using Tailwind CSS & Framer Motion & shadcn/ui.
- **Use-WebRTC Hook**: A hook to abstract the OpenAI WebRTC handling.
- **Tool Calling**: 6 example functions to demonstrate client side tools along with Realtime API: `getCurrentTime`, `partyMode`, `changeBackground`, `launchWebsite`, `copyToClipboard`, `scrapeWebsite` (requires FireCrawl API key)
- **Localization**: Select language for app strings and the voice agent (English, Spanish, French, Chinese)
- **Type Safety**: TypeScript with strict eslint rules (optional)

## Requirements

- **Deno runtime** or **Node.js**
- Azure AI Foundry (Azure OpenAI) endpoint, deployment name and API key configured in `.env` (see below)

## Installation

### 1. Clone the Repository

```bash
git clone https://github.com/cameronking4/openai-realtime-api-nextjs.git
cd openai-realtime-api-nextjs
```

### 2. Environment Setup

Create a `.env` file in the root directory:

```env
# Note: This is the Azure OpenAI endpoint of your AI Foundry resource, NOT the AI Foundry endpoint.
FOUNDRY_OPEN_AI_ENDPOINT=

# Note: This is the API key for your AI Foundry resource.
FOUNDRY_KEY=

# Note: This is the model deployment name of your realtime model (e.g. gpt-realtime).
MODEL_NAME=
```

### 3. Install Dependencies

If using **Node.js**:

```bash
npm install
```

If using **Deno**:

```bash
deno install
```

### 4. Run the Application

#### Using Node.js:

```bash
npm run dev
```

#### Using Deno:

```bash
deno task start
```

The application will be available at `http://localhost:3000`.

## Usage

1. Open the app in your browser: `http://localhost:3000`.
2. Select a voice and start the audio session.

## Deploy to Vercel

**Deploy in one-click**

[![Deploy with Vercel](https://vercel.com/button)](<https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2Fcameronking4%2Fopenai-realtime-api-nextjs&env=FOUNDRY_KEY&envDescription=OpenAI%20Key%20(Realtime%20API%20Beta%20access)&envLink=https%3A%2F%2Fplatform.openai.com%2Fapi-keys&project-name=openai-rt-shadcn&repository-name=openai-realtime-api-nextjs-clone&demo-title=OpenAI%20Realtime%20API%20(WebRTC)%20x%20shadcn%2Fui&demo-description=Next.js%2015%20template%20to%20create%20beautiful%20Voice%20AI%20applications%20with%20OpenAI%20Realtime%20API%20Beta&demo-url=https%3A%2F%2Fopenai-rt-shadcn.vercel.app&demo-image=http%3A%2F%2Fopenai-rt-shadcn.vercel.app%2Fdemo.gif>)

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

## Acknowledgements

- [OpenAI](https://openai.com/) for their API and models.
- [Next.js](https://nextjs.org/) for the framework.
- [Tailwind CSS](https://tailwindcss.com/) for styling.
- [Simon Willison’s Weblog](https://simonwillison.net/2024/Dec/17/openai-webrtc/) for inspiration
- [Originator: skrivov](https://github.com/skrivov/openai-voice-webrtc-next) for the WebRTC and Nextjs implementation
