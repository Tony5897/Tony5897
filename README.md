# Tony Martinez
### Frontend Software Engineer · Portland, OR · Performance & AI-Integrated Web Systems

I build **production-grade web applications** where design precision and engineering
rigor meet. My work spans AI-powered interfaces, browser extension architecture, and
the cross-platform, real-device complexity that comes with shipping multimodal systems
into the wild.

**[Portfolio](https://www.tonymartinez.tech)** · **[LinkedIn](https://www.linkedin.com/in/tonymartinez5897/)** · **[Email](mailto:hello@tonymartinez.tech)**

---

## Current Focus

- **Multimodal AI Interfaces:** Building streaming, voice-enabled, and media-aware interfaces that remain usable under real-world constraints — not just controlled demos.
- **AI-Integrated Systems:** Connecting models, browser capabilities, backend services, and user-facing workflows into applications that feel coherent in practice, not just impressive in isolation.
- **Cross-Platform Debugging:** Solving browser and device-specific issues on physical hardware using Safari Web Inspector, ngrok, and platform-level debugging workflows for camera, MediaPipe, WebGL, and mobile compatibility.
- **Release-Minded Frontend Systems:** Shipping with Next.js, TypeScript, testing, and CI in mind — treating reliability, maintainability, and debuggability as part of the product.

---

## Stack

| Domain | Technologies | Focus |
| :--- | :--- | :--- |
| **UI Architecture** | React, Next.js, TypeScript | State, component systems, performance-minded frontend architecture |
| **AI & Media** | Gemini, OpenAI, MediaPipe, Google Cloud TTS | Streaming UX, multimodal analysis, voice workflows |
| **Browser Platform** | Chrome MV3, Web Audio API, MutationObserver, Shadow DOM | Service worker lifecycle, DOM orchestration, extension-side UX |
| **Mobile & DevTools** | Safari Web Inspector, ngrok, iPhone camera handling | Real-device debugging, tunneled mobile QA, browser compatibility |
| **Ops & Quality** | Vitest, Jest, GitHub Actions, Husky | Linting, automated tests, release-minded workflows |

---

## Projects

### [AptivAi](https://github.com/Tony5897/aptiv-analytics) — Multimodal AI Analytics Platform *(In Progress)*

A full-stack AI email marketing analytics platform — the most technically complex
system in this portfolio.

**The Stack:** React + TypeScript frontend, Node.js/Express backend, MongoDB, Firebase
auth, Google Cloud TTS, Gemini API, and MediaPipe-based facial analysis workflows.

**The Hard Parts:**

- **Real-device cross-platform debugging:** iOS Safari required a separate camera access
  strategy. I enumerated physical device IDs, handled permission constraints, worked
  through MediaPipe `FilesetResolver` / WASM initialization, and debugged it live on a
  physical iPhone through Safari Web Inspector over an ngrok tunnel. Simulators would
  not have caught the same issues.

- **Streaming + voice workflow:** Gemini responses stream in real time via
  Server-Sent Events, with browser-side voice input and text-to-speech output layered
  into the same interface.

- **Emotional impact analysis:** The platform combines text/image analysis with live
  facial-reaction workflows using MediaPipe FaceLandmarker, then surfaces that analysis
  through user-facing emotional-congruence and campaign-review UI.

- **Browser capability troubleshooting:** Development involved working through camera
  behavior, WebGL capability warnings, resource cleanup, and mobile-browser
  compatibility constraints that do not show up in simpler AI demos.

- **Tunnel/auth friction during testing:** ngrok-based mobile QA surfaced environment
  issues like Firebase authorized-domain restrictions and access/control problems that
  had to be solved alongside media and browser debugging.

**The Result:** A platform that does things most demos fake — real facial tracking,
real streaming workflows, and real cross-platform behavior validated on physical
hardware.

---

### [Portland Timbers Matchday](https://chromewebstore.google.com/detail/ldecngkangcclhcjcckfldafdmjlpldi) — Published Chrome Extension

**The Problem:** Manifest V3's ephemeral service worker model makes stateful extension
behavior more complex by design. Workers can be suspended by Chrome at any point.

**The Architecture:** Built around `chrome.storage.local`, runtime messaging,
cached/fallback match data, and alarm-based refresh so the extension behaves reliably
across the MV3 service worker lifecycle.

**The Result:** **Live on the Chrome Web Store.** GitHub Actions CI runs linting and
Jest-based test coverage on push and pull request.  
**[GitHub →](https://github.com/Tony5897/timbers-chrome-ext)**

---

### [OfferEngine](https://coupon-generator-liard.vercel.app/) — Zero-Backend Utility

**The Constraint:** Full-featured coupon generation with zero backend operational cost
and no infrastructure burden.

**The Architecture:** Pure client-side — configurable discount codes, QR generation,
`localStorage` persistence, Vitest unit coverage, and GitHub Actions CI.

**The Result:** A fast, lightweight utility with zero backend operational cost and a
production-ready frontend UX.  
**[GitHub →](https://github.com/Tony5897/coupon-generator)**

---

### [Search Cashback Injector](https://github.com/Tony5897/search-cashback-injector) — DOM Orchestration *(In Development)*

**The Problem:** Injecting ranked cashback/deal UI into live search result pages without
creating a brittle, messy extension experience.

**The Architecture:** MutationObserver-driven page detection + Shadow DOM encapsulation
for isolated UI rendering inside real search environments, with early CI/test discipline
around merchant/domain logic.

**The Result:** An actively built browser-platform project focused on DOM orchestration,
extension-side UX, and safe injection patterns.  
**[GitHub →](https://github.com/Tony5897/search-cashback-injector)**

---

### [Oregon Lawn Barbers](https://www.oregonlawnbarbers.com/) — Client Site

End-to-end design and build for a Portland-area landscaping company. Conversion-focused,
responsive, deployed on Vercel with Next.js, TypeScript, and Tailwind.

---

## Engineering Philosophy

I treat AI tooling as an **architectural constraint**, not a productivity shortcut:

- `.cursorrules` / repo-specific conventions should keep generated output aligned with
  the actual system — not generic best practices
- Core projects run automated linting and test checks in CI where the workflow calls
  for it
- I read the Web Inspector logs. On the phone. While the app is running.

---

📍 Portland, OR · [Portfolio](https://www.tonymartinez.tech) · [LinkedIn](https://www.linkedin.com/in/tonymartinez5897/) · [Email](mailto:hello@tonymartinez.tech)
