# ROOTED Construction — Application Architecture

ROOTED Construction is a vertical UI shell that operates entirely on top of:

- ROOTED Core (providers, RFQs, bids, bulk, analytics)
- ROOTED Platform Governance (roles, tiers, contractor rules, safety law)
- Civic-grade compliance & documentation logic

This is *not* a standalone app.  
It is a governed extension of the ROOTED OS.

---

## 🧠 Inherited Architecture Layers

Construction uses all standard ROOTED subsystems:

### Identity & Governance
- Auth / roles / tiers
- Feature flags
- Admin governance
- Contractor & institution rule separation

### Marketplace & Procurement
- RFQs at institutional + residential scale
- Multi-bid vendor responses
- Premium+ contractor capabilities
- Binding bid timelines
- Award-to-workflow pipeline (future)

### Discovery & Intelligence
- Contractors by specialty
- Licensed professionals
- Permit-type filtering
- Radius + max markers
- Seasonal overlays (storm, winter, heat safety)

### Safety & Trust Layer
- License verification UI (backend optional)
- Kids Mode construction blackout
- Hazard suppression in Kids Mode
- No minors in workforce pathways

### Analytics
- Bid win-rate
- Lead funnels
- Bulk / materials procurement analytics

---

## 🧬 Vertical Plug-In Doctrine

ROOTED Construction may introduce:

- Specialty categories (plumbing, electrical, roofing, GC, etc.)
- Permit-type metadata
- Residential vs institutional RFQ templates
- Skill & license filtering

But Construction **does NOT**:

- Modify procurement laws  
- Modify Kids Mode  
- Add new billing tiers  
- Add new marketplaces  
- Create new governance rules  

Construction inherits platform law.  
It only contributes UI and category logic.

---

## 🏗️ Core Domain Concepts

### 1. Contractors (Vendors)
Types:
- Independent contractor  
- Small firm  
- General contractor  
- Specialty licensed provider  

Tier Rules:
- Free: Public profile only  
- Premium: Basic analytics  
- Premium+: Full bidding & RFQ access  

### 2. Institutions
Municipalities, schools, property groups.

They may:

- Issue RFQs  
- Review bids  
- Award projects  

### 3. Residential Requests
Individuals may submit:
- “Home repair” requests  
- Safety issues (e.g., storm impact)  
*These convert into RFQs for contractors.*

### 4. Safety Intelligence
Season-driven warnings:
- Heat index advisories  
- Storm recovery overlays  
- Winter hazard tags  
- Emergency-only contractor filters  

---

## 🛑 Architectural Non-Negotiables

- UI cannot show bid tools to non-Premium+  
- Kids Mode may *never* surface construction tools  
- No contractor may message minors  
- No contractor may receive a “Kids Mode RFQ”  
- Discovery limits cannot be overridden (6–8 cards, 50 miles, 25 markers)  
- Admins cannot create or alter contractor licenses  

ROOTED Construction is a safety-critical vertical — all actions pass through governance.

---

## 🚧 Development Boundaries

Allowed:
- License-check UI  
- Contractor discovery UI  
- RFQ creation templates  
- Bid comparison UI  
- Safety overlays  

Forbidden:
- Backend logic rewrites  
- Creating new markets  
- Creating new billing models  
- Bypassing role/tier gates  

---

END OF ARCHITECTURE