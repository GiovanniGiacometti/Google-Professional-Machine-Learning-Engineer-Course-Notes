
Offline or batch

Vertex ai batch prediction to run a batch prediction job for your data stored in big query or gcs

Online or real time

2 types of online predictions:

- sync -> the caller waits until it receives the prediction

Stack: vertex ai online prediction to deploy model as an https endpoint. Can use GKE or App Engine as a gateway to perform some feature preprocessing

- async -> the user gets notified or polls a feature store for prediction inr eal time