<img alt="" src="https://capsule-render.vercel.app/api?type=waving&color=0:F97316,50:FB923C,100:F97316&height=140&section=header&animation=fadeIn" width="100%"/>

<div align="center">

# Muhammad Naimatullah Khan

**DevOps &amp; Platform Engineer at Veeam Software**

I keep Kubernetes platforms boring, so the teams on top of them can be interesting.

[![Typing SVG](https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=20&pause=900&color=F97316&center=true&vCenter=true&width=640&height=40&lines=Jenkins+CI+%C2%B7+Spinnaker+CD+%C2%B7+Argo+CD+GitOps;AWS+core+%C2%B7+GCP+regional+%C2%B7+Karpenter+%C2%B7+Kyverno;If+it+is+not+in+git%2C+it+is+not+in+the+cluster)](https://git.io/typing-svg)

<a href="https://www.linkedin.com/in/muhammad-naimatullah-khan"><img alt="LinkedIn" src="https://skillicons.dev/icons?i=linkedin" height="40"/></a>
&nbsp;
<a href="mailto:muhammadnaimatullahkhan99@gmail.com"><img alt="Email" src="https://skillicons.dev/icons?i=gmail" height="40"/></a>
&nbsp;
<a href="https://naimss.vercel.app"><img alt="Portfolio" src="https://skillicons.dev/icons?i=vercel" height="40"/></a>
&nbsp;
<a href="https://github.com/Cyber-Naimo"><img alt="GitHub" src="https://skillicons.dev/icons?i=github" height="40"/></a>

<img alt="99.9 percent uptime" src="https://img.shields.io/badge/Uptime-99.9%25-F97316?style=flat-square&labelColor=1F2937"/>
<img alt="90 percent faster deploys" src="https://img.shields.io/badge/Deploys-90%25_faster-F97316?style=flat-square&labelColor=1F2937"/>
<img alt="100 percent tested recovery" src="https://img.shields.io/badge/Recovery-100%25_tested-F97316?style=flat-square&labelColor=1F2937"/>
<img alt="CKA certified" src="https://img.shields.io/badge/CKA-Certified-F97316?style=flat-square&labelColor=1F2937"/>
<img alt="Based in Karachi, Pakistan" src="https://img.shields.io/badge/Karachi-PK-1F2937?style=flat-square&labelColor=1F2937"/>

</div>

## `kubectl describe engineer naimatullah`

```yaml
apiVersion: platform.veeam.io/v1
kind: Engineer
metadata:
  name: muhammad-naimatullah-khan
  namespace: data-resilience
  labels:
    role: devops-platform
    focus: kubernetes
spec:
  replicas: 1
  owns:
    - jenkins-ci-templates
    - spinnaker-delivery
    - argocd-gitops
    - internal-tooling
  clouds: [aws, gcp]
  principles:
    - git is the only source of truth
    - alert before the customer notices
    - a backup is a rumour until you restore it
status:
  phase: Running
  uptime: 99.9%
  restartCount: 0
```

## Currently

Platform engineering for Veeam's data resilience products.

| | |
|:--|:--|
| **Runtime** | Kubernetes is the whole infrastructure, not a piece of it |
| **CI** | Jenkins, multiple shared pipeline templates so new services start with a working path |
| **CD** | Spinnaker promotion pipelines with real gates and real rollbacks |
| **Packaging** | Helm charts for everything that ships |
| **GitOps** | Argo CD keeping every cluster equal to git, drift visible on a dashboard |
| **Cloud** | AWS as core, GCP in select regions |
| **Scaling** | Karpenter provisioning against real demand instead of a fixed guess |
| **Policy** | Kyverno enforcing guardrails in the cluster, not in review comments |
| **Tooling** | Internal developer tools plus alerting and backup automation I build and maintain |

## Delivery pipeline I run

```mermaid
flowchart LR
    subgraph CI["SOURCE · CI"]
        direction TB
        APP(["git push"]) --> BUILD["Jenkins<br/>shared template"] --> TEST["build · test"] --> GATE{{"Trivy · SonarQube<br/>quality gate"}}
    end

    subgraph ART["ARTIFACTS"]
        direction TB
        IMG[("image<br/>registry")]
        CHART[("Helm<br/>charts")]
    end

    subgraph DEL["DELIVERY"]
        direction TB
        SPIN{{"Spinnaker<br/>promotion gates"}} --> CFG(["config repo"]) --> ARGO["Argo CD"]
    end

    subgraph RT["RUNTIME · KUBERNETES"]
        direction TB
        KYV["Kyverno<br/>admission policy"]
        WL["workloads"]
        KARP["Karpenter<br/>node capacity"]
        OBS["Prometheus · Grafana<br/>ELK"]
    end

    subgraph CLD["CLOUD"]
        direction TB
        AWS["AWS<br/>core"]
        GCP["GCP<br/>regional"]
    end

    GATE --> IMG
    GATE --> CHART
    IMG --> SPIN
    CHART --> SPIN
    ARGO -->|sync| WL
    KYV -.->|admit| WL
    KARP -.->|scale| WL
    WL -.->|metrics| OBS
    WL --> AWS
    WL --> GCP

    linkStyle default stroke:#9CA3AF,stroke-width:1.5px

    classDef proc fill:#1F2937,stroke:#4B5563,color:#F9FAFB
    classDef store fill:#0F766E,stroke:#134E4A,color:#F0FDFA
    classDef hot fill:#F97316,stroke:#C2410C,color:#111827
    class APP,BUILD,TEST,GATE,SPIN,CFG,KYV,KARP,OBS,AWS,GCP proc
    class IMG,CHART store
    class ARGO,WL hot
    style CI fill:#0D1117,stroke:#30363D,color:#8B949E
    style ART fill:#0D1117,stroke:#30363D,color:#8B949E
    style DEL fill:#0D1117,stroke:#30363D,color:#8B949E
    style RT fill:#0D1117,stroke:#30363D,color:#8B949E
    style CLD fill:#0D1117,stroke:#30363D,color:#8B949E
```

## Stack

<div align="center">

<img alt="Kubernetes, Docker, Jenkins, AWS, GCP, Terraform, Ansible, Linux" src="https://skillicons.dev/icons?i=kubernetes,docker,jenkins,aws,gcp,terraform,ansible,linux&theme=dark" height="48"/>
<br/>
<img alt="Prometheus, Grafana, Elasticsearch, GitLab, GitHub, Bash, Python, Postgres" src="https://skillicons.dev/icons?i=prometheus,grafana,elasticsearch,gitlab,github,bash,python,postgres&theme=dark" height="48"/>

<br/>

<img alt="Helm" src="https://img.shields.io/badge/Helm-1F2937?style=flat-square&logo=helm&logoColor=white"/>
<img alt="Argo CD" src="https://img.shields.io/badge/Argo_CD-1F2937?style=flat-square&logo=argo&logoColor=white"/>
<img alt="Spinnaker" src="https://img.shields.io/badge/Spinnaker-1F2937?style=flat-square&logo=spinnaker&logoColor=white"/>
<img alt="Karpenter" src="https://img.shields.io/badge/Karpenter-1F2937?style=flat-square&logo=kubernetes&logoColor=white"/>
<img alt="Kyverno" src="https://img.shields.io/badge/Kyverno-1F2937?style=flat-square&logo=kubernetes&logoColor=white"/>
<img alt="Velero" src="https://img.shields.io/badge/Velero-1F2937?style=flat-square&logo=kubernetes&logoColor=white"/>
<img alt="Trivy" src="https://img.shields.io/badge/Trivy-1F2937?style=flat-square&logo=trivy&logoColor=white"/>
<img alt="MinIO" src="https://img.shields.io/badge/MinIO-1F2937?style=flat-square&logo=minio&logoColor=white"/>

</div>

## Selected work

| Project | What it is | Outcome |
|:--|:--|:--|
| **[KubeForge](https://github.com/naimss-paysys/k8s-templates)** | Deployment CLI with preflight checks, diff preview, approval gate, auto rollback | 90% faster deploys, zero downtime |
| **DR pipeline** | Velero, OpenEBS and MinIO doing scheduled full cluster backups | Proven by deleting a cluster and restoring it |
| **ELK platform** | Filebeat to Logstash to Elasticsearch to Kibana across 9+ services | 60% faster detection |
| **[API platform](https://github.com/naimss-paysys/hoppscotch)** | Self hosted Hoppscotch with custom auth, RBAC, team workspaces | Postman licensing cost to zero |

## Open source

Code you can actually read.

| Repo | What it does |
|:--|:--|
| **[ai-devops](https://github.com/Cyber-Naimo/ai-devops)** | SRE command center for air gapped Linux fleets. FastAPI control plane, React dashboard, RPM packaged Python agent, SSH scanning, RBAC |
| **[ci-templates](https://github.com/Cyber-Naimo/ci-templates)** | Reusable GitLab CI templates for Java and Node microservices. One `include:` block and the pipeline is production ready |
| **[devsecops-assignment](https://github.com/Cyber-Naimo/devsecops-assignment)** | Two host Docker Swarm cluster, Consul over HTTPS, mTLS Docker, Terraform and Ansible, seven DevSecOps controls |
| **[FullStackChatApp-K8s](https://github.com/Cyber-Naimo/FullStackChatApp-K8s)** | Full stack chat app with a Jenkinsfile and Kubernetes manifests, built to be deployed rather than demoed |

## Experience

| Role | Company | Years |
|:--|:--|:--|
| DevOps Engineer | Veeam Software | 2026, present |
| Associate DevOps Engineer | Paysys Labs | 2025, 2026 |
| QA Engineer Intern | VentureDive | 2025 |
| Head of Offensive Security | ACM FAST NUCES | 2024 |

## Certifications

<img alt="CKA" src="https://img.shields.io/badge/CKA-Certified_Kubernetes_Administrator-F97316?style=flat-square&logo=kubernetes&logoColor=white&labelColor=1F2937"/>
<img alt="Gold Medalist" src="https://img.shields.io/badge/2×-Gold_Medalist,_FAST_NUCES-1F2937?style=flat-square"/>
<img alt="Raising the Bar Award" src="https://img.shields.io/badge/Award-Raising_the_Bar-1F2937?style=flat-square"/>
<img alt="Google Cloud Foundations" src="https://img.shields.io/badge/Google_Cloud-Foundations-1F2937?style=flat-square&logo=googlecloud&logoColor=white"/>
<img alt="EC-Council EHE" src="https://img.shields.io/badge/EC--Council-Ethical_Hacking-1F2937?style=flat-square"/>

## Résumé

Full history, certifications and project detail in one PDF.

<a href="https://github.com/Cyber-Naimo/Cyber-Naimo/raw/main/Muhammad_Naimatullah_Khan.pdf"><img alt="Download résumé as PDF" src="https://img.shields.io/badge/Download_PDF-F97316?style=for-the-badge&labelColor=F97316"/></a>
<a href="https://github.com/Cyber-Naimo/Cyber-Naimo/blob/main/Muhammad_Naimatullah_Khan.pdf"><img alt="View résumé on GitHub" src="https://img.shields.io/badge/View_in_browser-1F2937?style=for-the-badge"/></a>
<a href="https://naimss.vercel.app"><img alt="Portfolio site" src="https://img.shields.io/badge/Portfolio-1F2937?style=for-the-badge&logo=vercel&logoColor=white"/></a>

### Languages & Scripting
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=flat-square&logo=gnu-bash&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![YAML](https://img.shields.io/badge/YAML-CB171E?style=flat-square&logo=yaml&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=mysql&logoColor=white)

---

## 🚀 Featured Projects

### ⚙️ [KubeForge](https://github.com/naimss-paysys/k8s-templates) — Kubernetes Deployment CLI
> *One command to deploy any service to any country, safely and fast.*

- Bash CLI replacing hours of manual `kubectl` commands across 2 countries
- Pre-flight checks → diff preview → approval gate → **auto-rollback** on failure
- `70–90%` faster deployments · `0` downtime incidents

`Bash` `Kubernetes` `kubectl` `yq` `GitLab CI` `ELK Stack`

---

### 💾 [Enterprise DR Pipeline](https://github.com/Cyber-Naimo) — Disaster Recovery
> *Tested by actually deleting a cluster and restoring it — 100% recovery rate.*

- Velero + OpenEBS + MinIO full-cluster backup system
- Automated scheduled snapshots across all namespaces
- **100% data recovery** — not just backed up, proven to restore

`Velero` `OpenEBS` `MinIO` `Kubernetes` `Helm` `Bash`

---

### 📡 [ELK Stack Observability](https://github.com/Cyber-Naimo) — Log Intelligence Platform
> *One dashboard across 9+ microservices. Problems surface before users notice.*

- Filebeat → Logstash → Elasticsearch → Kibana full pipeline
- Custom alerting dashboards · `80%` faster detection · Real-time alerts

`Elasticsearch` `Logstash` `Kibana` `Filebeat` `Kubernetes`

---

### 🔧 [Internal API Platform](https://github.com/naimss-paysys/hoppscotch) — Self-Hosted Hoppscotch
> *Replaced paid Postman subscription with a self-hosted, fully owned alternative.*

- Custom auth, RBAC roles, private team workspaces
- `$0` licensing cost · Full internal data ownership

`Docker Compose` `Nginx` `PostgreSQL` `Redis` `OAuth` `RHEL 8.10`

---

## 🏅 Certifications & Awards

| Year | Award / Cert | Issuer |
|------|-------------|--------|
| 2025 | 🏆 **Raising the Bar Award** | Paysys Labs |
| 2025 | ⎈ **CKA — Certified Kubernetes Administrator** | KodeKloud |
| 2025 | 🥇 **Gold Medal — 1st Position** (Spring 2025) | FAST NUCES |
| 2024 | 🥇 **Gold Medal — 1st Position** (Fall 2024) | FAST NUCES |
| 2024 | ☁️ **Google Cloud Computing Foundations** | Google Cloud |
| 2024 | 🔒 **Google Cloud Cybersecurity Certificate** | Google Cloud |
| 2024 | 🔑 **Postman API Fundamentals Expert** | Postman |
| 2023 | 🛡️ **Ethical Hacking Essentials (EHE)** | EC-Council |

---

## 💼 Experience

**DevOps Engineer** · Veeam Software *(Aug 2026 – Present)*
> Building and operating infrastructure for data resilience and backup solutions, Kubernetes, CI/CD automation, and cloud platform reliability at enterprise scale.

**Associate DevOps Engineer** · Paysys Labs *(Aug 2025 – Aug 2026)*
> EKS Anywhere Kubernetes for RTGS fintech systems across Togo & Tanzania. Built KubeForge CLI, ELK Stack observability, DR pipeline, DevSecOps with Trivy + SonarQube. Trained 20+ engineers at partner banks.

**QA Engineer Intern** · VentureDive *(Mar 2025 – Jul 2025)*
> Automated Careem Dubai app with Maestro. Found 3+ critical security vulnerabilities. Built Selenium framework with Extent Reports and BDD/Cucumber.

**Head of Offensive Security** · ACM FAST NUCES *(2024)*
> Led offensive security wing, CTF events, penetration testing workshops, student security community.

---

## 📊 GitHub Stats

<div align="center">

<img height="170" src="https://github-readme-stats.vercel.app/api?username=Cyber-Naimo&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=3B82F6&icon_color=8B5CF6&text_color=CDD9E5&rank_icon=github"/>
<img height="170" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Cyber-Naimo&layout=compact&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=3B82F6&text_color=CDD9E5"/>

</div>

<div align="center">

[![GitHub Streak](https://streak-stats.demolab.com?user=Cyber-Naimo&theme=tokyonight&hide_border=true&background=0D1117&ring=3B82F6&fire=8B5CF6&currStreakLabel=3B82F6)](https://git.io/streak-stats)

</div>

---

## 🏆 GitHub Trophies

<div align="center">

[![trophy](https://github-trophies.vercel.app/?username=Cyber-Naimo&theme=tokyonight&no-frame=true&no-bg=true&margin-w=4&column=4)](https://github.com/ryo-ma/github-profile-trophy)

</div>

---

## 🐍 Contribution Snake

<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=Cyber-Naimo&theme=github_dark"/>
  <img alt="GitHub profile summary" src="https://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=Cyber-Naimo&theme=default"/>
</picture>

<img alt="Contribution activity graph" src="https://github-readme-activity-graph.vercel.app/graph?username=Cyber-Naimo&bg_color=00000000&color=F97316&line=F97316&point=FB923C&area_color=F97316&title_color=F97316&area=true&hide_border=true"/>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Cyber-Naimo/Cyber-Naimo/output/github-snake-dark.svg"/>
  <img alt="Contribution snake" src="https://raw.githubusercontent.com/Cyber-Naimo/Cyber-Naimo/output/github-snake.svg"/>
</picture>

</div>

## Get in touch

Open to conversations about platform engineering, GitOps, and running Kubernetes as the whole stack.

<a href="https://www.linkedin.com/in/muhammad-naimatullah-khan"><img alt="Connect on LinkedIn" src="https://img.shields.io/badge/Connect_on_LinkedIn-F97316?style=for-the-badge&labelColor=F97316"/></a>
<a href="mailto:muhammadnaimatullahkhan99@gmail.com"><img alt="Send an email" src="https://img.shields.io/badge/Send_an_email-1F2937?style=for-the-badge&logo=gmail&logoColor=white"/></a>

<img alt="" src="https://capsule-render.vercel.app/api?type=waving&color=0:F97316,50:FB923C,100:F97316&height=100&section=footer&animation=fadeIn" width="100%"/>
