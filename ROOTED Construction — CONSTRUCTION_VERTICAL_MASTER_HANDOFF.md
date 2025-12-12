# ROOTED Construction — Master Handoff (UI + Backend Alignment)

Status: Documentation-complete  
Scope: Construction vertical UI only  
Backend: Powered by ROOTED Core procurement engine  

If the app behavior and this document conflict → this document wins.

---

## 1. What ROOTED Construction Is

A civic-grade procurement + contractor discovery vertical designed for:

- Municipal RFQs  
- Institutional facility RFQs  
- Residential repair needs  
- Licensed trade discovery  
- Seasonal safety overlays  

Construction is:

✅ Civically aligned  
✅ Safety-first  
❌ NOT a gig-economy platform  
❌ NOT a bidding “race to the bottom”  
❌ NOT a messaging platform for minors  

---

## 2. Roles & Access (Backend-Enforced)

### 2.1 Guest
Can:
- Browse contractors  
- View safety overlays  
Cannot:
- Issue RFQs  
- Submit bids  

### 2.2 Individuals (Residents)
May:
- Submit home repair requests  
- View contractor profiles  

May NOT:
- View bid history  
- Act as vendors  

### 2.3 Contractors (Vendors)

Shared abilities:
- Public profile  
- Media gallery  
- Specialty tags  

Tiered abilities:

FREE  
- No bids  
- No analytics  
- No RFQ response

PREMIUM  
- Basic analytics  
- Highlighted discovery  
- No bidding

PREMIUM PLUS  
- Full bidding  
- Procurement analytics  
- Priority ranking  

### 2.4 Institutions
May:
- Issue RFQs  
- Review bids  
- Award projects  

### 2.5 Admin
May:
- Moderate contractor profiles  
- Validate documents  
- Enforce safety overlays  

May NOT:
- Override procurement laws  
- Assign licenses manually  

---

## 3. Kids Mode (Construction)

Kids Mode must remove ALL construction content.

Hidden:
- Contractors  
- Bids  
- RFQs  
- Repair requests  
- Safety warnings involving hazards  

Kids Mode may show:
- “What is construction?” educational micro-content (optional future)  

---

## 4. Discovery Surfaces

Contractor discovery must follow:

- 6–8 cards per category  
- No stacked lists  
- License + specialty filters  
- Max radius 50 miles  
- Max markers 25  
- Seasonal overlays ON  

---

## 5. RFQ Templates

Construction includes 3 template types:

1. Residential Repair  
2. Institutional Facility  
3. Municipal Capital Project  

All templates use the SAME backend objects:
`rfqs`, `bids`, `providers`, `specialty_types`.

Frontend template differences = UI-only.

---

## 6. Launch Checklist

- Contractor discovery  
- Specialty filtering  
- RFQ create flow  
- Bid comparison flow  
- Safety overlays  
- License metadata display  
- Premium+ enforcement  

---

END OF HANDOFF