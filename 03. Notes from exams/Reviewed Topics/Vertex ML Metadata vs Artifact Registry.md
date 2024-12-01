
Differences between [[Vertex ML Metadata]] and [[Artifact Registry]]

### Vertex ML Metadata

Vertex ML Metadata lets you record the metadata and artifacts produced by your ML system and query that metadata to help analyze, debug, and audit the performance of your ML system or the artifacts that it produces. 

Based on Open Source library ML Metadata

Metadata store: top level container

Resources, graph like data model

**Artifacts**: entity or piece of data consumed in an ML workflow
**Context**: group of artifacts and execution (many experiment trying different hyperparams, same context)
**Execution**: a step in ML workflow, can be annotated with runtime params
Events: connects artifacts and executions
Metadataschema: specifies the schema to be used by the particular types of data (artifact or executions) - yaml format
![[Pasted image 20241012184400.png]]

every metadata resource that is stored in Vertex ML Metadata follows a metadataschema

It also defines how the particular resource can be queried

```python
from typing import Optional

from google.cloud import aiplatform


def list_execution_sample(
    project: str,
    location: str,
    display_name_filter: Optional[str] = "display_name=\"my_execution_*\"",
    create_date_filter:  Optional[str] = "create_time>\"2022-06-11T12:30:00-08:00\"",
):
    aiplatform.init(
        project=project,
        location=location)

    combined_filters = f"{display_name_filter} AND {create_date_filter}"

    return aiplatform.Execution.list(filter=combined_filters)
```



### Artifact registry

Store artifacts and build dependencies centrally

Specifically, for packages and Docker Container Images