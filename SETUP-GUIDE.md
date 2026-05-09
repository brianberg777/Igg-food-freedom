# 🌻 IgG Food Freedom — Setup Guide
## (Written for non-technical people — you've got this!)

---

## What you have in this folder:
```
📁 igg-food-freedom/
   📁 api/
      📄 analyze.js      ← The secret kitchen (holds your API key)
   📁 public/
      📄 index.html      ← Your app (what customers see)
   📄 vercel.json        ← Tells Vercel how everything connects
   📄 SETUP-GUIDE.md     ← This file!
```

---

## STEP 1 — Get Your Anthropic API Key (5 minutes)

1. Go to **console.anthropic.com**
2. Click **Sign Up** (it's free to create an account)
3. Once logged in, click **API Keys** in the left menu
4. Click **Create Key**, give it a name like "IgG App"
5. Copy the key — it looks like: `sk-ant-api03-xxxxx...`
6. **Save it somewhere safe** — you only see it once!

💳 You'll need to add a credit card. Each analysis costs about **1–3 cents**.
For 100 customers using it once a day = roughly **$1–3/day** in API costs.

---

## STEP 2 — Create a Free Vercel Account (2 minutes)

1. Go to **vercel.com**
2. Click **Sign Up**
3. Sign up with your Google or GitHub account (easiest)
4. You're in! Vercel's free tier handles thousands of visits per month.

---

## STEP 3 — Install Git (one time only, 3 minutes)

Git is a free tool that sends your files to Vercel.

1. Go to **git-scm.com/downloads**
2. Download and install for your computer (Windows/Mac/Linux)
3. During install, just click Next/Continue for everything — defaults are fine

---

## STEP 4 — Deploy Your App (5 minutes)

### On a Mac:
1. Open the **Terminal** app (search for it in Spotlight)

### On Windows:
1. Open **Command Prompt** (search "cmd" in Start menu)

### Then type these commands one at a time, pressing Enter after each:

```
cd Desktop
```
*(or wherever you saved your igg-food-freedom folder)*

```
cd igg-food-freedom
```

```
npx vercel
```

**If it asks to install Vercel CLI:** type `y` and press Enter

**Follow the prompts:**
- "Set up and deploy?" → Press Enter (Yes)
- "Which scope?" → Press Enter (your account)
- "Link to existing project?" → Type `n`, press Enter
- "Project name?" → Type `igg-food-freedom`, press Enter
- "Directory?" → Press Enter (it'll find the folder)
- "Override settings?" → Type `n`, press Enter

⏳ Wait about 30 seconds... then it'll show you a URL like:
**`https://igg-food-freedom.vercel.app`**

🎉 **Your app is live!** But it won't work yet — you need to add your secret API key in Step 5.

---

## STEP 5 — Add Your Secret API Key to Vercel (3 minutes)

This is how you put your Anthropic key safely on the server
so customers never see it.

1. Go to **vercel.com** and log in
2. Click on your **igg-food-freedom** project
3. Click **Settings** (top menu)
4. Click **Environment Variables** (left menu)
5. Click **Add New**:
   - **Key:** `ANTHROPIC_API_KEY`
   - **Value:** paste your `sk-ant-api03-xxxxx...` key
   - Make sure **Production** is checked
6. Click **Save**
7. Go back to your project and click **Redeploy** → **Redeploy** again

✅ Now your app is fully working!

---

## STEP 6 — Test It!

1. Open your Vercel URL (e.g. `https://igg-food-freedom.vercel.app`)
2. Upload a test image of any food sensitivity results
3. Hit Analyze — you should get a beautiful meal plan!

---

## GIVING CUSTOMERS YOUR APP

Just share your Vercel URL! That's it. No downloads, no installs.
They open it on any phone or computer and it just works.

**Want a custom domain** like `www.myfoodapp.com`?
- Buy a domain at **namecheap.com** (~$12/year)
- In Vercel → Settings → Domains → Add your domain
- Vercel gives you step-by-step instructions to connect it

---

## MONITORING YOUR COSTS

- Vercel dashboard shows how many times the app was used
- Anthropic dashboard (console.anthropic.com) shows your API spend
- Set a **spending limit** in Anthropic console → Settings → Limits
  (e.g. max $20/month so you're never surprised)

---

## NEED HELP?

If something isn't working, the most common fixes are:
1. ✅ Check your API key is correct in Vercel Environment Variables
2. ✅ Make sure you redeployed after adding the key
3. ✅ Check your Anthropic account has a payment method added

---

*Built with 🌻 — You've got this!*
