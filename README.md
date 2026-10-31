# Awesome-Cloud-Machine-Learning-Platform

# Awesome-Cloud-Machine-Learning-Platform

**Top Cloud Machine Learning Platform (Opensource) 🌟 Star if you like it! 🌟**



**Curated List of SaaS Products & Open-Source GitHub Projects**

*Focused on MLOps, AutoML, Experiment Tracking, Model Serving & Self-Hosted ML Infrastructure*

**Last updated: October 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **Cloud Machine Learning Platforms**. These tools enable organizations to build, train, deploy, and monitor machine learning models at scale—from fully managed cloud ML platforms with integrated governance and GenAI tooling to open-source frameworks and self-hosted platforms that give teams complete control over their ML lifecycle and artifacts.



**Examples** include AWS SageMaker, Google Cloud Vertex AI, Azure Machine Learning, Databricks Mosaic AI, Snowflake ML, DataRobot, H2O.ai, Dataiku, Weights & Biases, and Domino Data Lab (the category leaders in commercial space).



**Open-source emphasis**: This section is expanded with every relevant project for self-hosted ML platforms, MLOps tooling, and open experiment tracking infrastructure. **Critical note**: The open-source ML landscape is deeply fragmented by function—**MLflow** dominates experiment tracking and model registry, **PyCaret** is emerging as a credible self-hosted AutoML platform , and **Evidently** leads open-source model monitoring . No single open-source project matches SageMaker's end-to-end lifecycle coverage or Vertex AI's Gemini-first GenAI integration, but a composed stack covers most ML engineering needs.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [Sector Overview & Market Dynamics](#sector-overview--market-dynamics)
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## Sector Overview & Market Dynamics

The global Cloud Machine Learning Platform market is estimated between **$114B and $135B in 2026** (scaling from ~$89B in 2025 at a ~30% CAGR), accelerated by widespread enterprise deployment of foundation models, agentic workflows, and cloud-scale GPU clusters.
The sector exhibits a **barbell concentration dynamic**: foundational compute infrastructure and managed core services are highly consolidated among the top 3 hyperscalers (AWS, Microsoft Azure, Google Cloud), whereas the upper MLOps tooling, lakehouse data management, visual AutoML, and model observability layers remain **moderately fragmented** among specialized commercial vendors (Databricks, Snowflake, Dataiku, W&B) and rapidly emerging modular open-source stacks.

## SaaS/Hosted Platforms

| Platform | Company Scale (Valuation / Market Cap / Revenue) | Description & Key Strengths | Pricing (Starting Tier) | Free Tier / Trial Limits | Best For |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **[Microsoft Azure Machine Learning](https://azure.microsoft.com/en-us/products/machine-learning)** | **~$3.1T** Market Cap (Microsoft) | Enterprise ML platform featuring comprehensive governance via Azure Policy, automated compliance (ISO, SOC, HIPAA, GDPR), ML Studio visual pipelines, and AKS cluster deployment. | Pay-as-you-go compute infrastructure only ($0 platform fee; compute starts at ~$0.04/hr for `Standard_B2s` / ~$0.29/hr for `Standard_DS3_v2`). | **$200 credit for 30 days** on sign-up; plus 12 months access to select free services (capped at 4 vCPUs quota on trial accounts). | Microsoft-centric enterprises needing rigid governance and automated Azure DevOps integration. |
| **[Google Cloud Vertex AI](https://cloud.google.com/vertex-ai)** | **~$2.1T** Market Cap (Alphabet) | Unified ML and GenAI platform optimized for Gemini foundation models; Vertex Pipelines (Kubeflow-based), Model Garden, and native AutoML. | Pay-as-you-go by resource consumption (e.g., custom training from ~$0.056/node-hr; Gemini 1.5 Flash text output from ~$0.30 per 1M tokens; online prediction from ~$0.05/node-hr). | **$300 credit for 90 days** across Google Cloud (no always-free compute tier for Vertex AI endpoints; charges incur once credits expire). | GCP-native organizations building GenAI products on Gemini and foundation model workflows. |
| **[AWS SageMaker](https://aws.amazon.com/sagemaker/)** | **~$2.0T** Market Cap (Amazon) | Comprehensive end-to-end managed ML platform covering data labeling, pipelines, training, Model Registry, Clarify governance, and Bedrock/JumpStart integration. | Pay-as-you-go based on compute/storage (e.g., `ml.t3.medium` notebooks from ~$0.05/hr; serverless inference from $0.00002/sec). | **2-month (60-day) Free Tier**: 250 hrs/mo `ml.t3.medium` notebooks, 50 hrs/mo `m4/m5.xlarge` training, 125 hrs/mo `m4/m5.xlarge` inference, and 150K serverless inference seconds. | AWS-native organizations requiring complete lifecycle governance and large-scale model deployments. |
| **[Databricks Mosaic AI](https://www.databricks.com/product/machine-learning)** | **$190B** Valuation (Series L/M 2026; ~$7B ARR) | Lakehouse ML platform unifying data pipelines and ML; MLflow 3.0, Unity Catalog governance, high-throughput model serving, and Mosaic AI custom fine-tuning. | Pay-as-you-go consumption based on DBUs (Jobs compute from ~$0.15/DBU; All-Purpose / Model Serving compute from ~$0.55/DBU). | **Free Edition (perpetual)**: Serverless compute, 1 `2X-Small` SQL warehouse, up to 5 concurrent tasks, 3 apps (subject to daily fair usage caps); or **14-day evaluation trial** with **$400 in DBUs**. | Code-first data science and ML engineering teams committed to open lakehouse formats and MLflow. |
| **[Snowflake ML](https://www.snowflake.com/en/product/features/machine-learning/)** | **~$50B** Market Cap (~$3.6B ARR) | In-database ML capabilities on the AI Data Cloud; Snowpark for Python, Native Model Registry, Snowpark Container Services (SPCS) for GPUs, and Cortex AI SQL functions. | Pay-as-you-go consumption based on Snowflake credits (Standard Edition starts at **$2.00 per credit**; Enterprise Edition at **$3.00 per credit**). | **30-day Free Trial with $400 in usage credits** (no credit card required; access expires when credits are depleted or 30 days elapse). | Snowflake-centric teams seeking to train and query ML/GenAI models directly inside the warehouse boundary. |
| **[Dataiku](https://www.dataiku.com/)** | **$3.7B** Valuation (~$350M ARR) | Everyday AI platform designed for collaborative data science, visual drag-and-drop ML recipes, AutoML, code notebooks, and LLM Mesh routing. | Annual enterprise subscription; entry-tier business plans start at approximately **$4,000/month** (~$48,000/yr). | **Free Edition (perpetual)**: Self-hosted on local hardware for up to **3 users**; or a **14-day fully-managed cloud trial** with 4 CPUs / 32 GiB RAM provisioned. | Cross-functional teams pairing citizen data scientists with technical coders in a visual collaborative workspace. |
| **[Weights & Biases](https://wandb.ai/)** | **$1.7B** Valuation / Acquired by CoreWeave | Specialized MLOps platform for experiment tracking, hyperparameter tuning (Sweeps), model registry, and LLM observability (Weave). | Team/Pro tier starts at **$50 to $60/user/month** (billed monthly); custom pricing for Enterprise. | **Free Forever Personal Tier**: 1 user, up to 5 model seats, **5 GB cloud storage/month**, 1 GB Weave tracing/month, capped at 50 requests/min. | Researchers and ML engineering teams wanting dedicated experiment tracking and deep training visualization. |
| **[H2O.ai](https://h2o.ai/)** | **$1.7B** Valuation (~$75M ARR) | Enterprise automated ML platform featuring H2O Driverless AI, automated feature engineering, model explainability, and open-source H2O-3 core. | Annual enterprise license starting at approximately **$100,000 to $130,000/year** (or custom private offers on AWS/Azure Marketplace). | **21-day Free Trial License** for self-hosted or cloud evaluation of Driverless AI; or **2-hour interactive test drive** on H2O Aquarium cloud. | Enterprise predictive modeling teams prioritizing automated tabular modeling, compliance, and explainable AI. |
| **[DataRobot](https://www.datarobot.com/)** | **$500M - $1B** Implied Valuation (~$285M ARR) | Enterprise AI platform specializing in automated machine learning (AutoML), GenAI playgrounds, and model governance/deployment automation. | Enterprise annual contracts starting at approximately **$24,000 to $50,000/year** for entry-level team scopes (median contracts ~$212,000/year). | **30-day Free Trial**: Shared modeling workers, batch predictions, up to 15 vector databases, and 1,000 LLM calls (no dedicated GPUs; no credit card required). | Organizations wanting automated end-to-end ML model creation and compliance guardrails without extensive custom code. |
| **[Domino Data Lab](https://www.dominodatalab.com/)** | **$500M - $1B** Valuation (~$35M - $45M ARR) | Regulated enterprise MLOps platform offering hybrid/multi-cloud orchestration, reproducible project environments, and governed model deployment. | Custom enterprise quotes; entry commitments typically start in the **$30,000 to $50,000/year** range depending on user seats and VPC tier. | **14-day guided enterprise PoC / evaluation trial** upon sales request (or 2-week lab access via NVIDIA LaunchPad partnership with pre-allocated compute). | Highly regulated enterprise data science teams (pharma, banking, insurance) requiring reproducible and governed workflows. |

## Open-Source GitHub Projects



- **[MLflow](https://github.com/mlflow/mlflow)**

  **Open-source platform for the ML lifecycle** (Apache 2.0) — **the de facto standard for experiment tracking and model registry**, originally created by Databricks. **Features**: **Experiment tracking** for logging parameters, metrics, and artifacts; **Model Registry** with versioning—MLflow 3.x deprecates stages in favor of **aliases** (`@champion`, `@candidate`) making promotion and rollback single pointer reassignments ; **Projects** for packaging reproducible runs; **Models** for deployment to diverse serving platforms. Integrates with Spark, TensorFlow, PyTorch, and scikit-learn. **Tech stack**: Python, Java, R. **Deploy**: Self-hosted (`pip install mlflow`) or managed via Databricks. **Trade-off**: **Tracking and registry focus—not a full orchestration or serving platform**. Requires integration with orchestration (Prefect, Airflow) and serving (FastAPI, BentoML) for end-to-end MLOps . **Best for**: teams wanting the most widely adopted experiment tracking and model registry foundation—the starting point for most open-source MLOps stacks.



- **[PyCaret 4.0](https://github.com/pycaret/pycaret)**

  **Open-source, self-hosted ML platform for tabular data** (Apache 2.0) — **the most credible open-source alternative to DataRobot and H2O.ai that teams actually own** . **Features**: **PyCaret Engine** (`pip install pycaret`)—config-driven, stateless, notebook-friendly, built on scikit-learn 1.7+; AutoML, preprocessing, model training, evaluation, immutable pipeline artifacts. **PyCaret Control Plane**—full web application with auth, workspaces, projects, datasets, experiments, runs, artifact registry, deployment & serving, monitoring, drift detection, and LLM-assisted experiment design. **Config is the contract**—a single `RunConfig` JSON drives notebook runs, API runs, UI wizard runs, and LLM-generated runs . **Tech stack**: Python. **Deploy**: Local (`uv run pycaret-server`), single Docker host, or Kubernetes + Terraform. **Trade-off**: **PyCaret 4.0 is a vision/roadmap**—the Control Plane is not yet shipped; Engine is the current production component. Not a feature store or data platform. **Best for**: data scientists and small teams (≤20) wanting AutoML without lock-in and a path to a self-hosted platform they control—especially those who find Databricks licensing prohibitive .



- **[Evidently AI](https://github.com/evidentlyai/evidently)**

  **Open-source ML monitoring and observability** (Apache 2.0) — **the most adopted open-source library for model monitoring**, making drift detection cheap enough to start . **Features**: **100+ built-in tests** for data quality, drift, target drift, classification and regression performance; **LLM observability** for monitoring outputs and RAG pipelines; runs in notebooks, CI, or pipelines; **Evidently Cloud** for managed dashboards. **Tech stack**: Python. **Deploy**: `pip install evidently`; cloud available. **Trade-off**: **Monitoring library, not a full platform**—for very large-scale observability (millions of predictions/day, complex SLOs), commercial alternatives like Arize or WhyLabs may scale better . **Best for**: teams wanting to add drift and quality monitoring to production models without a commercial platform—the most pragmatic starting point for open-source model observability.



- **[Feast](https://github.com/feast-dev/feast)**

  **Open-source feature store** (Apache 2.0) — **the standard open-source feature store** for managing ML features across training and serving. **Features**: **Offline store** for batch historical features; **online store** for low-latency real-time serving (Redis, DynamoDB); **feature registry** with metadata, lineage, versioning, and discovery; **AS OF joins** for point-in-time correctness ; transformation engine shared between training and serving. **Tech stack**: Python, Go. **Deploy**: Self-hosted. **Trade-off**: **Feature store only**—not a full ML platform; requires integration with training and serving infrastructure. **Best for**: teams needing consistent feature definitions across training and inference—especially those building real-time ML systems where train/serve skew is a risk.



- **[ZebraOps](https://github.com/flexiana/zebraops)**

  **Local-first, open-source MLOps platform for beginners and small teams** (Apache 2.0) — **the easiest entry point to a complete self-hosted MLOps stack**. **Features**: **`mlops` CLI** with full lifecycle—`init-project`, `up`, `ingest`, `train`, `eval`, `promote`, `serve`, `monitor`; **contract-first** model specs and immutable dataset manifests; **MLflow** for tracking and model registry; **Prefect** for orchestration; **FastAPI** serving with Prometheus metrics; **Evidently** drift monitoring with retrain recommendations; **Docker Compose** devstack (Postgres, MinIO, Grafana, Prometheus); profile adapters for Vast, SageMaker, Vertex . **Tech stack**: Python, Docker. **Deploy**: `pip install zebraops`; `mlops up`. **Trade-off**: **Small teams focus**—not enterprise-scale; newer project with limited community validation. **Best for**: beginners and small teams wanting a batteries-included MLOps stack that runs locally—especially those who want to learn the full lifecycle without assembling five separate tools.



### Additional Strong Open-Source Options



- **Kubeflow** — Kubernetes-native ML toolkit (Apache 2.0). Full ML lifecycle on Kubernetes; powerful but **high learning curve and DevOps difficulty**—not beginner-friendly . **Best for**: platform teams with strong Kubernetes expertise serving many models at scale.

- **Metaflow** — Python-friendly ML framework from Netflix (Apache 2.0). **Easiest orchestration tool** for data scientists—versioning, scaling, deployment without heavy DevOps; feels like writing regular Python . **Best for**: Python-loving data scientists wanting reproducibility and cloud integration without infrastructure friction.

- **Apache Airflow** — Workflow orchestration (Apache 2.0). **De facto platform for orchestrating ML and data pipelines in production**; not ML-specific but widely adopted . **Best for**: teams already using Airflow for data pipelines wanting to extend to ML workflows.

- **Langfuse** — Open-source LLM observability (MIT). Prompt management, RAG observability, eval frameworks, cost tracking—**one of the two most-adopted LLMOps tools** alongside LangSmith . **Best for**: teams shipping GenAI features needing an LLMOps layer alongside classical MLOps.



**Frameworks for building custom systems**: Combine **MLflow** for experiment tracking and model registry with **Feast** for feature management, **Evidently** for production monitoring, and **ZebraOps** or **Metaflow** for orchestration and serving—creating a complete open-source ML stack. **None of these match SageMaker's end-to-end managed coverage or Vertex's Gemini integration**, but for teams prioritizing control and cost, the composed stack covers core MLOps needs.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, license (for open-source), and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- ML platforms handling model artifacts and training data must comply with data protection regulations (GDPR, CCPA, etc.) and implement appropriate access controls for proprietary models and datasets.

- **The "end-to-end platform" vs. "component tool" vs. "AutoML platform" vs. "monitoring library" distinction is critical.** **AWS SageMaker, Vertex AI, Azure ML, Databricks Mosaic AI, and Snowflake ML** are **end-to-end platforms**—they cover the full ML lifecycle with managed infrastructure. **MLflow, Feast, and Evidently** are **component tools**—they solve specific problems (tracking, features, monitoring) and compose together. **PyCaret 4.0 and ZebraOps** are **open-source platforms**—they aim for end-to-end coverage but are earlier in maturity. **Kubeflow and Metaflow** are **orchestration frameworks**—they manage workflow execution but not tracking or monitoring. **Choose based on whether you need managed convenience, best-of-breed components, or a self-hosted platform.**

- **MLflow is the safest foundation for any open-source MLOps stack.** It is the most widely adopted experiment tracking and model registry tool, with MLflow 3.x aliases (@champion, @candidate) making promotion and rollback single pointer reassignments . **The trade-off**: it is not an orchestration or serving platform—pair it with Prefect/Airflow and FastAPI/BentoML.

- **PyCaret 4.0 is the most ambitious open-source AutoML platform**—a credible alternative to DataRobot and H2O.ai that teams own . **The trade-off**: the Control Plane is a vision, not shipped—Engine (`pip install pycaret`) is production-ready today. **For teams wanting self-hosted AutoML without lock-in, it is the most promising path.**

- **Evidently AI is the pragmatic default for open-source model monitoring.** 100+ built-in tests, LLM observability, and a free library make drift detection accessible . **The trade-off**: for very large-scale observability with complex SLOs, commercial tools may scale better.

- **SageMaker's surface area is both its strength and weakness.** It covers every stage of ML but is "twenty products in a trench coat"—figuring out which piece to use is its own learning curve, and endpoint costs escalate if unmonitored . **Vertex AI is more opinionated and Gemini-first**, making the path from data to deployed model shorter but locking you into GCP .

- **Pricing opacity varies.** SageMaker, Vertex AI, and Databricks publish consumption-based pricing. Azure ML, DataRobot, H2O.ai (enterprise), Dataiku, W&B (enterprise), and Domino require sales contact. MLflow, Evidently, Feast, and ZebraOps are free open source. **Validate with direct vendor conversations against your training volume and inference requirements.**

- Self-hosted open-source solutions require proper infrastructure (compute for training, serving endpoints, monitoring backends), security hardening, and ongoing maintenance. **ML platforms handle proprietary models and training data**—ensure your deployment meets your organization's security and IP protection requirements before migrating production ML workflows.



---



**Made for ML engineers, data scientists, and organizations building transparent cloud ML platform solutions.**

Let's make Cloud Machine Learning Platforms more open, data-driven, and ML-lifecycle-friendly.
