# PHASE 1: MASTER OUTPUT & SPECIFICATION ARCHIVE
**Project Working Title:** CravePlan (Playful Culinary Operating System)  
**Document Type:** Phase 1 Design & Information Architecture Reference  
**Creative Director & Product Lead:** Aarchi (Fashion Communication, NIFT Hyderabad)  
**Technical Architect & UX Mentor:** Antigravity  
**Repository Location:** `Aarchi_BD-24-1972/PHASE_1_OUTPUT.md`  
**Status:** Phase 1 Completed & Locked  

---

## 1. PROJECT VISION & STRATEGIC NARRATIVE

### 1.1 The Core Purpose
CravePlan is a playful, visual-first culinary planning companion designed to eliminate daily decision fatigue around food. It bridges the gap between **passive recipe discovery** and **real-world execution** by connecting three core pillars into an unbroken loop:
```
[ 🍜 Playful Discovery ] ──▶ [ 🗓️ Bento Weekly Board ] ──▶ [ 🛒 Single Living Grocery Basket ]
```

### 1.2 Brand Persona & Emotional Tone
* **Personality:** Playful, tactile, warm, editorial, and approachable.
* **Visual Language:** Hand-drawn culinary sticker accents, soft rounded geometric surfaces (Bento grid), warm culinary tones (toasted almond, matcha green, terracotta, warm cream).
* **Core Emotional Benefit:** Relieving the mental burden of *"What do I cook today?"* while making weekly meal planning feel like assembling a creative moodboard rather than a chore.

---

## 2. COMPETITIVE DIFFERENTIATION: WHY CRAVEPLAN OVER YOUTUBE & STATIC APPS

| Friction Dimension | YouTube / Video Reels | Static Recipe Apps (e.g. Tasty) | CravePlan Solution |
| :--- | :--- | :--- | :--- |
| **Kitchen Usability** | 12-minute monologues; messy screen pausing with wet/oily hands. | Long text blogs with intrusive ads. | **Bimodal Format:** 30s micro-reel for visual inspiration + glanceable step-by-step kitchen cards. |
| **Weekly Planning** | Non-existent; recipes get lost in random saved playlists. | Isolated bookmark folders with no calendar integration. | **Full-Week Bento Board:** Seamless 7-day visual meal schedule with breakfast, lunch, and dinner slots. |
| **Portion Scaling** | Static numbers; forces cooks to do mental math in the kitchen. | Static or clunky text adjustments. | **Live Portion Stepper `[-] N [+]`:** Instantly recalculates ingredient quantities across recipes and grocery lists. |
| **Grocery Sourcing** | Manual note-taking and typing each item into delivery apps. | Static PDF or unorganized text checklists. | **1-Tap Quick-Commerce Export:** Automatically pushes consolidated ingredients into Blinkit / Zepto / Instamart. |

---

## 3. STRATEGIC DECISION AUDIT (KEPT, ADDED & DELETED)

### ❌ What Was Deleted & Why:
1. **AI-Generated Videos:** Removed due to high latency, expensive compute, and synthetic/unappetizing food physics. Replaced with curated 30-second video micro-reels (YouTube Shorts / TikTok embeds).
2. **Dense Recipe Steps on Front Cards:** Removed truncated text walls (`...`) from feed cards to prevent visual clutter and cognitive fatigue.
3. **Hostel-Only Constraint:** Broadened from a restrictive student/hostel tool to a universal, flexible household culinary platform.
4. **Complex "Virtual Pantry Inventory Trackers":** Removed cumbersome two-list inventory management that felt like an Excel spreadsheet.

### ➕ What Was Added & Why:
1. **Samsung Food / Whisk Benchmark Architecture:** Integrated a 7-day meal board and an automated ingredient aggregation engine.
2. **Bento-Accordion Planner:** An uncluttered full-week calendar showing the active day in detail and the remaining week as compact mini-tags.
3. **"Single Living Checklist" for Groceries:** One unified shopping list with auto-collapsed kitchen staples and 1-tap tap-to-strike interactions.
4. **1-Tap Quick-Commerce Deep-Linking:** Direct integration with existing on-device delivery apps (Blinkit, Zepto, Swiggy Instamart).

### 🔄 What Was Refined (Visual & UX):
1. **Connected Card Anatomy:** Recipe cards display live calendar states (e.g., `📅 Scheduled: Tue Dinner`) and quick-action buttons (`[+ Plan]`, `[🛒 + Grocery]`).
2. **Sensory Mood Badges:** Converted plain hashtags into colorful sensory flavor pills (`🔥 Spicy`, `🍋 Tangy`, `🧀 Creamy`, `🌿 Fresh`).

---

## 4. INFORMATION ARCHITECTURE & SYSTEM SPECIFICATIONS

### 4.1 The Connected Recipe Card
```
┌────────────────────────────────────────────────────────┐
│  [ CONTINENTAL ]                [ 📅 Mon Dinner (Active) ] │
│                                                        │
│  [ 🖼️ Hero Illustration / ▶️ 0:30 Reel Badge ]          │
│                                                        │
│  MUSHROOM & TRUFFLE PASTA              [ ❤️ Saved ]    │
│  #Creamy • 🟢 Veg                                      │
│  ⏱️ 40 mins   |   👥 Serves: [- 2 +]                   │
├────────────────────────────────────────────────────────┤
│  ⚡ QUICK ACTIONS                                      │
│  [ 📅 Add to Meal Plan ]     [ 🛒 +8 to Grocery List ] │
└────────────────────────────────────────────────────────┘
```

### 4.2 The Uncluttered Weekly Meal Board (Bento-Accordion Layout)
* **Weekly Strip:** Horizontal row showing Monday through Sunday.
* **Active Day Expanded:** The selected day displays clean bento cards for Breakfast, Lunch, Dinner, and Snack.
* **Week at a Glance:** Other days are summarized as playful, space-saving mini-stickers below.
* **Ghost Slot Buttons:** Empty slots appear as clean dashed outlines (`+ Plan Dinner`) that slide up recommended recipes in 1 tap.
* **"Surprise Me!" (Dice Roll):** A playful button that auto-populates unassigned slots based on favorite cuisines and moods.

```
┌────────────────────────────────────────────────────────┐
│  🗓️ WEEKLY MEAL BOARD       [ 🎲 Surprise Me ] [ 🛒 List ]│
├────────────────────────────────────────────────────────┤
│  [ Mon ]  [ TUE (Today) ]  [ Wed ]  [ Thu ]  [ Fri ]  [ Sat ]│
├────────────────────────────────────────────────────────┤
│  ⚡ TUESDAY MEALS (Active Day Expanded)                 │
│  🥞 Breakfast: Avocado Toast (10m)        [ 🟢 Done ]  │
│  🥗 Lunch:     Quinoa Green Bowl (15m)    [ 👥 Serves 2]│
│  🍝 Dinner:    Truffle Pasta (30m)        [ ▶️ 30s Reel ]│
│  🍪 Snack:     [ + Add Snack ]                         │
├────────────────────────────────────────────────────────┤
│  👀 WEEK AT A GLANCE (Compact Mini-Pill Tags)           │
│  Wed: 🥪 Paneer Wrap  •  🍜 Miso Ramen                 │
│  Thu: 🥗 Greek Salad  •  🥘 Thai Curry                 │
│  Fri: 🍕 Homemade Pizza night                          │
└────────────────────────────────────────────────────────┘
```

### 4.3 The Simplified Grocery Engine (Single Living Checklist)
* **No Manual Pantry Inventory:** Users do not manage an inventory spreadsheet.
* **The "Assumed Staples" Rule:** Basic universal items (*Salt, Pepper, Cooking Oil, Water*) are automatically tucked into a quiet, collapsed row at the bottom.
* **1-Tap "Already Have It" Strike:** Tapping an item greys it out with a strike-through line, moves it to the bottom, and updates the checkout button live.
* **Cadence Toggle:** 
  * `[ 📦 Shop Whole Week (24 items) ]` — For weekend supermarket stocking.
  * `[ ⚡ Shop Today Only (6 items) ]` — For fresh daily prep.
* **5 Universal Supermarket Aisle Categories:**
  1. 🥬 **Fresh Produce:** Vegetables, mushrooms, onions, herbs, garlic.
  2. 🥛 **Dairy & Plant Alternatives:** Milk, coconut milk, butter, cheeses.
  3. 🍞 **Pantry & Dry Grains:** Pasta, rice, noodles, flour, bread.
  4. 🧂 **Oils, Sauces & Condiments:** Truffle paste, olive oil, vinegar, sauces.
  5. 🌶️ **Spices & Seasonings:** Salt, black pepper, chili flakes, nutritional yeast.
* **Ingredient Data Structure:**
  $$\text{Ingredient} = [\text{Quantity}] + [\text{Standard Unit}] + [\text{Core Item Name}] + [\text{Aisle Category}]$$
* **1-Tap Delivery Deep Link:**
  `[ 🛵 Order 5 Fresh Items via Blinkit / Zepto ]`

---

## 5. SUMMARY OF PHASE 1 DELIVERABLES FOR FUTURE REFERENCE
* [x] Problem Statement & Brand Narrative defined
* [x] Competitor Friction Audit completed (YouTube vs. Static Apps vs. CravePlan)
* [x] Feature Architecture scoped (Card, Planner, Grocery Engine)
* [x] Data Model & Taxonomy structured for ingredients and aisles
* [x] Mobile layout principles defined (Bento-Accordion, Single Living Checklist)
* [x] Phase 1 master reference file archived to `c:\Users\aarch\OneDrive\Documents\Aarchi_BD-24-1972\PHASE_1_OUTPUT.md`

---
*Ready to serve as the baseline blueprint for Phase 2 (Empathy & User Experience Modeling).*
