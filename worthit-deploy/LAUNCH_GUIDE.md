# Worth It? — Complete Launch Guide
## From files on your computer → live worldwide in 30 minutes

---

## PART 1: Deploy the Website (15 minutes, free forever)

### Step 1 — Get your Claude API key
1. Go to https://console.anthropic.com
2. Sign up / log in
3. Click "API Keys" → "Create Key"
4. Copy the key (starts with sk-ant-...)
5. Keep it safe — you'll use it in Step 4

### Step 2 — Create a free Vercel account
1. Go to https://vercel.com
2. Sign up with GitHub (easiest) or email
3. It's completely free for this

### Step 3 — Upload your files
Option A (Easiest — drag and drop):
1. Go to https://vercel.com/new
2. Click "Browse" or drag the entire `worthit-deploy` folder
3. Vercel detects it automatically

Option B (Via GitHub — recommended for updates):
1. Create a free GitHub account at github.com
2. Create a new repository called "worthit"
3. Upload all files from the `worthit-deploy` folder
4. In Vercel, click "Import Git Repository"
5. Select your "worthit" repo
6. Click Deploy

### Step 4 — Add your API key (CRITICAL)
1. In Vercel, go to your project → Settings → Environment Variables
2. Click "Add New"
3. Name: ANTHROPIC_API_KEY
4. Value: paste your API key from Step 1
5. Click Save
6. Go to Deployments → click the three dots → Redeploy

### Step 5 — Your site is live!
Your URL will be: https://worthit-[random].vercel.app
Or set a custom domain in Vercel settings for ~$10/year

Custom domain ideas:
- worthit.app (check availability at namecheap.com)
- isthisworthit.com
- worthitcheck.com

---

## PART 2: Submit Chrome Extension (1 week, $5 one-time)

### Step 1 — Generate icons
Go to https://favicon.io or https://www.canva.com
Create a simple icon (the ✦ symbol on dark purple background)
Export as:
- icon16.png (16x16px)
- icon48.png (48x48px)  
- icon128.png (128x128px)
Put all three in the `worthit-extension/icons/` folder

### Step 2 — Update your website URL
Open `popup.js` and replace both instances of:
  https://YOUR-APP.vercel.app
With your real Vercel URL from Part 1

### Step 3 — Package the extension
1. Open Chrome → go to chrome://extensions
2. Toggle "Developer mode" ON (top right)
3. Click "Load unpacked"
4. Select your `worthit-extension` folder
5. Test it! Go to amazon.com and look for the floating ✦ button
6. Click the extension icon in your toolbar to test the popup

### Step 4 — Submit to Chrome Web Store
1. Go to https://chrome.google.com/webstore/devconsole
2. Pay the $5 one-time developer fee
3. Click "Add new item"
4. Zip your `worthit-extension` folder → upload the .zip
5. Fill in:
   - Name: Worth It? — AI Shopping Gut-Check
   - Description: Instant AI verdict on any product. Worth It, Skip It, or Wait.
     Analyzes price value, review quality, and your personal context.
   - Category: Shopping
   - Screenshots: take 2-3 screenshots of your popup working
6. Submit for review (takes 2-7 business days)

---

## PART 3: Monetization Setup (Do this week 2)

### Free tier vs Pro
Current app = unlimited free (good for launch, gets users)

To add paid tier later:
1. Create account at https://stripe.com
2. Add a "Go Pro — $4.99/month" button to your site
3. Free users get 5 checks/month, Pro = unlimited

### Track usage
Add free analytics:
1. Create account at https://plausible.io or https://umami.is (privacy-friendly, free)
2. Add their 1-line script to your index.html before </body>
3. See which countries, how many daily users, what they click

---

## PART 4: Launch Strategy (Week 1)

### Day 1 — Post everywhere
Post this exact message:

"I built a free AI tool that tells you if something is actually worth buying.
Paste any Amazon/Target link → get WORTH IT, SKIP IT, or WAIT in 10 seconds.
It calculates cost-per-use, checks if reviews are fake, and gives you one honest verdict.
Try it: [YOUR URL]"

Post on:
- Reddit: r/frugal, r/personalfinance, r/shutupandtakemymoney, r/productivity
- Twitter/X with a screen recording
- TikTok showing it analyzing a product in real time
- Product Hunt (https://producthunt.com) — submit Monday morning 12:01am PST

### Week 1 goal: 500 users
If you hit 500 users organically, you have proof. Then:
- Submit Chrome extension
- Start charging $4.99/month for unlimited
- Consider iOS app

---

## COSTS SUMMARY

| Item | Cost |
|------|------|
| Vercel hosting | FREE |
| Claude API (per analysis) | ~$0.003 per check |
| Chrome Web Store | $5 one-time |
| Custom domain (optional) | ~$10-15/year |
| Apple Developer (iOS later) | $99/year |
| **Total to launch** | **$5** |

At 1,000 users doing 5 checks/month = 5,000 API calls = ~$15/month in API costs
At $4.99/month with 100 paying users = $499 MRR → profit from month 1

---

## YOU'RE READY. SHIP IT.
