# Architecture

Draft design for SahayakSHG. Nothing here has been implemented yet.

## Overview

Input (voice, tap, photo) -> Intake -> Pricing -> Allocation -> Tracking -> Payout.
Pricing and payout arithmetic run in a plain-code layer. Every change is written to an append-only ledger. Each member can hear her own record, and the group approves the work split and payouts.

Save the architecture diagram here as `architecture-diagram.png` (export it from the project document).

## Agents

| Agent | Input | Output | Language model used for | Plain code used for |
|---|---|---|---|---|
| Intake | Voice or text in a regional language | Structured order | Understanding speech, follow-up questions | Validating numbers and dates |
| Pricing | Order, material, labour hours, overhead, margin | Unit price and total with explanation | Asking for missing inputs, explaining | Cost and margin calculation |
| Allocation | Order, members' capacity, skill, recent workload | Quantity per member with reasons | Explaining the split | Weighted split, largest-remainder rounding |
| Tracking and quality | Output entries, early sample photos | Progress vs deadline, risk alerts | Reading voice updates, summarising risk | Totals, projection, accepted/rejected counts |
| Payout | Accepted pieces, approved piece rate | Payout matrix, ledger entries, audio statement | Writing the spoken statement | Payout arithmetic, reconciliation |

## Calculations (illustrative numbers)

- Cost per piece = material + labour hours x rate + overhead
- Price = cost x (1 + target margin)
- Member weight = capacity x skill factor x fairness factor; shares use largest-remainder rounding
- Payout = accepted pieces x piece rate; reconciliation: member payouts + group fund + material cost = buyer payment

## Data model

Group, Member, Order, PriceQuote, Task, OutputEntry, Payout, LedgerEntry (append only). See the project document, section B6.

## Stack (planned)

Mobile-first web app (React or Next.js), FastAPI, SQLite for prototype and Postgres for a demo, Bhashini for speech, Lyzr for orchestration, local offline queue.
