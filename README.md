## Governance Boundaries

This repository:

- Does NOT define roles, tiers, or access laws
- Does NOT change database schema or RLS
- Does NOT define Kids Mode or sanctuary rules

All governance and access control lives in:

→ https://github.com/.../rooted-platform

---

Any change that attempts to bypass ROOTED governance is invalid by design.


# ROOTED Construction Vertical

> Regional Construction & Built Environment Operating Layer  
> **Not** a standalone app — this vertical plugs into the ROOTED Core.

---

## What This Repo Is

This repo contains the **specs, hardening plan, and future UI wiring** for the **ROOTED Construction vertical**, built on top of the existing ROOTED platform.

It reuses the **same governed core** as ROOTED Community:

- Supabase Auth (no custom auth here)
- Roles: `guest`, `individual`, `vendor`, `institution`, `admin`
- Tiers: `free`, `premium`, `premium_plus`
- `user_tiers` + `feature_flags` as the **single source of truth**
- Shared tables:
  - `providers`
  - `rfqs`, `bids`, `bulk_offers`, `bulk_offer_analytics`
  - `events`, `event_registrations`
  - `conversations`, `messages`
  - `landmarks`
  - `feed_items`, `feed_comments`, `feed_likes`
  - `vendor_analytics_*`
  - `account_deletion_requests`
  - `kv_store_f009e61d`

This vertical **does not** change any of that.  
It only adds **construction-specific logic, flows, and UI**.

---

## What the Construction Vertical Does

The Construction vertical models:

- Contractors, trades, suppliers (as `providers`)
- Institutional RFQs for:
  - Schools
  - Municipal projects
  - Infrastructure
- Bids and bulk offers using the existing marketplace engine
- Inspections, permits, safety workflows (as specs + flows)
- Workforce and education experiences (tied to construction)
- Landmarks:
  - Bridges, historic buildings, mills (education-only)

It is meant to support:

- Safer construction
- Cleaner procurement
- Clearer audit trails
- Real-world civic infrastructure work

---

## What It Is NOT

- ❌ Not a separate authentication system  
- ❌ Not a replacement for ROOTED Community  
- ❌ Not a crypto or token system  
- ❌ Not a way to bypass Kids Mode or cultural consent  
- ❌ Not financial custody on its own (escrow must use licensed rails)

All **roles, safety rules, consent systems, and RLS** remain governed by ROOTED Core.

---

## Key Documents in This Repo

- `ROOTED_CONSTRUCTION_AUDIT_REPORT.md`  
  Full pre-production audit: logic, security, compliance, failure modes.

- `CONSTRUCTION_BACKEND_HARDENING_CHECKLIST.md`  
  Short checklist of critical hardening items and their status.

As this vertical grows, new files will live under:

- `docs/` for specs, flows, and diagrams  
- `ui/` or `app/` for construction-specific UI wiring (reusing ROOTED Core APIs)

---

## Status

- ✅ Audit completed (pre-production)
- ✅ Critical hardening items implemented in Supabase (per your work)
- 🟡 UI wiring not yet implemented
- ⏳ No production launch announced — this vertical is still in build phase

All future work in this repo must:

1. Reuse ROOTED Core (no forked auth / roles / tiers)  
2. Respect existing Kids Mode, consent, and RLS rules  
3. Stay aligned with the ma
