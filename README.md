## 🧿 Phantom+Specter v5.4 (Adblocker)

An ultra-lightweight, privacy-focused content filtering engine designed to reduce unwanted advertising, trackers, and suspicious embedded content while maintaining exceptional performance and low runtime overhead.

---

## ⚡ Features

### 🧩 Ultra-lean Core

- Runs at `document-start` for maximum early-page protection.
- Singleton guard prevents duplicate execution across reinjections.
- Designed for minimal CPU, memory, and layout impact.
- Avoids heavy polling loops and unnecessary recalculations.

---

### 🚫 Site Exclusion System

Allows full opt-out per domain for compatibility and control.

- Stores excluded sites locally via `GM_getValue`
- Instantly bypasses all filtering logic on excluded domains
- Lightweight lookup with no runtime scanning overhead

### Menu Options

- 🚫 Exclude this site
- 🔄 Clear exclusions

---

## 🛡 Network Request Blocking

Intercepts and blocks unwanted requests at the browser level using:

- `fetch()` interception
- `XMLHttpRequest` interception
- Dynamic `src` assignment filtering (images, scripts, iframes)

### Targets include:

- Advertising networks
- Analytics services
- Tracking & fingerprinting providers
- Sponsored content delivery platforms

---

## 👻 Hybrid Intelligence Engine

A two-tier adaptive filtering system:

### ⚡ Fast Path

- Immediately removes known ad scripts, images, and iframe sources
- Executes only on DOM additions (no continuous scanning)
- Minimal CPU overhead per mutation batch

### 🧠 Deep Intelligence Mode

- Activates only under increased DOM activity
- Performs broader inspection of newly injected nodes
- Detects suspicious iframe patterns dynamically
- Avoids full DOM traversal unless necessary

---

## 🎯 CSS-Based Filtering Layer

Instant visual suppression of common advertising elements:

- Sponsored content blocks
- Banner and promotional containers
- Ad iframes and embeds
- Known ad-related IDs and class patterns

Applied instantly at `document-start` for zero delay.

---

## 🧠 Smart Mutation Monitoring

A lightweight MutationObserver system designed for efficiency:

- Observes only DOM additions
- Applies fast-path filtering immediately
- Uses adaptive “budgeting” to prevent CPU spikes
- Escalates to deeper scanning only when needed

---

## 🎥 Minimal Video Observer

Uses `IntersectionObserver` to improve media efficiency:

- Activates videos only when in viewport
- Reduces background decoding and playback overhead
- Improves GPU/CPU efficiency on media-heavy pages

---

## 🔐 Privacy

This script operates with strict privacy guarantees:

- ❌ No data collection
- ❌ No external server communication
- ❌ No analytics or telemetry
- ❌ No user tracking
- ❌ No account requirements

All processing happens locally in the browser.

---

## ⚙️ Performance Philosophy

Phantom+Specter is designed around three principles:

### 🧭 Lightweight. Intelligent. Invisible.

Instead of aggressively rewriting pages, it:

- Targets only known unwanted patterns
- Avoids unnecessary DOM traversal
- Minimizes observer workload
- Prefers selective intervention over blanket modification

The goal is **silent, efficient improvement** without destabilizing modern web applications.

---

## 📜 License

Released under the MIT License.

You are free to:

- Use it personally or commercially
- Modify and extend it
- Redistribute or fork it

Provided “as-is”, without warranty of any kind.
