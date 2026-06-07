# Vita — Personal Health Assistant 🌿

> Small steps, stronger you.

Vita is a **handy, private, offline** health assistant. You answer a short assessment about
your **body**, your **budget**, and **where you live**, and Vita builds a personalized daily
checklist of health "requirements" plus tips — then tracks your progress and streaks.

There's a **"Try a sample profile"** button on the welcome screen if you just want to see how it
works before entering your own details.

**Languages:** English and **繁體中文（台灣）**. Vita auto-detects your device language and you can
switch anytime (Profile → Language, or on the welcome screen).

---

## 🔒 Privacy & security by design

- **Zero external dependencies.** No CDNs, web fonts, frameworks, analytics, or trackers — just
  hand-written vanilla HTML/CSS/JS.
- **No network access — by enforcement.** A strict `Content-Security-Policy` (`connect-src 'none'`,
  `default-src 'none'`) means the app *cannot* contact any server or load any external resource.
- **Your data never leaves your device.** Everything lives in your browser's `localStorage`. No
  account, no sign-up, no cloud, no shared server. Two people using the same link each get their
  own private copy — neither can see the other's data. Export your data as JSON or delete all of it
  with one tap (Profile tab).
- **XSS-safe.** All user-entered text is HTML-escaped; no `eval`, no external code.

> This hosted copy ships only the app code and a **generic sample profile** — no real personal
> health data.

---

## 📲 Install on your phone (works fully offline)

This is a Progressive Web App, so you can install it to your Home Screen:

**iPhone / iPad (Safari):** open the site → tap **Share** (□↑) → **Add to Home Screen** → **Add**.

**Android (Chrome):** open the site → menu **⋮** → **Install app** / **Add to Home Screen**.

After the first load it caches itself, so it launches full-screen and **works with no internet** —
the server is never needed again.

You can also just open `index.html` directly on a computer to use it.

---

## 📱 What's inside

| Tab | What it does |
|-----|--------------|
| **Today** | Progress ring, streak, a tap-to-log water counter, today's checkable requirements, and a daily tip. |
| **Plan** | Daily targets (calories, protein/carbs/fat, water, BMI), requirements by category, budget-appropriate food ideas, a sample day's meals, climate/area guidance, and a Share / copy-plan button. |
| **Insights** | A 4-week completion heatmap, 7-day completion %, a body-composition view, a weight-trend chart, and an editable weight history. |
| **Profile** | Your details, weight logging, light/dark theme, metric/imperial units, manual goal override, data export/delete. |

### The 5-step assessment
1. **Welcome** — your name (optional) + an optional sample profile.
2. **Your body** — units (metric or imperial), sex, age, height, weight, optional body-fat %, activity.
3. **How you feel** — energy / sleep / stress sliders.
4. **Budget** — Low / Medium / High (drives food suggestions).
5. **Where you live** — climate + area (tune hydration, training timing, food access).

---

## 🧠 How the recommendations are calculated

Uses established formulas: **BMR** (Mifflin-St Jeor) → **TDEE** (× activity factor) → **goal
auto-detection** from BMI and body-fat band → **calorie target** (gain +15 %, maintain ±0, lose
−18 %, with safe weekly caps) → **macros** (protein/fat per kg, carbs fill the rest) → **hydration**
(~35 ml/kg, raised in hot climates). You can override the detected goal anytime.

### Safety guardrails
Vita shows a **"see a professional"** alert and steps back on red flags (BMI < 16, under-18, very
high BMI, or self-reported very low energy *and* sleep), and always notes it is **educational
guidance, not medical advice**.

---

## ♿ Accessibility

Tab/tablist/tabpanel structure for screen readers, ARIA labels on icon controls, decorative icons
hidden, keyboard-operable checklist items, visible focus rings, ≥44px tap targets, and state shown
by more than colour. Respects `prefers-reduced-motion` and `prefers-color-scheme`.

---

## 🧪 Testing

Open **`vita-selftest.html`** — it re-implements the health engine and checks it against known-good
values for several profiles, rendering a PASS/FAIL table. Runs entirely offline.

---

## ⚠️ Disclaimer

Vita provides general wellness and lifestyle information for educational purposes only. It is
**not medical advice** and is not a substitute for professional diagnosis or treatment. Consult a
clinician or registered dietitian before significant diet, exercise, or supplement changes —
especially if you are under 18, pregnant or breastfeeding, or have a medical condition.

---

Built dependency-free, offline, with privacy first.
