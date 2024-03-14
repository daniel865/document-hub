# Document Storage

## Summary

### Issue
We want to store documents, pdfs or images in a single repository (source of truth).

- To accomplish this we want to have a solution that provides scability and reliability to storing large amount of documents.

- The documents need to be shared between diferent employees and managers (admins)

### Decision
Use Amazon S3 as a cloud storage service.

### Status
Decided. Mainly decided because the client already has an AWS account

### Group
Integration, data

### Assumptions
- We assume that kind of documents to be stored are not growth in diferent formats and encoding. 
- We assume we don't need any specific metadata information about the document
- We assume that we want to use technologies more closely aligned with AWS as platform given that is already used inside the organization.

### Constraints
We need to chose a solution that closely aligns with tools already used by the client.

### Positions
- Create a bespoke solution to allow store documents
- Use Google Cloud Storage. This allows to have documents in different tiers: Standard, Nearline, Coldline, Archive. This can help to reduce costs

### Argument
S3 is the best solution due to the familiarity of the client with some AWS services. Given the above assumptions we don't think our requirements could change a lot in short-term obligating us to use a more robust solution.

### Implications
- The client is being tied up to a cloud provider as AWS and this implies that could be more difficult in the future to move to another cloud provider. The solution is not cloud agnostic.

