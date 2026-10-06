# Phase 1: Narrative & Objectives Specification
**Project Working Title:** CravePlan (Playful Culinary Operating System)  
**Product Lead & Creative Director:** Aarchi (Fashion Communication, NIFT Hyderabad)  
**Technical Architect & UX Mentor:** Antigravity  
**Lifecycle Stage:** Phase 1 Complete — Moving to Phase 2 (Empathy & Modeling)  

---

## 1. Executive Summary & Brand Narrative

### 1.1 The Core Vision
A playful, visual-first culinary planning companion that turns the chaotic question *"What should I cook this week?"* into a delightful, zero-friction ritual. 

Unlike traditional recipe blogs and YouTube videos—which demand passive watching, messy kitchen screen interaction, and manual grocery calculations—this platform connects **Inspiration, Weekly Scheduling, and Automated Grocery Fulfillment** in one cohesive loop:
```
[ 🍜 Playful Discovery ] ──▶ [ 🗓️ Bento Week Board ] ──▶ [ 🛒 Smart Consolidated Basket ]
```

### 1.2 Brand Personality & Visual Tone
* **Aesthetic Vibe:** Playful, tactile, editorial, and warm. Hand-drawn sticker accents, soft rounded geometric bento surfaces, and vibrant culinary tones (matcha, saffron, terracotta, whipped cream).
* **Emotional Experience:** Relieving decision paralysis. Cooking feels like assembling a personalized lifestyle moodboard rather than completing household chores.

---

## 2. Competitor & Platform Friction Audit

| Dimension | YouTube / Social Reels | Static Recipe Apps (e.g., Tasty) | Our Platform (CravePlan) |
| :--- | :--- | :--- | :--- |
| **Primary Interaction** | Passive video entertainment (10–15m monologues). | Text walls with ad popups. | **Bimodal:** 30s micro-reel preview + step-by-step kitchen cards. |
| **Weekly Planning** | Non-existent; saves into messy playlists. | Disconnected bookmark lists. | **Interactive 7-day Bento Board** with breakfast, lunch, and dinner slots. |
| **Portion Scaling** | Static text (serves 4; user must calculate). | Static or clunky calculator. | **Live stepper `[-] N [+]`** dynamically recalculating ingredients across recipes. |
| **Grocery Sourcing** | Manual typing into grocery apps item by item. | Static unorganized PDF checklists. | **Smart Aisle Categorization** + **1-tap deep link to Zepto / Blinkit / Instamart**. |

---

## 3. High-Impact Feature Architecture

### 3.1 The "Uncluttered" Full-Week Visual Board
To prevent cognitive overload while displaying an entire 7-day plan, we implement the **Bento-Accordion Pattern**:

```
┌──────────────────────────────────────────────────────────────────────────────┐
│  🗓️ WEEKLY MEAL BOARD                   [ 🎲 Surprise Fill ]  [ 🛒 View List ] │
├──────────────────────────────────────────────────────────────────────────────┤
│  [ MON ]    [ TUE (Today) ]    [ WED ]    [ THU ]    [ FRI ]    [ SAT ]    [ SUN ]│
├──────────────────────────────────────────────────────────────────────────────┤
│  ⚡ ACTIVE DAY: TUESDAY                                                       │
│                                                                              │
│  🥞 BREAKFAST      Avocado Sourdough Toast (10m)                  [ 🟢 Prep Done ] │
│  🥗 LUNCH          Mediterranean Quinoa Bowl (15m)               [ 👥 Serves 2 ]  │
│  🍝 DINNER         Truffle Mushroom Pasta (30m)                  [ ▶️ 30s Reel ]  │
│  🍪 SNACK          + Tap to add snack                                        │
├──────────────────────────────────────────────────────────────────────────────┤
│  💡 WEEK AT A GLANCE (Compact Mini-Pills)                                    │
│  Mon: 🥪 Toast  • 🍛 Dal Tadka • 🥗 Greek Salad                              │
│  Wed: 🥣 Oats   • 🥪 Paneer Wrap • 🍜 Ramen Bowl                             │
│  Thu: 🥞 Crepes • 🥗 Caesar Salad • 🥘 Thai Curry                             │
└──────────────────────────────────────────────────────────────────────────────┘
```

#### Key Anti-Clutter Principles:
1. **Compact Day-Pills:** High-level overview shows meals as playful mini-stickers/tags rather than giant cards.
2. **Focus-Day Accordion:** Tapping any day smoothly slides open its visual meal cards while collapsing the others.
3. **Ghost Slot Invites:** Empty slots appear as clean dashed outlines (`+ Plan Dinner`) that open a curated discovery drawer with 1 tap.
4. **"Surprise Fill" (Dice Roll):** A playful feature that auto-populates unassigned slots based on favorite cuisines and mood tags.

---

### 3.2 Smart Consolidated Grocery List
The shopping list acts as the real-world execution engine:

#### Core Capabilities:
1. **Multi-Recipe Consolidation:** Automatically adds quantities across meals (e.g., 2 cloves garlic from Pasta + 1 clove from Curry = *3 Cloves Garlic* under Produce).
2. **Dual Mode Selector:**
   * `[ 📦 Shop Whole Week (24 items) ]` — For weekend supermarket restocking.
   * `[ ⚡ Shop Today Only (6 items) ]` — For fresh daily prep.
3. **"In My Pantry" Filter:** Allows users to mark household staples (salt, oil, turmeric) as already stocked so they don't clutter the shopping cart.
4. **1-Tap Quick-Commerce Deep Link:**
   ```
   [ 🛵 Export Missing Items to Blinkit / Zepto ]
   ```
5. **Zero-Waste Synergy Indicator:** Highlights ingredients shared across multiple scheduled meals (e.g., *"✨ Mushroom pack fully utilized across Mon & Wed"*).

---

### 3.3 Connected Card System & Media Integration
Every recipe card links directly into the planning and shopping ecosystem:
* **Visual Media Tag:** `▶️ 0:30 Micro-Reel` badge for visual learners to see preparation technique without reading long paragraphs.
* **Context State Pill:** Shows if and where the recipe is scheduled (`📅 Scheduled: Tue Dinner`).
* **Dynamic Servings Stepper:** Scalable `[-] 1 / 2 / 4 [+]` toggle updating measurements in real time.
* **One-Tap Actions:** Direct `[ + Plan ]` and `[ 🛒 + Grocery ]` icon buttons.

---

## 4. Phase Gate Sign-Off & Transition

### Status: Phase 1 Approved
- **Problem Statement:** Defined.
- **Value Proposition:** Crystallized.
- **Core Pillars & Information Model:** Structured.

### Up Next: **Phase 2: Empathy & User Experience Modeling**
- User Persona Profiles (The Busy Design Student, The Working Professional).
- Empathy Mapping (Feelings, pains, desires around daily food decisions).
- End-to-End User Journey Map (Sunday Planning $\rightarrow$ Quick-Commerce Checkout $\rightarrow$ Evening Kitchen Cooking).
