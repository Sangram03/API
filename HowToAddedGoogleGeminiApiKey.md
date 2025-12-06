
![Image](https://cdn-ilchfdp.nitrocdn.com/hGpElsrpCSEvLMbwvQvsVGzAGjRDCWsG/assets/images/optimized/rev-d693464/delivix.digital/wp-content/uploads/2025/01/Generating-API-Key-in-Google-AI-Studio-1024x454.webp?utm_source=chatgpt.com)

![Image](https://cdn.extendoffice.com/images/stories/doc-outlook/google-key/doc-google-api-key-9.png?utm_source=chatgpt.com)

![Image](https://images.ctfassets.net/lzny33ho1g45/4Fj9xzuM4yjbkOnojSIdX7/a0a6e4a3b3c5d35a25a5c345fd628193/gemini-api-image13.png?utm_source=chatgpt.com)

![Image](https://d33v4339jhl8k0.cloudfront.net/docs/assets/589c78fadd8c8e73b3e9710e/images/6812148e9ec92547ba8e4a6d/file-nCloOuN54Q.png?utm_source=chatgpt.com)

![Image](https://miro.medium.com/0%2A-QUD9NhpK5rjHrrz?utm_source=chatgpt.com)

![Image](https://miro.medium.com/v2/resize%3Afit%3A1280/0%2AITvdqOtEK5PsH8FG?utm_source=chatgpt.com)

---

# ⭐ **How to Create Google Gemini API Keys (2025 Updated)**

## ✅ **Step 1: Open Google AI Studio**

Go to:
👉 **[https://aistudio.google.com/](https://aistudio.google.com/)**

Log in with your Google account.

---

## ✅ **Step 2: Create a New API Key**

1. On the left side, click **“Get API Key”** or **"API Keys"**
2. Click **“Create API Key”**
3. Select:

   * **“Create API Key in Google Cloud Project”**
4. Choose a project or create a new one
5. Click **Create**

Now Google will generate your **Gemini API key**.

---

## 🎉 **Your Gemini API key is ready!**

You will see something like:

```
AIzaSyD***************
```

Click **Copy**.

---

## 🔒 **Step 3: Secure Your Gemini API Key**

Gemini API Keys must be kept private.

### Store in `.env` file:

```
GEMINI_API_KEY=AIzaSyD*********
```

---

# 🚀 **How to Use Gemini API Key in Node.js**

Install SDK:

```bash
npm install @google/generative-ai
```

Use it:

```javascript
import { GoogleGenerativeAI } from "@google/generative-ai";

const genAI = new GoogleGenerativeAI(process.env.GEMINI_API_KEY);

async function run() {
  const model = genAI.getGenerativeModel({ model: "gemini-1.5-flash" });

  const result = await model.generateContent("Hello Gemini!");
  console.log(result.response.text());
}

run();
```

---

# 🌐 **Use Gemini API Key in React/Next.js**

⚠️ **Don't expose key in frontend.**
Create an API route (Next.js):

```javascript
// /app/api/gemini/route.js
import { GoogleGenerativeAI } from "@google/generative-ai";

export async function POST(req) {
  const { prompt } = await req.json();

  const genAI = new GoogleGenerativeAI(process.env.GEMINI_API_KEY);
  const model = genAI.getGenerativeModel({ model: "gemini-1.5-flash" });

  const result = await model.generateContent(prompt);
  return Response.json({ data: result.response.text() });
}
```

