
Best practices from Andrew NG
https://cs230.stanford.edu/blog/datapipeline/#best-practices
#### Functions


**shuffle**

```python
shuffle (buffer_size, seed=None, reshuffle_each_iteration=None, name=None) -> 'DatasetV2'
```

Randomly shuffles the elements of this dataset.

This dataset fills a buffer with `buffer_size` elements, then randomly samples elements from this buffer, replacing the selected elements with new elements. For perfect shuffling, a buffer size greater than or equal to the full size of the dataset is required.

To shuffle an entire dataset, set `buffer_size=dataset.cardinality()`. This is equivalent to setting the `buffer_size` equal to the number of elements in the dataset, resulting in uniform shuffle.

Why is there a buffer size? As the dataset might be too big and loading it all into memory might cause a memory overflow.

On the importance of buffer size in shuffle: https://stackoverflow.com/questions/46444018/meaning-of-buffer-size-in-dataset-map-dataset-prefetch-and-dataset-shuffle/48096625#48096625


**repeat**

```python
repeat(count=None, name=None) -> 'DatasetV2'
```

Repeats this dataset so each original value is seen `count` times.

If count is None, it goes on indefinitely.


**batch**

```python
batch(batch_size,    drop_remainder=False,    num_parallel_calls=None,    deterministic=None,    name=None) -> 'DatasetV2'
```

Combines consecutive elements of this dataset into batches.

---

The typical piece of code uses both these 3 functions, in a way similar to this:

https://colab.research.google.com/drive/1VS6-dYk3YAzoRmALhgTK7bb2_tBPrB4c?usp=sharing

from https://stackoverflow.com/questions/53514495/what-does-batch-repeat-and-shuffle-do-with-tensorflow-dataset

From ng:



To summarize, one good order for the different transformations is:

1. create the dataset
2. shuffle (with a big enough buffer size) 3, repeat
3. map with the actual work (preprocessing, augmentation…) using multiple parallel calls
4. batch
5. prefetch

---


**prefetch**

```python
prefetch(buffer_size, name=None) -> 'DatasetV2'
```

Creates a `Dataset` that prefetches elements from this dataset.

Most dataset input pipelines should end with a call to `prefetch`. This allows later elements to be prepared while the current element is being processed. This often improves latency and throughput, at the cost of using additional memory to store prefetched elements.

Like other `Dataset` methods, prefetch operates on the elements of the input dataset. It has no concept of examples vs. batches. `examples.prefetch(2)` will prefetch two elements (2 examples), while `examples.batch(20).prefetch(2)` will prefetch 2 elements (2 batches, of 20 examples each).

From https://www.tensorflow.org/guide/data_performance

"Prefetching overlaps the preprocessing and model execution of a training step. While the model is executing training step `s`, the input pipeline is reading the data for step `s+1`. Doing so reduces the step time to the maximum (as opposed to the sum) of the training and the time it takes to extract the data."

From NG
"When the GPU is working on forward / backward propagation on the current batch, we want the CPU to process the next batch of data so that it is immediately ready. As the most expensive part of the computer, we want the GPU to be fully used all the time during training. We call this consumer/producer overlap, where the consumer is the GPU and the producer is the CPU.

With `tf.data`, you can do this with a simple call to `dataset.prefetch(1)` at the end of the pipeline (after batching). This will always prefetch one batch of data and make sure that there is always one ready."