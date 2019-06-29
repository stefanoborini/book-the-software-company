---
nav_order: 1
---
# 1 The Software Company

If your company creates software of any kind, from basic scripts to complex applications, it is a software company.
It is irrelevant that its core business is not software. While this seems to be a trivial point to make, my personal
experience with multiple companies from manufacturing to pharmaceuticals points at how often this fundamental
concept is downplayed.

As a software company, you carry a set of requirements to meet the goals of handling software. You need to handle the software
production chain, which generally can be represented as follows:

- handling of the runtime the software depends on (compilers, libraries etc).
- software, its creation and its maintenance
- documentation of the software
- testing of the software
- handling of the infrastructure to perform testing, possibly hardware.
- versions and releases of the software, and their interactions.
- deployment of the software, either in house, off-site (e.g. with third parties), or in the cloud.
- interaction of the software with your core business
- interaction of software development process with your core business process.

We will investigate each of these points in more details.

# Handling the runtime

When you want to develop some software, it relies on external components of
various nature, such as interpreters, compilers, libraries. These components
are either bought or opensource, and have different level of quality,
documentation, bug tracking and user support. They might be pre-built as a
binary, or need to be built from source within your company, therefore needing
a well-known, reproducible build chain to ensure the quality and reliability of
the resulting artefact. 

If you want a running product, you need to take care of your runtime as if it
were a product in itself. You must keep track of its changes, its affecting
bugs, any backward compatibility breakages, platform inconsistencies or
differences and so forth. This is not only a loose recommendation. It is an actual
regulatory requirement in some industries, and a massive one in some cases
where human life may be in danger. Even when not a regulatory requirement, 
not organising your runtime will eventually lead to broken installations with
hard to reproduce, random crashes, or unexpected bugs appearing or reappearing.

You therefore need a proper process in place to manage, build, maintain,
deliver, update, and track your runtime effectively, and ensure that your
company uses your runtime's software packages, and not else.

# Creating and mainining the software

On top of the runtime, you create your software.
versioncontrol, bug tracking, process tracking, feature tracking, version planning,
quality assurance (review, linting)
build infrastructure.
- boilerplate stuff should come at no cost (e.g. linting, testing setup etc). Must be there


# Documenting the software




# Testing the software

, unit testing, integration testing)
mocks, testing infrastructure and reporting system, testing rigs


# Handling the testing infrastructure

# Handing the network and cloud infrastructure

databases (production, testing) 

# Version and release the software

# Deploy the software

creating installation scripts that are adequate for the target platform, smooth out
unexpected circumstances and differences in the target machine (proxy, antivirus, 
ACL).

# Handle deprecation, upgrades and migration.

of file formats, database schema changes.

# Interaction of the software with the core business

# Interaction with the development process with the core business process


