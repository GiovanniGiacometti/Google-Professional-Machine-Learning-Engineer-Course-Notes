
https://cloud.google.com/retail/docs

These 4 are described in the book

"Recommended for you" -> for home pages, brings attention to the most likely products based on current trends and user behaviour

"Similar items" -> product information only, ideal when there is no history

"Others you may like" -> based on browsing history

"Frequently bought together" -> shown at checkout, so that users can quickly add more into their cart

Others are in the doc https://cloud.google.com/retail/docs/models

- Buy it again
- On-sale
- Recently viewed
- Page Level Optimization

----

Requirements to create a new model:
- import catalog (should also be kept updated)
- record user events data
- identify recommendation type and optimization objective
- determine user data requirements
- import historical data
- create model and serving config -> vertex ai search initiates model training and tuning
- Confirm model is working correctly using the prediction preview
- a/b experiment