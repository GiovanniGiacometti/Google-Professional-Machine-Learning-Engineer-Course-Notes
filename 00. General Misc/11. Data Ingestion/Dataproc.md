
Managed service that runs and manages Hadoop and Spark workloads on Google Cloud. It provisions clusters rapidly and is integrated with other GCP services.

What is the difference from traditional hadoop clusters? It is managed, it's easy and faster to spin up spark or hadoop clusters

Batch preprocessing, querying, streaming, machine learning

- cheap: can include preemptible instances
- fast: clusters are quick to start, scale, shutdown
- integrated: with all gcp services
- managed: use spark and hadoop clusters without the assistance of an admin

---

When creating a dataproc cluster, standard apache hadoop ecosystem components are automatically installed. You can specify additional components to be installed (docker, jupyter notebook, presto...)

It automatically installs a cloud storage connector that can be used to move data in and out of a cluster

---

Dataproc clusters are built on compute engine instances -> dataproc clusters support some predefined compute engine mchine types

---

It also exists dataproc serverless, which lets you run spark jobs without specifying machines

---

Dataproc Workflow Templates -> managing and executing workflows on a cluster

Can be run with [[Cloud Scheduler]], [[Cloud Function]] and [[Cloud Composer]]

