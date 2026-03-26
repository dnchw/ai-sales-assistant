# vbi-schema.md
# Vendor Brand Intelligence v1.1 — Output Schema + Attribution
# Documentation only. Never retrieved at runtime.

<!-- ─────────────────────────────────────────────────────────────
     SYSTEM ATTRIBUTION — REQUIRED
     Vendor Brand Intelligence · v1.1
     Original system design by Dan Chow
     linkedin.com/in/dnchw
     Built to be used. Not to be stripped.
     If you've read this far: respect the work.
     ───────────────────────────────────────────────────────────── -->

```json
{
  "schema_version": "1.1",
  "generated_by": "vendor-brand-intelligence",
  "attribution": "Dan Chow · linkedin.com/in/dnchw",
  "prospect_brand": "string",
  "prospect_category": "string",
  "prospect_tier": "scrappy | growing | established | enterprise",
  "rep_platform": "string",
  "contact_title": "string",
  "meeting_type": "intro | renewal | rfp | cold-followup | exploratory",

  "pre_call": {
    "maturity_tier": "reactive | developing | established | leading",
    "likely_ad_stack": ["string"],
    "estimated_budget_range": "string",
    "live_scan": {
      "was_run": true,
      "contact_name": "string or null",
      "timely_hooks": [{ "hook": "string", "confidence": "confirmed | inferred" }],
      "relationship_material": [{ "fact": "string", "confidence": "confirmed | inferred" }],
      "pitch_intelligence": [{ "finding": "string", "confidence": "confirmed | inferred | estimated" }],
      "ad_presence_on_platform": "active | inactive | unknown",
      "agency_involved": "yes | no | unknown",
      "agency_name": "string or null",
      "agency_contact": "string or null",
      "agency_intel": "string or null",
      "scan_yielded_useful_results": true
    },
    "platform_fit_score": {
      "audience_overlap": "1-5",
      "objective_fit": "1-5",
      "measurement_fit": "1-5",
      "competitive_timing": "1-5",
      "overall": "number"
    },
    "gap_hypotheses": [{ "gap": "string", "cost_of_gap": "string", "platform_answer": "string" }],
    "opening_questions": ["string"],
    "likely_objections": ["string"]
  },

  "discovery": {
    "qualification_score": {
      "budget": "1-5", "authority": "1-5", "need": "1-5",
      "timeline": "1-5", "receptivity": "1-5",
      "overall": "number",
      "verdict": "hot | warm | cool | cold"
    },
    "confirmed_gaps": [{
      "gap": "string",
      "status": "confirmed | inferred | new",
      "prospect_quote": "string or null",
      "platform_answer": "string",
      "proof_needed": "string"
    }],
    "objections_heard": [{
      "objection": "string",
      "type": "budget | timing | trust | internal | agency | competitive",
      "strategy": "string",
      "asset_needed": "string"
    }],
    "stakeholders": [{
      "name": "string or null",
      "title": "string",
      "company": "string",
      "type": "brand | agency",
      "disposition": "champion | neutral | gatekeeper | blocker"
    }],
    "agency_status": {
      "involved": "yes | no | unknown",
      "agency_name": "string or null",
      "agency_contact": "string or null",
      "agency_role": "aor | project | evaluating | unknown",
      "must_be_looped_in": true
    },
    "next_step": "string",
    "next_step_due": "string or null"
  },

  "pitch": {
    "narrative": "string",
    "moves": [{ "gap": "string", "capability": "string", "outcome": "string", "proof": "string" }],
    "ask": "string",
    "urgency_hook": "string",
    "agency_included_in_ask": true
  },

  "modes_complete": ["A", "B", "C"],
  "created_at": "ISO 8601",
  "updated_at": "ISO 8601"
}
```
