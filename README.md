# Vishal Portfolio - Next.js Setup & Deployment

This is the source code for Vishal's Portfolio project, built with Next.js and styled for a dynamic, professional experience. 

## 🚀 Setting up GitHub Pages (For Deployment)

This project is perfectly pre-configured to automatically build and deploy to **GitHub Pages** using GitHub Actions, and specifically to map to the custom domain `vishalanivilla.studio`. 

When you fork or push this repository to your own GitHub account, follow these exact steps to make it go live:

### 1. Enable GitHub Actions for Pages
- Open your GitHub repository in the browser.
- Go to the **Settings** tab at the top.
- On the left sidebar, click **"Pages"**.
- Under **Build and deployment -> Source**, change the dropdown from "Deploy from a branch" to **"GitHub Actions"**.
- _(GitHub will now automatically read the `.github/workflows/nextjs.yml` file and start building the site.)_

### 2. Configure the Custom Domain in GitHub
- On the same **Settings -> Pages** screen, scroll down to the **"Custom domain"** section.
- Type `vishalanivilla.studio` and click **Save**.
- Wait for a DNS check to appear. GitHub will start generating an SSL/HTTPS certificate.

### 3. Connect your DNS Records (Domain Provider)
- Log in to your domain provider (where you bought `vishalanivilla.studio`, e.g., GoDaddy, Namecheap, Route53).
- Go to the **DNS Management / Nameservers** section.
- Add these **A Records** (Points your root domain directly to GitHub):
  - Type: `A` | Host/Name: `@` (or leave blank) | Value: `185.199.108.153`
  - Type: `A` | Host/Name: `@` (or leave blank) | Value: `185.199.109.153`
  - Type: `A` | Host/Name: `@` (or leave blank) | Value: `185.199.110.153`
  - Type: `A` | Host/Name: `@` (or leave blank) | Value: `185.199.111.153`
- Add a **CNAME Record** (To redirect the www version):
  - Type: `CNAME` | Host/Name: `www` | Value: `<YOUR-GITHUB-USERNAME>.github.io` (Replace `<YOUR-GITHUB-USERNAME>` with your exact GitHub username)

Once you've done this, it may take anywhere from 15 minutes to a few hours for the DNS changes to fully propagate worldwide and the SSL certificate to be provisioned.

---

## 🛠️ Local Development

If you'd like to run or test the project locally on your machine:

1. Make sure you have [Node.js](https://nodejs.org/en/) installed.
2. Clone this repository locally.
3. Open a terminal in the project folder and run:
   ```bash
   npm install
   ```
4. Start the development server:
   ```bash
   npm run dev
   ```
5. Open [http://localhost:3000](http://localhost:3000) with your browser.

The page will auto-update as you edit files, typically found inside the `src/` or `app/` folder.
