# Genesys Cloud CX — Exam Tips & Strategies

Architect-validated pitfalls, strategy notes, and test-taking guidance.

---

## General Test-Taking Strategy

**All questions are scenario-based.** Multiple answers may be technically correct — choose the most operationally sound option. Ask yourself: "What would a senior Genesys engineer recommend in production?"

**Time management:** 55 questions in 120 minutes = ~2 min/question. Flag uncertain questions and return. Don't get stuck.

**"Best practice" answers beat technically valid answers.** If two options both work but one is cleaner or less disruptive, choose it.

---

## GCX-GCP: Professional

### High-Value Topics (appear frequently)

1. **Bullseye routing mechanics** — Know how skill tier timeouts work and when to use vs skills-based routing
2. **Wrap-up and after-call work** — Know the difference between timeout vs manual completion
3. **Architect flow error paths** — Always know what the Default/Failure action does in each action type
4. **Queue utilization settings** — Know how max interactions per agent is configured and its effect on routing
5. **Real-time vs historical distinction** — Exam distinguishes these sharply; don't confuse them

### Common Mistakes

- **Confusing transfer types:** Blind vs consult vs attended transfer — know each precisely
- **Underestimating telephony domain:** BYOC, Edge, and trunk config appear in ~20% of questions; many candidates skip this
- **Forgetting role/division scope:** Permissions questions often hinge on whether an action is org-wide or division-scoped
- **Selecting "more capable" over "appropriate" options:** Choose the minimal-disruption approach for admin scenario questions

### Recommended Prep Split

- 40% Genesys Beyond official courses (GCX-GCP track)
- 30% Hands-on lab in trial or sandbox org
- 20% Practice exams (certificationbox, ExamTopics community notes)
- 10% Review community.genesys.com for real-world edge cases

---

## GCX-ARC: Architect

### High-Value Topics

1. **Migration scenarios** — Legacy CCaaS to Genesys Cloud cutover planning; risk mitigation
2. **Multi-site telephony design** — Edge topology, trunk redundancy, geo-routing
3. **Data Action design** — When to use data actions vs pre-built integrations
4. **Capacity planning math** — Erlang-C basics; traffic sizing for trunks and agents
5. **Security architecture** — SSO, OAuth scoping, PCI compliance zone design

### Common Mistakes

- **Treating ARC as GCP+** — ARC requires architectural *design* thinking, not just configuration knowledge
- **Ignoring migration domain** — ~20% weight; requires real-world migration experience to answer well
- **Missing HA requirements:** Exam expects you to identify single points of failure and recommend redundancy
- **Underspecifying in answers:** ARC answers need specifics — "configure Edge with SRTP" not just "secure the call"

### Recommended Prep Split

- 30% Genesys Beyond Architect track courses
- 40% Real migration/design projects or case study review
- 20% Community forum deep dives (migration threads)
- 10% Official Genesys architecture whitepapers

---

## GCX-GCD: Developer

### High-Value Topics

1. **OAuth2 flows** — Client Credentials vs Auth Code vs Implicit; know when each applies
2. **Notifications API** — WebSocket channel lifecycle; topic subscription syntax
3. **Analytics query structure** — Filter object shape, time range format, metric names
4. **Data Actions in Architect** — How to authenticate to external APIs from within flows
5. **Conversation API state machine** — Know participant states (alerting, connected, disconnected)

### Common Mistakes

- **Token scope confusion:** Know which scopes are needed for read-only vs write operations
- **Region endpoint errors:** API base URL is region-specific — exam tests whether you know this
- **Conflating REST and WebSocket:** Notifications use WebSocket (not REST polling); confusing them = wrong answers
- **Analytics query filter mistakes:** Filter syntax errors are a common developer trap; practice with live API

### Recommended Prep Split

- 25% Genesys Cloud Developer Center documentation (thorough read)
- 40% API Explorer hands-on (build and test real API calls)
- 20% Genesys Beyond Developer track courses
- 15% SDK samples and open-source Genesys GitHub repos

---

## Scheduling Your Exams

- **Register at:** [Genesys Beyond → Certifications](https://beyond.genesys.com)
- **Proctoring:** Online via Pearson VUE — test from home or test center
- **Reschedule:** Free if done 24+ hours before exam
- **Retake policy:** 14-day wait after first fail; 60-day wait after second fail
- **Validity:** 3 years from pass date; recertify via updated exam or continuing education credits

---

## Recommended Study Timeline

### GCX-GCP (6–8 weeks for beginners, 3–4 weeks with 6+ months Genesys experience)

| Week | Focus |
|------|-------|
| 1–2 | Genesys Beyond GCX-GCP courses + org setup in trial |
| 3–4 | Routing, Architect flows, IVR hands-on labs |
| 5–6 | Analytics, reporting, practice exams |
| 7–8 | Weak area review + final practice exam (target 80%+) |

### GCX-GCD (4–6 weeks for experienced devs)

| Week | Focus |
|------|-------|
| 1 | OAuth2, API structure, SDK setup |
| 2–3 | Core APIs: Users, Conversations, Routing |
| 4 | Notifications + Analytics API |
| 5–6 | Integration patterns + practice exams |

---

## Key URLs

| Resource | URL |
|----------|-----|
| Genesys Beyond (training + cert registration) | https://beyond.genesys.com |
| Developer Center (API docs) | https://developer.genesys.cloud |
| API Explorer (live API testing) | https://developer.genesys.cloud/devapps/api-explorer |
| Community forums | https://community.genesys.com |
| AppFoundry | https://appfoundry.genesys.com |
| GitHub (SDK samples) | https://github.com/MyPureCloud |
