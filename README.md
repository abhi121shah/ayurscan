# 🌿 Āyurveda Food Scanner

Scan any food photo and get a detailed Ayurvedic analysis — doshas affected, properties, what's good/bad, and recommendations.

---

## 🚀 Deploy to Vercel (Free) — Step by Step

### Step 1: Get a Free Anthropic API Key
1. Go to https://console.anthropic.com
2. Sign up for a free account
3. Go to **API Keys** → click **Create Key**
4. Copy the key (starts with `sk-ant-...`)

> Free tier gives you $5 credit — enough for hundreds of food scans!

---

### Step 2: Deploy to Vercel

#### Option A — GitHub (Recommended)
1. Create a free account at https://github.com
2. Create a new repository, upload all these files
3. Go to https://vercel.com → sign up free with GitHub
4. Click **"Add New Project"** → import your GitHub repo
5. Click **Deploy** (don't change any settings)
6. Go to your project → **Settings** → **Environment Variables**
7. Add: `ANTHROPIC_API_KEY` = `sk-ant-your-key-here`
8. Go to **Deployments** → click **Redeploy**
9. ✅ Your app is live!

#### Option B — Vercel CLI
```bash
npm install -g vercel
cd ayurveda-scanner
vercel
# Follow prompts, then add env variable:
vercel env add ANTHROPIC_API_KEY
vercel --prod
```

---

## 📁 Project Structure

```
ayurveda-scanner/
├── public/
│   └── index.html      ← The entire frontend (one file)
├── api/
│   └── scan.js         ← Serverless function (API proxy)
├── vercel.json         ← Vercel configuration
└── README.md
```

---

## ✨ Features
- 📸 Upload or take a photo of any food
- 🌿 Dosha analysis (Vāta, Pitta, Kapha)
- 📜 Ayurvedic properties (Rasa, Vīrya, Vipāka)
- ✓/✗ Good and bad aspects per Ayurveda
- 💬 Personalized recommendation
- 🏷 Who should eat / avoid the food

---

## 🔒 Security
The API key is stored as a server environment variable — users never see it. The `api/scan.js` proxy handles all Anthropic calls server-side.
