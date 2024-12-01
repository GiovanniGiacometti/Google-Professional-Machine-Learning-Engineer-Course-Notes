
Efficient input pipeline

- prefetch transformation to overlap preprocessing and model execution 
- interleave parallelizes the data reading
- cache data in memory during the first epoch
- vectorize user defined functions

---

You can create transform pipelines using [[Dataflow]]

