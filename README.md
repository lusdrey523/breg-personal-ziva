# BREG Personal — Ziva Intelligence Data Engine (v0)

## Overview

BREG Personal is a Progressive Web App (PWA) designed to capture and structure financial behavior data from informal economic users.

This system is not a traditional finance app.

It is a **data engine** built to generate longitudinal behavioral datasets that power the Ziva Intelligence scoring system.

---

## Purpose

The primary goal of BREG Personal is to:

- Capture real-world financial activity
- Enforce disciplined economic behavior
- Generate structured, auditable datasets
- Serve as the foundation for alternative credit scoring

---

## Core Architecture

The system implements a hybrid architecture:

### 1. Event Store (Immutable)
All user actions are stored as append-only events.

### 2. Snapshot Engine
Daily computed states derived from events.

### 3. Feature Engine
Behavioral features extracted from historical activity.

### 4. Scoring Engine
Computes user score based on consistency, stability, and behavior.

### 5. Trust Engine
Evaluates data reliability and manipulation risk.

### 6. Anomaly Detection
Flags suspicious patterns and inconsistencies.

### 7. Behavior Engine
Applies reinforcement loops (rewards, penalties, streaks).

### 8. Decision Engine
Simulates credit eligibility decisions.

---

## Key Concepts

### Valid Day
A valid financial day requires:
- Income > 0
- At least one expense
- Defined working hours

### Behavior Loop
INPUT → PROCESS → FEEDBACK → ACTION

### Data Integrity
- Immutable records
- Full traceability
- Versioned calculations

---

## Data Model

- Event Store → `breg_events_v1`
- Snapshots → `breg_snapshots_v1`
- Features → `breg_features_v1`
- Audit Logs → `breg_audit_v1`

All stored in localStorage (offline-first).

---

## Scoring System (v0)

Score is computed using:

- Consistency (30%)
- Stability (25%)
- Frequency (15%)
- Income Quality (20%)
- Anomalies (10%)

---

## Behavioral System

- Daily rewards for valid activity
- Progressive penalties for inactivity
- Streak tracking
- Level system (Bronze → Diamond Black)
- Recovery challenges after sanctions

---

## Security

- Local-only data storage
- No external network calls
- CSP enforced
- PIN-based access control

---

## Roadmap

### v0.x
- Data collection
- Behavioral modeling
- Score calibration

### v1
- Ziva Intelligence integration
- Real credit decisioning

### v2+
- ZivaPay / ZivaOS integration
- Automated data ingestion

---

## Strategic Position

BREG Personal is not competing with finance apps.

It is building a **financial behavior dataset layer** for:
- Alternative credit scoring
- Informal economy intelligence
- Risk modeling infrastructure

---

## Status

Active development — experimental data engine.

Not production-ready for financial decisions.

---

## Author

Ziva Latam / Breto’s Holding Group
