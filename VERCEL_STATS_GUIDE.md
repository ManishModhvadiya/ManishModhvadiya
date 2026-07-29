# 🚀 Vercel Self-Hosting Guide for GitHub Readme Stats

To prevent hitting public API rate limits on `github-readme-stats` and to ensure your GitHub profile stats card renders 100% reliably 24/7, self-hosting on Vercel is the recommended industry standard.

---

## 📋 Step-by-Step Deployment Instructions

### Step 1: Fork the Official Repository
1. Open the official repository: [github-readme-stats](https://github.com/anuraghazra/github-readme-stats).
2. Click **Fork** in the top-right corner to create your own copy under your GitHub account (`ManishModhvadiya/github-readme-stats`).

### Step 2: Create a Personal Access Token (PAT)
1. Go to your GitHub **Settings** &rarr; **Developer Settings** &rarr; **Personal Access Tokens** &rarr; **Tokens (classic)**.
2. Click **Generate new token (classic)**.
3. Set Note to `Vercel GitHub Readme Stats`.
4. Select Scopes:
   - `repo` (Full control of private repositories - optional, for accurate stat counting)
   - `read:user` (Read all user profile data)
5. Click **Generate token** and copy your token value (e.g. `ghp_xxxxxxxxxxxxxxxxxxxx`).

### Step 3: Deploy to Vercel
1. Log in or create a free account at [Vercel.com](https://vercel.com).
2. Click **Add New** &rarr; **Project**.
3. Import your forked repository (`github-readme-stats`).
4. In the **Environment Variables** section during setup, add:
   - **Key:** `PAT_1`
   - **Value:** `ghp_xxxxxxxxxxxxxxxxxxxx` (Your generated GitHub token)
5. Click **Deploy**.

### Step 4: Update Your README Links
Once deployed, Vercel will grant you a custom domain (e.g., `https://github-readme-stats-manish.vercel.app`).
Replace the standard API domain in your `README.md` with your Vercel URL:

```markdown
<img src="https://YOUR-VERCEL-DOMAIN.vercel.app/api?username=ManishModhvadiya&show_icons=true&theme=dark&bg_color=020617&title_color=00FF88&text_color=F8FAFC&icon_color=00E5FF&border_color=00FF88&border_radius=8" width="48%"/>
```

---

## ✅ Benefits of Self-Hosting
- **0 Rate Limits:** Your stats will load instantly without 429 Too Many Requests errors.
- **Private Repository Support:** Accurately counts commits across all your private and public repositories.
- **100% Uptime:** Powered by Vercel serverless edge infrastructure.
