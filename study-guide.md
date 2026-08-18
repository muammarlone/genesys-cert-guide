# Genesys Cloud CX — Study Guide

## GCX-GCP: Professional Certification

**Exam:** 55 questions | 120 min | 65% pass | $580 | 3-year validity

### Domain Weights (approximate)

| Domain | Weight | Key Topics |
|--------|--------|------------|
| Platform & Architecture | ~30% | Org structure, regions, edge devices, telephony, security |
| Contact Center Admin & Implementation | ~50% | ACD, queues, routing, IVR, scripts, agents, campaigns |
| Reporting & Analytics | ~20% | Views, exports, historical vs real-time, dashboards |

### Platform & Architecture (~30%)

- Genesys Cloud organization hierarchy (org → divisions → locations)
- Edge appliances and BYOC (Bring Your Own Carrier) configuration
- WebRTC vs SIP phone options
- Telephony: DID, toll-free, trunk configuration
- Single Sign-On (SSO) and OAuth integration
- Roles and permissions model (built-in vs custom roles)
- Data retention policies and compliance features
- High availability and disaster recovery concepts

### Contact Center Admin & Implementation (~50%)

**ACD & Routing**
- Queue creation and configuration (utilization, skills, wrap-up)
- Skills-based routing vs queue-based routing
- Routing rules: bullseye, preferred agent, last-agent
- In-queue and on-hold flows
- Transfer types: blind, consult, voicemail

**IVR & Flows**
- Architect flow types: Inbound Call, Outbound, IVR, In-Queue, Bot
- Flow variables, data actions, and decision trees
- DTMF vs speech recognition input
- Prompt management and TTS configuration
- Error handling and fallback paths

**Agents & Workforce**
- Agent status states and transitions
- Wrap-up codes and after-call work
- Scripts and customer cards
- Callbacks and voicemail handling
- Outbound campaigns: preview, predictive, power dialing

**Digital Channels**
- Chat, email, messaging channel setup
- Web messaging configuration
- Co-browse and screenshare setup

### Reporting & Analytics (~20%)

- Real-time vs historical data distinction
- Key metrics: handle time, hold time, abandon rate, SLA
- Standard views: Queue Activity, Agent Activity, DNIS
- Custom report creation and scheduling
- Data export options (CSV, API)
- Performance dashboards

---

## GCX-ARC: Architect Certification

**Exam:** ~60 questions | 120 min | 65% pass | $580

### Domain Weights (approximate)

| Domain | Weight | Key Topics |
|--------|--------|------------|
| Solution Design | ~35% | Architecture patterns, scalability, HA |
| Platform Configuration | ~30% | Advanced routing, integrations, telephony |
| Migration & Implementation | ~20% | PSTN migration, legacy CCaaS transitions |
| Optimization | ~15% | Capacity planning, performance tuning |

### Key Architect Topics

**Architecture Patterns**
- Multi-region deployment strategies
- Edge network topology design
- Redundancy and failover configuration
- Hybrid deployment (Genesys Cloud + on-prem)

**Advanced Configuration**
- Data actions for CRM integration (Salesforce, ServiceNow)
- Genesys Cloud CTI adapter architecture
- Custom authentication flows
- Complex routing algorithms and expressions

**Migration**
- PSTN cutover planning (risk windows, rollback)
- Agent desktop migration strategies
- Legacy IVR to Architect flow migration
- Data migration from Avaya, Cisco, NICE

**Optimization**
- Trunk utilization analysis
- Concurrent call capacity planning
- Architect flow performance profiling
- Analytics API for custom reporting

---

## GCX-GCD: Developer Certification

**Exam:** ~60 questions | 120 min | 65% pass | $580

### Domain Weights (approximate)

| Domain | Weight | Key Topics |
|--------|--------|------------|
| Platform & Auth | ~20% | OAuth2, API structure, SDKs |
| Core APIs | ~35% | Users, conversations, routing, flows |
| Analytics & Notifications | ~20% | Analytics API, WebSocket notifications |
| Integrations & SDK | ~25% | AppFoundry, web messaging SDK, custom actions |

### Key Developer Topics

**Authentication**
- OAuth2 flows: Client Credentials, Authorization Code, Implicit
- Token scopes and least-privilege access
- OAuth client creation and rotation

**Core APIs**
- Users and Groups API
- Conversations API (real-time state, history)
- Routing API (queues, skills, utilization)
- Flows and Architect API
- Station and telephony endpoints

**Notifications**
- WebSocket notification channels
- Event types and subscription management
- Presence and conversation events

**Analytics API**
- Conversation aggregates vs detail queries
- Query filter structure and time ranges
- Bulk export via Analytics API

**Integration Patterns**
- Data Actions: REST actions in Architect flows
- Web Messaging SDK embedding
- Custom embedded client apps in agent desktop
- AppFoundry premium app architecture

---

## Architect Validation: Key Insights

**Strategy: Start with GCX-GCP** — Routing and ACD config (~50% of exam) overlaps heavily with GCX-ARC. Pass GCX-GCP first; architect exam builds on it.

**Warning: Domain weights are approximate** — Genesys does not publish official percentages. Study all domains; do not under-invest in "lower weight" areas.

**Warning: Exam questions are scenario-based** — Multiple answers may be technically correct. Choose the most operationally sound option (least disruption, best practice alignment).

**Tip: Hands-on Genesys Beyond labs are non-optional** — Text study alone fails against scenario questions. Allocate 60%+ of prep time to live environment practice.

**Tip: BYOC/Edge is frequently tested on GCX-GCP** — Many candidates skip telephony config. Edge appliance and BYOC trunk setup appear in ~20% of platform questions.

**Strategy: For GCX-GCD, master OAuth2 first** — Every API call depends on it. Auth failures block all subsequent development work and are a common exam trap.

**Strategy: GCX-ARC requires migration experience** — Architecture exam expects real-world migration scenario knowledge. Use community.genesys.com migration case studies as supplemental study.
