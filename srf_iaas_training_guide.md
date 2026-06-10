# SRF IaaS Team — Internal Training Guide
> Farm Solutions Group (FSG) · Super Renders Farm

---

## Table of Contents
1. [Team & Roles](#1-team--roles)
2. [SaaS → IaaS Shift](#2-saas--iaas-shift)
3. [IaaS Pricing Reference](#3-iaas-pricing-reference)
4. [Pre-Sales Playbook](#4-pre-sales-playbook)
5. [Support Procedures](#5-support-procedures)
6. [Case Study: Adcetera #33493](#6-case-study-adcetera-33493)

---

## 1. Team & Roles

The **Farm Solutions Group (FSG)** is SRF's dedicated unit for high-touch IaaS accounts. It bridges pre-sales and ongoing support under a single team so clients never fall through the gap between "closed deal" and "render day."

> **Why a unified team?** IaaS deals involve long discovery, custom pricing, onboarding, and real-time render support — all with the same client. Splitting these across separate sales and support orgs creates handoff failures (as seen in Adcetera). FSG owns the account end-to-end.

---

### Roles & Responsibilities

#### Solutions Lead `Pre-sales + Account`
*Owns the full client journey from first contact to account health*

- Qualifies inbound leads and determines IaaS vs SaaS fit
- Runs discovery calls to scope node count, duration, software stack, and deadline
- Generates formal quotes in writing within 24 hours of any verbal estimate
- Owns pricing negotiation and escalation to Director when discounts are needed
- Introduces clients to the Render Engineer at handoff; stays CC'd throughout
- Monitors account health and surfaces renewal / upsell opportunities

#### Render Engineer `Technical Support`
*Technical owner from onboarding through wrap-up*

- Provisions dedicated nodes and installs agreed software (3ds Max, Maya, C4D, Blender, Houdini, render engines)
- Sets up client pipeline integrations: Deadline, Backburner, LucidLink filespace, Suite Studios environment
- Responds to technical issues within 1 hour during active render windows
- Verifies node stability and uptime before client's start date (pre-flight check)
- Documents any custom configurations per account for future reference

#### FSG Coordinator `Operations`
*Keeps all active accounts moving and documented*

- Tracks all active IaaS accounts: start dates, end dates, invoicing status
- Sends invoices and follows up on payment confirmation before capacity is secured
- Logs all verbal commitments in the CRM immediately; nothing lives only in chat
- Manages vendor onboarding paperwork (company details, billing email, PO numbers)
- Flags accounts approaching end-of-period to Solutions Lead for renewal conversation

---

### Team Operating Norms

| Norm | Rule |
|------|------|
| ⏱ **Quote SLA** | Any rough estimate must be labeled "this is a rough estimate." A formal written quote follows within 24 hours. No verbal pricing is binding. |
| ✏️ **Paper trail rule** | Every pricing discussion, commitment, or scope change must be confirmed in writing in the shared chat or by email before work begins. |
| 🔄 **Handoff protocol** | Solutions Lead formally introduces Render Engineer in the client chat before start date, with a summary of agreed scope posted for all parties. |
| 📅 **Capacity lock** | Nodes are reserved in the system only after invoice payment confirmation — not on verbal go-ahead. |

---

## 2. SaaS → IaaS Shift

SRF has historically operated as a managed SaaS render farm. The IaaS rental model is a fundamentally different product. Every FSG member must understand this distinction to set accurate expectations.

### SaaS vs IaaS Comparison

| | Managed SaaS (legacy) | IaaS Rental (new focus) |
|---|---|---|
| **Client does** | Upload scene file, set parameters, download output | Full remote access, runs own pipeline |
| **SRF does** | Job scheduling, software, licensing, farm management | Provision hardware, pre-install software, 24/7 uptime |
| **Billing** | Per frame or node-hour, pay-as-you-go | Flat weekly/monthly rate per dedicated node block |
| **Best for** | Occasional renders, known pipelines | Recurring production, custom pipelines, events |

> ⚠️ **Critical mindset shift:** In IaaS, the client operates the nodes. SRF is the infrastructure provider, not the render operator. When a client says "the render isn't working," first determine: hardware/node issue (SRF's responsibility) or pipeline/software issue (client-operated, SRF assists)?

---

### Key Differences That Affect Quoting

| Topic | IaaS reality |
|-------|-------------|
| Pricing basis | Per dedicated node, per week/month — regardless of render usage |
| Node availability | Dedicated reservation pulls from public pool — costs more than shared access |
| Duration premium | Shorter periods have a higher per-week cost than monthly commitments |
| Software | SRF pre-installs; client may need own renderer licenses (check per engine) |
| Support scope | Priority 24/7 included; covers hardware issues + basic pipeline guidance |

---

### Supported Integrations to Know

When a client mentions their pipeline stack, mention which integrations SRF can pre-install. This shifts the conversation from "renting hardware" to "getting a ready-to-go production environment."

`LucidLink filespace` `Suite Studios environment` `AWS Thinkbox Deadline` `Backburner` `Royal Render / OpenCue` `Cyberduck file transfer` `Forest Pack / RailClone` `Anima crowd simulation` `After Effects + plugin matrix` `V-Ray / Arnold / Redshift / Octane` `3ds Max / Maya / C4D / Houdini / Blender`

---

## 3. IaaS Pricing Reference

> Current rates from [superrendersfarm.com/render-farm-rental](https://superrendersfarm.com/render-farm-rental). Always send the link alongside any quote — never quote from memory alone.

---

### CPU Server Nodes
**2x Intel Xeon E5-2680 V4 · 28 cores / 56 threads @ 3.2 GHz · 82 GB RAM · 400 GB storage**

| Render Nodes | Week | 1 Month |
|---|---:|---:|
| 5 nodes | $300 | $750 |
| 10 nodes | $600 | $1,500 |
| 20 nodes | $1,200 | $3,000 |
| 50 nodes | $3,000 | $7,500 |
| 100 nodes | $6,000 | $15,000 |

---

### GPU Render Machines (RTX 5090)
**AMD Ryzen 9 9950X @ 4.3 GHz · 2x RTX 5090 (32 GB vRAM each) · 256 GB RAM · 2 TB SSD**

IaaS dedicated rental saves **33%+** vs standard pay-as-you-go rates.

| Machine Count | Standard Weekly Rate | Discount | IaaS Weekly Rate |
|---|---:|:---:|---:|
| 1 GPU Machine | ~~$1,750~~ | 33% Off | **$1,172.50** |
| 3 GPU Machines | ~~$5,250~~ | 33% Off | **$3,517.50** |

> **Adcetera benchmark:** 18x RTX 5090 machines, dedicated 24/7, 3-week block (May 23 – June 13) = **$25,500** (director-approved floor). Use as a calibration reference for similar-scale GPU fleet quotes.

---

### Quoting Rules

1. **Always distinguish estimate vs quote** — A rough estimate based on standard node-hour rates is NOT a locked price. Say: *"This is a rough estimate — I'll send you the formal quote once I confirm dedicated availability."* Never let a rough number become the anchor without that caveat.

2. **Dedicated reservation premium exists** — Pulling nodes from the public pool for exclusive use incurs a premium — especially for high-demand hardware like RTX 5090s. This WILL make the formal quote higher than a casual estimate. Flag this proactively.

3. **Duration affects per-week cost** — In the Adcetera case: 2-week = $17k, 4-week = $34k, 3-week = $25.5k. The rate doesn't scale linearly — confirm with your Director for non-standard durations rather than interpolating.

4. **Loyalty / volume discounts require Director approval** — For clients with 5+ shows/year or confirmed multi-project commitments, a Yearly Capacity & Price Lock can be offered — fixed rates, guaranteed access, reserved environment. This needs Director sign-off before quoting.

---

## 4. Pre-Sales Playbook

The pre-sales motion for IaaS is fundamentally different from SaaS upsells. It requires deep discovery, careful expectation-setting, and a written quote before any commitment is accepted.

---

### Step 1 — Qualify the Lead

Determine if IaaS is the right fit before investing in a full scope conversation. Ask:

- [ ] Do they have a custom pipeline or software SaaS can't accommodate?
- [ ] Is their project on a tight deadline that requires dedicated capacity (no queue)?
- [ ] Is the scale large enough to justify a dedicated environment ($5k+ engagement)?
- [ ] Do they have recurring production (events, shows, series) where capacity lock has value?

---

### Step 2 — Run Discovery

Collect **all** of the following before generating any number. Missing items = inaccurate quote.

| Field | What to ask |
|-------|-------------|
| **Node count** | How many dedicated nodes? What GPU/CPU preference? |
| **Duration** | Start date, end date. Exact dates matter for capacity planning. |
| **Software stack** | DCC app, render engine, plugins, render manager (Deadline, etc.) |
| **Pipeline extras** | LucidLink? Suite Studios? Custom storage integration? |
| **Deadline pressure** | Is there a hard broadcast / event date? Queue risk is the key fear. |
| **Future projects** | How many projects/year? Opens Yearly Capacity Lock conversation. |

---

### Step 3 — Quote Correctly

Check current dedicated availability with your provisioning team **before** sending numbers. A formal written quote must include:

1. Node count & hardware spec
2. Exact start and end dates
3. Software to be pre-installed
4. Flat rate total (not hourly)
5. Payment terms (invoice before capacity lock)
6. Validity period for the quote (recommend 48–72 hours)

---

### Step 4 — Handle Objections

**"The price is higher than your estimate"**
> Acknowledge the gap directly. Explain that the initial estimate was based on standard pool rates, and dedicated reservation for high-demand hardware (especially RTX 5090) carries a premium. Own the communication gap. Then ask: what budget range are we working with? Can we adjust node count or duration to fit?

**"We're also talking to Rebus / iRender / another provider"**
> Don't compete on price alone. Emphasize: dedicated 24/7 environment (no shared queue), pre-installed Suite Studios / LucidLink support, priority tech support during active renders, 99.9% uptime SLA, and free setup.

**"We only need X weeks, not a month"**
> Non-standard durations require Director approval — do not interpolate the rate yourself. Be transparent: *"Let me confirm the rate with my team — I'll have it for you within a few hours."*

---

### Step 5 — Lock Capacity

> ✅ **Capacity is reserved only after payment confirmation.** Once the client agrees, send the invoice immediately. Inform them: *"I'll mark the dates as reserved once we receive payment confirmation — this guarantees no one else gets those nodes before your start date."* Do not reserve in the system before payment unless your Director explicitly approves a hold.

---

## 5. Support Procedures

IaaS clients have dedicated hardware and a right to priority response. These procedures replace the standard SaaS support queue for any active rental account.

---

### Onboarding Timeline

| Milestone | Action |
|-----------|--------|
| **D-7** | Invoice sent, payment confirmed, company details and billing email collected. |
| **D-5** | Render Engineer sets up dedicated environment, pre-installs all agreed software and plugins. |
| **D-3** | Pre-flight check: Render Engineer verifies all nodes stable, software licensed, storage/filespace mounted. Logs results. |
| **D-1** | Solutions Lead posts handoff message in client chat: confirmed scope, node specs, access credentials, RE contact, support channel. Nothing verbal. |
| **Day 1** | Render Engineer available for first 2 hours. Proactive check-in if no job submitted by midday. |

---

### Active Render Period

| Type | Ownership | Response target |
|------|-----------|----------------|
| 🔴 **Hardware issues** — node down, connectivity failure, software crash, storage mount lost | **SRF owns** | Within 1 hour |
| 🔵 **Pipeline issues** — bad scene file, render settings errors, job queue config | **Client-owned, SRF assists** | Best effort guidance |
| ⚡ **Escalation path** | RE → Solutions Lead → Director | Node down 3+ hours = escalate + consider SLA credit |

---

### LucidLink & Suite Studios

**LucidLink** — Client mounts their existing filespace onto SRF's Windows GPU nodes — no re-uploading large asset libraries. Render Engineer handles the mount configuration. Reference the SRF LucidLink article for setup steps.

**Suite Studios** — A preconfigured studio environment on SRF nodes for broadcast/event production (e.g. Adcetera). SRF keeps this environment ready between sessions for clients on a Yearly Capacity Lock. Emphasize this in long-term account conversations.

---

### Wrap-up & Renewal

At **D+3** (3 days after end date), Solutions Lead sends a wrap-up message covering: how the render period went, any unresolved issues, and next project timeline. This is the natural moment to introduce the Yearly Capacity & Price Lock.

> **Yearly Capacity & Price Lock pitch:** *"Since you run 5–6 shows a year, we can lock in fixed rates + guaranteed node access for all of them. You don't pay all at once — but agreeing to use SRF for your full slate gets you a dedicated discounted rate."*

---

## 6. Case Study: Adcetera #33493

> Drawn from the actual support chat transcript. Study both the mistakes — they are the source of the new procedures — and the wins, which show what good looks like.

### Final Result

| Machines secured | Period | Deal value |
|:---:|:---:|:---:|
| 18x RTX 5090 | 3 weeks | $25,500 |

Dates: May 23 – June 13 · Vendor setup: May 12 · Full render production: May 29

---

### ❌ What Went Wrong

#### Mistake 1 — Rough estimate without a caveat → 80% price surprise

> **SRF:** *"The $10k was my rough estimate for standard priority access, not a locked-in quote for a dedicated 14-day pool of 5090s."*
>
> **Thomas King:** *"An 80% increase on 'rough pricing' doesn't exactly instill confidence… I'm feeling like the partnership isn't going to be there."*

**New rule:** Every rough estimate must include: *"This is based on standard rates — formal quote follows after I confirm dedicated availability."* Without that caveat, the client hears a price, not a placeholder.

---

#### Mistake 2 — Scope mismatch not caught in discovery

> **Thomas King:** *"It's less cards than we asked for and is quoted for 2 weeks instead of 4 as requested."*

**New rule:** Discovery must lock in node count AND duration before any number is shared. A change in either changes the price significantly.

---

### ✅ What Went Well

#### Win 1 — Acknowledged the gap without deflecting

> **SRF:** *"Yes, that's on me. My initial estimate was based on our standard node/hour rates, and I clearly didn't account for the dedicated reservation premium for the 5090s."*

**Lesson:** Owning a mistake directly is more trust-building than explaining it away. The client had already said the partnership felt shaky — a clear acknowledgment shifted the tone and kept the deal alive.

---

#### Win 2 — Yearly Capacity Lock offered at exactly the right moment

> **Thomas King:** *"We also do 5–6 of these shows a year. We currently use Rebus in Germany but were hoping for a better solution."*
>
> **SRF:** *"Since you have 5–6 shows a year, let's look at a Yearly Capacity & Price Lock after we wrap this first run. Fixed Rates, Guaranteed Access, and we'll keep your Suite Studios environment ready."*

**Lesson:** Tie the Yearly Lock pitch directly to the client's stated problem (pricing surprise, capacity anxiety). This converts a one-off deal into a recurring account.

---

#### Win 3 — Escalated to Director before promising a lower rate

> **SRF:** *"I've gone back to my director. To guarantee the 18 nodes and maintain a 24/7 dedicated environment, we've hit our floor: 2 week: $17k / 4 week: $34k."*

**Lesson:** Never promise a lower price without Director sign-off. Presenting a "floor" is credible — it signals there's a real limit, which actually closes deals faster than open-ended negotiation.

---

> **Next step:** Approach Adcetera for Yearly Capacity Lock renewal before their late-July event.
