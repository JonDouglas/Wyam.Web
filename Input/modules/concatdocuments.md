Title: ConcatDocuments
Description: Inserts previously processed documents into your pipeline
---
This module *copies* documents from other pipelines and places them into the current pipeline after all input documents. Note that because this module does not remove the documents from their original pipeline it's likely you will end up with documents that have the same content and metadata in two different pipelines.

# Usage
---

  - `ConcatDocuments(string pipeline = null)`
  
    If `pipeline` is null then all existing documents from all pipelines (except the current one) will be concatenated with the input documents. Otherwise, the documents from the specified pipeline will be concatenated with the input documents.
    
## Fluent Methods

Chain these methods together after the constructor to modify behavior.
  
  - `Where(Func<IDocument, bool> predicate)`
  
    Only documents that satisfy the predicate will be concatenated with the input documents.