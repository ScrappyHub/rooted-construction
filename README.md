# ROOTED Construction — Vertical Application

This repository is the **Construction vertical** for ROOTED.

It is a governed B2B layer on top of:

- `rooted-core` (shared schema, RLS, RFQs, bids, bulk, workforce)
- `rooted-platform` (governance, safety, access law)

Construction is **backend-first**:  
the markets and enforcement live in `rooted-core`; this repo wires them into UI.

---

## 🏗 What ROOTED Construction Is

ROOTED Construction exists to:

- Connect **institutions, owners, and GC’s** with verified contractors
- Run **RFQ → bid** workflows for projects
- Offer **bulk materials** and logistics marketplace (Premium+)
- Coordinate **workforce & subcontractor pools** within governance limits
- Surface **jobsite conditions** via `vertical_conditions_v1`

Construction is:

- ✅ B2B-only
- ✅ Heavily governed
- ✅ Safety and compliance focused
- ❌ Not a gig app
- ❌ Not an open job board

---

## 🔒 Governance Boundaries

This repository:

- ❌ Does **NOT** define roles or tiers
- ❌ Does **NOT** alter bid/bulk schemas
- ❌ Does **NOT** bypass billing or subscription checks
- ❌ Does **NOT** change workforce protections or abuse rules
- ❌ Does **NOT** modify Kids, Sanctuary, or Community law

Those live in:

- `rooted-platform/governance/`
- `rooted-core/docs/`

Construction UI must obey:

- `ROOTED_VERTICAL_ACCESS_CONTRACT.md`
- `BILLING_ARCHITECTURE.md`
- `ROOTED_ACCESS_POWER_LAW.md`
- `ROOTED_DEBUG_TOOLKIT_CORE.md`

---

## 🧬 Vertical Scope

Within those boundaries, Construction focuses on:

- Institution & owner **project dashboards**
- RFQ creation and management screens
- Vendor-side **bid submission** flows (Premium+ only)
- Bulk materials **offer** and **selection** flows
- Workforce / subcontractor pool **surfacing** (not open gig spam)
- Jobsite **conditions widgets** sourced from `vertical_conditions_v1`

Construction does **not**:

- Invent new payment flows
- Allow unverified or mis-tiered accounts into markets
- Expose workforce tools in Kids Mode or Community

---

## ✅ Allowed Work Here

- UI wiring for RFQ, bid, and bulk flows
- Construction-specific dashboards and views
- Workforce pool presentation (respecting tier + law)
- Performance, mobile, and UX polishing
- Data visualizations on **approved analytics** from core

## ❌ Forbidden Work Here

- “Quick hacks” that bypass RLS or feature_flags
- Turning workforce into public gig listings
- Creating construction-only identity or login flows
- Bypassing the abuse / debug toolkits and admin audit logs

---

## 🔗 Source of Authority

Construction is bound by:

- `rooted-core` → actual RFQ, bid, bulk, workforce logic
- `rooted-platform` → law and power limits

If Construction UI and root governance disagree →  
**governance wins**.
