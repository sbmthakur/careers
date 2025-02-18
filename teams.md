# Summary

This page is meant to be a general guide to learn about the different teams at
Teleport to help candidates decide which may be the best fit for them.

## Core

The Teleport Core team is focused on design and development of the core
product: Teleport. It is split into multiple sub-teams that work on specific
areas of the product.

### Technologies

We use the following technologies to build Teleport.

* Go
* Rust
* Typescript, React, and Vite
* GitHub Actions
* Docker

### Performance and Scaling

The Performance and Scaling team is focused on scaling, performance,
reliability and robustness of Teleport in large deployments. This team often
works directly with our customers to diagnose and remediate performance issues.
They also consult with other Teleport teams on matters related to scaling and
performance, and ensure that we have appropriate monitoring and tracing in
place to investigate performance problems.

Recent projects:

* Add support for transparent session resumption
* Add support for optimistic locking and atomic write operations for all supported backends
* Improve `tsh` connection latency

### Platform Security

The Platform Security team is focused on application security for the Teleport
product. This team implements security controls and works with security
researchers to find and fix security vulnerabilities.

Teleport also has a general [Security
team](https://github.com/gravitational/careers/blob/main/teams.md#security) that
focuses on holistic security across the organization.

Recent projects:

* [Teleport Device Trust](https://goteleport.com/docs/access-controls/guides/device-trust/)
* Add support for a new S3-based audit log
* Enable storing private key material in AWS and GCP KMS

### Server Access

The Server Access team works on secure access to SSH servers using short-lived
credentials. The team is responsible for learning the SSH protocol and related
protocols (i.e. SFTP) and various aspects of Linux (i.e. PAM, BPF, auditd,
cgroups) to ensure that Teleport is able to provide seamless access to SSH
servers.

Recent projects:

* Add support for remote port forwarding in tsh
* Automatic discovery and enrollment of servers on Azure and GCP
* Add support for headless login
* Add agentless mode for OpenSSH nodes

### Kubernetes Access

The Kubernetes Access team works on secure access to Kubernetes clusters using
short-lived credentials. The team is responsible for learning Kubernetes RBAC
and Kubernetes APIs to ensure that Teleport is able to provide seamless access
to all resources running in Kubernetes.

Recent projects:

* Automatic discovery and enrollment of AWS EKS clusters
* Automatic discovery and enrollment of applications running within Kubernetes
* Extend Teleport RBAC to control access to resources in Kubernetes

### Application Access

The Application Access team works on providing access to web and console
applications behind NATs and firewalls with security and compliance
needs.

Recent projects:

* Teleport as a [SAML Identity Provider](https://goteleport.com/docs/access-controls/idps/?scope=enterprise)

### Database Access

The Database Access team works on providing access to databases behind NATs and
firewalls with security and compliance needs.

Recent projects:

* Added support Oracle databases [#23227](https://github.com/gravitational/teleport/pull/23227)
* Added support for connecting to database resources across multiple AWS accounts

### Desktop Access

The Teleport Desktop Access team is focused on secure and user-friendly remote
desktop access, with a focus on Windows hosts.

This team's work spans across several domains:

* High performance browser rendering: our remote desktop client is implemented
  in the browser with an HTML5 canvas and web assembly
* Rust: while Teleport is primarily written in Go, the RDP client is written in
  Rust and called via CGo.
* Windows authentication: Teleport's RDP client is
  [unique](https://goteleport.com/blog/secure-rdp-client/) in that user logins
  are passwordless. This work often requires research into little known and/or
  poorly documented areas of Windows.

Recent projects:

* Optimize the desktop decoding process
* Add support for resizing the desktop window on the fly
* Add support for additional keyboard layouts

### Machine ID

The Machine ID team is focused on bringing all the advantages and convenience
that Teleport provides for human users to machine use cases.

Recent projects:

* Added support for FIPS builds
  [#23563](https://github.com/gravitational/teleport/pull/23563)
* Added support for securely joining bots running on Azure
  [#23112](https://github.com/gravitational/teleport/pull/23112)
* Added support for securely joining bots running on GitLab CI
  [#22705](https://github.com/gravitational/teleport/pull/22705)

### Web Applications

The Access Provider team is focused on web applications that make
Teleport easier to use and more secure.

Recent projects:

* Added support for joining moderated sessions from the UI
* Added support for session locking in the web UI
* Added a light theme to the Teleport web IU

### Teleport Connect

The Teleport Connect team is focused on building a great desktop experience
for users who prefer not to use CLI-driven workflows.

Recent projects:

* Allow users to customize terminal fonts and keyboard shortcuts
* Add a new cross-cluster search experience

### Access Graph

The team is responsible for the design and implementation of [Access Graph](https://goteleport.com/platform/policy/),
a tool that provides Teleport users with insights and enhanced visibility
into their infrastructure by visualizing access paths to cluster resources
in a unified graph view with querying capabilities.

Recent projects:

* Import of Teleport RBAC and AWS IAM into a unified representation.
* Implementing SQL-like query language for querying the access paths.
* Designing scalable graph UI that can display hundreds of resources while maintaining responsiveness and user-friendliness.

### Access Manager

The Access Manager team is focused on simplifying connecting and configuring
Teleport.

Recent projects:

* Add a simplified onboarding flow for AWS RDS databases

### Integrations

The Integration team is focused on building strong integrations with tools like
Kubernetes, Terraform, Ansible, and more.

Recent projects:

* Added support for Microsoft Teams to Access Requests
* Added Teleport Kubernetes Operator
  [#13331](https://github.com/gravitational/teleport/pull/13331)

### Tools

The Core Tooling team contributes force multiplication efforts to help
engineers developing Teleport and across the org. This team is the backbone to
ensuring the rest of the development team remains incredibly productive, and
that we operate in the open, with an open source code base.

This team is responsible for the tooling necessary to build and release
Teleport artifacts, including container images, AMIs, Helm Charts, and
integration/distribution to package managers.

Recent projects:

* Create hardened container images
* Add universal binaries to our build infrastructure

## Cloud

The Teleport Cloud team develops and operates Teleport Cloud for customers as
service. Cloud exists to help alleviate the burden of running and maintaining
secure global low-latency access to infrastructure.

### Technologies

We use the following technologies to build Teleport Cloud:

* Go
* Typescript & React
* PostgreSQL
* Terraform and Packer
* Amazon Web Services (AWS)
* Kubernetes
* Prometheus/Alertmanager/Loki/Grafana

### Product Growth

The team is focused on customer acquisition, user experience, usage reporting,
billing, and internal customer support tooling. They build a frictionless
UX while driving prospects to become new enterprise customers.

In recent
quarters this team has delivered a new usage reporting platform, the team plan,
PQAs, onboarding questionnaire, upgrade to enterprise features, Machine ID UI.

The team is focused on delivering a great user experience for Cloud users.

Recent projects:

* Usage-based reporting/user journey tracking
* New product plans
* Onboarding questionnaire
* Product conversions
* Machine ID UI
* Usage limits

### Cloud Platform

The team architects a performant and scalable cloud platform that
realizes the promise of Teleport as a SaaS product. The team is focused on scalability,
security, and analytics of Teleport on our Cloud platform. They build
multi-cluster Kubernetes controllers, networking services, platform monitoring tools,
and more.

Recent projects:

* Multi-cluster Kubernetes operators for managing Teleport at scale
* Zero-downtime upgrades for services with long-lived tunnels
* Global ingress stack with Envoy, Gateway API, and ALPN routing
* Reduced onboarding time for new customer instances
* Migration to EKS

### Cloud Operations

The team ensures the cloud platform is reliable and secure while
also optimizing the cloud development and deployment experience for all
engineers. They focus on monitoring, release engineering, service levels,
vulnerability management, CI/CD, and developing automation for component
upgrades.

Recent projects:

* CI/CD with GitHub Actions
* Moniting enhancements
* Security vulnerabilities
* Disaster recovery drill
* AMI migration
* Regional customer data

## Security

At Teleport, each and every engineer is responsible for security of their work.
In addition to this individual mandate and our [Product Security
team](#product-security), we maintain a Security team focused on
organization-wide efforts. We're currently working on the following areas:

* Software supply chain security. We ensure infrastructure and code is
  protected and auditable from developer to production.
* Teleport's bug bounty program.
* Working with consultants and independent experts to perform blackbox,
  whitebox, and red team validation of our code and security controls.
* Updating compliance documentation, internal controls, and our corporate
  policies.

### What is the difference between the "Product Security" and "Security" teams?

The Product Security team works primarily in the Teleport codebase, developing
new security features and fixing bugs for the next Teleport release. The
Security team addresses all elements of information security, including cloud
security, app security, IT security, GRC, policies, training, and our bug
bounty.

To illustrate, you'd find a Product Security team member hacking on issues like
[#10375](https://github.com/gravitational/teleport/issues/10375). You might
find a Security team member improving our internal Okta terraform or improving
the policies and infrastructure backing our promises at
https://goteleport.com/security/.
