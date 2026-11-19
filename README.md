# Hi, I'm Oluwagbade Odimayo (OJ) 👋

**Data Scientist · Data Engineer · ML Engineer.** I build the pipelines, the models and the systems that serve them, and test each one before it's trusted.

I came to data from the lab, with an MSc in Plant Genetics and Molecular Biology (Ibadan) and then an MSc in Applied Data Science (Essex). Biology taught me that a result is only as good as the evidence behind it. So my engineering leans on validation, provenance and testing, and my recent repos say plainly what has been checked and what hasn't. I've also worked as a domain-expert AI evaluator and reviewer, grading model outputs against expert rubrics and quality-checking other evaluators' assessments.

The question running through all of it decides whether a system can be trusted in production: *is it correct, is it validated, and does it fail safely?*

- A pipeline that completed successfully hasn't proven the data is right. Schemas, volumes, freshness and reconciliation still have to be tested.
- A deployment that can't roll back in seconds isn't a deployment. It's a hope.
- A model reporting 95% confidence should be right 95% of the time, and should abstain when it can't be.

📍 **Based in the UK** · open to data science, data engineering, ML engineering, analytics and bioinformatics roles<br>
🔗 **[gbadedata.com](https://gbadedata.com)** for case studies, architecture and engineering evidence

---

## 🚀 Start here

If you only open three repos, open these.

| Project | What it shows |
|---|---|
| **[genome-vault](https://github.com/gbadedata/genome-vault)**<br><sub>Data engineering on real genomic data</sub> | All of chromosome 22 from the 1000 Genomes 30x cohort (1.07M variants, 3,202 people, 207.5M genotypes) in a BigQuery star schema built with dbt, joined to ClinVar, Ensembl, gnomAD and Genome in a Bottle. 69 of 69 dbt models and tests pass on BigQuery, every allele count is recomputed and checked against the source, and a [read-only API](https://genome-vault-api-guovahumxq-nw.a.run.app/docs) is live on Cloud Run. No synthetic data anywhere. |
| **[nhs-access-equity-lab](https://github.com/gbadedata/nhs-access-equity-lab)**<br><sub>Analytics written for the person who has to act</sub> | 150.3 million NHS outpatient appointments (2025-26) broken down by age, deprivation and ethnicity, and reconciled to published totals. Hospitals cancelled 1.7 times as many appointments as patients missed, and while plain statistics flag 144 of 151 trusts as outliers, comparing like with like leaves only 3. [Live report](https://gbadedata.github.io/nhs-access-equity-lab/). |
| **[clinvar-interpretation-benchmark](https://github.com/gbadedata/clinvar-interpretation-benchmark)**<br><sub>LLM evaluation</sub> | Can a frontier LLM be trusted to classify germline variants? Scored against ClinVar's expert consensus, with and without supplied ACMG evidence, it made zero confident errors across 200 interpretations of 100 real variants. When the evidence ran short, it abstained instead of guessing. |

---

## 🎯 Is the confidence honest?

One question applied to four very different models: when a model says it is 95% sure, is it right 95% of the time, and does it abstain when it can't be? Accuracy alone can't answer that.

| Project | Model under test | What it found |
|---|---|---|
| **[imputation-calibration-benchmark](https://github.com/gbadedata/imputation-calibration-benchmark)** | Beagle genotype imputation, 1000 Genomes chr20 | Calibration error rises about 8-fold (ECE 0.026 to 0.205) when the reference panel's ancestry doesn't match the cohort, and an abstention rule tuned on the matched panel stops protecting the mismatched one |
| **[finemap-calibration-benchmark](https://github.com/gbadedata/finemap-calibration-benchmark)** | SuSiE statistical fine-mapping, by simulation | 95% credible sets contain the causal variant 98.7-100% of the time, and SuSiE keeps that promise by abstaining: on up to 85% of loci in the lowest-power setting |
| **[variant-calling-calibration-benchmark](https://github.com/gbadedata/variant-calling-calibration-benchmark)** | Variant caller QUAL scores | A framework that scores calls against GIAB, stratifies by genomic difficulty, measures QUAL calibration and treats filtering as an abstention decision. Validated on a synthetic caller with planted miscalibration, so every layer has a known signal to find |
| **[clinvar-interpretation-benchmark](https://github.com/gbadedata/clinvar-interpretation-benchmark)** | Frontier LLM on clinical variants | Zero confident errors in 200 interpretations, with safe abstention scored separately from dangerous error (see Start here) |

`calibration` `abstention` `expected calibration error` `bootstrap CIs` `GIAB` `ClinVar` `1000 Genomes` `Beagle` `plink2` `SuSiE` `LLM evaluation`

---

## ☁️ Data engineering & cloud

Pipelines built to be operated, not demoed: data contracts, quality gates, idempotent loads, alerting and runbooks. Each one states whether its data is real or synthetic.

| Project | What it does |
|---|---|
| **[azure-adf-dbt-warehouse](https://github.com/gbadedata/azure-adf-dbt-warehouse)** | Data Factory loads a CRM API and CSV exports into Azure SQL, and dbt builds separate dev and prod marts, with Terraform, managed identities and Azure Monitor alerts throughout. Deployed to Azure and tested end to end, including late-arriving rows and a deliberately broken file that raised an alert within 3 to 7 minutes. Synthetic charity data |
| **[ecb-market-data-pipeline](https://github.com/gbadedata/ecb-market-data-pipeline)** | C# / .NET 8 ingestion of the ECB's daily FX reference rates against an explicit data contract, with SHA-256 provenance for every source payload, idempotent atomic writes and a scheduled run every weekday on GitHub Actions |
| **[urbanflow-ml](https://github.com/gbadedata/urbanflow-ml)** | 103.5M NYC taxi trip records taken through validation and leakage-controlled features to a deployed forecasting API with prediction intervals. On a frozen eight-week test block, gradient boosting cuts Poisson deviance by 55% against an hour-of-week baseline |
| **[dockerfile-data-validation](https://github.com/gbadedata/dockerfile-data-validation)** | A Docker build that refuses to produce an image unless the dataset, schema and model pass validation, labels every image with its contents by hash, and fails CI on any fixable HIGH or CRITICAL Trivy finding |
| **[commerce-elt-platform](https://github.com/gbadedata/commerce-elt-platform)** | Snowflake ELT loading from S3 external stages, modelled with dbt and run through GitHub Actions, where the same data-quality rules find the same rows on Snowflake and on DuckDB. Synthetic data with defects planted on purpose |
| **[genomicflow-platform](https://github.com/gbadedata/genomicflow-platform)** | Streaming on GCP from Pub/Sub through Cloud Run to BigQuery, with dead-lettering and a rejected-records table so failures stay visible. Terraform-provisioned and verified on GCP against simulated sequencing instruments |

**Platform & delivery**

| Project | What it does |
|---|---|
| **[enterprise-progressive-delivery-eks](https://github.com/gbadedata/enterprise-progressive-delivery-eks)** | Argo Rollouts canary releases on AWS EKS, promoted or rolled back on Prometheus analysis, with Trivy image scanning, Checkov-hardened Terraform and a private self-hosted runner |
| **[mediflow](https://github.com/gbadedata/mediflow)** | Azure deployment platform with AKS, ACR, Key Vault, Helm, Prometheus and Grafana, provisioned with Terraform and shipped through a three-stage Azure DevOps pipeline |
| **[zero-downtime-bluegreen-eks](https://github.com/gbadedata/zero-downtime-bluegreen-eks)** | Blue-green releases on AWS EKS with an instant traffic switch and automated rollback when errors spike |

`dbt` `BigQuery` `Snowflake` `Azure SQL` `Data Factory` `DuckDB` `PostgreSQL` `C# / .NET` `Terraform` `Docker` `Kubernetes` `Argo Rollouts` `Helm` `Prometheus` `Grafana` `GitHub Actions` `Azure DevOps`

<details>
<summary><b>More data, cloud & MLOps work</b> (14 repos)</summary>

<br>

**Data platforms** · [bioseq-platform](https://github.com/gbadedata/bioseq-platform) (NCBI SRA ingestion into an S3 data lake with Glue, Athena and a PostgreSQL star schema) · [clintrial-stream](https://github.com/gbadedata/clintrial-stream) (clinical-trial event streaming with Kinesis and DynamoDB, on synthetic events) · [governed-semantic-model-api](https://github.com/gbadedata/governed-semantic-model-api) (Fabric / Power BI semantic-model metrics served through Lambda behind an IAM-authorised API Gateway)

**Deployment & delivery** · [ecommerce-blue-green-aks](https://github.com/gbadedata/ecommerce-blue-green-aks) (NestJS API from Minikube to AKS) · [shopswift-blue-green](https://github.com/gbadedata/shopswift-blue-green) (Minikube to EKS with Prometheus and Grafana) · [swiftdeploy](https://github.com/gbadedata/swiftdeploy) (declarative CLI turning one manifest into a running stack, with OPA policy checks) · [hng14-stage3](https://github.com/gbadedata/hng14-stage3) (real-time DDoS detection daemon that blocks via iptables)

**Infrastructure as code** · [terraform-aws-web-server](https://github.com/gbadedata/terraform-aws-web-server) (a whole AWS network stack from one command) · [secure-nginx-linux-server](https://github.com/gbadedata/secure-nginx-linux-server) (SSH hardening, UFW and Let's Encrypt on EC2) · [azure-arm-linux-vm-iac](https://github.com/gbadedata/azure-arm-linux-vm-iac) · [azure-web-deployment-project](https://github.com/gbadedata/azure-web-deployment-project) (IaaS vs PaaS compared)

**MLOps & workflow** · [ml_inference_api](https://github.com/gbadedata/ml_inference_api) (notebook to deployed API with monitoring and Kubernetes) · [ml-training-pipeline-ci](https://github.com/gbadedata/ml-training-pipeline-ci) · [engineering-workflow-automation](https://github.com/gbadedata/engineering-workflow-automation) (CI and Trello enforcing process rather than individual discipline)

</details>

---

## 🧬 Bioinformatics & health data

Reproducible pipelines on real reference data, with a clear line between computational evidence and biological interpretation.

| Project | What it does |
|---|---|
| **[nhs-fhir-quality-gateway](https://github.com/gbadedata/nhs-fhir-quality-gateway)** | Two-layer FHIR R4 validation run on every GP practice in England from the NHS ODS register: 6,162 active practices mapped to UK Core with 0 errors from the official HL7 validator, plus business rules that caught 4 of 4 planted defects where the validator alone caught 1. [Live report](https://gbadedata.github.io/nhs-fhir-quality-gateway/) |
| **[biomarker-concordance-pipeline](https://github.com/gbadedata/biomarker-concordance-pipeline)** | Nextflow DSL2 germline variant calling on AWS Batch, benchmarked with hap.py against the GIAB HG001 v4.2.1 truth set, with run-over-run reproducibility statistics |
| **[ecm-target-discovery-pipeline](https://github.com/gbadedata/ecm-target-discovery-pipeline)** | Provenance-preserving workflow combining CPTAC pancreatic cancer transcriptomics and proteomics to prioritise extracellular-matrix targets |
| **[bioagent](https://github.com/gbadedata/bioagent)** | LangGraph and Claude agent that pulls live QC metrics from the concordance pipeline's API, searches PubMed when the findings call for it, and writes a structured quality report |
| **[plant-read-placement](https://github.com/gbadedata/plant-read-placement)** *(in progress)* | Adapting the PlantCaduceus DNA language model to place noisy Nanopore reads from unsequenced plants, benchmarked against minimap2 and a k-mer baseline, with targets frozen before the test split is scored |

`Nextflow` `nf-core` `nf-test` `GIAB` `hap.py` `scanpy` `squidpy` `scVelo` `Bioconductor` `FHIR R4` `UK Core` `RNA-seq` `single-cell` `spatial transcriptomics`

<details>
<summary><b>More bioinformatics work</b> (8 repos)</summary>

<br>

**Pipelines & tools** · [variantlens](https://github.com/gbadedata/variantlens) (VCF parsing, validation, annotation and a REST API) · [ngs-results-explorer](https://github.com/gbadedata/ngs-results-explorer) (RNA-seq differential expression with a volcano-plot dashboard) · [clinvar-variant-prioritisation-workflow](https://github.com/gbadedata/clinvar-variant-prioritisation-workflow) (inherited-disease variant ranking with transparent evidence rules)

**Benchmarks** · [squidpy-spatial-benchmark](https://github.com/gbadedata/squidpy-spatial-benchmark) (persistent homology vs Moran's I on Visium) · [scvelo-trajectory-benchmark](https://github.com/gbadedata/scvelo-trajectory-benchmark) (RNA velocity on pancreatic endocrinogenesis) · [sc-celltype-benchmark](https://github.com/gbadedata/sc-celltype-benchmark) · [single-cell-marker-reasoning-benchmark](https://github.com/gbadedata/single-cell-marker-reasoning-benchmark) · [cellfatebench-single-cell-analysis](https://github.com/gbadedata/cellfatebench-single-cell-analysis)

</details>

---

## 🤖 AI systems & applied ML

The work is the decision a model supports, not its accuracy score: rare positives, asymmetric costs, explanations a reviewer can check, and evaluation on data the model hasn't seen.

| Project | What it does |
|---|---|
| **[mcp-research-agent](https://github.com/gbadedata/mcp-research-agent)** | One toolset served three ways (an MCP server any client can plug into, an autonomous Claude agent and a read-only dashboard) so they can't drift apart. Tested end to end without an API key using a scripted model |
| **[biomedical-rag-qa](https://github.com/gbadedata/biomedical-rag-qa)** | Retrieval-augmented QA over PubMed abstracts, benchmarked on 1,000 PubMedQA questions: BM25 ranks a supporting passage first 94.3% of the time and beats dense FAISS retrieval on every metric |
| **[transaction-classification](https://github.com/gbadedata/transaction-classification)** | 259k real bank transactions sorted into 31 categories and tested on unseen customers as well as a random split. The most confident 80% stays at 96.7% accuracy for new customers, while macro-F1 falls from 0.80 to 0.65, a gap the random split hides |
| **[ifrs9-ecl-engine](https://github.com/gbadedata/ifrs9-ecl-engine)** | IFRS 9 expected credit loss on 1.35M real Lending Club loans: PD, LGD, EAD, three-stage staging and probability-weighted macroeconomic scenarios |
| **[pd-scorecard-validation](https://github.com/gbadedata/pd-scorecard-validation)** | A Weight-of-Evidence PD scorecard, then an independent validation of it (discrimination, calibration, PSI stability, challenger models), split the way first and second line would split it |
| **[credit-default-prediction](https://github.com/gbadedata/credit-default-prediction)** | 30k real card customers: PR-AUC and KS rather than accuracy, a cost-based approval threshold, SHAP explanations and fair-lending feature exclusions |
| **[transaction-fraud-scoring](https://github.com/gbadedata/transaction-fraud-scoring)** | Fraud scoring built around a fixed daily review budget: a calibrated model, rules and an anomaly layer ranked by expected loss, with drift monitoring. Runs on synthetic data and on the real IEEE-CIS dataset |
| **[mule-network-detection](https://github.com/gbadedata/mule-network-detection)** | Graph features (fan-in, fan-out, chains) for money-mule detection, with recall reported per laundering typology, on IBM's public synthetic AML data |

Also: **[airline-feedback-transformer](https://github.com/gbadedata/airline-feedback-transformer)** (a transformer encoder written from scratch in PyTorch, held to the same evaluation as classical baselines on ~14,600 real airline tweets) · **[drug-review-nlp](https://github.com/gbadedata/drug-review-nlp)** (~215k patient drug reviews, 0.95 ROC-AUC) · **[affordability-default-risk](https://github.com/gbadedata/affordability-default-risk)** · **[credit-risk-monitoring](https://github.com/gbadedata/credit-risk-monitoring)** · **[bustout-detection](https://github.com/gbadedata/bustout-detection)** and **[fuel-card-fraud-monitoring](https://github.com/gbadedata/fuel-card-fraud-monitoring)** (both on synthetic data, as each README states)

`LangGraph` `MCP` `RAG` `BM25` `FAISS` `PyTorch` `scikit-learn` `XGBoost` `SHAP` `calibration` `imbalanced learning` `cost-sensitive thresholds` `model validation` `fair lending`

---

## 📊 Analytics

Analysis that ends in something a manager can use: a recommendation, an Excel pack, a number reconciled to the source.

| Project | What it does |
|---|---|
| **[retail-customer-segmentation](https://github.com/gbadedata/retail-customer-segmentation)** | 1.07M invoice lines from a UK online retailer, reconciled to the penny after finding 22,523 double-counted rows. Segments are built on one date and judged on what customers did next: Champions and Loyal are 37.8% of customers and 82.5% of next-period spend. Delivered as an Excel segment pack |
| **[b2b-lead-funnel-analytics](https://github.com/gbadedata/b2b-lead-funnel-analytics)** | A real B2B funnel: 8,000 Olist leads, 842 closed deals and what those customers ordered next. Conversion by source with confidence intervals, time to close, a time-split lead score and a formula-driven Excel dashboard |

Also: sustainability analyses on FAOSTAT and supply-chain data · [livestock-emission-intensity](https://github.com/gbadedata/livestock-emission-intensity) · [food-environmental-footprint](https://github.com/gbadedata/food-environmental-footprint) · [meat-carbon-footprint](https://github.com/gbadedata/meat-carbon-footprint)

`SQL` `pandas` `statsmodels` `scikit-learn` `RFM` `BG/NBD` `funnel analysis` `Excel` `Power BI`

---

## 🌐 Open-source contributions

Code reviewed and merged by the maintainers of projects I don't run.

| Project | Contribution | Status |
|---|---|---|
| **[nf-core/modules](https://github.com/nf-core/modules/pull/12018)** | Corrected three FreeBayes nf-tests that ran on human data but were labelled `sarscov2`, updated their snapshot keys, added missing EDAM ontology entries and fixed the stub gzip syntax that module lint required. Closes [#7766](https://github.com/nf-core/modules/issues/7766) | ✅ Merged |
| **[Meltano](https://github.com/meltano/meltano/pulls?q=is%3Apr+author%3Agbadedata+is%3Amerged)** | Three PRs: colour output switched off when stderr isn't a TTY, so redirected logs stay clean ([#10118](https://github.com/meltano/meltano/pull/10118)); `FORCE_COLOR` support with `NO_COLOR` keeping precedence ([#10139](https://github.com/meltano/meltano/pull/10139)); and `--refresh-catalog` for `meltano invoke` ([#10181](https://github.com/meltano/meltano/pull/10181)) | ✅ Merged |

---

## 🧪 Certifications

[![DP-700](https://img.shields.io/badge/Microsoft-DP--700_Fabric_Data_Engineer-0078D4?style=flat-square&logo=microsoft)](https://learn.microsoft.com/en-gb/users/OluwagbadeOdimayo-8921/credentials/ABE9871D1917291F)
[![DP-600](https://img.shields.io/badge/Microsoft-DP--600_Fabric_Analytics_Engineer-0078D4?style=flat-square&logo=microsoft)](https://learn.microsoft.com/en-gb/users/oluwagbadeodimayo-8921/credentials/36ab7c802fb7da99)
![DP-750](https://img.shields.io/badge/Microsoft-DP--750_Azure_Databricks_Data_Engineer-0078D4?style=flat-square&logo=microsoft)

**Microsoft Certified:** Fabric Data Engineer Associate (DP-700) · Fabric Analytics Engineer Associate (DP-600) · Azure Databricks Data Engineer Associate (DP-750)

---

## 📚 Research & writing

- **Publications** · seven papers and preprints on [ResearchGate](https://www.researchgate.net/profile/Oluwagbade-Odimayo-2), spanning plant genetics, in-silico drug discovery, deep learning for network attack detection and LLMs in education
- **Writing** · [Hashnode](https://gbadedata.hashnode.dev) for build logs on what broke and why · [dev.to](https://dev.to/gbadedata) on fraud, genomics and evaluation · [Medium](https://medium.com/@gbadedata)

---

## 🛠 Toolkit

**Languages** · Python · SQL · R · C# · Bash · HCL

**Data** · dbt · BigQuery · Snowflake · Azure SQL · Data Factory · Microsoft Fabric · Power BI · DuckDB · PostgreSQL · pandas

**ML & AI** · scikit-learn · XGBoost · PyTorch · statsmodels · SHAP · LangGraph · MCP · RAG · LLM evaluation

**Cloud & platform** · AWS · Azure · GCP · Terraform · Docker · Kubernetes · Helm · Argo Rollouts · Prometheus · Grafana · GitHub Actions · Azure DevOps

**Bioinformatics** · Nextflow · nf-core · nf-test · scanpy · Bioconductor · plink2 · Beagle · SuSiE · FHIR

**Practice** · data contracts · testing in CI · calibration · provenance · runbooks · infrastructure as code

---

## 📫 Get in touch

- 🌐 **[gbadedata.com](https://gbadedata.com)** for case studies, architecture diagrams and engineering evidence
- 💼 [LinkedIn](https://www.linkedin.com/in/oluwagbade-odimayo-)
- ✉️ [o.odimayo@gbadedata.com](mailto:o.odimayo@gbadedata.com)
