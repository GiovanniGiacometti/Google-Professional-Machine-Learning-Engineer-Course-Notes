
2 main paradigms:

- data parallelism: dataset is split into parts and then assigned to parallel computational machines

The same parameters are used, the gradient is computed, sent back to the main node

2 types:

Sync -> wait for other workers to finish
Async -> workers don't have to wait for each other, they update variables asynchronously

Typically, sync training is supported via all reduce, async through parameter server architecture

- model parallelism: to train a big model, it is split into multiple machines


---


TF supported strategies:

- mirrored strategy: sync distributed training on multiple GPUs on one machine
- central storage strategy: sync training, no mirroring
- multi worker mirrored: sync distributed across multiple workers
- tpu strategy: sync distributed across multiple tpu cores
- some machine are workers, other parameter servers