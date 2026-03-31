# Onecredit Fullstack - Complete Project and Pages Documentation

This branch is documentation-only and intentionally contains only this README file.

## Branch Purpose

- Branch name: `docs/pages-documentation`
- Goal: provide a single, complete reference for product pages, workflows, architecture, and setup
- Scope: frontend advisor hub experience, integrations, data behavior, and operational notes

## Project Overview

Onecredit Fullstack (FieldDesk Advisor Hub implementation) is an advisor-first agricultural decision platform designed for:
- FPO officers
- Extension agronomists
- Field advisors

The product focuses on turning fragmented field operations into a structured workflow:
1. Identify high-priority farmers quickly
2. Interpret soil data into practical recommendations
3. Share recommendations via WhatsApp-ready messaging
4. Track outcomes across farmer portfolios and villages

## Product Goals

- Improve advisor productivity for large farmer portfolios
- Reduce fertilizer inefficiency through optimized recommendations
- Improve action completion via trusted advisor communication
- Provide measurable pilot outcomes through dashboard metrics

## Core Modules and Pages

### 1. Intro and Story Flow (`/`)
Purpose:
- Onboarding storytelling for the product
- Team visibility and mission context
- Real-world scenario examples

Key behavior:
- Intro flow displays on every fresh app load
- Team members appear with individual animations
- Scenario block rotates automatically and can be manually selected
- Buttons guide users into core modules

### 2. FPO Command Center (`/portfolio`)
Purpose:
- Daily operations cockpit for field advisors

Key sections:
- Priority queue of farmers by urgency
- KPI cards for managed farmers, urgent cases, adoption, savings
- Village health visuals
- Weather-aware irrigation advisory panel
- WhatsApp dispatch actions

### 3. Portfolio Live (`/portfolio-live`)
Purpose:
- Searchable, filterable list of managed farmers

Key sections:
- Status filters: all, green, yellow, red
- Search by name, village, crop
- Add farmer profile form
- Quick status updates and profile navigation

### 4. Farmer 360 (`/farmer/:id`)
Purpose:
- Full farmer intelligence and action workspace

Key sections:
- Profile summary, cluster context, risk status
- Crop-stage guidance and recommended next action
- Soil history timeline
- Recommendation timeline with status flags
- Quick actions (call, copy, reminder, edit, soil test)

### 5. Soil Intelligence (`/farmer/:id/soil`)
Purpose:
- Convert soil data into recommendation outputs

Key sections:
- Soil input fields (N, P, K, pH, EC, organic matter)
- Recommendation generation and cost comparison
- Expected yield range
- WhatsApp message preview and copy flow

### 6. Advisor Intelligence (`/insights`)
Purpose:
- Portfolio-level outcomes and pilot evidence

Key sections:
- Aggregated performance metrics
- Village-level breakdowns
- Export capability for reports (CSV)
- POC outcome snapshot cards

## Navigation and Routing Summary

- `/` -> Intro and onboarding flow
- `/portfolio` -> Command Center
- `/portfolio-live` -> Portfolio table/list operations
- `/insights` -> Analytics and outcome layer
- `/farmer/:id` -> Farmer 360 profile
- `/farmer/:id/soil` -> Soil and recommendation flow

## Data Strategy

The app supports two global data modes:
- `Demo Data` mode:
  - Uses local mock datasets
  - Enables complete UI flows without backend
- `Live Data` mode:
  - Uses backend API endpoints
  - Requires API service availability

### Mock Coverage

Demo mode includes structured seed data for:
- Farmers
- Soil history
- Recommendation timelines
- Village distribution and status segmentation

## API Surface (Live Mode)

The frontend client integrates with endpoints for:
- Auth
- Farmer CRUD and status updates
- Priority farmer retrieval
- Soil test creation and history retrieval
- Recommendation generation and lifecycle actions
- Advisor-level statistics

Base URL expected by frontend:
- `VITE_API_URL` (default pattern: `http://localhost:8000/api/v1`)

## UI and Experience Highlights

- Creative, advisor-centric interface design
- Animated onboarding and scenario storytelling
- Risk-first workflow emphasis
- Data-rich cards and chart-driven summaries
- Mobile-friendly responsive layout

## Technology Stack

Frontend:
- React + TypeScript + Vite
- Tailwind CSS + component primitives
- Framer Motion for animation
- Recharts for visualization
- React Query and Axios for data handling

Supporting:
- ESLint and TypeScript checks
- Vitest and Playwright configuration present

## Local Development (Reference)

Typical workflow:
1. Install dependencies
2. Configure environment variables
3. Start development server
4. Switch between demo/live modes in header

Core commands:
- `npm install`
- `npm run dev`
- `npm run build`
- `npm run test`

## Environment Variables

Expected frontend env entries:
- `VITE_API_URL`
- `VITE_APP_NAME`
- `VITE_APP_DESCRIPTION`

## Known Operational Notes

- Live mode requires backend service health
- If backend is unavailable, use Demo mode for complete experience coverage
- Weather panel relies on Open-Meteo fetch and falls back gracefully when unavailable

## Current Documentation Branch Constraint

This branch intentionally includes only one file:
- `README.md`

No application source files are included here by design.