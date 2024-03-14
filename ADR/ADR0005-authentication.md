# Authentication

## Summary

### Issue
We want to provide a way to authenticate and authorize users. We need to manage permissions given a role.

### Decision
Implement JSON Web Tokens (JWT) with AWS Cognito.

### Status
Decided

### Group
Integration

### Assumptions
- We can integrate with other services to manage authentication and authorization.
- There are only two roles and this is not going to change.

### Constraints
There are not constraints

### Positions
- Use LDAP to handle auth
- Use basic auth

### Argument
Given we are leveraging existing AWS services we can integrate with AWS Cognito to handle the users and permissions. JWT is one of the most adequate ways to have permissions in the payload

### Implications
- The authentication is tied up to AWS and is going to be harder to migrate to another service.