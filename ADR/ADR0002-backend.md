# Backend services

## Summary

### Issue
We want to have multiple backend services to manage the main functionality as create,edit, and delete project/categories. It is also required being able to upload documents and set categories for them.

### Decision
Use Java with Spring flux

### Status
Decided

### Group
Integration, data

### Assumptions
- We need to upload documents in an asynchronous way.
- We need high performance.
- We need to be able gracefully any error uploading documents.
- We don't want incurr in very costly solutions.

### Constrains
There's no constraint

### Positions
- Use languages/frameworks as Node.js with Express.js
- Use Java and Spring Webflux as very performant tools.
- Use bespoke or commercial document management system.

### Argument
Java with Spring Webflux is one of the most performant solutions and allow us to handle multiple document uploads at the same asynchronously. The Java ecosystem provides a vast set of libraries/dependencies to do file handling/proccesing and we can leverage those tools.

### Implications
- We need a team proficient in this tools. The team needs to understand very well how to handle concurrency and use paradigm that uses Spring Webflux.
