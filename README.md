基于项目：https://github.com/livekit-examples/realtime-playground

填入你的baseurl和填入openai-key，即可开启你的实时语音对话旅程。

如何使用：
1. 注册并创建一个app --> https://cloud.livekit.io
2. 创建.env文件，并把环境变量填上，具体环境变量参考下方
3. docker compose up -d

LIVEKIT_URL=wss://xxx.livekit.cloud
LIVEKIT_API_KEY=xxx
LIVEKIT_API_SECRET=xxx

# LiveKit + OpenAI Realtime Playground

This project is an interactive playground that demonstrates the capabilities of OpenAI's Realtime API, allowing users to experiment with the API directly in their browser. It's built on top of LiveKit Agents.

See it in action at [realtime-playground.livekit.io](https://realtime-playground.livekit.io)

## Repository Structure

### /agent

This directory contains the agent implementation. There are two versions, one in Python and one in TypeScript.

1. `playground_agent.py` - Built on the LiveKit [Python Agents framework](https://github.com/livekit/agents)
2. `playground_agent.ts` - Built on the LiveKit [Node.js Agents framework](https://github.com/livekit/agents-js)

### /web

This directory houses the web frontend, built with Next.js.

## Prerequisites

- Node.js and pnpm (for web frontend and Node.js agent)
- Python 3.9 or higher (for Python agent)
- pip (Python package installer)
- LiveKit Cloud or self-hosted LiveKit server

## Getting Started

### Agent Setup

1. Navigate to the `/agent` directory
2. Copy the sample environment file: `cp .env.sample .env.local`
3. Open `.env.local` in a text editor and enter your LiveKit credentials

#### Python Version

1. Create a virtual environment: `python -m venv .venv`
2. Activate the virtual environment:
   - On macOS and Linux: `source .venv/bin/activate`
   - On Windows: `.venv\Scripts\activate`
3. Load the environment variables:
   - On macOS and Linux: `source .env.local`
   - On Windows: `set -a; . .env.local; set +a`
4. Install dependencies: `pip install -r requirements.txt`
5. Run the agent in development mode: `python playground_agent.py dev`

#### Node.js Version

1. Install dependencies: `pnpm install`
2. Run the agent in development mode: `pnpm dev`

### Web Frontend Setup

1. Navigate to the `/web` directory
2. Copy the sample environment file: `cp .env.sample .env.local`
3. Open `.env.local` in a text editor and enter your LiveKit credentials:
4. Install dependencies: `pnpm install`
5. Run the development server: `pnpm dev`
6. Open [http://localhost:3000](http://localhost:3000) in your browser

## Deployment

The agent can be deployed in a variety of ways: [Deployment & Scaling Guide](https://docs.livekit.io/agents/deployment/)

The web frontend can be deployed using your preferred Next.js hosting solution, such as [Vercel](https://vercel.com/).

## Troubleshooting

Ensure the following:

- Both web and agent are running
- Environment variables are set up correctly
- Correct versions of Node.js, pnpm, and Python are installed

## Additional Resources

For more information or support, please refer to [LiveKit docs](https://docs.livekit.io/).

## License

Apache 2.0
