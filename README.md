# Nagad Digital Financial Services - Interactive Mobile Prototype

A high-fidelity, responsive interactive prototype of the **Nagad MFS Mobile Application** featuring e-KYC registration, biometric onboarding (Apple Face ID & Google Android Fingerprint), account recovery, and dual-state Base UI (Guest Mode vs. Authenticated User Mode).

---

## 🚀 Instant Deployment on Vercel (First-Time Success Guaranteed)

This project is pre-configured for **zero-configuration instant static deployment** on [Vercel](https://vercel.com).

### Method 1: Deploy via GitHub (Recommended)

1. **Push this folder to a GitHub Repository**:
   ```bash
   git init
   git add .
   git commit -m "Initial commit: Nagad prototype ready for Vercel"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<your-repo-name>.git
   git push -u origin main
   ```

2. **Import to Vercel**:
   - Log in to your [Vercel Dashboard](https://vercel.com).
   - Click **Add New... > Project**.
   - Select your GitHub repository and click **Import**.

3. **Deploy Settings**:
   - **Framework Preset**: `Other` *(Auto-detected)*
   - **Root Directory**: `./` *(Default)*
   - **Build Command**: *(Leave empty)*
   - **Output Directory**: *(Leave empty)*
   - Click **Deploy**.

Your prototype will be live globally on a free `*.vercel.app` domain in less than 10 seconds!

---

### Method 2: Deploy via Vercel CLI

If you have Node.js and the Vercel CLI installed:

```bash
# 1. Install Vercel CLI globally (if not already installed)
npm i -g vercel

# 2. Deploy from this project directory
vercel

# 3. Follow terminal prompts:
# ? Set up and deploy? [Y/n] y
# ? Which scope? (select your account)
# ? Link to existing project? [y/N] n
# ? What's your project's name? nagad-prototype
# ? In which directory is your code located? ./
# ? Want to modify these settings? [y/N] n
```

To deploy directly to production:
```bash
vercel --prod
```

---

## 🛠️ Project Structure & Configuration

```text
├── index.html                    # Primary static entry point for Vercel
├── nagad-prototype.html          # Prototype source file (synced with index.html)
├── vercel.json                   # Vercel configuration (clean URLs, rewrites, security & cache headers)
├── package.json                  # Project metadata
├── .gitignore                    # Ignored artifacts & build caches
├── new-logo.14fe8a5.png          # Nagad official branding asset
├── Grameenphone_Logo_GP_Logo...  # Operator branding asset (GP)
├── banglalink.svg                # Operator branding asset (Banglalink)
├── robi-logo.svg                 # Operator branding asset (Robi)
├── Cirkle_logo.svg.webp          # Operator branding asset (Cirkle/Airtel)
└── teletalk.png                  # Operator branding asset (Teletalk)
```

---

## 📱 Core Features Tested & Ready

1. **e-KYC Onboarding**:
   - Dynamic operator selection (GP, Banglalink, Robi, Cirkle, Teletalk) with validation.
   - Dual-side NID scanning with automated contour detection.
   - Profile demographic fields (Gender, Income Source, Monthly Income, Occupation).
   - 3-rule selfie guideline screen + animated liveness detection scan.
   - Comprehensive e-KYC preview & confirmation overview screen.

2. **Nagad 5-Digit PIN Security & Device Switcher**:
   - 5-digit PIN creation with sequence & repetition validation.
   - Explicit two-step confirmation buttons.
   - Instant live switcher between **Apple iPhone 18 Pro** (Face ID) and **Google Pixel 11 Pro** (Fingerprint).

3. **Android Forgot PIN & Reset Journey**:
   - "Forgot PIN?" on login screen -> "Reset PIN" option selection.
   - Android SMS auto-fill simulation for 6-digit OTP with gated confirmation button.
   - Face liveness scanning according to instructions.
   - "Wait without closing the app" status progress timeline.
   - Compact zero-scroll Temporary PIN screen (`74921`).
   - New 5-digit PIN setup & confirmation redirecting back to login.

4. **Nagad Base UI (Dual-Mode Home Dashboard)**:
   - **Guest Explorer Mode**: Locked balance pill, 8 core services with `🔒` lock badges, onboarding cashback promo, and quick login CTA.
   - **Authenticated User Mode**: Active user profile (`মো: আরিফুল ইসলাম • ০১৭১২-৩৪৫৬৭৮`), interactive tap-to-reveal balance (`৳ ২৫,৪৫০.০০`), 8 unlocked active services, and live recent transactions.
   - **Inline Demo Switcher Pill**: Instant 1-click toggle between Guest and User modes.
