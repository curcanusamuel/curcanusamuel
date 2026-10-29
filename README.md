# Samuel-Adrian Curcanu

**Full-Stack Software Developer** · Healthcare & business systems · FileMaker ↔ web integrations · Cluj-Napoca, Romania

I build production software that replaces or extends legacy FileMaker systems with modern web and desktop apps, for clinics in Romania and for business clients in Germany. Most of my work sits where domain rules meet the database: clinical workflows, national health-insurance reporting, working-time law, billing.

B.Sc. in Computers and Information Science, Technical University of Cluj-Napoca (2025).

---

## 💼 Experience

### Software Developer — Integrated Data Solutions
*Oct 2024 – present · Cluj-Napoca*

- Lead frontend developer of **IDS Clinic**, a full-stack clinic management platform migrating a FileMaker system used in production by oncology clinics (see below).
- Develop features for **PROJEKT PRO** (Germany): the Angular time-tracking web app and the FileMaker solution behind it.
- Design FileMaker data models and scripts, and connect FileMaker to web services (Data API, Insert from URL, n8n, JavaScript).
- Integrate LLM agents into internal development and business workflows.

---

## 🚀 Main projects

### 🏥 IDS Clinic — clinic management platform
*React · TypeScript · Vite · Node.js · Express · PostgreSQL · AWS · Electron · Cloudflare Workers*

Replacement for a large FileMaker clinic system, covering the patient's whole path: registration, appointments, medical letters, evolution, oncology, **chemotherapy**, imaging, genetics, occupational medicine, wards, pricing, invoicing and administration. It runs in the browser, on phones, and as a desktop app.

- **Frontend (main contributor):** React + TypeScript SPA with 25+ feature modules, a shared design system on Untitled UI / react-aria, RO / EN / DE translations, and phone layouts for every page. Deployed on Cloudflare Workers and packaged with Electron for macOS and Windows.
- **Chemotherapy module:**
  - treatment sheets with line and cycle logic;
  - body-surface and dose calculations (Mosteller, Du Bois…, AUC);
  - premedication, postmedication, antiemetic and preparation protocols;
  - a dose-by-dose administration flow (validate → dissolve → print → administer) with a day-by-day administration board;
  - oral therapy sheets with interaction and compliance tracking.
  
  The rules were reverse-engineered from the clinic's FileMaker scripts.
- **Data integrity:** every save sends only the changed fields with a record version. Concurrent edits get a field-level conflict dialog, not a silent overwrite.
- **Security & audit:** fine-grained role permissions. Actions the user isn't allowed to take stay visible but disabled, with the reason shown. Every change goes to an audit log, with per-record history.
- **Backend (contributor):**
  - Express + TypeScript REST API with zod validation;
  - session auth in PostgreSQL, Helmet, rate limiting and structured logging (pino);
  - 50+ SQL migrations and keyset (cursor) pagination for large lists;
  - S3 presigned uploads for medical documents and AWS Secrets Manager for credentials.
- **Tooling:** Vitest and Playwright tests, ESLint, a Docker PostgreSQL setup for development, and an issue-driven workflow between the frontend and backend teams.

### ⏱️ PROJEKT PRO — web time tracking (Germany)
*Angular · NgRx · Angular Material · PWA · FileMaker*

Web time-tracking and project-accounting app for a German project-management product used by architecture and engineering firms, with FileMaker as its data platform.

- Develop new modules and features in the **Angular** app (NgRx state, Angular Material UI), from the interface down to the data exchange with FileMaker.
- Work on time recording, project costs and expenses, and the generated reports and PDFs.
- Implement business rules on both sides, in the web app and in FileMaker scripts, including German working-time regulations.
- Maintain the app: bug fixes, translations, and security and dependency updates.

### 📑 IDS SIUI Reporter — national health-insurance reporting
*Node.js · Express · TypeScript · React · Tailwind · XML / XSD*

Generates the monthly **CNAS / SIUI XML report** (Romanian national health insurance) for outpatient clinics from FileMaker data, replacing manual entry in the official reporting app.

- FileMaker pushes each visit to the API. The app validates and normalizes the data, builds a summary per doctor and day, and writes the XML file.
- A single TypeScript rule engine is shared by the server, the dynamic forms and the XML writer. The rules come from the official CNAS XSD, so a service that passes local validation is guaranteed to pass the national schema.
- Checked against a real monthly report of **2,788 services**: no errors, identical values, and the file passes the CNAS XSD.
- Maps the clinic's price-list operations to CNAS service codes, with suggestions ranked by rare words in their names.

### 🏗️ ArchiPlan — software for architecture practices
*React · TypeScript · Electron · Cloudflare*

Web and desktop app for architecture firms: projects, schedules and hours, clients, documents, a materials catalogue, and an in-browser **floor-plan editor**. Packaged for macOS and Windows.

### 🚗 ServiceAuto — car service management
*React · Vite · Tailwind · Supabase (Postgres, Auth, Edge Functions)*

Management app for a car service: clients, cars and insurance, stock, and print templates.

- **Access control in the database:** role-based permissions enforced with Row Level Security.
- **Admin-only operations:** user management runs through an Edge Function.
- **Audit and accounts:** who created or changed each record is tracked, and new accounts must change their temporary password.

### 🔍 DDR Lint — CI for FileMaker
*Node.js · GitHub Actions*

Automated validation of FileMaker DDR XML exports in GitHub Actions. Already-known issues are whitelisted, so a build fails only on new ones, and every run produces an HTML report.

---

## 🛠 Tech stack

| Area | Tools |
|---|---|
| **Languages** | TypeScript, JavaScript, SQL, Java, C, C++, Python |
| **Frontend** | React, Angular, NgRx, Vite, Tailwind CSS, react-aria / Untitled UI, Angular Material |
| **Backend** | Node.js, Express, zod, Spring, REST API design |
| **Data** | PostgreSQL (migrations, keyset pagination, RLS), Supabase, FileMaker (data modelling, scripting, Data API) |
| **Cloud & delivery** | AWS (RDS, S3, Secrets Manager), Cloudflare Workers, Electron, Docker, GitHub Actions |
| **Testing** | Vitest, Playwright, Node test runner |
| **Automation & AI** | n8n, LLM agents in development and business workflows |

---

## 🎓 Education

**Technical University of Cluj-Napoca** — B.Sc. Computers and Information Science (2021 – 2025)

---

## 📫 Contact

[Email](mailto:curcanusamuel@gmail.com) · [LinkedIn](https://linkedin.com/in/samuel-adrian-curcanu-b529b3261) · [GitHub](https://github.com/curcanusamuel)
