# PROJECT ABSTRACT

## IoT Lab Inventory Management System
### A Collaborative, Role-Based Hardware Asset Tracking & Laboratory Automation Platform

---

### Academic & Project Metadata
- **Institution**: IILM University, Gurugram — School of Computer Science & Engineering
- **Course**: Version Control System (CSE25303) · B.Tech (CSE) · Semester III (Batch 2025–2029)
- **Primary Repository**: [lakshayverma2610/IOT-INVENTORY-MANAGEMENT-SYSTEM](https://github.com/lakshayverma2610/IOT-INVENTORY-MANAGEMENT-SYSTEM)
- **Collaborative Engineering Team**:
  - **Lakshay Verma** (URN: 2581008 · `@lakshayverma2610`) — *System Architecture, Core Engine & Security*
  - **Keshav** (`@Keshav01-ai`) — *Backend Data Architecture, Supabase Client & Faculty Admin Portal*
  - **Sparsh Gigoo** (`@gigoosparsh`) — *Student Experience, Requisition Engine & Real-Time Catalog*
  - **Mayank Bisht** (`@mayank-bisht1`) — *UI/UX Design System, GitHub Actions CI/CD & Custom Git Hooks*

---

### 1. Executive Abstract
Modern engineering universities and maker spaces maintain complex hardware laboratories with hundreds of microcontrollers (ESP32, Arduino, Raspberry Pi), sensor breakout modules, and electronic consumables. Traditional asset tracking relying on paper registers or static spreadsheets frequently fails, resulting in inventory discrepancies, component misplacement, delayed experiment approvals, and lack of accountability. 

This project presents the **IoT Lab Inventory Management System**, a high-performance web platform engineered using React 18, Vite, and Supabase Cloud PostgreSQL. The system implements a dual-role access control model (Student and Instructor portals) that digitizes component requisition, real-time availability tracking, automated faculty approvals, and stock telemetry. The engineering lifecycle was conducted using collaborative Git/GitHub best practices, enforcing automated Conventional Commit validation via Git hooks and Continuous Integration (CI) pipelines.

---

### 2. Problem Statement & Objectives
1. **Inefficient Asset Visibility**: Students lack real-time visibility into component availability, causing lab delays.
2. **Manual Requisition Friction**: Paper-based approval slips cause administrative bottlenecks and lack return audits.
3. **Consumable vs. Asset Divergence**: Difficulty distinguishing permanent returnable hardware from consumable components (e.g., resistors, jumper cables, ICs).
4. **Engineering Objectives**: Deliver a sub-second search catalog, role-based security, automated overdue audits, and a scalable cloud-backed inventory ledger.

---

### 3. System Architecture & Key Modules

```text
┌─────────────────────────────────────────────────────────────┐
│                 PRESENTATION LAYER (REACT 18 + VITE)         │
│   Student Portal (Catalog & Requisitions)                   │
│   Faculty Admin Portal (Approvals & Stock Management)       │
└──────────────────────────────┬──────────────────────────────┘
                               │
┌──────────────────────────────▼──────────────────────────────┐
│                  BUSINESS LOGIC & STATE ENGINE              │
│   AuthContext (RBAC)         │  InventoryContext (Live Sync) │
│   Security Utilities         │  Batch Import Scripts        │
└──────────────────────────────┬──────────────────────────────┘
                               │
┌──────────────────────────────▼──────────────────────────────┐
│                 PERSISTENCE & AUTOMATION LAYER              │
│   Supabase Cloud PostgreSQL  │  Local Resilient Cache       │
│   GitHub Actions CI Pipeline │  Client-side Git Hooks       │
└─────────────────────────────────────────────────────────────┘
```

- **Student Requisition Portal**: Real-time debounced catalog search, category filtering, availability badges, and one-click item request submissions with automated due-date scheduling.
- **Faculty / Admin Controller**: Complete inventory CRUD, batch quantity updates, real-time pending request approvals/rejections, and issued hardware return audit trails.
- **Enterprise Security & Data Layer**: Role-based access control (RBAC), sanitized user input, and automated batch student roster ingestion scripts.

---

### 4. Version Control System (VCS) & DevOps Implementation
- **Conventional Commits**: Strict adherence to semantic prefixes (`feat:`, `fix:`, `docs:`, `chore:`, `ci:`).
- **Client-Side Git Hooks**:
  - `pre-commit`: Scans staged files and aborts commits containing forbidden markers (`TODO`, `FIXME`).
  - `commit-msg`: Enforces message syntax rules and issue references.
- **Continuous Integration (CI)**: Automated GitHub Actions pipeline running `oxlint` static code analysis and production bundle compilation on every push and pull request.
- **Semantic Versioning**: Lightweight milestone tags (`v0.1.0`) and signed production release tags (`v1.0.0`).

---

### 5. Results & Academic Impact
The deployed system was evaluated against real lab hardware records (50+ active component categories). Key verified outcomes include:
- **100% Paperless Requisition**: Replaced manual logbooks with instant digital approvals and automated return tracking.
- **Sub-100ms Search Response**: Instant filtering across component names, vendors, folio numbers, and bill references.
- **Zero-Error Collaborative Codebase**: Clean, multi-author Git history with 100% CI pass rates across all functional modules.

---
*© 2026 IILM University, Gurugram · School of Computer Science & Engineering*
