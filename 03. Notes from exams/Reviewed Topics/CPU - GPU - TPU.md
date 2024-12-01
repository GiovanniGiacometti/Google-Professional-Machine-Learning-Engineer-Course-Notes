

TPU: can be connected in groups called Pods that scale up your workload with little to no code changes

Cloud TPU provide the following configurations:

- single TPU device
- TPU pod (a group of tpu devices)
- TPU slice (subdivision of TPU Pod)
- TPU VM

---

CPU
Custom C++ operations
Limited by I/O or networking bandwidth

GPU
Significant number of custom tf operations so that they need to run at least partially on a cpu

TF ops that are not available on tpus

TPU
majority of matrix mult
no custom tf operations

NO TPU for:
- high precision
- custom ops in c++
- sparse data (lots of zeros)
- programs that require frequent branching

---

Coral.ai -> edge tpu production devices (can be in several forms)
