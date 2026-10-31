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

- [SaaS/Hosted Platforms](#saas-hosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **[AWS SageMaker](https://aws.amazon.com/sagemaker/)**

  **End-to-end managed ML platform** covering labeling, training, tuning, deployment, monitoring, and governance. Named the **most-mentioned MLOps platform in 2026 job listings** . **Features**: Pipelines, Studio, Model Registry, Endpoints, Model Monitor, Feature Store, and Clarify—all integrated; deep AWS integration (IAM, S3, VPC, CloudWatch); **Bedrock and JumpStart** for foundation models and GenAI workloads; mature governance with model cards and lineage tracking for regulated industries . **Pricing**: Pay-as-you-go on compute, storage, and platform features; free tier available. **Free tier**: Yes, for experimentation. **Best for**: AWS-native organizations of any size needing full lifecycle coverage and compliance—**trade-off**: sprawling surface area; costs escalate if endpoint usage is not monitored .



- **[Google Cloud Vertex AI](https://cloud.google.com/vertex-ai)**

  **Unified ML and GenAI platform** built around foundation models from day one. **Gemini-first** with first-party access to Google's models; **Vertex Pipelines** (built on Kubeflow Pipelines) handle classical ML and LLM workflows; **Model Garden** for curated open and proprietary models; **strong AutoML** for teams without deep ML expertise . **Pricing**: Pay-as-you-go; training, prediction endpoints, and pipelines billed separately. **Free tier**: Limited trial credits. **Best for**: GCP-native organizations and teams building GenAI products on Gemini—**trade-off**: less mature than SageMaker on some governance fronts; GCP lock-in .



- **[Azure Machine Learning](https://azure.microsoft.com/en-us/products/machine-learning)**

  **Enterprise ML platform** with deep Azure DevOps integration and strong governance. **Governance is Azure's strongest differentiator** through Azure Policy; broad compliance certifications (ISO, SOC, HIPAA, GDPR) and responsible AI dashboards for fairness and interpretability . **Pipelines** can be designed in code or visually in ML Studio; retraining triggers from monitoring events; scales via AKS for deployment and distributed GPU/CPU clusters . **Pricing**: Quote-only; enterprise-oriented. **Free tier**: Limited trial. **Best for**: Microsoft-centric enterprises needing governance and DevOps integration—**trade-off**: efficiency optimized for Microsoft ecosystem; cross-cloud portability reduced .



- **[Databricks Mosaic AI](https://www.databricks.com/product/machine-learning)**

  **Lakehouse ML platform** unifying data engineering and ML on open formats. **MLflow 3.0** with GenAI features (prompt versioning, agent observability); **model serving** with 250K+ QPS throughput; **Feature Store** and **Unity Catalog** governance; **Mosaic AI** for custom LLM training, fine-tuning on proprietary data with managed serverless GPU clusters, and **Agent Bricks** for multi-step AI agents . **Pricing**: Consumption-based (DBUs). **Free tier**: Community Edition limited. **Best for**: code-first teams wanting open lakehouse architecture with deep ML and GenAI integration—**trade-off**: requires Databricks platform commitment .



- **[Snowflake ML](https://www.snowflake.com/en/product/features/machine-learning/)**

  **ML capabilities within the AI Data Cloud**, emphasizing low-code and in-database processing. **Snowpark for Python** for in-database data science and model training; **Native Model Registry** with first-class model objects and access control; **Snowpark Container Services (SPCS)** for GPU workloads and custom containers; **Cortex AI** with built-in SQL functions (AI_COMPLETE, AI_EXTRACT, AI_TRANSLATE, AI_SENTIMENT) GA November 2025 for text, image, audio, and video analysis . **Pricing**: Consumption-based (credits). **Free tier**: Trial credits. **Best for**: Snowflake customers wanting AI/ML without moving data outside the warehouse perimeter—**trade-off**: less flexible for custom ML workflows than Databricks .



- **[DataRobot](https://www.datarobot.com/)**

  **Enterprise AI platform** with automated machine learning and GenAI capabilities. **Pricing**: Quote-only. **Free tier**: Trial available. **Best for**: enterprises wanting AutoML with governance and deployment automation.



- **[H2O.ai](https://h2o.ai/)**

  **AI platform** with Driverless AI (AutoML) and H2O-3 open-source core. **Pricing**: Quote-only; H2O-3 is open source. **Free tier**: H2O-3 available. **Best for**: organizations wanting AutoML with an open-source foundation.



- **[Dataiku](https://www.dataiku.com/)**

  **Everyday AI platform** for collaborative data science and ML. **Pricing**: Quote-only; tiered by users. **Free tier**: Limited free edition. **Best for**: teams wanting a collaborative, visual interface for building ML pipelines.



- **[Weights & Biases](https://wandb.ai/)**

  **ML experiment tracking and MLOps platform** (now part of CoreWeave). **Pricing**: Free tier for personal use; paid by users. **Free tier**: Yes, for individuals. **Best for**: teams wanting best-in-class experiment tracking and visualization—**trade-off**: tracking focus, not a full ML platform.



- **[Domino Data Lab](https://www.dominodatalab.com/)**

  **Enterprise MLOps platform** for model development and deployment. **Pricing**: Quote-only. **Free tier**: None. **Best for**: regulated enterprises needing governed, reproducible ML workflows.



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
