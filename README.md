<h1 align="center">
  <br>
  <img src="https://raw.githubusercontent.com/Tanish1808/My_Portfolio/main/assets/og_preview.png" alt="Tanish Shah" width="120px" style="border-radius: 50%;">
  <br>
  Tanish Shah
  <br>
</h1>

<p align="center">
  <strong>Software Engineer &bull; Backend Systems &bull; Applied Machine Learning</strong>
</p>

<p align="center">
  <a href="https://tanish1808.github.io/My_Portfolio/">
    <img src="https://img.shields.io/badge/LIVE_PORTFOLIO-00F5A0?style=for-the-badge&logo=googlechrome&logoColor=black" alt="Live Portfolio" />
  </a>
  <a href="https://linkedin.com/in/tanish-shah-703489349">
    <img src="https://img.shields.io/badge/LINKEDIN-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" />
  </a>
  <a href="mailto:tanishshah1808@gmail.com">
    <img src="https://img.shields.io/badge/GMAIL-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" />
  </a>
</p>

<p align="center">
  <a href="#-about-me">About</a> &bull;
  <a href="#-live-deployments">Deployments</a> &bull;
  <a href="#-core-projects">Projects</a> &bull;
  <a href="#-skills--technologies">Tech Stack</a> &bull;
  <a href="#-connect">Contact</a>
</p>

---

### ⚡ About Me

I design and build **multi-tier web systems**, **stateless authentication architectures**, and **cost-optimized data pipelines**. My engineering focus is on transactional data integrity, algorithmic efficiency, and building robust APIs that scale under real-world constraints.

```
• Primary Disciplines : Backend Engineering, REST/Async API Design, Distributed Workflows
• Core Technologies   : Python (FastAPI, Django, Flask), Java, PostgreSQL, MongoDB, PyTorch
• Current Focus       : Microservice Orchestration & Spatial Deduplication Pipelines
```

---

### 🌐 Live Deployments

<table>
  <thead>
    <tr>
      <th>Project</th>
      <th>Status</th>
      <th>Hosting</th>
      <th>Link</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>Developer Portfolio</strong></td>
      <td><code>🟢 Live</code></td>
      <td>GitHub Pages</td>
      <td><a href="https://tanish1808.github.io/My_Portfolio/"><strong>Open App ↗</strong></a></td>
      <td>Interactive terminal shell simulator, responsive canvas graphics, and dynamic milestone inspector.</td>
    </tr>
    <tr>
      <td><strong>Ticket Tally</strong></td>
      <td><code>🟢 Live</code></td>
      <td>Render Cloud (Free Tier)</td>
      <td><a href="https://github.com/Tanish1808"><strong>Repository ↗</strong></a></td>
      <td>Enterprise incident dispatch system with priority queue scheduling and JWT role-based access control.</td>
    </tr>
    <tr>
      <td><strong>Civic Lens</strong></td>
      <td><code>🟢 Architecture</code></td>
      <td>Microservices</td>
      <td><a href="https://github.com/Tanish1808"><strong>Repository ↗</strong></a></td>
      <td>Municipal incident intelligence platform with two-stage spatial & CNN duplicate detection.</td>
    </tr>
  </tbody>
</table>

---

### 🛠️ Core Projects

#### 1. 🌍 Civic Lens — AI Civic Issue Reporting & Deduplication System
> **Problem:** Public issue tracking portals are overwhelmed with duplicate submissions of the same localized incidents.  
> **Solution:** A cost-ordered two-stage deduplication pipeline that prevents expensive deep metric computation on non-candidate records.

* **Stage 1 (Spatial Indexing):** Uses MongoDB `2dsphere` spatial indexing for fast proximity radius queries ($O(\log N)$).
* **Stage 2 (Visual Similarity):** Calculates perceptual hashing (pHash) hamming distance and PyTorch CNN embedding cosine similarity on localized candidates ($O(K)$ where $K \ll N$).
* **Service Isolation:** FastAPI async service handles ML inference tasks independently from Django REST Framework business logic to maintain low latency on standard requests.

```
Citizen Upload ──► FastAPI (PyTorch CNN) ──► MongoDB 2dsphere (Proximity Filter) ──► Candidate Embeddings ──► Django REST ──► Dashboard
```

---

#### 2. 🎫 Ticket Tally — Smart IT Support & Priority Queue Dispatch
> **Problem:** FIFO or basic timestamp sorting causes critical system-down incidents to queue behind trivial support tickets.  
> **Solution:** Algorithmic Priority Queue scheduling coupled with deterministic state-machine SLA monitors.

* **Algorithmic Dispatch:** High-severity incident tickets are assigned to urgent dispatch queues deterministically.
* **Role-Based Authorization:** Three distinct user tiers (`Employee`, `IT Staff`, `Admin`) enforced via stateless JWT claims.
* **Event-Driven SLAs:** SLA countdown clocks are tied directly to state transition events (`CREATED` &rarr; `IN_PROGRESS` &rarr; `RESOLVED`).
* **Deployment:** Containerized and hosted on **Render Cloud (Free Tier)** with health check management.

```
Employee / Admin ──► JWT Route Guard ──► Priority Queue Scoring ──► IT Staff Desk ──► State Transitions & SLAs ──► PostgreSQL
```

---

### 💻 Skills & Technologies

```
Languages     : Python, Java, JavaScript (ES6+), SQL
Backend       : FastAPI, Django, Django REST Framework, Flask, Node.js, Express.js
Databases     : PostgreSQL, MySQL, MongoDB (2dsphere Indexing)
Machine Learning : PyTorch, CNN Embeddings, Perceptual Hashing (pHash), Scikit-Learn
Frontend      : React.js, Tailwind CSS, HTML5, CSS3, Bootstrap
DevOps & Tools: Git, GitHub, Render, Postman, pgAdmin, VS Code
```

---

### 📬 Connect

<p align="left">
  <a href="https://tanish1808.github.io/My_Portfolio/"><strong>🌐 Interactive Portfolio</strong></a> &bull;
  <a href="https://linkedin.com/in/tanish-shah-703489349"><strong>LinkedIn</strong></a> &bull;
  <a href="mailto:tanishshah1808@gmail.com"><strong>Email</strong></a> &bull;
  <a href="https://github.com/Tanish1808"><strong>GitHub</strong></a>
</p>