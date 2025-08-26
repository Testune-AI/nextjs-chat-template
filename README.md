# Next.js AI Chat App (with Testune Integration)

This is a **Next.js AI Chat App** template with built-in integration for [Testune](https://testune.xyz), making it easy to experiment with and optimize your LLM prompts.

---

## 🚀 Features

-   ⚡ Next.js 14 (App Router)
-   📝 Pre-configured Testune SDK for prompt A/B testing
-   🔑 Bring Your Own LLM API key (OpenAI)
-   📊 Feedback & analytics pipeline via Testune
-   💬 Ready-to-use chat interface

---

## 📂 Project Structure

```bash
.
├── app/                # Next.js app router pages
├── components/         # Reusable React components
├── lib/                # Testune + LLM utilities
├── styles/             # Global styles
└── package.json
```

---

## 🔧 Setup

### 1. Clone the repo

```bash
git clone https://github.com/your-org/nextjs-ai-chat-app.git
cd nextjs-ai-chat-app
```

### 2. Install dependencies

```bash
npm install
# or
yarn install
```

### 3. Configure environment variables

Create a `.env.local` file with:

```bash
NEXT_PUBLIC_TESTUNE_API_KEY=your_testune_api_key
NEXT_PUBLIC_LLM_API_KEY=your_llm_api_key
```

### 4. Run locally

```bash
npm run dev
```

---

## 📊 Using Testune

This template comes pre-wired with **Testune analytics and A/B testing** for LLM prompts.

Example usage:

```ts
import { testuneClient } from "@/lib/testune";

async function getResponse(userMessage: string) {
	const response = await testuneClient.sendMessage({
		message: userMessage,
		promptGroup: "chat-prompt-v1",
	});

	return response;
}
```

You can monitor performance and run A/B tests directly from the [Testune dashboard](https://testune.xyz).

---

## 🧑‍💻 Example Usage

1. Run the app locally (`npm run dev`).
2. Open the chat UI at [http://localhost:3000](http://localhost:3000).
3. Enter a message and see the Testune-powered LLM respond.
4. Check the dashboard for analytics.

---

## 📜 License

MIT License. See [LICENSE](./LICENSE) for details.
