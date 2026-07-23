# Hi, I'm Oluwagbade Odimayo 👋

**I build production data and ML systems — then prove they actually work.**

Most projects stop at a number: an F1 score, a green pipeline, a UMAP plot. Mine start there. Across data science, genomics, and cloud infrastructure, the consistent question in my work is the one that decides whether a system can be trusted in production — *is it calibrated, is it validated, and does it fail safely?*

That question looks different in each domain, but it's the same discipline:

- A variant caller that reports 95% confidence should be right 95% of the time — and should abstain when it can't be.
- A credit scorecard built by the first line should survive independent challenge from the second.
- A deployment that can't roll back in seconds isn't a deployment, it's a hope.

🌍 **Working remotely, available worldwide** · 🔎 **Open to opportunities** in data science, ML engineering, data engineering, and computational biology

---

## 🧬 Computational Biology & Genomics

Production bioinformatics pipelines and rigorous evaluation of the tools the field relies on.

| Project | What it does |
|---|---|
| **[biomarker-concordance-pipeline](https://github.com/gbadedata/biomarker-concordance-pipeline)** | Nextflow DSL2 germline variant calling on AWS, benchmarked against the GIAB HG001 truth set with clinical-grade VAF reproducibility statistics |
| **[clinvar-interpretation-benchmark](https://github.com/gbadedata/clinvar-interpretation-benchmark)** | Can a frontier LLM be trusted to classify germline variants? Scored against ClinVar expert consensus, with and without supplied ACMG evidence |
| **[variant-calling-calibration-benchmark](https://github.com/gbadedata/variant-calling-calibration-benchmark)** | Treats quality filtering as an abstention decision — stratified by genomic difficulty, with QUAL calibration measured, not assumed |
| **[bioagent](https://github.com/gbadedata/bioagent)** | Autonomous QC analyst built with LangGraph and Claude — pulls live pipeline metrics, reasons over them, searches PubMed, produces a clinical-grade report |
| **[squidpy-spatial-benchmark](https://github.com/gbadedata/squidpy-spatial-benchmark)** | Spatial transcriptomics on Visium mouse brain, showing persistent homology detects structure that Moran's I underestimates |

`Nextflow` `scanpy` `AnnData` `Bioconductor` `GIAB` `ClinVar` `VCF` `RNA-seq` `single-cell` `spatial transcriptomics`

<details>
<summary><b>More computational biology work</b> (12 repos)</summary>

<br>

**Pipelines & platforms** — [variantlens](https://github.com/gbadedata/variantlens) (VCF parsing, validation, annotation, REST API) · [ngs-results-explorer](https://github.com/gbadedata/ngs-results-explorer) (RNA-Seq differential expression with volcano-plot dashboard) · [bioseq-platform](https://github.com/gbadedata/bioseq-platform) (NCBI SRA ingestion into a multi-zone AWS data lake) · [genome-vault](https://github.com/gbadedata/genome-vault) (variant warehouse on BigQuery + Dataflow) · [genomicflow-platform](https://github.com/gbadedata/genomicflow-platform) (Pub/Sub streaming from sequencing instruments to Cloud Run) · [clinvar-variant-prioritisation-workflow](https://github.com/gbadedata/clinvar-variant-prioritisation-workflow) (inherited-disease variant ranking with transparent evidence rules)

**Benchmarks** — [sc-celltype-benchmark](https://github.com/gbadedata/sc-celltype-benchmark) (does the annotation pipeline recover true cell identities?) · [scvelo-trajectory-benchmark](https://github.com/gbadedata/scvelo-trajectory-benchmark) (RNA velocity on pancreatic endocrinogenesis) · [single-cell-marker-reasoning-benchmark](https://github.com/gbadedata/single-cell-marker-reasoning-benchmark) · [cellfatebench-single-cell-analysis](https://github.com/gbadedata/cellfatebench-single-cell-analysis) · [finemap-calibration-benchmark](https://github.com/gbadedata/finemap-calibration-benchmark) (does SuSiE's 95% credible set contain the causal variant 95% of the time?) · [ecm-target-discovery-pipeline](https://github.com/gbadedata/ecm-target-discovery-pipeline) (multi-omics ECM targets in pancreatic cancer)

</details>

---

## 📊 Data Science & Machine Learning

Modelling on real, messy, imbalanced data — where the interesting work is the decision the model supports, not the accuracy score. Mostly applied to credit risk and financial crime, because that's where the constraints bite hardest: rare positives, asymmetric costs, mandatory explainability, and regulators who ask how you got there.

| Project | What it does |
|---|---|
| **[credit-default-prediction](https://github.com/gbadedata/credit-default-prediction)** | Imbalance handled with PR-AUC and KS rather than accuracy, a cost-based approval threshold instead of a blind 0.5 cutoff, SHAP at portfolio and applicant level, demographics excluded for fair lending |
| **[affordability-default-risk](https://github.com/gbadedata/affordability-default-risk)** | A hypothesis tested head-on across 1.35M completed loans: affordability features alone out-predict a full credit bureau record |
| **[mule-network-detection](https://github.com/gbadedata/mule-network-detection)** | Feature engineering from graph structure — fan-in, fan-out, chains — because per-transaction scoring catches almost none of a sub-1% positive class |
| **[transaction-fraud-scoring](https://github.com/gbadedata/transaction-fraud-scoring)** | Calibrated scoring built around a real operational constraint: an investigation team can only review so many alerts a day |
| **[transaction-classification](https://github.com/gbadedata/transaction-classification)** | 259k noisy bank transaction strings into 31 categories — multi-class, imbalanced, messy text, taken to a production-style routing pipeline |
| **[bustout-detection](https://github.com/gbadedata/bustout-detection)** | Behavioural and trajectory features that catch a credit line cultivated to be drained, while there's still time to stop it |
| **[pd-scorecard-validation](https://github.com/gbadedata/pd-scorecard-validation)** | Builds a Weight-of-Evidence scorecard, then independently validates it — both halves, as they'd actually be split between first and second line |

Also: **[ifrs9-ecl-engine](https://github.com/gbadedata/ifrs9-ecl-engine)** (PD/LGD/EAD impairment modelling on 1.35M loans) · **[drug-review-nlp](https://github.com/gbadedata/drug-review-nlp)** (215k patient reviews) · **[airline-feedback-transformer](https://github.com/gbadedata/airline-feedback-transformer)** (transformer encoder from scratch in PyTorch) · a three-part [food-systems sustainability analysis](https://github.com/gbadedata/food-environmental-footprint)

`imbalanced learning` `cost-sensitive thresholds` `SHAP` `explainability` `feature engineering` `calibration` `XGBoost` `scikit-learn` `PyTorch` `NLP` `model validation` `fair lending`

<details>
<summary><b>More data science work</b> (7 repos)</summary>

<br>

**Fraud & risk** — [fuel-card-fraud-monitoring](https://github.com/gbadedata/fuel-card-fraud-monitoring) (fuel-aware rules plus a learned model, with a reason a person can read) · [credit-risk-monitoring](https://github.com/gbadedata/credit-risk-monitoring) (vintage performance, model drift, concentration, committee-ready MI pack)

**NLP & AI systems** — [biomedical-rag-qa](https://github.com/gbadedata/biomedical-rag-qa) (BM25 and dense FAISS retrieval over biomedical literature) · [mcp-research-agent](https://github.com/gbadedata/mcp-research-agent) (an MCP server and a standalone Claude agent from one toolset)

**Applied analytics** — [livestock-emission-intensity](https://github.com/gbadedata/livestock-emission-intensity) (a 70-fold spread in beef carbon intensity worldwide) · [meat-carbon-footprint](https://github.com/gbadedata/meat-carbon-footprint) (how the changing *mix* of demand drives emissions) · [Predictive-Modelling-for-Agriculture](https://github.com/gbadedata/Predictive-Modelling-for-Agriculture-Using-Machine-Learning) (crop selection from soil chemistry) · [TfL-Journey-Analysis-and-Prediction](https://github.com/gbadedata/TfL-Journey-Analysis-and-Prediction) (predicting London network journey volumes, 2010–2022)

</details>

---

## ☁️ Cloud, DevOps & Data Engineering

Infrastructure as code, zero-downtime delivery, and pipelines built to be operated rather than demoed.

| Project | What it does |
|---|---|
| **[enterprise-progressive-delivery-eks](https://github.com/gbadedata/enterprise-progressive-delivery-eks)** | Argo Rollouts canary releases on AWS EKS with automatic rollback, container security scanning, and Terraform-provisioned infrastructure |
| **[mediflow](https://github.com/gbadedata/mediflow)** | Production-grade Azure platform for clinical data ingestion — AKS, Key Vault, Terraform, Helm, through a three-stage Azure DevOps pipeline |
| **[zero-downtime-bluegreen-eks](https://github.com/gbadedata/zero-downtime-bluegreen-eks)** | Blue-green on EKS with instant traffic switching and sub-5-second rollback |
| **[aws-supplyshield-lakehouse](https://github.com/gbadedata/aws-supplyshield-lakehouse)** | Retail supply-chain lakehouse on AWS consolidating orders, inventory, and supplier shipments |
| **[clintrial-stream](https://github.com/gbadedata/clintrial-stream)** | Real-time clinical trial event streaming — Kinesis, DynamoDB, sub-second latency, regulatory-grade audit trails |
| **[commerce-elt-platform](https://github.com/gbadedata/commerce-elt-platform)** | Snowflake ELT platform with dbt, S3, Snowpipe, and CI-enforced transformations |

`Terraform` `Kubernetes` `Docker` `AWS` `Azure` `GCP` `Argo Rollouts` `Helm` `Airflow` `dbt` `Snowflake` `Kafka` `Prometheus` `Grafana` `GitHub Actions`

<details>
<summary><b>More cloud & engineering work</b> (15 repos)</summary>

<br>

**Deployment & delivery** — [ecommerce-blue-green-aks](https://github.com/gbadedata/ecommerce-blue-green-aks) (NestJS API, local to AKS) · [shopswift-blue-green](https://github.com/gbadedata/shopswift-blue-green) (Minikube to EKS with Prometheus/Grafana) · [swiftdeploy](https://github.com/gbadedata/swiftdeploy) (declarative CLI turning one manifest into a running stack, with OPA policy enforcement) · [hng14-stage3](https://github.com/gbadedata/hng14-stage3) (real-time DDoS detection daemon that blocks via iptables)

**Infrastructure as code** — [terraform-aws-web-server](https://github.com/gbadedata/terraform-aws-web-server) (a whole AWS network stack from one command) · [azure-arm-linux-vm-iac](https://github.com/gbadedata/azure-arm-linux-vm-iac) · [secure-nginx-linux-server](https://github.com/gbadedata/secure-nginx-linux-server) (SSH hardening, UFW, Let's Encrypt on EC2) · [azure-web-deployment-project](https://github.com/gbadedata/azure-web-deployment-project) (IaaS vs PaaS compared) · [webapp-azure-demo](https://github.com/gbadedata/webapp-azure-demo)

**MLOps & pipelines** — [ml_inference_api](https://github.com/gbadedata/ml_inference_api) (notebook to deployed API with monitoring and Kubernetes) · [ml-training-pipeline-ci](https://github.com/gbadedata/ml-training-pipeline-ci) · [tfl-cycle-pipeline](https://github.com/gbadedata/tfl-cycle-pipeline) (TfL BikePoint to dbt dimensional model via Airflow) · [engineering-workflow-automation](https://github.com/gbadedata/engineering-workflow-automation) (CI and Trello enforcing process over individual discipline) · [governed-semantic-model-api](https://github.com/gbadedata/governed-semantic-model-api) (Fabric/Power BI metrics served through AWS) · [stage1-personal-api](https://github.com/gbadedata/stage1-personal-api)

</details>

---

## 📋 Data Operations & Business Systems

Analyst-side work: SQL exception reporting, ERP data integrity, and the unglamorous process improvement that keeps operational data trustworthy.

| Project | What it does |
|---|---|
| **[sap-process-improvement-project](https://github.com/gbadedata/sap-process-improvement-project)** | 720 SAP orders audited over six weeks, four discrepancy types traced to root cause, error rate cut from 27.8% to under 2% |
| **[sap-order-management-project](https://github.com/gbadedata/sap-order-management-project)** | Full SAP SD order lifecycle on 200 B2B orders — pricing validated against condition records, error rate taken to 0% |
| **[Project-Asset-Ops-Reporting](https://github.com/gbadedata/Project-Asset-Ops-Reporting)** | Operational reporting over energy meter assets — SQLite, SQL views, Power BI dashboard with exception reporting |
| **[Project-Asset-Lifecycle-Monitoring](https://github.com/gbadedata/Project-Asset-Lifecycle-Monitoring)** | Rule-based anomaly escalation producing a pack with row-level evidence and severity classification |
| **[dataops-asset-data-integrity](https://github.com/gbadedata/dataops-asset-data-integrity)** | Reproducible SQL validation checks producing an auditable exception report |
| **[Project---Data-Pipeline-Improvement](https://github.com/gbadedata/Project---Data-Pipeline-Improvement)** | A manual reporting process redesigned for reliability, traceability, and reduced manual effort |

`SQL` `SQLite` `Power BI` `SAP SD` `Excel` `exception reporting` `data governance` `root cause analysis`


<details>
<summary><b>Earlier academic work</b> — MSc, University of Essex</summary>

<br>

[Street-level Crime & Climate Data, Colchester 2023](https://github.com/gbadedata/Street-level-Crime-Incidents-and-Daily-Climate-Data-in-Colchester-year-2023) (EDA and visualisation in R) · [MA334 Individual Project](https://github.com/gbadedata/MA334_Individual_Project) (proportional species richness) · [Modelling Experimental & Observational Data](https://github.com/gbadedata/Modelling-Experimental-and-Observational-Data-FEV.csv-and-BreatCancer-) (hypothesis testing, logistic regression, random forest, chi-square) · [Python-Project](https://github.com/gbadedata/Python-Project) (CE156 introductory programming)

</details>

---

## 🛠 Toolkit

**Languages** — Python · SQL · R · Bash · HCL

**Data & ML** — pandas · scikit-learn · PyTorch · XGBoost · SHAP · dbt · Airflow · Spark · DuckDB

**Cloud** — AWS · Azure · GCP · Terraform · Kubernetes · Docker

**AI systems** — LangGraph · MCP · RAG · LLM evaluation

**Practice** — CI/CD · testing · reproducibility · model validation · IaC

---

## 📫 Get in touch

- 🌐 [gbadedata.com](https://gbadedata.com) — built with React + Vite on AWS Amplify ([source](https://github.com/gbadedata/gbadedata-web))
- 💼 [LinkedIn](https://www.linkedin.com/in/oluwagbade-odimayo-)
- ✉️ [oluwagbadeodimayo@gmail.com](mailto:oluwagbadeodimayo@gmail.com)
