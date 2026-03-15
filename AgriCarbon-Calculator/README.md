# AgriCarbon Calculator — MVP

Presentation-ready minimum viable product to help farmers quickly understand estimated carbon credits, annual revenue, and steps to qualify for carbon markets.

---

## 1. Product summary

**AgriCarbon Calculator** is a single-page web app that turns complex carbon-market concepts into a simple calculator and dashboard. Farmers enter farm size, choose a regenerative practice, and optionally set a carbon price. The app shows estimated tonnes of CO₂ credits per year, estimated annual income, a small “carbon potential” progress bar, and a clear list of steps to qualify. A “How it works” section and a CTA (“Check eligibility & talk to an advisor”) make it demo- and investor-friendly. All estimates are clearly labeled as illustrative only, with a visible disclaimer.

---

## 2. MVP feature list

- **Inputs:** Farm size (acres), farming practice (dropdown), carbon price per tonne (USD, with default).
- **Outputs:** Estimated carbon credits (tonnes CO₂e/year), estimated annual income (USD).
- **Dashboard:** Summary cards for credits and income; progress-style bar for “carbon potential.”
- **Qualification:** Six steps to qualify for carbon markets.
- **Content:** “How it works” copy, disclaimer, single CTA button.
- **UX:** Auto-updating results, formatted numbers, responsive layout, preloaded demo values (2,000 acres, No-till → 32 t CO₂/year, $1,200/year).

---

## 3. Estimation logic and assumptions

**Formulas:**

- **Estimated Carbon Credits (tonnes CO₂e/year)** = Farm size (acres) × Practice factor (tonnes per acre per year).
- **Estimated Income (USD/year)** = Estimated Carbon Credits × Carbon price (USD per tonne).

**Default carbon price:** $37.50 per tonne CO₂e.

**Practice factors (tonnes CO₂e per acre per year):**

| Practice           | Factor  |
|--------------------|--------|
| No-till            | 0.016  |
| Reduced till       | 0.020  |
| Rotational grazing | 0.024  |
| Cover crops        | 0.028  |
| Agroforestry       | 0.050  |

**Example check:** 2,000 acres × 0.016 = 32 tonnes CO₂e/year; 32 × $37.50 = $1,200/year.

---

## 4. How to run

1. Open the project folder and double-click `index.html`, or  
2. From the project folder run a simple server, e.g.  
   - **Python 3:** `python -m http.server 8080` then visit `http://localhost:8080`  
   - **Node (npx):** `npx serve .` then use the URL shown  
3. Use the inputs to change farm size, practice, and price; results update automatically.

No build step or extra dependencies required.

---

## 5. 60-second demo script

- **0:00–0:10**  
  “This is AgriCarbon Calculator. It helps farmers see how much they could earn from carbon markets without wading through complicated programs.”

- **0:10–0:25**  
  “You enter your farm size—here we have 2,000 acres—pick a practice like No-till, and optionally the carbon price. We use 37 dollars 50 per tonne as a default. Hit enter or change anything, and the numbers update.”

- **0:25–0:40**  
  “So for 2,000 acres and No-till we get 32 tonnes of CO₂ per year and about 1,200 dollars a year. The bar shows how this practice compares to others. Below you see the six steps farmers need to actually qualify—land eligibility, record-keeping, maintaining the practice, working with a program, verification, and then selling credits.”

- **0:40–0:55**  
  “There’s a short ‘How it works’ and a button to check eligibility or talk to an advisor. Everything is clearly marked as illustrative; we’re not giving official carbon-market advice. The goal is to make the opportunity concrete so farmers can decide if they want to go deeper with a real program.”

- **0:55–1:00**  
  “That’s AgriCarbon Calculator—simple estimates, clear next steps, built for a fast demo. Questions?”

---

## 6. Three ideas for future enhancements

1. **Multi-practice and multi-year:** Let users select multiple practices and acreage per practice, and show a simple multi-year projection (e.g. 5–10 years) with optional discounting or price scenarios.

2. **Eligibility quiz:** A short “Check eligibility” flow (e.g. land type, current tillage, existing contracts) that ends with a simple “likely eligible / talk to an advisor” result and pre-filled calculator inputs.

3. **Export and share:** One-click export of the current scenario (inputs + outputs) as a PDF or shareable link so farmers can send it to advisors or use it in applications.
