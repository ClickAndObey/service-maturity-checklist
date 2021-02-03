# Security Self Review

## Static Analysis

1. [ ] Code uses a static analysis tool on every build to ensure security.

## Connections

1. [ ] All connections to and from the service are tracked, and an alert exists for any connection that isn't
       authorized.

## Credentials

1. [ ] Admin level credentials are stored via a proper mechanism (i.e. not plain-text obfuscated somewhere), and are not
       accessible by any members who should not have them.

## Code Review

1. [ ] All code must be reviewed before being merged.
2. [ ] Code ownership file exists to ensure the correct code reviewer looks at the change.

## Deployment

1. [ ] Only one deployment is allowed at any time.
2. [ ] Deployments only happen via a read-only image/binary which has been programmatically created from the proper
       build service.