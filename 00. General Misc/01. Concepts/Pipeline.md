
Many services are based on the concept of pipeline. It would be nice to clarify what each pipeline actually is and how they relate to each other.

---

**Kubeflow** pipelines

---

**TFX** pipelines. These can be orchestrated in 3 ways:
- beam (i think some tfx components are translated into beam components)
- kubeflow (does this mean that the pipeline developed in tfx becomes a kubeflow pipeline or it's just that kubeflow supports the orchestration?)
- airflow (composer)

---

Some clarification is done here [[04. Automation and Orchestration]]

Vertex AI Pipelines can run pipelines built using Kubeflow and TFX. They recommend to use TFX if using tensorflow, kubeflow if using any other framework. Then, execute both on Vertex AI serverless pipeline system

----

General on Pipelines:
https://cloud.google.com/vertex-ai/docs/pipelines/introduction