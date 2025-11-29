# ROOTED Construction — Backend Hardening Checklist

> Source of truth: `ROOTED_CONSTRUCTION_AUDIT_REPORT.md`  
> This file tracks **what’s actually done** in the database.

---

## Critical Fixes (Must Be True Before Production)

| # | Item | Status | Notes |
|---|------|--------|-------|
| 1 | Admin credential verification (`admin_credentials` table + `check_admin_credential_valid`) | ✅ DONE (per Supabase work) | Regional/admin actions require valid, active, MFA-enforced credentials. |
| 2 | Atomic bid deadline enforcement (`bid_submission_windows` + `submit_bid_atomic`) | ✅ DONE | Bids use server time, no client-time cheating, locked windows. |
| 3 | Escrow modeling (if/when payments are added) | ⚠️ NOT IMPLEMENTED YET | Escrow tables designed in audit, but NOT live until payments exist. |
| 4 | Entity relationship graph for COI detection (`entity_relationships`) | ✅ DONE / or ⚠️ PLANNED | Needed for inspector conflict-of-interest detection. Update as you implement. |
| 5 | Explicit role permissions model (no inheritance) | ⚠️ PARTIAL | Long-term goal: use explicit `permission_definitions` + `role_permissions`. |
| 6 | API rate limiting spec (app-layer, not DB) | ⚠️ TODO | To be implemented at API gateway / backend layer when service is live. |
| 7 | Inspection photo tampering prevention (`inspection_photos` schema) | ⚠️ PLANNED | Schema designed in audit; AI/tamper logic can be phased in. |
| 8 | Legal hold + export mechanism (`legal_holds` + export function) | ⚠️ PLANNED | Required before serious municipal/legal contracts. |

---

## Compliance & Data Protection

| Item | Status | Notes |
|------|--------|-------|
| PII anonymization strategy for safety + audit logs | ⚠️ Designed, not fully implemented | `data_retention_policies` + anonymization functions described in audit. |
| Data retention vs. GDPR/CCPA conflict handling | ⚠️ In progress | Safety records anonymized, not deleted. |
| Legal hold freeze behavior | ⚠️ To be implemented | Records under `legal_holds` cannot be modified/deleted. |

---

## Operational Safeguards

| Scenario | Covered? | Notes |
|----------|----------|-------|
| License expires mid-project → emergency work stoppage | ⚠️ Designed in audit | `emergency_license_expiration_halt` function to be implemented. |
| Critical inspection fails → remediation & liability tracking | ⚠️ Designed | `failed_inspection_remediation` table + flow. |
| Municipal permit API is offline | ⚠️ Designed | `external_api_health` + `submit_permit_with_retry`. |

---

## Multi-Vertical Compatibility

| Item | Status | Notes |
|------|--------|-------|
| `vertical_id` support in roles/permissions | 🟡 Planned | Needed as ROOTED adds more verticals beyond Community + Construction. |
| Platform-wide unified analytics view | 🟡 Future | Aggregate metrics across all verticals. |

---

## How to Use This File

- Update the ✅ / ⚠️ as you actually implement each piece.  
- For anything marked **⚠️**, you’re allowed to:
  - Launch small regional pilots (with clear limits)
  - But NOT claim “enterprise-ready” for large municipalities until resolved.

For **full details**, always defer to:  
`ROOTED_CONSTRUCTION_AUDIT_REPORT.md`
