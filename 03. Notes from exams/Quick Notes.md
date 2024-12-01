

#### How to find the correct BigQuery table among hundreds of them?

Use [[GCP Data Catalog]]. Do not use SQL query for information schema.

---

For AutoML image, video, and text data, you can use Vertex AI managed datasets and upload your data from your local drive directly to the managed dataset in Vertex AI.

---

For pre‐built container training, you do not need to create a custom container or Dockerfile. You can just package the code as a Python distribution and upload it to cloud storage as per the folder structure required.

---

Only the integrated gradient method is supported by AutoML images. You can use XRAI on a custom TensorFlow trained model. SHAP is for tabular datasets.

---

In Vertex AI Model Monitoring, there are three types of schema formats. Which of the following is not a valid type?

A. Object
B. Array
C. Number
D. String

Explanation

The schema “type” could be one of the following: _object_ (key‐value pairs), _array_ (array‐like format) or _string_ (csv‐string).