# ROOTED Construction — UI Front-End QA Requirements

Construction is safety-critical and procurement-critical.  
UI must preserve trust and non-manipulation.

Backend authority ALWAYS wins.

---

## 1. Navigation & Routing

### MUST:
- Hide contractor bidding tools for non-Premium+  
- Hide RFQ tools from vendors  
- Display Institution dashboards only to institutions  

### MUST NOT:
- Show pricing in Kids Mode  
- Leak municipal overlays publicly  

---

## 2. Contractor Profiles

Must show:
- License tags  
- Specialty  
- Service radius  
- Media gallery  

Must not show:
- Admin data  
- Pricing without context  
- Bid history outside institution dashboard  

---

## 3. RFQ UI

RFQ Creation UI must:
- Match backend categories  
- Use controlled inputs (no free text for scopes)  
- Show required fields clearly  
- Prevent past dates  
- Indicate bidding deadlines  

RFQ Review UI must:
- Sort by allowed metrics only  
- Never prefer one contractor visually  
- Remove pricing in Kids Mode  

---

## 4. Bid UI

Bids MUST display:
- Price  
- Scope summary  
- Timeline estimate  
- Vendor specialty  

Bids MUST NOT display:
- Disallowed metadata  
- Weighting outside governance  

Gateway rules enforced:
- Premium+ only  
- specialty must match RFQ  

---

## 5. Discovery Surfaces

### Required:
- 6–8 contractor cards per row  
- Strict specialty grouping  
- Rotation logic via backend only  

### Forbidden:
- Infinite horizontal scrolling  
- Algorithmic “best picks”  
- Contractor ranking beyond governance  

---

## 6. Safety Overlays (CRITICAL)

Storm, heat, and winter overlays must:
- Load only when activated by governance  
- Display clean icons  
- Avoid panic-like UI wording  
- Never load in Kids Mode  

---

## 7. Accessibility

- Full-size tap targets  
- Dyslexia-friendly label spacing  
- High-contrast warnings  

---

END OF QA