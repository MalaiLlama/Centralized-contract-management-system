# Centralized-contract-management-system
Contracts signed by vendors which can be accessed from a centralized platform for Regional managers and Sales Controllers to access along with generating insights for senior leadership
# ContractHub — Contract Management System MVP

Contracts signed by vendors which can be accessed from a centralised platform for Regional Managers and Sales Controllers to access, along with generating insights for senior leadership.

---

## Overview

ContractHub was built to streamline the end-to-end contract lifecycle, from initial creation through to customer e-signature, automated plan generation, and CRM synchronisation. It replaces fragmented, manual processes with a single interface where each role has clearly defined visibility and actions.

The application runs entirely in the browser as a single HTML file with no dependencies, no build step, and no server required.

---

## User Roles

**Key Account Manager (KAM)**
Creates and submits contracts for review. Can attach contract documents via drag-and-drop. Tracks contract status from draft through to active.

**Regional Sales Manager (RSM)**
Reviews contracts submitted by KAMs. Can approve, deny, or request changes. Approved contracts are forwarded to the customer for e-signature.

**Sales Controller (SC)**
Reviews and approves customer plans that are auto-generated once a contract is signed. Approves plan synchronisation to CRM and connected systems.

---

## Features

**Contract Creation**
- Multi-step form with fields for customer details, contract value, dates, rebate terms, volume targets, and counterpart requirements
- Choice of contract templates: Framework Agreement, Rebate Agreement, Distribution Contract, Service Level Agreement
- Inline notes and special conditions field

**Drag-and-Drop File Upload**
- Drop a contract file anywhere on the browser window to trigger the upload flow
- Dedicated upload tab in the new contract modal with a large drop zone
- Optional file attachment in the form flow at the review-and-submit step
- Supports PDF, DOCX, DOC, XLSX formats
- Simulated upload progress bar
- Attached files are visible in the contract detail view

**Approval Workflow**
- Contracts move through statuses: Draft, Under Review, Approved, E-Sign, Active, Denied
- RSMs can approve, deny, or request changes directly from the review queue or contract detail panel
- Status changes trigger in-app notifications and activity log entries

**E-Signature Tracking**
- Approved contracts are queued for customer e-signature
- KAMs can mark contracts as signed, which triggers automated customer plan creation

**RPA-Simulated Customer Plans**
- Signing a contract automatically generates a customer plan entry, simulating an RPA integration with a planning system
- Plans include rebate percentage, annual volume target, and CRM sync status

**Sales Controller Plan Approval**
- SC reviews auto-generated plans and approves them for CRM synchronisation
- Approved plans reflect as synced across CRM, dashboards, and connected tools

**Profitability Overview**
- Per-customer breakdown of contract value, rebates issued, net revenue, and gross margin
- Visual margin bars for at-a-glance profitability assessment

**Dashboard**
- Live counters for total contracts, pending reviews, and active contracts
- Recent activity timeline
- Contract status breakdown with proportional bars

**Filtering and Search**
- Search across all contracts by customer name or contract ID
- Filter by status and region

---

## Tech Stack

| Layer | Technology |
|---|---|
| Runtime | Browser (no server required) |
| Markup | HTML5 |
| Styling | CSS3 with custom properties |
| Logic | Vanilla JavaScript (ES6+) |
| Fonts | DM Serif Display, DM Sans (Google Fonts) |
| State | In-memory JavaScript objects |
| File handling | File API, DataTransfer API |

No frameworks, no build tools, no package manager. The entire application is a single `.html` file.

---

## Getting Started

1. Download `contract-management-mvp.html`
2. Open it in any modern browser (Chrome, Firefox, Edge, Safari)
3. Use the role switcher in the bottom-left sidebar to switch between KAM, RSM, and Sales Controller views

No installation, no dependencies, no internet connection required after the page loads.

---

## Project Status

This is an MVP built to validate the to-be process flow for a cost profitability and contract management system. It is intended for internal demonstration and feedback gathering, not production use. Data is held in memory and resets on page reload.
