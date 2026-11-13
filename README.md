# SahayakSHG

**A voice-first AI assistant that helps Self-Help Groups price, deliver and pay fairly.**

Tech4Bharat: GAVS Hackathon 2026 | Theme: Youth and Women | Problem Statement 8.1
*Women's self-help groups lose orders and members' trust because fulfilment and pay are chaotic.*

> **Status: design-stage concept.** No prototype has been built yet. The evidence in this repository comes from public sources (desk research). Field interviews with SHGs are planned.

> **License: all rights reserved. Not open source. Contributions are not accepted.** See [LICENSE](LICENSE) and [CONTRIBUTING.md](CONTRIBUTING.md).

## The problem

When a self-help group (SHG) wins a bulk order for garments, food or crafts, the leader must split work across 10 to 15 members who mostly work from home, hold quality, consolidate output and share payment. Today this runs on verbal instructions, a notebook and estimates. The problem statement reports that groups often underprice by 30 to 40 percent because material, labour and margin are never calculated, and that many members have low literacy.

Public reports on large government uniform orders show the stakes: thin per-piece rates and, in some states, delays and quality gaps. See `research/references.md`.

## The idea

SahayakSHG walks a group leader through the life of one order in six steps:

1. **Order intake** by voice in a regional language
2. **Pricing** with a margin, computed from material, labour and overhead
3. **Fair work split** with reasons the group can see
4. **Progress and quality tracking**, with early sample checks
5. **Deadline-risk alerts** and redistribution suggestions
6. **Payout** with a reconciliation check, approved by the group

Every member can hear her own record read aloud. The group approves the work split and every payout. No agent can lock a record or release a payout on its own.

## How it is designed

- Five cooperating agents: Intake, Pricing, Allocation, Tracking and Quality, Payout
- All money arithmetic runs in plain deterministic code; the language model only understands speech, asks follow-up questions and explains results
- An append-only ledger records every change
- Voice and icon-led screens, audio playback, leader-assisted use, offline queue
- Planned stack: mobile-first web app, FastAPI, SQLite/Postgres, Bhashini for speech, Lyzr for orchestration

Details: `architecture/README.md`

## Where it fits

LokOS and SHE-LEAPS (DAY-NRLM) digitise SHG records and monitor enterprises. We found no public description of per-order pricing, member-level allocation and group-approved payouts, so SahayakSHG is designed as a complementary order-to-payout layer.

## Milestones

- [x] Problem selection and desk research
- [x] Full project document (`docs/`)
- [ ] Idea submission, due 15 Nov 2026
- [ ] Shortlist announcement, 23 Nov 2026
- [ ] Prototype round, 23 Nov to 15 Dec 2026 (if shortlisted): thin end-to-end slice on synthetic data
- [ ] Online session with shortlisted teams, 24 Dec 2026
- [ ] Grand finale and pitch, 27 Dec 2026, Bangalore Palace
- [ ] After the hackathon: pilot with about 10 groups through one federation

## Planned prototype scope 

Order intake in one regional language, pricing, allocation, a payout matrix with the reconciliation check, an audio statement for one member, a group-approval screen and a ledger view, all on synthetic data.

## Repository structure

| Folder | What it holds |
|---|---|
| `architecture/` | System design, agent specs, data model, diagrams |
| `assets/` | Logo, images and other media |
| `data/` | Synthetic sample data and schemas only (no real personal data) |
| `docs/` | The full project document (PDF) |
| `presentation/` | Pitch deck |
| `research/` | References and notes; wireframes and mock diagrams in `research/wireframes/` |
| `submission/` | Text submitted to the hackathon form |
| `team/` | Team members and roles |

## Team

Kumuda, Komal, Sony, Priya. See `team/README.md`.
