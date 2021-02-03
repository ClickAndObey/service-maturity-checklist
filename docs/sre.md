# SRE Checklist

## Level 1 - The Prototype Phase (Build, Test and Deploy)

### Build

1. [ ] You have an automated build of your main branch via a CI tool. I.e. Jenkins/TravisCI.
2. [ ] Users are able to build your project locally without having to install dependencies, or there is a single script
       that can be used to install and uninstall the dependencies.
3. [ ] Builds can be run via a single command. This can be either a Makefile target, Script, etc...

### Tests

1. [ ] Unit tests exist to ensure basic functionality.
2. [ ] An integration test exists to ensure your service works as a running entity.
3. [ ] Tests can be run via a single command. This can be either a Makefile target, Script, etc...

### Deploy

1. [ ] Deployments are run from a centralized location. i.e. They aren't done from a developer machine.
2. [ ] You have the ability to deploy via a single command. This can be either a Makefile target, Script, etc...

## Level 2 - Turning this into a Real Thing (Documentation and Continuous Integration)

### Documentation

1. [ ] Development, Deployment, and Testing are all documented and linked in the main README.
2. [ ] Documents exist for all major decisions about the service.
3. [ ] Design document exists detailing the need of this service with impacted services and customers called out.

### Continuous Integration

1. [ ] Continuous Integration file (Jenkinsfile/.travis.yaml) exists, and is linked to the Continuous Integration
       Environment.
2. [ ] Continuous Integration file runs build and test at minimum.

## Level 3 - Operational (Security, Monitoring)

### Security

1. [ ] Self Security Review has been completed.

### Monitoring

1. [ ] Monitoring exists for anything that might become an immediate response issue.
2. [ ] Alerts exist for anything that might become an immediate response issue.
3. [ ] SLA exists for the service to describe what is an immediate response issue, and generally expected behavior.

## Level 4 - Ready for SRE Handholding (System and Automated Testing, Architecture and Runbooks)

### System Testing

1. [ ] System test exists that ensures the service works with the entire system as expected. Test(s) must be automated.
2. [ ] Load test should exist that describes the peak capacity for your system.

### Automation

#### Automated Testing

1. [ ] All testing is automated and part of the CI pipeline. Testing must also be runnable from the command line.

#### Automated Deploy

1. [ ] Continuous Deploy must be available, but doesn't have to be turned on.

### Architecture

#### Diagrams

1. [ ] System Diagram should exist that details the design of your system without any dependent services.
2. [ ] System Diagram should exist that details the design of your system as it integrates into the architecture of the
       project as a whole

### Runbooks

[Runbook Template](./sre/runbooks/runbookTemplate.md)

1. [ ] Runbooks exist for all immediate response issues.
2. [ ] Escalation policy exists for issues that aren't covered in runbooks.
3. [ ] Runbooks are linked to a corresponding alert via code (i.e. terraform).

#### Owner Information

* __How to Contact__
  * _Discord/Hipchat/Slack_:
  * _Email_:

## Level 5 - Ready for SRE Handoff (Dependencies, Reporting, Planning)

### Planning

#### Volume Estimates

1. [ ] Volume estimates must be provided for the next 6 months, with a new volume estimate every 6 months going forward.
2. [ ] Volume estimates should be gone over every 6 months to determine any issues in estimation.

#### Growth Planning

1. [ ] Horizontal and Vertical Scaling must be documented on what the expectations are for either form.

#### Dependencies

1. [ ] Internal Dependencies should be listed.
2. [ ] External Dependencies should be listed.

### Reporting

1. [ ] Reporting should exist to get the State of the System at a glance.
2. [ ] Daily, Weekly, and Monthly Report should be available via UI or automated reporting mechanism.