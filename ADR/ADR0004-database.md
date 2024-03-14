# Database

## Summary

### Issue
We need a database to store project information, categories, notes and document metadata.

### Decision
Use Amazon RDS

### Status
Decided

### Group
data

### Assumptions
- We only need the text from the documents

### Constraints
There's no constraint

### Postitions
- Use a a self-hosted database as Postgres
- Use Amazon Aurora to have high-performance
- Use Node.js deployed in Atlas

### Argument
The client is used to use AWS service so this seems as a natural move. We don't need the high performance of Aurora and also we only need text from the documents so we can cloude that every document has a similar structure. Therefore is not required to use NoSQL databases as MongoDB

### Implications
- We are tied up to AWS as cloud provider. We are not cloud agnostic.
- If we want to store something diferent to text we need to choose a different alternative.
