# Genesys Cloud CX — Flashcards

Quick Q&A pairs for GCX-GCP, GCX-ARC, and GCX-GCD exam prep. Cover all domains.

---

## Platform & Architecture

**Q: What are the three main queue routing strategies in Genesys Cloud?**
A: Skills-based routing, bullseye routing, and preferred agent routing.

**Q: What is a Division in Genesys Cloud?**
A: A logical organizational unit for grouping resources (queues, flows, users) with separate permission boundaries within an org.

**Q: What is BYOC (Bring Your Own Carrier)?**
A: Connecting a third-party SIP trunk to Genesys Cloud instead of using Genesys-managed telephony.

**Q: What is the difference between WebRTC and SIP phones in Genesys Cloud?**
A: WebRTC runs in the browser — no hardware needed. SIP requires a physical or software phone registered to Genesys Cloud SIP infrastructure.

**Q: What is an Edge appliance?**
A: On-premises hardware or VM that bridges the customer's telephony/network to Genesys Cloud, enabling BYOC and local call processing.

**Q: What does SSO integration allow?**
A: Users authenticate via their corporate identity provider (e.g., Okta, Azure AD) instead of a Genesys Cloud password.

**Q: Name three built-in admin roles in Genesys Cloud.**
A: Admin, Analyst, and Attendant. (Other built-ins vary by org configuration.)

---

## ACD & Routing

**Q: What is bullseye routing?**
A: A routing method where agents are progressively expanded by skill match — starts with full skill match, then relaxes requirements after configurable wait times.

**Q: What is wrap-up in Genesys Cloud?**
A: Post-interaction time for agents to complete after-call work before becoming available again.

**Q: What is the difference between a blind transfer and a consult transfer?**
A: Blind transfer sends the call immediately without speaking to the destination first. Consult transfer lets the agent talk to the destination before completing the transfer.

**Q: What triggers an in-queue flow?**
A: When a caller is waiting in queue — used for estimated wait time messaging, callbacks, or queue escape options.

**Q: What is a wrap-up code?**
A: A label agents apply at end of interaction to categorize outcome (e.g., "Sale", "Support", "Escalation") for reporting.

**Q: What is utilization in Genesys Cloud?**
A: Setting that controls how many simultaneous interactions an agent can handle per media type (voice, chat, email).

---

## Architect Flows

**Q: What are the five main flow types in Architect?**
A: Inbound Call, Outbound Call, IVR, In-Queue Call, and Bot.

**Q: What is a Data Action in Genesys Cloud?**
A: A configured REST API call made from within an Architect flow to fetch or push data to external systems (CRM, databases, etc.).

**Q: What is the purpose of a Default Action in a flow?**
A: Handles outcomes when no other conditions match — the fallback path.

**Q: What is a flow variable?**
A: A named container that stores data within a flow execution (e.g., customer ID, account balance).

**Q: What is the difference between TTS and a pre-recorded prompt?**
A: TTS (Text-to-Speech) generates audio dynamically from text. Pre-recorded prompts are uploaded audio files — higher quality but static.

---

## Reporting & Analytics

**Q: What is the difference between historical and real-time analytics?**
A: Real-time shows current queue/agent state with minimal delay. Historical aggregates completed interaction data for trend analysis.

**Q: What metric measures the percentage of calls answered within a target time?**
A: Service Level (SL%) — typically expressed as "X% of calls answered within Y seconds."

**Q: What is abandon rate?**
A: Percentage of inbound calls that disconnect before an agent answers.

**Q: Name two standard views in Genesys Cloud reporting.**
A: Queue Activity view and Agent Activity view.

**Q: What is ASA (Average Speed of Answer)?**
A: Average time callers wait from entering queue to being connected to an agent.

---

## Developer & API

**Q: What OAuth2 grant type is used for server-to-server API calls with no user context?**
A: Client Credentials grant.

**Q: What OAuth2 grant type is used for web applications where a user authenticates?**
A: Authorization Code grant.

**Q: What is the base URL for Genesys Cloud API?**
A: Region-specific — e.g., `https://api.mypurecloud.com` (US East), `https://api.mypurecloud.ie` (EU Ireland).

**Q: How do you receive real-time events in Genesys Cloud?**
A: Notifications API via WebSocket channels — subscribe to topics to receive event payloads.

**Q: What is a channel in the Notifications API?**
A: A WebSocket connection endpoint that the client subscribes topics to in order to receive real-time event data.

**Q: What does the Conversations API return?**
A: Conversation details including participants, segments, timestamps, media type, and state history.

**Q: What is the Analytics API used for?**
A: Querying aggregated and detail conversation data — metrics like handle time, wait time, and queue volumes.

**Q: What is an AppFoundry app?**
A: A third-party or custom integration published to the Genesys AppFoundry marketplace, installable into Genesys Cloud orgs.

---

## Architect-Level Concepts

**Q: What is a multi-region Genesys Cloud deployment used for?**
A: Geographic redundancy, data residency compliance, and minimizing latency for globally distributed contact centers.

**Q: What is the recommended approach for a legacy IVR migration to Genesys Architect?**
A: Map existing DNIS/call flows first → rebuild in Architect flows → parallel-test with production traffic → cut over by DNIS.

**Q: What is the risk of a PSTN cutover during business hours?**
A: Live call disruption if trunk routing fails; always schedule cutovers in low-traffic windows with rollback plan.

**Q: What is capacity planning in Genesys Cloud?**
A: Sizing trunks, agents, and queues to handle peak concurrent call volumes without queue overflow or abandonment spikes.

**Q: What does CTI (Computer Telephony Integration) enable in Genesys Cloud?**
A: Screen-pop, automatic call logging, and click-to-dial between the agent desktop and CRM systems like Salesforce or ServiceNow.
