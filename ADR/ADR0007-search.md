# Search

## Summary

### Issue
We want to have the posibility to search by document content. All the documents are text only.

### Decision
Use Elastic Search

### Status
Decided

### Group
Integration, Data

### Assumptions
- We only need to search text

### Constraints
No constrains

### Positions
- Use AI Search tool as Algolia
- Use a database that allows full-text search
- Use Elastic Search

### Argument
Elastic Search is the most known solution. We don't need advanced search features as the one provided by Algolia. The full-text search feature in a database could be a good option at the begining but can fall short when the amount of documents is increased (We think this can increase rapidly).

### Implications
- An extra service to manage
- Increasing complexity in the system
- Extra cost