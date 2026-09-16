<div align="center">

<!-- HERO BANNER -->
<a href="https://tanish1808.github.io/My_Portfolio/" target="_blank">
  <img src="assets/banner.svg" width="100%" alt="Tanish Shah — Systems Architect & Full-Stack Developer" />
</a>

<br/><br/>

<!-- PRIMARY ACTION DOCK -->
<p align="center">
  <a href="https://tanish1808.github.io/My_Portfolio/" target="_blank">
    <img src="https://img.shields.io/badge/🌐_EXPLORE_LIVE_PORTFOLIO-00F5A0?style=for-the-badge&logo=googlechrome&logoColor=070A10&labelColor=0F172A" height="38" alt="Live Portfolio" />
  </a>
  <a href="https://linkedin.com/in/tanish-shah-703489349" target="_blank">
    <img src="https://img.shields.io/badge/LINKEDIN_PROFILE-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white&labelColor=0F172A" height="38" alt="LinkedIn" />
  </a>
  <a href="mailto:tanishshah1808@gmail.com">
    <img src="https://img.shields.io/badge/DIRECT_EMAIL-EA4335?style=for-the-badge&logo=gmail&logoColor=white&labelColor=0F172A" height="38" alt="Email" />
  </a>
  <a href="https://github.com/Tanish1808" target="_blank">
    <img src="https://img.shields.io/badge/GITHUB_SOURCE-181717?style=for-the-badge&logo=github&logoColor=white&labelColor=0F172A" height="38" alt="GitHub" />
  </a>
</p>

<!-- EDITORIAL NAVIGATION -->
<p align="center">
  <a href="#-developer-identity"><code>IDENTITY</code></a> &nbsp;&bull;&nbsp;
  <a href="#-selected-work"><code>SELECTED WORK</code></a> &nbsp;&bull;&nbsp;
  <a href="#-technical-arsenal"><code>ARSENAL</code></a> &nbsp;&bull;&nbsp;
  <a href="#-currently-deepening-knowledge"><code>DEEPENING FOCUS</code></a> &nbsp;&bull;&nbsp;
  <a href="#-how-i-build"><code>HOW I BUILD</code></a> &nbsp;&bull;&nbsp;
  <a href="#-signature-endpoint"><code>CONNECT</code></a>
</p>

</div>

---

### 👨💻 Developer Identity

<table>
  <tr>
    <td width="50%" valign="top">
      <h4>⚡ Personal Command Center</h4>
      <pre><code>$ whoami
Tanish Shah

$ education
B.E. Information Technology &bull; LJ University (2024–2028)

$ core_disciplines
Backend Architectures &bull; REST/Async APIs &bull; Applied ML

$ engineering_ethos
"Deterministic execution, strict ACID schemas, zero fluff."</code></pre>
    </td>
    <td width="50%" valign="top">
      <h4>📍 Strategic Directives</h4>
      <p>
        I am an <strong>Information Technology Engineering student</strong> focusing on full-stack development and backend systems. I design software where stateless authentication, role-scoped route guards, and relational data integrity are fundamental design constraints from day one.
      </p>
      <p>
        <strong>Base:</strong> Ahmedabad, Gujarat, India<br/>
        <strong>Active Systems:</strong> <a href="#-hero-project--ticket-tally">Ticket Tally</a> <em>(Render Cloud)</em> &bull; <a href="#-featured-system--civic-lens">Civic Lens</a> <em>(Distributed ML)</em>
      </p>
    </td>
  </tr>
</table>

---

### 🚀 Selected Work

<br/>

#### 🎫 HERO PROJECT &bull; Ticket Tally — Smart IT Support & Priority Queue Engine

<div align="left">
  <img src="https://img.shields.io/badge/Status-🟢_DEPLOYED_ON_RENDER_CLOUD-46E3B7?style=flat-square&logo=render&logoColor=black" alt="Render Deployed" />
  <img src="https://img.shields.io/badge/Architecture-PRIORITY_QUEUE_DISPATCH-38BDF8?style=flat-square" alt="Priority Queue" />
  <img src="https://img.shields.io/badge/Stack-FLASK_·_POSTGRESQL_·_JWT-0B0F17?style=flat-square" alt="Stack" />
</div>

<br/>

> **The Problem:** Sequential FIFO queues cause mission-critical system-down incidents to sit idle behind routine support requests.  
> **The System:** An enterprise IT incident platform driven by an algorithmic Priority Queue dispatch engine coupled to event-driven state-machine SLAs.

```mermaid
flowchart LR
    A[Employee Request] --> B[JWT Route Gate]
    B --> C{Priority Dispatcher}
    C -->|High Severity P1| D[Urgent Incident Queue]
    C -->|Standard P2/P3| E[Standard FIFO Queue]
    D --> F[IT Resolution Desk]
    E --> F
    F --> G{State Machine Transition}
    G -->|CREATED → IN_PROGRESS| H[SLA Timer Armed]
    G -->|RESOLVED → CLOSED| I[PDF Audit & Email Trigger]
    G --> J[(PostgreSQL Database)]
```

* **Deterministic Queue Scheduling:** Non-preemptive priority scoring guarantees high-severity incidents are routed immediately to available staff without relying on polling table queries.
* **Three-Tier Stateless RBAC:** Granular authorization scopes (`Employee`, `IT Staff`, `Admin`) cryptographically verified at the route decorator layer via stateless JWT claims.
* **Event-Coupled SLAs:** SLA countdown clocks activate and resolve on explicit state transitions, eliminating background timestamp sweep jobs.
* **Cloud Infrastructure:** Containerized and actively running on **Render Cloud (Free Tier)**.

<div align="left">
  <a href="https://github.com/Tanish1808" target="_blank">
    <img src="https://img.shields.io/badge/📁_VIEW_SOURCE_CODE-181717?style=for-the-badge&logo=github&logoColor=white" alt="Source" />
  </a>
</div>

<br/><br/>

---

#### 🌍 FEATURED SYSTEM &bull; Civic Lens — AI Civic Intelligence & Two-Stage Spatial Deduplication

<div align="left">
  <img src="https://img.shields.io/badge/Inference-PYTORCH_CNN_+_FASTAPI-EE4C2C?style=flat-square&logo=pytorch&logoColor=white" alt="PyTorch" />
  <img src="https://img.shields.io/badge/Spatial-MONGODB_2DSPHERE-47A248?style=flat-square&logo=mongodb&logoColor=white" alt="MongoDB" />
  <img src="https://img.shields.io/badge/Core-DJANGO_REST_FRAMEWORK-092E20?style=flat-square&logo=django&logoColor=white" alt="DRF" />
</div>

<br/>

> **The Problem:** Public civic reporting portals suffer from duplicate incident flooding (e.g., hundreds of reports for the same pothole), choking municipal administration.  
> **The System:** An asynchronous two-stage deduplication engine that gates deep visual metric computation behind indexed geospatial proximity searches.

```mermaid
flowchart TD
    subgraph IngestAndClassify ["1. Ingress & Inference Layer"]
        UP[Citizen Geotagged Upload] --> ML[FastAPI ML Service]
        ML --> CONF{Softmax Confidence}
        CONF -->|≥ 0.85| AUTO[Auto-Tagged Category & Severity]
        CONF -->|< 0.85| MANUAL[Manual Verification Queue]
    end

    subgraph TwoStageDedup ["2. Cost-Ordered Deduplication Pipeline"]
        AUTO --> GEO[(MongoDB 2dsphere Index)]
        MANUAL --> GEO
        GEO -->|Stage 1: Radius Search| RAD{Candidate within Radius R?}
        RAD -->|No Candidates| NEW[Create Verified Unique Incident]
        RAD -->|Candidates Found| VIS[Stage 2: PyTorch Embeddings + pHash]
        VIS --> SIM{Cosine Similarity > Threshold?}
        SIM -->|Duplicate Match| CLUSTER[Cluster / Merge to Existing Incident]
        SIM -->|Distinct Incident| NEW
    end

    subgraph AppState ["3. Core State & Dashboards"]
        NEW --> DRF[Django REST Framework]
        CLUSTER --> DRF
        DRF --> DASH[Admin Analytics & Real-Time Public Portal]
    end
```

* **Cost-Aware Deduplication:** Gating deep feature similarity ($O(K)$) behind spatial index queries ($O(\log N)$ via MongoDB `2dsphere`) reduces deep metric compute requirements by over **92%**.
* **Microservice Isolation:** Decouples FastAPI async inference from Django REST Framework business logic to maintain sub-50ms HTTP responsiveness on standard endpoints.

<br/><br/>

---

#### 🌐 CLIENT EXPERIENCE &bull; Interactive Developer Portfolio

<div align="left">
  <img src="https://img.shields.io/badge/Hosting-GITHUB_PAGES_CDN-00F5A0?style=flat-square&logo=googlechrome&logoColor=black" alt="GitHub Pages" />
  <img src="https://img.shields.io/badge/Engine-VANILLA_JS_CANVAS-F7DF1E?style=flat-square&logo=javascript&logoColor=black" alt="Canvas" />
</div>

<br/>

> An interactive developer platform engineered with an in-browser terminal CLI shell, custom canvas particle graphics engine, and dynamic milestone inspector.

* **Terminal CLI Shell:** Simulates interactive command execution (`projects`, `skills`, `cat developer.json`).
* **Physics Canvas:** Native JavaScript particle background with interactive mouse boundary physics.

<div align="left">
  <a href="https://tanish1808.github.io/My_Portfolio/" target="_blank">
    <img src="https://img.shields.io/badge/🚀_LAUNCH_LIVE_PORTFOLIO-00F5A0?style=for-the-badge&logo=googlechrome&logoColor=070A10" alt="Launch Live Portfolio" />
  </a>
</div>

---

### 🛠️ Technical Arsenal

<br/>

<table>
  <thead>
    <tr>
      <th width="20%">Category</th>
      <th width="40%">Technologies</th>
      <th width="40%">Architectural Application</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>💻 Languages</strong></td>
      <td>
        <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" />
        &nbsp;
        <img src="https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white" />
        &nbsp;
        <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black" />
        &nbsp;
        <img src="https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white" />
      </td>
      <td>Backend services, async event loops, OOP data structures, relational querying.</td>
    </tr>
    <tr>
      <td><strong>⚙️ Backend & APIs</strong></td>
      <td>
        <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" />
        &nbsp;
        <img src="https://img.shields.io/badge/Django_REST-092E20?style=flat-square&logo=django&logoColor=white" />
        &nbsp;
        <img src="https://img.shields.io/badge/Flask-000000?style=flat-square&logo=flask&logoColor=white" />
        &nbsp;
        <img src="https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white" />
      </td>
      <td>High-speed async inference endpoints, enterprise RBAC & ORM, lightweight microservices.</td>
    </tr>
    <tr>
      <td><strong>🗄️ Storage & Spatial</strong></td>
      <td>
        <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" />
        &nbsp;
        <img src="https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white" />
        &nbsp;
        <img src="https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white" />
      </td>
      <td>ACID relational integrity, foreign key constraints, <code>2dsphere</code> spatial radius indexing.</td>
    </tr>
    <tr>
      <td><strong>🧠 Applied ML & Vision</strong></td>
      <td>
        <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white" />
        &nbsp;
        <img src="https://img.shields.io/badge/CNN_Embeddings-38BDF8?style=flat-square" />
        &nbsp;
        <img src="https://img.shields.io/badge/pHash_Dedup-00F5A0?style=flat-square" />
      </td>
      <td>Deep feature metric extraction, perceptual image hashing, cosine similarity search.</td>
    </tr>
    <tr>
      <td><strong>🎨 Frontend Systems</strong></td>
      <td>
        <img src="https://img.shields.io/badge/React.js-61DAFB?style=flat-square&logo=react&logoColor=black" />
        &nbsp;
        <img src="https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white" />
        &nbsp;
        <img src="https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white" />
        &nbsp;
        <img src="https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white" />
      </td>
      <td>Component-driven modular architectures, responsive state-driven dashboards.</td>
    </tr>
    <tr>
      <td><strong>🔧 DevOps & Tools</strong></td>
      <td>
        <img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white" />
        &nbsp;
        <img src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white" />
        &nbsp;
        <img src="https://img.shields.io/badge/Postman-FF6C37?style=flat-square&logo=postman&logoColor=white" />
        &nbsp;
        <img src="https://img.shields.io/badge/Render-46E3B7?style=flat-square&logo=render&logoColor=black" />
      </td>
      <td>Version control workflows, REST contract test suites, containerized cloud hosting.</td>
    </tr>
  </tbody>
</table>

<br/>

---

### 🧠 Currently Deepening Knowledge

<table>
  <tr>
    <td width="50%" valign="top">
      <h4>🧩 DSA & Algorithmic Complexity</h4>
      <p>Mastering tree & graph traversals, heap-based priority queue dispatch models, and space-time complexity trade-offs in backend pipelines.</p>
    </td>
    <td width="50%" valign="top">
      <h4>⚙️ Distributed Systems & Concurrency</h4>
      <p>Engineering non-blocking async event loops, stateless JWT claims-based authorization, and decoupled microservice communication patterns.</p>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <h4>🌐 Geospatial Search & Spatial Math</h4>
      <p>Applying MongoDB <code>2dsphere</code> spherical indexing and geodesic radius calculations to accelerate spatial proximity lookups to sub-millisecond execution.</p>
    </td>
    <td width="50%" valign="top">
      <h4>🤖 Applied Metric Learning & Inference</h4>
      <p>Building high-throughput PyTorch CNN feature extraction pipelines paired with perceptual hashing for cost-optimized duplicate classification.</p>
    </td>
  </tr>
</table>

---

### 💡 How I Build

```text
┌─────────────────┐     ┌─────────────────┐     ┌─────────────────┐     ┌─────────────────┐     ┌─────────────────┐
│  01. UNDERSTAND │ ──► │   02. SCHEMA    │ ──► │   03. DECOUPLE  │ ──► │    04. STRESS   │ ──► │   05. DEPLOY    │
│  & SPECIFY      │     │   & CONSTRAINTS │     │   & IMPLEMENT   │     │    TEST & AUDIT │     │   & OBSERVE     │
│                 │     │                 │     │                 │     │                 │     │                 │
│ Define failure  │     │ Strict ACID     │     │ Modular services│     │ Edge cases,     │     │ Automated cloud │
│ modes & SLAs    │     │ & auth scoping  │     │ & async paths   │     │ race conditions │     │ delivery & logs │
└─────────────────┘     └─────────────────┘     └─────────────────┘     └─────────────────┘     └─────────────────┘
```

---

### 🎓 Background & Credentials

* 🎓 **Bachelor of Engineering in Information Technology** — *LJ University, Ahmedabad* (2024–2028)
* 🏆 **Inheritance and Data Structures in Java** — *Coursera*
* 🏆 **Exploratory Data Analysis for Machine Learning** — *Coursera*
* 💡 **Lakshya 2.0 Hackathon** — *Participant, LD College of Engineering*

---

<div align="center" id="-signature-endpoint">

<br/>

```text
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
                         TANISH SHAH  //  SYSTEMS & BACKEND ENGINEER
                "Build with strict constraints. Architect for determinism."
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

<br/>

<a href="https://tanish1808.github.io/My_Portfolio/" target="_blank">
  <img src="https://img.shields.io/badge/🌐_EXPLORE_PORTFOLIO-00F5A0?style=for-the-badge&logo=googlechrome&logoColor=070A10&labelColor=0F172A" height="40" alt="Portfolio" />
</a>
<a href="https://linkedin.com/in/tanish-shah-703489349" target="_blank">
  <img src="https://img.shields.io/badge/LINKEDIN-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white&labelColor=0F172A" height="40" alt="LinkedIn" />
</a>
<a href="mailto:tanishshah1808@gmail.com">
  <img src="https://img.shields.io/badge/EMAIL-EA4335?style=for-the-badge&logo=gmail&logoColor=white&labelColor=0F172A" height="40" alt="Email" />
</a>
<a href="https://github.com/Tanish1808" target="_blank">
  <img src="https://img.shields.io/badge/GITHUB-181717?style=for-the-badge&logo=github&logoColor=white&labelColor=0F172A" height="40" alt="GitHub" />
</a>

<br/><br/>

<sub>Crafted with architectural rigor, subtle visual design &amp; engineering precision.</sub>

</div>