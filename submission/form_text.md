# Form text: Tech4Bharat (HackCulture)

Copy each section into the matching form field. Fields marked * are required.

---

## Project Title *

SahayakSHG: A Voice-First AI Assistant That Helps Self-Help Groups Price, Deliver and Pay Fairly

---

## Brief about your idea *

SahayakSHG is a voice-first, multi-agent AI assistant for Self-Help Group (SHG) leaders. The leader speaks in her own language, and the system turns a buyer's bulk order into a fair price, a fair split of work, a tracked delivery and a transparent payout. Every member can hear her own record read aloud, and the group approves every work split and every payout. Over time each group builds a delivery-reliability record that buyers can trust, which turns an informal group into a supplier worth seeking out.

---

## Detailed explanation of the idea *

**The problem.** When a self-help group wins a bulk order for garments, food or crafts, the leader must split the work across 10 to 15 members who mostly work from home, hold quality, consolidate the output and share the payment. Today this runs on verbal instructions, a notebook and estimates. The problem statement notes that groups often underprice by 30 to 40 percent because material, labour and margin are never calculated. Public reports on large government uniform orders show what is at stake: groups are paid thin per-piece rates, and in some states delays and quality gaps put the arrangement under question. A Tamil Nadu study of 288 SHG members found marketing to be the top constraint, with internal conflicts and members leaving also reported.

**Our solution.** SahayakSHG walks a group leader through the life of one order in six steps: (1) order intake by voice, (2) a price with a margin, (3) a fair work split, (4) progress and quality tracking, (5) early deadline-risk alerts with redistribution suggestions, and (6) a payout matrix. Each member can hear her own record read aloud. The group approves the work split and every payout before it becomes final.

**How it works.** Five cooperating agents (Intake, Pricing, Allocation, Tracking and Quality, Payout) are orchestrated on Lyzr, which supports manager-style and workflow-style multi-agent orchestration and custom tools. Voice input and audio playback use Indian-language speech services such as Bhashini. All pricing, allocation and payout arithmetic runs in deterministic code, and the language model is used only to understand speech, ask follow-up questions and explain results in simple language. Every action is written to an append-only ledger so disputes can be settled from a shared history.

**Built for low literacy and poor connectivity.** Research on interfaces for low-literate users supports graphics plus voice instead of text, and field work with rural women entrepreneurs shows that hand-holding and daybook-first habits help adoption. SahayakSHG therefore uses icon-led, voice-prompted screens in regional languages, leader-assisted use, audio playback of every member's own record, a mobile-first web app for low-cost phones, and an offline queue that syncs when the network returns.

**What exists today, and our gap.** LokOS digitises SHG registers, savings and loans for about 94 lakh SHGs, and SHE-LEAPS (launched 29 June 2026) tracks and monitors SHG enterprises. We found no public description of per-order pricing, member-level work allocation and group-approved payouts, so SahayakSHG is designed as a complementary operations layer that can sit alongside these platforms.

**Venture path.** SHG federations, state livelihood missions and NGOs pay a small per-group subscription. Buyers and marketplaces can later pay a commission for orders routed to groups with a proven reliability record. The rollout starts with about 10 groups under one federation, then scales through the federation structure, where an average cluster-level federation covers roughly 270 SHGs.

**Status and next steps.** SahayakSHG is at design stage. If shortlisted, the team will build a thin end-to-end prototype in the 23 November to 15 December window and validate it with real SHGs.

---

## Short version (use only if the form has a tight length limit)

SahayakSHG helps SHG leaders run a bulk order from start to finish by voice. Five agents handle intake, pricing, work allocation, progress and quality tracking, and payout. All money arithmetic runs in plain code, and every action goes into an append-only ledger. The group approves the work split and every payout, and each member can hear her own record. It addresses underpricing (30 to 40 percent per the problem statement), unfair work splits and distrust in the accounts, and it is built for low literacy and poor connectivity. LokOS and SHE-LEAPS digitise SHG records and monitor enterprises, and SahayakSHG adds the order-to-payout layer. Federations and missions pay per group, with buyer commissions later. The idea is at design stage, with a prototype planned if shortlisted.

---

## Presentation Deck (optional)

Upload a PDF or PPTX. Suggested 10 slides: problem with public evidence, who we build for, the six-step flow, architecture, trust and fairness, low-literacy design, what exists today and our gap, venture model and rollout, roadmap and validation plan, team.

---

## Additional supporting links (GitHub / research reference)

- GitHub repository: https://github.com/kumudasrip/SahayakSHG
- Project proposal (PDF): [add link]
- Research references: https://github.com/kumudasrip/SahayakSHG/tree/main/research