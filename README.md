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

---

## 🛠 Toolkit

**Languages** — Python · SQL · R · Bash · HCL

**Data & ML** — pandas · scikit-learn · PyTorch · XGBoost · SHAP · dbt · Airflow · Spark · DuckDB

**Cloud** — AWS · Azure · GCP · Terraform · Kubernetes · Docker

**AI systems** — LangGraph · MCP · RAG · LLM evaluation

**Practice** — CI/CD · testing · reproducibility · model validation · IaC

---

## 📫 Get in touch

- 🌐 [gbadedata.com](https://gbadedata.com)
- 💼 [LinkedIn](https://www.linkedin.com/in/oluwagbade-odimayo-)
- ✉️ [oluwagbadeodimayo@gmail.com](mailto:oluwagbadeodimayo@gmail.com)
