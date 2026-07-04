# Vault-D1 MCP Read Contract v1.0
# Momentum Lab XV — Stable Interface Document

## Base ID
appP5870oQzfNRBcI

## Lead CRM Base ID
appDi2SzStH9A83Od

## Table Registry

| Contract File | Airtable Table | Table ID | Filter |
|---|---|---|---|
| business.md | Master_Industry_Library | tbltViC9sU5gyVi7o | Match Industry_Tag |
| audience.md | Core_Context_Matrix | tble58BjSLqe8y8l7 | Industry_Link + Component_Type = Audience_Pain |
| services.md | Core_Context_Matrix | tble58BjSLqe8y8l7 | Industry_Link + Component_Type = Service_Tier |
| faq.md | Core_Context_Matrix | tble58BjSLqe8y8l7 | Industry_Link + Component_Type = FAQ_Objection |

## Query Rules for Mo-15 Agents

1. Query Core_Context_Matrix filtered by Industry_Link → Industry_Tag = [target industry]
2. Pull all three Component_Types separately
3. NEVER read unverified records — filter by Data_Verified = true
4. Mo-15 agents NEVER write to Vault-D1. Read only.

## Hard Rules

- Data_Verified = false records do not exist to any agent
- Only Custos (Agent 13) writes to Vault-D1 intelligence tables
- Client contact data lives in Lead CRM base only — never in Vault-D1
- Four immutable contract files: business.md, audience.md, services.md, faq.md
