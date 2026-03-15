# Tony Martinez
### Frontend Software Engineer · Portland, OR · Performance & AI-Integrated Web Systems

I build **production-grade web applications** where design precision and engineering
rigor meet. My work spans AI-powered interfaces, browser extension architecture, and
the cross-platform, real-device complexity that comes with shipping multimodal systems
into the wild.

**[LinkedIn](https://www.linkedin.com/in/tonymartinez5897/)** · **[Email](mailto:tony5897@gmail.com)**

---

## 2026 Focus

> "In an era of generated code, the differentiator is the engineer who understands
> what's actually running beneath it."

- **Multimodal AI Interfaces:** Real-time SSE streaming + off-main-thread inference
  via Web Workers — keeping AI-heavy UIs fluid under load.
- **Cross-Platform Depth:** Debugging at the Safari Web Inspector level on physical
  iOS devices — camera enumeration, WebGL context sharing, WASM asset resolution.
- **Edge-First Performance:** Next.js 15 + Edge runtime targeting sub-500ms TTI,
  validated against real Core Web Vitals — not just Lighthouse scores.

---

## Stack

| Domain | Technologies | Focus |
| :--- | :--- | :--- |
| **UI Architecture** | React 19, Next.js 15, TypeScript | Concurrent rendering, hydration strategy |
| **AI & Inference** | Gemini, OpenAI, MediaPipe, Claude | Streaming pipelines, multimodal orchestration |
| **Browser Platform** | Chrome MV3, Web Audio API, Web Workers | Service worker lifecycle, off-thread execution |
| **Mobile & DevTools** | Safari Web Inspector, ngrok, iOS Camera API | Real-device debugging, localhost tunneling |
| **Ops & Quality** | Vitest, Jest, GitHub Actions, Husky | CI/CD, automated quality gates per PR |

---

## Projects

### [AptivAi](https://github.com/Tony5897/aptiv-analytics) — Multimodal AI Analytics Platform *(In Progress)*

A full-stack AI email marketing analytics platform — the most technically complex
system in this portfolio.

**The Stack:** React + TypeScript frontend, Node.js/Express backend, MongoDB, Firebase
auth, Google Cloud TTS, Gemini API.

**The Hard Parts:**

- **Off-thread inference:** MediaPipe FaceLandmarker runs inside a **Web Worker**
  with a shared WebGL context, completely decoupled from the render cycle. Keeping
  facial sentiment tracking at 60fps while Gemini streams tokens required treating
  the inference pipeline as a first-class architectural concern — not an afterthought.

- **Real-device cross-platform debugging:** iOS Safari required a completely separate
  camera access strategy. Enumerated physical device IDs, handled iOS permission
  constraints, and resolved WASM asset paths through the MediaPipe FilesetResolver —
  all debugged live on a physical iPhone via Safari Web Inspector over an ngrok
  tunnel. Simulators wouldn't have caught any of it.

- **SSE token streaming:** Gemini responses stream token-by-token via Server-Sent
  Events, with voice synthesis layered on top through Web Audio API and Google Cloud
  TTS — producing a coherent voice + text experience without blocking the UI.

- **Sentiment pipeline:** Each email/message is scored for emotional state (Joy,
  Curiosity, Friendship, etc.) in real-time, with facial expression data merged into
  campaign-level analytics in MongoDB.

**The Result:** A platform that does things most demos fake — real facial tracking,
real streaming inference, real cross-platform behavior validated on physical hardware.

---

### [Portland Timbers Matchday](https://chromewebstore.google.com/detail/ldecngkangcclhcjcckfldafdmjlpldi) — Published Chrome Extension

**The Problem:** Manifest V3's ephemeral service worker model makes stateful data
persistence unreliable by design. Workers can be killed by Chrome at any point.

**The Architecture:** Built a state-sync engine using `chrome.storage.local` and
runtime messaging that guarantees zero data loss across worker hibernation cycles —
the extension behaves identically whether the worker has been running for 10 seconds
or just reinitialized from hibernation.

**The Result:** **Live on the Chrome Web Store.** Automated zero-touch CI/CD via
GitHub Actions — a push to `main` ships to production. [GitHub →](https://github.com/Tony5897/timbers-chrome-ext)

---

### [OfferEngine](https://coupon-generator-liard.vercel.app/) — Zero-Backend Utility

**The Constraint:** Full-featured coupon generation with zero backend operational cost
and no scaling ceiling.

**The Architecture:** Pure client-side — configurable discount codes, QR generation,
`localStorage` persistence, Vitest unit coverage, GitHub Actions CI on every push.

**The Result:** **100/100 Core Web Vitals.** Zero hosting cost, permanently.
[GitHub →](https://github.com/Tony5897/coupon-generator)

---

### Search Cashback Injector — DOM Orchestration *(In Development)*

**The Problem:** Injecting ranked cashback/deal UI into live, high-traffic search
result pages without causing layout shift or performance regression.

**The Architecture:** MutationObserver pattern + Shadow DOM encapsulation for complete
visual isolation and guaranteed zero CLS — the host page remains entirely unaffected.

**The Result:** Sub-50ms injection overhead on real search pages.

---

### [Oregon Lawn Barbers](https://www.oregonlawnbarbers.com/) — Client Site

End-to-end design and build for a Portland-area landscaping company. Conversion-focused,
responsive, deployed on Vercel with Next.js, TypeScript, and Tailwind.

---

## Engineering Philosophy

I treat AI tooling as an **architectural constraint**, not a productivity shortcut:

- `.cursorrules` files that encode codebase-specific patterns — the output matches
  the system's actual conventions, not generic best practices
- Every PR runs automated unit tests and accessibility audits before merge
- I read the Web Inspector logs. On the phone. While the app is running.

---

📍 Portland, OR · [LinkedIn](https://www.linkedin.com/in/tonymartinez5897/) 

