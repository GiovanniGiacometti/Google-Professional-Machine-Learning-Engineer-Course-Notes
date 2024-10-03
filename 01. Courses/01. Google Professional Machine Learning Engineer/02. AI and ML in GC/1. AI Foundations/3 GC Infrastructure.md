
3 layers

- Networking and security
- Compute and Storage -> separated so that they can scale independently on need
-  Data and AI products

---

**Compute**

Services:
- Compute Engine (IaaS)
- GKE (Google Kubernetes Engine)
- App Engine (PaaS)
- Cloud Functions: serverless, execute code in response to events
- Cloud Run: run workflows, abstract infrastructure management.

The processing power comes from:

- CPU
- GPU
- TPU (introduced by Google in 2016) - custom developed ASICs. It's a domain specific hardware, higher efficiency - generally faster and more energy efficient for AI and ML products.

**Storage**

- Cloud Storage
- Big Table
- Big Query
-  ...

What to choose? It depends on the data type
- Unstructured 

Cloud Storage is the most suited for them. It has different types of storage according to the needs, offered at different costs based on how frequently they are accessed

- Structured

2 types: 
- Transactional workloads
- Analytical workloads

Both can be accessed with SQL or NoSQL and an option is provided for each combination, depending on the latency and so on


