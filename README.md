# 🌐 IoT Lab Inventory Management System

[![Vite](https://img.shields.io/badge/Vite-6.0-646CFF?logo=vite&logoColor=white)](https://vitejs.dev/)
[![React](https://img.shields.io/badge/React-18-61DAFB?logo=react&logoColor=black)](https://react.dev/)
[![Supabase](https://img.shields.io/badge/Supabase-Database-3ECF8E?logo=supabase&logoColor=white)](https://supabase.com/)
[![CI Pipeline](https://img.shields.io/badge/CI-GitHub_Actions-2088FF?logo=githubactions&logoColor=white)](.github/workflows/ci.yml)
[![Version](https://img.shields.io/badge/Release-v1.0.0-success)](https://github.com/lakshayverma2610)

An enterprise-grade laboratory inventory management platform engineered for engineering colleges, maker spaces, and IoT development centers. Designed to track microcontrollers, sensor kits, test equipment, and student requests with real-time stock synchronization, role-based authentication, and automated audit trails.

---

## 👥 Collaborative Engineering Team

This project was built collaboratively by a dedicated team of four engineers, with each member owning a major domain of the system architecture:

| Contributor | GitHub Profile | Role & Responsibilities | Key Deliverables |
| :--- | :--- | :--- | :--- |
| **Lakshay Verma** | [@lakshayverma2610](https://github.com/lakshayverma2610) | **Lead Architect & Core Engineering** | Project scaffolding, authentication context, security utilities, and system architecture. |
| **Keshav** | [@Keshav01-ai](https://github.com/Keshav01-ai) | **Backend & Administration Lead** | Supabase integration, inventory data models, teacher admin dashboard, and approval workflow. |
| **Sparsh** | [@gigoosparsh](https://github.com/gigoosparsh) | **Frontend & Student Experience Lead** | Student portal, request tracking system, real-time catalog search, and interactive component modals. |
| **Mayank Bisht** | [@mayank-bisht1](https://github.com/mayank-bisht1) | **UI/UX & Quality Systems Engineer** | Modern design system, 3D card components, GitHub Actions CI pipeline, and automated Git hooks. |

---

## 🚀 Key Features

- **🔐 Dual Role-Based Portals**:
  - **Teacher / Admin Portal**: Complete inventory CRUD operations, quick quantity adjustments, pending request approval/rejection, and issued item audits.
  - **Student Portal**: Interactive visual item catalog, category filtering, live availability status, and one-click component requisition.
- **⚡ Real-Time Search & Filtering**: Instant debounce-powered search across component names, categories, specifications, and storage locations.
- **🛡️ Enterprise Security**: Role-based access control (RBAC), sanitized user input, and protected administrative routes.
- **🔄 Version Control & Git Hooks**:
  - pre-commit: Automatically scans staged files and rejects forbidden markers (TODO, FIXME).
  - commit-msg: Enforces strict Conventional Commit specifications (eat:, ix:, docs:, chore:, etc.).
- **⚙️ Automated CI/CD**: GitHub Actions workflow running automated lint checks (oxlint) and production builds on every push and pull request.

---

## 🛠️ Technology Stack

- **Frontend Core**: React 18, Vite, React Router DOM
- **UI & Styling**: Modern Glassmorphic CSS, 3D Card tilt effects, responsive layout
- **Database & Auth**: Supabase Cloud PostgreSQL, Local Storage Fallback, Mock Service
- **Quality & Automation**: Oxlint, Custom Git Hooks (POSIX shell), GitHub Actions CI
- **Deployment**: Vercel Cloud Hosting

---

## 📂 Project Structure

`	ext
IOT-INVENTORY-MANAGEMENT/
├── .github/
│   └── workflows/
│       └── ci.yml               # Automated CI test and build workflow
├── .githooks/
│   ├── commit-msg               # Enforces Conventional Commits
│   └── pre-commit               # Blocks commits with TODO/FIXME markers
├── public/                      # Static assets and SVG icons
├── scripts/
│   ├── importStudents.js        # Student roster batch ingestion script
│   └── generate_docx_report.py  # Automated report generator
├── src/
│   ├── assets/                  # Graphics and brand assets
│   ├── components/
│   │   ├── layout/              # Header, Sidebar, and Layout Shell
│   │   ├── student/             # ItemCatalog, MyRequests, StudentDashboard
│   │   ├── teacher/             # InventoryManager, IssuedItems, RequestsPanel
│   │   └── ui/                  # Badge, Card3D, Modal, StatCard
│   ├── context/
│   │   ├── AuthContext.jsx      # Authentication & User State
│   │   └── InventoryContext.jsx # Stock state & inventory mutations
│   ├── data/
│   │   └── mockData.js          # Hardware seed catalogue
│   ├── lib/
│   │   └── supabase.js          # Supabase client configuration
│   ├── pages/                   # Login, StudentApp, TeacherApp
│   └── utils/
│       └── security.js          # Input sanitation and audit helpers
├── package.json
└── vite.config.js
`

---

## 💻 Local Setup & Development

1. **Clone the repository**:
   `ash
   git clone https://github.com/lakshayverma2610/IOT-INVENTORY-MANAGEMENT.git
   cd IOT-INVENTORY-MANAGEMENT
   `

2. **Install dependencies**:
   `ash
   npm install
   `

3. **Configure Environment Variables**:
   `ash
   cp .env.example .env
   # Add your Supabase credentials (optional for mock mode)
   `

4. **Activate Client Git Hooks**:
   `ash
   git config core.hooksPath .githooks
   `

5. **Start Development Server**:
   `ash
   npm run dev
   `

---

## 📜 Version Control Standards

We adhere to the [Conventional Commits](https://www.conventionalcommits.org/) specification:
- eat: A new feature for the user
- ix: A bug fix
- docs: Documentation updates only
- efactor: Code restructuring without functional changes
- chore: Maintenance, dependency updates, and build tooling
- ci: Continuous integration pipeline updates

---

## 📄 License & Attribution

Academic project developed for the **Version Control Systems (CSE25303)** curriculum at **IILM University**. 
Released under the MIT License.
