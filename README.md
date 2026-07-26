# HarvestTrust - Transparent Farmer Collection Ledger

An automated produce collection register and payment tracking system built for farmer producer organizations.

---

## 1. Candidate & Assessment Profile

- **Assessment:** SIH 2026 - Internal Practical Assessment
- **Student Name:** `JANARTHANAN V`
- **Register Number:** `411723205021`
- **Department & Year:** Information Technology, Year IV, PSVPEC
- **PS/Track Level:** Easy (suggested duration: 2 days, marks: 70)

---

## 2. Technology Stack & Packages

### Frontend Web Client (`apps/web`)
- **Core:** React 19, TypeScript, Vite
- **Styling:** Tailwind CSS v4, Lucide Icons
- **Visualization:** Recharts (Intake share, 7-day trends)
- **Router:** React Router DOM

### API Backend Server (`apps/api`)
- **Core:** Express, Node.js, TypeScript
- **ORM:** Prisma Client
- **Database:** SQLite
- **Validation:** Zod schemas
- **Auth:** JWT and password hashing using bcryptjs

### Machine Learning Engine (`ml`)
- **Language:** Python 3 (venv)
- **Frameworks:** Scikit-learn (RandomForestClassifier), Pandas, Joblib

---

## 3. Project Directory Structure

```text
SIH_Project/
├── apps/
│   ├── api/                   # Express API TypeScript codebase
│   │   ├── prisma/            # SQLite schema and seed scripts
│   │   └── src/               # Controllers, routes, validators, tests
│   └── web/                   # Vite React SPA client codebase
│       └── src/               # Pages, layout wrappers, theme styling
├── docs/                      # Technical reports and documentation
│   ├── architecture.md        # Request diagrams & sequence maps
│   ├── er-diagram.md          # Mermaid entity relations
│   ├── model-card.md          # ML RandomForest accuracy & metrics
│   ├── calculation-verification.md  # 125.50 * 32.40 math proof
│   ├── database-constraint-tests.md # SQLite unique error logs
│   ├── test-report.md         # Automated backend test logs
│   └── demo-script.md         # 3-minute video recording narration
├── ml/                        # ML classifier pipeline scripts
│   └── venv/                  # Python virtual environment interpreter
├── scripts/                   # Slide presentation generators
├── presentation.pdf           # 8-slide PDF deck
└── package.json               # Monorepo workspaces coordinator
```

---

## 4. Quick Start Setup Guide

Follow these steps to run the complete HarvestTrust application locally.

### Step 4.1: Install Dependencies
Run from the root directory to bootstrap both frontend and backend workspaces:
```bash
npm install
```

### Step 4.2: Database Migrations & Seeding
Prepare the SQLite database schema and load seed datasets:
```bash
npm run db:setup
```
This runs the Prisma migrations, client generation, and executes the deterministic seeder.

### Step 4.3: ML Pipeline Training
Initialize virtual environment and train the RandomForest model:
```bash
cd ml
python3 -m venv venv
./venv/bin/pip install -r requirements.txt
./venv/bin/python3 generate_demo_history.py
./venv/bin/python3 train.py
cd ..
```

### Step 4.4: Run Servers
Start the backend server on port 4000 and Vite client on port 5173:
```bash
npm run dev
```

---

## 5. Verification Documents

- **Math Calculations Proof:** [calculation-verification.md](file:///Users/sakithyavishwanathan/Documents/SIH_Project/docs/calculation-verification.md)
- **SQLite Constraint Violations:** [database-constraint-tests.md](file:///Users/sakithyavishwanathan/Documents/SIH_Project/docs/database-constraint-tests.md)
- **System Architecture:** [architecture.md](file:///Users/sakithyavishwanathan/Documents/SIH_Project/docs/architecture.md)
- **Database ER Design:** [er-diagram.md](file:///Users/sakithyavishwanathan/Documents/SIH_Project/docs/er-diagram.md)
- **ML Model Metrics Card:** [model-card.md](file:///Users/sakithyavishwanathan/Documents/SIH_Project/docs/model-card.md)
- **Full Test Outcomes:** [test-report.md](file:///Users/sakithyavishwanathan/Documents/SIH_Project/docs/test-report.md)
- **Presentation Slide Deck:** [presentation.pdf](file:///Users/sakithyavishwanathan/Documents/SIH_Project/presentation.pdf)
