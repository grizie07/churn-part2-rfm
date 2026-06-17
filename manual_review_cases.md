# Manual Review Cases
**D2C Customer Churn Capstone — Part 2**

These 10 customers present non-obvious retention decisions where the RFM segment label alone is insufficient to determine the right action.

---

## Case 1 — CUST01148
**Profile:** recency=128d, frequency=7, monetary=₹5,448, tickets=0, sessions=1, **churn_label=1**

**Why it's hard:** This customer has the highest frequency (7 orders) in the dataset and very high spend — yet they churned. The recency gap of 128 days after 7 orders suggests an abrupt stop, not a gradual fade. With zero support tickets, there's no complaint signal to explain it.

**Decision:** Treat as a high-priority win-back. The absence of complaint tickets means they likely left due to a product/experience issue they never reported. A personal outreach (not an automated email) asking "what went wrong" has a realistic chance of recovery. Offer a ₹500 credit as a gesture, not a discount.

---

## Case 2 — CUST00883
**Profile:** recency=126d, frequency=2, monetary=₹4,601, tickets=0, sessions=1, **churn_label=0**

**Why it's hard:** Similar recency to CUST01148 — 126 days since last order, very high spend — yet this customer did NOT churn. This means they made a purchase in the target window despite months of silence.

**Decision:** Don't treat as dormant. They are a slow but high-value buyer. Sending a win-back campaign could irritate a customer who was going to come back anyway. Monitor passively; trigger only if recency exceeds 180 days at next snapshot.

---

## Case 3 — CUST00005
**Profile:** recency=38d, frequency=3, monetary=₹1,782, avg_discount=48%, **churn_label=0**

**Why it's hard:** This customer buys frequently and recently — but nearly half their spend is at heavy discount (48%). They're currently "safe" (not churned), but are they a loyal customer or a deal-hunter?

**Decision:** Do NOT send another discount. Instead, enrol in the loyalty programme and send a product education email. If they respond positively to non-discount messaging, they can graduate out of the Discount Sensitive segment. If not, accept that they're a promotional buyer.

---

## Case 4 — CUST00021
**Profile:** recency=77d, frequency=2, monetary=₹1,059, avg_discount=44%, **churn_label=1**

**Why it's hard:** Similar profile to CUST00005 but this one churned. They also rely heavily on discounts. Sending a discount to win them back would simply confirm the pattern.

**Decision:** Send one win-back offer — but make it a loyalty enrolment ("Join Silver tier, get ₹100 welcome credit") rather than a straightforward percentage discount. If they don't respond, remove from active campaign list to save budget.

---

## Case 5 — CUST01430
**Profile:** recency=5d, frequency=high, monetary=₹2,363, tickets=3, negative_ticket_rate=33%, **churn_label=0**

**Why it's hard:** This customer ordered just 5 days ago — extremely recent — but has filed 3 support tickets. They haven't churned yet, but active complaints from a buying customer is a warning sign.

**Decision:** Trigger an immediate proactive support outreach — not a promotional email. Acknowledge the ticket history. Assign to a human agent rather than chatbot. The goal is to resolve underlying frustration before it converts to churn. Do NOT send a promotional offer while their tickets are unresolved.

---

## Case 6 — CUST00006
**Profile:** recency=51d, tickets=2, negative_ticket_rate=100%, monetary=₹2,990, sessions=2, **churn_label=0**

**Why it's hard:** Both of this customer's recent tickets had fully negative sentiment — yet they have not churned and are still spending. They're clearly unhappy but haven't left yet.

**Decision:** Immediate service recovery action. This customer is a ticking clock. A human outreach acknowledging their frustration, combined with a service recovery offer (e.g. priority support access, or a complimentary product sample), is the right move. Budget: ₹300–500 recovery gesture.

---

## Case 7 — CUST00030
**Profile:** recency=5d, tickets=2, negative_ticket_rate=100%, monetary=₹2,820, sessions=11, **churn_label=0**

**Why it's hard:** Extremely active online (11 sessions) and recent buyer — but 100% negative support sentiment across 2 tickets. High engagement + high dissatisfaction = volatile.

**Decision:** Same as CUST00006 but even more urgent due to the high session count — this customer is actively browsing, possibly comparing alternatives. A proactive call or priority email from a senior agent within 24 hours is recommended before they switch.

---

## Case 8 — CUST00630
**Profile:** recency=93d, abandoned_carts=5, sessions=20, monetary=₹1,968, **churn_label=0**

**Why it's hard:** This customer has 20 sessions and 5 abandoned carts in the last 30 days — they are clearly engaged online and browsing heavily, but haven't ordered in 93 days and have a large cart abandonment rate.

**Decision:** Send a cart abandonment recovery email with free shipping as the incentive (not a % discount). They are clearly interested in buying but something is stopping them — price, delivery cost, or indecision. Free shipping has a lower margin cost than a 20% discount and may be sufficient to convert.

---

## Case 9 — CUST00689
**Profile:** recency=70d, abandoned_carts=4, sessions=13, monetary=₹4,514, **churn_label=0**

**Why it's hard:** Very high historical spend (₹4,514) with high web engagement but hasn't ordered in 70 days and has 4 abandoned carts. Similar to CUST00630 but at much higher value.

**Decision:** High-priority cart recovery. This is one of the highest-value customers showing purchase intent. Assign to the premium retention track: personalised email from CRM (not automated), offer a curated "top picks for you" recommendation, with free express delivery. Budget up to ₹500 for this recovery.

---

## Case 10 — CUST00001
**Profile:** recency=107d, frequency=1, monetary=₹363, last_campaign=welcome_offer, **churn_label=1**

**Why it's hard:** This customer received a welcome offer, made exactly one purchase 107 days ago, and then churned. A very common pattern — "one and done" customers acquired via promotional channels.

**Decision:** This is a low-ROI recovery case. The welcome offer did not convert them into a habit buyer. Sending another discount risks attracting them back only for another single purchase. Recommended: send a one-time "product education" email (no offer) focused on the category they purchased. If no engagement in 7 days, remove from active campaign budget. Investigate what acquisition channel brought this customer to avoid over-investing in similar profiles.

---

## Summary Patterns from Manual Review

| Pattern | Cases | Implication |
|---|---|---|
| High-value, sudden silence, no complaint | CUST01148 | Personal outreach; product issue likely |
| Discount-dependent, now churning | CUST00021 | Loyalty enrolment, not another discount |
| Active complaints + still buying | CUST01430, CUST00006, CUST00030 | Service recovery before promotion |
| High cart abandonment + long recency | CUST00630, CUST00689 | Free shipping trigger, not % discount |
| One-and-done acquisition | CUST00001 | Investigate channel quality; low ROI to recover |
