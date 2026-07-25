# Hi, I'm Oluwagbade Odimayo 👋

**Data and Cloud Engineer** — I build reliable data platforms, cloud infrastructure and reproducible workflows for operational and scientific data.

I design data-intensive systems with Python, SQL, AWS, Azure, GCP, Terraform, Docker, Kubernetes, Nextflow and CI/CD. My work spans data engineering, cloud platform automation, applied machine learning and bioinformatics — with a foundation in life sciences that shapes how I treat data: computational outputs must be reproducible, traceable and explicit about their limitations. So the engineering emphasises validation, provenance, observability, testing and clear documentation.

The consistent question across all of it is the one that decides whether a system can be trusted in production — *is it correct, is it validated, and does it fail safely?*

- A pipeline that completed successfully hasn't proven the data is right — schemas, volumes, freshness and reconciliation have to be tested.
- A deployment that can't roll back in seconds isn't a deployment, it's a hope.
- A variant caller reporting 95% confidence should be right 95% of the time — and should abstain when it can't be.

🌍 **Available for remote work worldwide** · 🔎 Data Engineering · Cloud & Platform Engineering · Bioinformatics Engineering
🔗 **[gbadedata.com](https://gbadedata.com)** — full case studies, architecture and engineering evidence

---

## 🧪 Certifications

[![DP-700](https://img.shields.io/badge/Microsoft-DP--700_Fabric_Data_Engineer-0078D4?style=flat-square&logo=microsoft)](https://learn.microsoft.com/en-gb/users/OluwagbadeOdimayo-8921/credentials/ABE9871D1917291F)
[![DP-600](https://img.shields.io/badge/Microsoft-DP--600_Fabric_Analytics_Engineer-0078D4?style=flat-square&logo=microsoft)](https://learn.microsoft.com/en-gb/users/oluwagbadeodimayo-8921/credentials/36ab7c802fb7da99)

**Microsoft Certified: Fabric Data Engineer Associate (DP-700)** · **Fabric Analytics Engineer Associate (DP-600)**

---

## 🌐 Open-source contributions

Code merged upstream into projects I don't maintain — the most externally-validated work here, because someone else's maintainers reviewed and accepted it.

| Project | Contribution | Status |
|---|---|---|
| **[nf-core/modules](https://github.com/nf-core/modules/pull/12018)** | Fixed the FreeBayes module — corrected three nf-test cases running on human data but labelled `sarscov2`, updated snapshot keys, added missing EDAM ontology entries, and fixed stub gzip syntax for nf-core linting (PR #12018) | ✅ Merged |
| **[Meltano](https://github.com/meltano/meltano/pulls?q=is%3Apr+author%3Agbadedata+is%3Amerged)** | Three merged PRs — TTY-aware colour suppression for clean redirected logs, `FORCE_COLOR` support with `NO_COLOR` precedence, and `--refresh-catalog` for `meltano invoke` | ✅ Merged |
| **[Pydantic Settings](https://github.com/pydantic/pydantic-settings)** | Regression tests for nested environment-variable aliases, validation aliases and alias choices | Local validation |
| **[AEGIS](https://github.com/gbadedata/AEGIS)** | Replaced inaccurate install instructions with a reproducible local setup | Docs |

---

## ☁️ Data & Cloud Engineering

Infrastructure as code, zero-downtime delivery, and pipelines built to be operated rather than demoed.

| Project | What it does |
|---|---|
| **[aws-supplyshield-lakehouse](https://github.com/gbadedata/aws-supplyshield-lakehouse)** | Incremental supply-chain ingestion into an S3 lakehouse with data contracts, schema validation and source-to-target reconciliation |
| **[enterprise-progressive-delivery-eks](https://github.com/gbadedata/enterprise-progressive-delivery-eks)** | Argo Rollouts canary releases on AWS EKS with automatic rollback, container security scanning, and Terraform-provisioned infrastructure |
| **[mediflow](https://github.com/gbadedata/mediflow)** | Production-grade Azure platform for clinical data ingestion — AKS, Key Vault, Terraform, Helm, through a three-stage Azure DevOps pipeline |
| **[zero-downtime-bluegreen-eks](https://github.com/gbadedata/zero-downtime-bluegreen-eks)** | Blue-green on EKS with instant traffic switching and sub-5-second rollback |
| **[commerce-elt-platform](https://github.com/gbadedata/commerce-elt-platform)** | Snowflake ELT platform with dbt, S3, Snowpipe, and CI-enforced transformations |
| **[clintrial-stream](https://github.com/gbadedata/clintrial-stream)** | Real-time clinical-trial event streaming — Kinesis, DynamoDB, sub-second latency, regulatory-grade audit trails |

`Terraform` `Kubernetes` `Docker` `AWS` `Azure` `GCP` `Argo Rollouts` `Helm` `Airflow` `dbt` `Snowflake` `Kafka` `Prometheus` `Grafana` `GitHub Actions`

<details>
<summary><b>More cloud &amp; engineering work</b> (15 repos)</summary>

<br>

**Deployment & delivery** — [ecommerce-blue-green-aks](https://github.com/gbadedata/ecommerce-blue-green-aks) (NestJS API, local to AKS) · [shopswift-blue-green](https://github.com/gbadedata/shopswift-blue-green) (Minikube to EKS with Prometheus/Grafana) · [swiftdeploy](https://github.com/gbadedata/swiftdeploy) (declarative CLI turning one manifest into a running stack, with OPA policy enforcement) · [hng14-stage3](https://github.com/gbadedata/hng14-stage3) (real-time DDoS detection daemon that blocks via iptables)

**Infrastructure as code** — [terraform-aws-web-server](https://github.com/gbadedata/terraform-aws-web-server) (a whole AWS network stack from one command) · [azure-arm-linux-vm-iac](https://github.com/gbadedata/azure-arm-linux-vm-iac) · [secure-nginx-linux-server](https://github.com/gbadedata/secure-nginx-linux-server) (SSH hardening, UFW, Let's Encrypt on EC2) · [azure-web-deployment-project](https://github.com/gbadedata/azure-web-deployment-project) (IaaS vs PaaS compared) · [webapp-azure-demo](https://github.com/gbadedata/webapp-azure-demo)

**MLOps & pipelines** — [ml_inference_api](https://github.com/gbadedata/ml_inference_api) (notebook to deployed API with monitoring and Kubernetes) · [ml-training-pipeline-ci](https://github.com/gbadedata/ml-training-pipeline-ci) · [tfl-cycle-pipeline](https://github.com/gbadedata/tfl-cycle-pipeline) (TfL BikePoint to dbt dimensional model via Airflow) · [engineering-workflow-automation](https://github.com/gbadedata/engineering-workflow-automation) (CI and Trello enforcing process over individual discipline) · [governed-semantic-model-api](https://github.com/gbadedata/governed-semantic-model-api) (Fabric/Power BI metrics served through AWS) · [stage1-personal-api](https://github.com/gbadedata/stage1-personal-api)

</details>

---

## 🧬 Bioinformatics & Scientific Computing

Reproducible pipelines and rigorous evaluation of the tools the field relies on — with provenance, quality control, and a clear line between computational evidence and biological interpretation.

| Project | What it does |
|---|---|
| **[biomarker-concordance-pipeline](https://github.com/gbadedata/biomarker-concordance-pipeline)** | Nextflow DSL2 germline variant calling on AWS, benchmarked against the GIAB HG001 truth set with clinical-grade VAF reproducibility statistics |
| **[ecm-target-discovery-pipeline](https://github.com/gbadedata/ecm-target-discovery-pipeline)** | Provenance-preserving multi-omics workflow for extracellular-matrix target prioritisation in pancreatic cancer |
| **[clinvar-interpretation-benchmark](https://github.com/gbadedata/clinvar-interpretation-benchmark)** | Can a frontier LLM be trusted to classify germline variants? Scored against ClinVar expert consensus, with and without supplied ACMG evidence |
| **[variant-calling-calibration-benchmark](https://github.com/gbadedata/variant-calling-calibration-benchmark)** | Treats quality filtering as an abstention decision — stratified by genomic difficulty, with QUAL calibration measured, not assumed |
| **[bioagent](https://github.com/gbadedata/bioagent)** | Autonomous QC analyst built with LangGraph and Claude — pulls live pipeline metrics, reasons over them, searches PubMed, produces a clinical-grade report |

`Nextflow` `scanpy` `AnnData` `Bioconductor` `GIAB` `ClinVar` `VCF` `RNA-seq` `single-cell` `spatial transcriptomics`

<details>
<summary><b>More bioinformatics work</b> (12 repos)</summary>

<br>

**Pipelines & platforms** — [variantlens](https://github.com/gbadedata/variantlens) (VCF parsing, validation, annotation, REST API) · [ngs-results-explorer](https://github.com/gbadedata/ngs-results-explorer) (RNA-Seq differential expression with volcano-plot dashboard) · [bioseq-platform](https://github.com/gbadedata/bioseq-platform) (NCBI SRA ingestion into a multi-zone AWS data lake) · [genome-vault](https://github.com/gbadedata/genome-vault) (variant warehouse on BigQuery + Dataflow) · [genomicflow-platform](https://github.com/gbadedata/genomicflow-platform) (Pub/Sub streaming from sequencing instruments to Cloud Run) · [clinvar-variant-prioritisation-workflow](https://github.com/gbadedata/clinvar-variant-prioritisation-workflow) (inherited-disease variant ranking with transparent evidence rules)

**Benchmarks** — [squidpy-spatial-benchmark](https://github.com/gbadedata/squidpy-spatial-benchmark) (persistent homology vs Moran's I on Visium) · [sc-celltype-benchmark](https://github.com/gbadedata/sc-celltype-benchmark) · [scvelo-trajectory-benchmark](https://github.com/gbadedata/scvelo-trajectory-benchmark) (RNA velocity on pancreatic endocrinogenesis) · [single-cell-marker-reasoning-benchmark](https://github.com/gbadedata/single-cell-marker-reasoning-benchmark) · [cellfatebench-single-cell-analysis](https://github.com/gbadedata/cellfatebench-single-cell-analysis) · [finemap-calibration-benchmark](https://github.com/gbadedata/finemap-calibration-benchmark) (does SuSiE's 95% credible set contain the causal variant 95% of the time?)

</details>

---

## 📊 Applied AI & Machine Learning

Modelling on real, imbalanced data — where the work is the decision the model supports, not the accuracy score. Mostly applied to credit risk and financial crime, where the constraints bite hardest: rare positives, asymmetric costs, mandatory explainability.

| Project | What it does |
|---|---|
| **[transaction-fraud-scoring](https://github.com/gbadedata/transaction-fraud-scoring)** | Calibrated, leakage-aware scoring built around a real operational constraint: an investigation team can only review so many alerts a day |
| **[credit-default-prediction](https://github.com/gbadedata/credit-default-prediction)** | Imbalance handled with PR-AUC and KS rather than accuracy, a cost-based approval threshold, SHAP at portfolio and applicant level, demographics excluded for fair lending |
| **[pd-scorecard-validation](https://github.com/gbadedata/pd-scorecard-validation)** | Builds a Weight-of-Evidence scorecard, then independently validates it — both halves, as first and second line would split them |
| **[mule-network-detection](https://github.com/gbadedata/mule-network-detection)** | Feature engineering from graph structure — fan-in, fan-out, chains — because per-transaction scoring catches almost none of a sub-1% positive class |
| **[transaction-classification](https://github.com/gbadedata/transaction-classification)** | 259k noisy bank-transaction strings into 31 categories — multi-class, imbalanced, messy text, taken to a production-style routing pipeline |

Also: **[ifrs9-ecl-engine](https://github.com/gbadedata/ifrs9-ecl-engine)** (PD/LGD/EAD impairment modelling on 1.35M loans) · **[bustout-detection](https://github.com/gbadedata/bustout-detection)** · **[mcp-research-agent](https://github.com/gbadedata/mcp-research-agent)** (an MCP server and standalone Claude agent from one toolset) · **[biomedical-rag-qa](https://github.com/gbadedata/biomedical-rag-qa)** (BM25 + dense FAISS retrieval)

`imbalanced learning` `cost-sensitive thresholds` `SHAP` `explainability` `calibration` `XGBoost` `scikit-learn` `PyTorch` `NLP` `model validation` `fair lending`

---

## 📋 Data Operations & Business Systems

Analyst-side work: SQL exception reporting, ERP data integrity, and the process improvement that keeps operational data trustworthy.

| Project | What it does |
|---|---|
| **[sap-process-improvement-project](https://github.com/gbadedata/sap-process-improvement-project)** | 720 SAP orders audited over six weeks, four discrepancy types traced to root cause, error rate cut from 27.8% to under 2% |
| **[sap-order-management-project](https://github.com/gbadedata/sap-order-management-project)** | Full SAP SD order lifecycle on 200 B2B orders — pricing validated against condition records, error rate taken to 0% |
| **[Project-Asset-Ops-Reporting](https://github.com/gbadedata/Project-Asset-Ops-Reporting)** | Operational reporting over energy-meter assets — SQLite, SQL views, Power BI dashboard with exception reporting |
| **[dataops-asset-data-integrity](https://github.com/gbadedata/dataops-asset-data-integrity)** | Reproducible SQL validation checks producing an auditable exception report |

`SQL` `SQLite` `Power BI` `SAP SD` `Excel` `exception reporting` `data governance` `root cause analysis`

---

## 🛠 Toolkit

**Languages** — Python · SQL · R · Bash · HCL

**Data & ML** — pandas · scikit-learn · PyTorch · XGBoost · SHAP · dbt · Airflow · Spark · DuckDB

**Cloud** — AWS · Azure · GCP · Terraform · Kubernetes · Docker

**Bioinformatics** — Nextflow · nf-core · nf-test · scanpy · Bioconductor · Conda

**AI systems** — LangGraph · MCP · RAG · LLM evaluation

**Practice** — CI/CD · testing · reproducibility · provenance · IaC

---

## 📫 Get in touch

- 🌐 **[gbadedata.com](https://gbadedata.com)** — case studies, architecture diagrams and engineering evidence
- 💼 [LinkedIn](https://www.linkedin.com/in/oluwagbade-odimayo-)
- ✍️ [dev.to](https://dev.to/gbadedata) · [Medium](https://medium.com/@gbadedata) · [Hashnode](https://hashnode.com/@gbade-oj)
- ✉️ [o.odimayo@gbadedata.com](mailto:o.odimayo@gbadedata.com)
