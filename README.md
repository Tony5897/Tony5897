# Tony Martinez
### Frontend Developer · Portland, OR · Browser Platforms, Product UI, and AI-Integrated Web Systems

Production-grade web products where interface quality, browser behavior, and real implementation detail matter. Work at the intersection of frontend engineering, browser extension architecture, AI-assisted systems, and cross-platform debugging — especially when a polished UI still has to survive real device constraints, service worker lifecycles, and production deployment realities.

**[Portfolio](https://www.tonymartinez.tech)** · **[LinkedIn](https://www.linkedin.com/in/tonymartinezpdx/)** · **[Email](mailto:hello@tonymartinez.tech)**

---

## Current Focus

- **Browser-platform engineering:** Building Chrome Manifest V3 extensions, service-worker-driven workflows, isolated UI injection, and frontend systems that have to work inside real browser constraints.
- **AI-integrated product systems:** Using models as part of the product stack where they support workflow quality, reasoning, and UX — not as a substitute for real implementation or human evidence.
- **Cross-platform debugging:** Solving browser- and device-specific issues on physical hardware using Safari Web Inspector, ngrok, and live debugging workflows across iPhone, Safari, WebGL, and media/runtime edge cases.
- **Release-minded frontend systems:** Shipping with TypeScript, testing, CI, and production behavior in mind — treating maintainability, debuggability, and deployment quality as part of the product.

---

## Stack

| Domain | Technologies | Focus |
| :--- | :--- | :--- |
| **Frontend Engineering** | React, Next.js, TypeScript, Tailwind CSS | Component systems, state flow, performance-minded frontend architecture |
| **Browser Platform** | Chrome MV3, Service Workers, MutationObserver, Shadow DOM, Web APIs | Extension lifecycle, DOM orchestration, isolated UI injection |
| **AI & Media** | Gemini, OpenAI, MediaPipe, Google Cloud TTS | AI-assisted product workflows, multimodal analysis, voice features |
| **Mobile & Debugging** | Safari Web Inspector, ngrok, iPhone camera handling | Real-device debugging, mobile QA, browser/runtime troubleshooting |
| **Ops & Quality** | Vitest, Jest, GitHub Actions, Husky | Linting, automated tests, CI discipline, release-minded workflows |

---

## Projects

### [AptivAI](https://github.com/Tony5897/aptiv-analytics) — Pre-Send Email Testing Platform *(In Progress)*

AptivAI is being re-centered around **Signal Lab**: a pre-send email testing workflow where users create email variants, generate reviewer links, capture human-response signals, compare outcomes, and improve copy before launch.

**The Product Direction:**  
Instead of treating AI as the source of truth, AptivAI is moving toward a system where **human evidence comes first**. The strongest version of the product is not a generic AI email analytics platform. It is a **structured experimentation product** for trust, clarity, and action intent before an email is sent.

**The Stack:** React + TypeScript frontend, Node.js/Express backend, MongoDB, Firebase Auth, Gemini API, Google Cloud TTS, and MediaPipe.

**What makes it hard:**
- **Signal Lab architecture:** building tests, variants, reviewer sessions, public tokenized review links, event capture, survey collection, and comparison reporting without tearing apart the broader app
- **Public reviewer session flow:** secure token handling, expiration, stateful session tracking, and event capture without requiring reviewer authentication
- **Additive product evolution:** reshaping a broader analytics prototype into a sharper product while preserving working flows like the dashboard assistant and existing authenticated product areas
- **Cross-platform complexity:** earlier multimodal and browser/device-specific work introduced real debugging constraints, especially across Safari/iPhone behavior and client-side runtime handling

**The Result:**  
AptivAI is evolving into a more credible software product: **variant creation, reviewer sessions, human-response capture, comparison reporting, and later evidence-backed AI revision** — with the broader assistant and analytics platform still supporting the product around it.

**CI/CD:** GitHub Actions — lint, typecheck, tests, and build on every PR.  
**[Live Demo →](https://aptiv-analytics.vercel.app)**

---

### [Portland Timbers Matchday](https://chromewebstore.google.com/detail/ldecngkangcclhcjcckfldafdmjlpldi) — Published Chrome Extension with Safari Support

A Manifest V3 extension that shows upcoming Portland Timbers matches with a live countdown, TV/streaming info, and a fan confidence poll.

**The Architecture:** `chrome.storage.local` for state, alarm-based hourly refresh, runtime messaging between popup and service worker, and a three-tier data resolution strategy (live ESPN API → cache → bundled fallback). Safari support is handled through Xcode conversion with no polyfills required.

**The Result:** Published on the Chrome Web Store, with Safari support built into the codebase and workflow. GA4 telemetry via Measurement Protocol, Jest coverage, GitHub Actions CI, and Codecov integration.

**[GitHub →](https://github.com/Tony5897/timbers-chrome-ext)**

---

### [Search Cashback Injector](https://github.com/Tony5897/search-cashback-injector) — MV3 DOM Injection Proof-of-Concept *(In Development)*

A Manifest V3 Chrome extension that detects supported merchant domains in Google Search results and injects inline cashback banners next to matching results.

**The Architecture:** TypeScript + Vite build. Content script handles result link detection and domain normalization; background service worker resolves offers via a configuration-driven merchant registry with `chrome.storage.local` caching and JSON fallback data. Injected UI uses Shadow DOM for full style isolation from the host page.

**The Result:** A focused proof-of-concept for safe DOM orchestration, content script ↔ service worker messaging, and isolated UI injection in live search environments. Vitest coverage with GitHub Actions CI.

**[GitHub →](https://github.com/Tony5897/search-cashback-injector)**

---

### [OfferEngine](https://coupon-generator-liard.vercel.app/) — Zero-Backend Coupon Utility

A client-side coupon generator for configurable discount codes, QR output, and persistent storage with no backend required.

**The Architecture:** Next.js 15 (App Router) + TypeScript + Tailwind. Coupon codes use `crypto.getRandomValues` for suffix generation. QR rendering via `qrcode.react`. `localStorage` persistence across sessions. Input validation for discount ranges, code length, and expiration dates.

**The Result:** Deployed on Vercel with Vitest unit coverage, ESLint, TypeScript type-checking, and GitHub Actions CI.

**[GitHub →](https://github.com/Tony5897/coupon-generator)**

---

### [Oregon Lawn Barbers](https://www.oregonlawnbarbers.com/) — Client Site

End-to-end design and build for a Portland-area landscaping company. Conversion-focused, responsive, and deployed on Vercel with Next.js, TypeScript, and Tailwind.

---

## Engineering Philosophy

I treat AI tooling as an **architectural constraint**, not a substitute for engineering judgment.

That means:
- generated code should fit the actual system, not generic defaults
- repo-specific rules and conventions should keep implementation aligned with the product
- core projects should validate through linting, tests, and CI where the workflow calls for it
- browser behavior, runtime detail, and production reality matter just as much as clean code in the editor

I care about understanding what is actually running — especially when the debugging gets messy.

---

📍 Portland, OR · [Portfolio](https://www.tonymartinez.tech) · [LinkedIn](https://www.linkedin.com/in/tonymartinezpdx/) · [Email](mailto:hello@tonymartinez.tech)
