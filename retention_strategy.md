# Retention Strategy by Segment
**D2C Customer Churn Capstone — Part 2**
Snapshot date: `2025-09-30` | 2,400 customers across 8 segments

---

## Segment Overview

| Segment | Count | Churn Rate | Priority |
|---|---|---|---|
| Dormant | 372 | 91.1% | ⛔ Low (too far gone) |
| Silent Disengaged | 19 | 84.2% | ⛔ Low (very small, low ROI) |
| At-Risk | 390 | 72.1% | 🔴 HIGH |
| Needs Attention | 245 | 66.1% | 🔴 HIGH |
| Discount Sensitive | 130 | 63.8% | 🟡 MEDIUM |
| High Value Unhappy | ~66* | ~55%* | 🔴 HIGH (high value) |
| Loyal Customers | 578 | 25.4% | 🟢 Protect |
| Promising New | 265 | 21.9% | 🟢 Nurture |
| Champions | 401 | 10.2% | 🟢 Reward lightly |

---

## Segment Details & Retention Actions

### 🔴 At-Risk (390 customers, 72.1% churn rate)
**Who they are:** Customers who used to buy frequently (F≥3) but have not placed an order recently (R≤2). These are high-value relationships that are slipping away.

**Behaviour signals:** High frequency in the past, long recency gap now, moderate web activity.

**Retention action:**
- Send a "We miss you" personalised email with a time-limited offer (e.g. 15% off their preferred category)
- Follow up with a push notification if the email is not opened within 3 days
- Do NOT send a blanket discount — check if they are also Discount Sensitive before discounting

**Expected business value:** Recovering even 20% of these 390 customers at their historical spend rate represents significant revenue recovery.

---

### 🔴 High Value Unhappy (ticket_count≥2, M≥3)
**Who they are:** High-spending customers who have raised multiple support tickets recently. They are still buying but at risk of leaving due to unresolved frustration.

**Behaviour signals:** High monetary score, multiple recent tickets, potentially negative sentiment.

**Retention action:**
- Trigger a proactive outreach from a senior support agent (not automated email)
- Acknowledge their complaint history explicitly: "We noticed you've had some issues recently"
- Offer a service recovery gesture (free gift, expedited shipping on next order, or small credit)
- Do NOT send a generic promotional email — they need to feel heard, not sold to

**Expected business value:** These are your highest-spending customers. Losing one is worth 3–5× the campaign cost to recover.

---

### 🟡 Discount Sensitive (130 customers, 63.8% churn rate)
**Who they are:** Customers who have consistently purchased at high discount levels (≥35% average), but whose overall RFM score is mediocre. They likely only buy during sales.

**Behaviour signals:** High avg_discount_pct_180d, mid-range frequency, mid-range recency.

**Retention action:**
- Do NOT lead with another discount — this deepens dependency
- Instead, introduce them to the loyalty programme: highlight points, early access, and member pricing
- A/B test: send half a loyalty enrolment prompt, send half a product education email about ingredient quality
- Goal: shift their buying motivation from "cheapest price" to "brand value"

**Expected business value:** Converting even 20% of discount buyers into loyalty-enrolled buyers reduces long-term margin erosion.

---

### 🟢 Loyal Customers (578 customers, 25.4% churn rate)
**Who they are:** Consistent, moderately recent buyers with solid RFM scores. The backbone of the brand.

**Behaviour signals:** R≥3, F≥3, RFM≥9. Regular purchasers across multiple categories.

**Retention action:**
- Enrol in the loyalty programme if not already enrolled
- Send exclusive early access to new launches (no discount needed)
- Recognise their loyalty: "You've been with us for X months" milestone emails

**Expected business value:** Prevention is cheaper than recovery. A small loyalty investment here avoids expensive win-back campaigns later.

---

### 🟢 Promising New (265 customers, 21.9% churn rate)
**Who they are:** Recently acquired customers (R≥4) who haven't yet built a habit (F≤2). Critical onboarding window.

**Behaviour signals:** High recency score, low frequency, decent monetary value per order.

**Retention action:**
- Send a structured onboarding email series (Day 7, Day 14, Day 30 after first purchase)
- Highlight product categories they haven't tried yet
- Prompt loyalty programme sign-up before their second order
- Use in-app prompts to increase session depth (product views, wishlist adds)

**Expected business value:** Every customer who makes a second purchase is statistically far more likely to make a third. Onboarding investment here has compounding returns.

---

### 🟢 Champions (401 customers, 10.2% churn rate)
**Who they are:** The best customers. High recency, high frequency, high spend.

**Behaviour signals:** R≥4, F≥4, M≥4. Very low churn risk.

**Retention action:**
- Minimal intervention needed — over-messaging risks annoying them
- Invite to a referral programme ("Refer a friend, get ₹200 credit")
- Give Platinum loyalty tier or exclusive community access
- Do NOT send discounts — they buy at full price

**Expected business value:** Low cost to retain. High value as brand advocates via referral.

---

### ⛔ Dormant (372 customers, 91.1% churn rate)
**Who they are:** Customers who have not ordered in 150+ days and have low frequency. Essentially lapsed.

**Retention action:**
- One final "win-back" email with a strong offer (free shipping + 20% off)
- If no response in 14 days, remove from active campaign budget
- These customers are expensive to retain and may inflate your mailing costs
- Investigate: did they leave a bad review anywhere? Did a product reaction drive them away?

**Expected business value:** Low. Budget for this segment should be near zero. Only act if the offer cost is below expected LTV recovery.

---

### ⛔ Silent Disengaged (19 customers, 84.2% churn rate)
Small segment — 0 web sessions and recency > 60 days. Treat like Dormant. Very low ROI.

---

## Campaign Budget Prioritization

**Assumed total campaign budget: ₹100,000**

| Segment | Budget % | INR | Rationale |
|---|---|---|---|
| At-Risk | 35% | ₹35,000 | Highest recoverable value, large group |
| High Value Unhappy | 25% | ₹25,000 | Small group but highest per-customer value |
| Needs Attention | 15% | ₹15,000 | Large group, moderate risk |
| Discount Sensitive | 10% | ₹10,000 | Loyalty conversion attempt |
| Loyal Customers | 10% | ₹10,000 | Protection investment |
| Promising New | 5% | ₹5,000 | Onboarding emails (low cost) |
| Champions | 0% | ₹0 | Self-sustaining, referral only |
| Dormant | 0% | ₹0 | Too far gone; remove from active budget |
| Silent Disengaged | 0% | ₹0 | Too small, too risky |

**First action:** Before spending a rupee, enrol the At-Risk + High Value Unhappy segments into the loyalty programme if they are not already enrolled. Loyalty enrolment costs nothing and dramatically changes retention outcomes.
