
From the book:

Use sparse categorical cross-entropy when your classes are mutually exclusive (when each sample belongs exactly to one class) and categorical cross-entropy when one sample can have multiple classes or labels

---

From the book glossary:

**Categorical hinge-loss**: typical for svm training

**Categorical cross-entropy** is used when true labels are onehot encoded. It is recommended to use categorical cross-entropy for multiclass (classes are mutually exclusive) problems but binary cross- entropy for multi-label problems.

**Sparse categorical cross-entropy**: computes the cross-entropy loss between the labels and predictions. Use this cross-entropy loss function when there are two or more integer-encoded label classes while using TensorFlow for classification