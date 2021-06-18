# Simplify mainframe application deployments using Ansible

## Summary

Ansible is a simple yet powerful automation tool, which makes it a very popular open-source automation tool. Using Ansible on z/OS, you can extend all the goodies of Ansible to z/OS platform including platform agnostic integrated DevOps.

This code pattern shows you how to use Ansible on z/OS to complete common actions needed to do a simple deploy of a sample CICS-COBOL application. 

## Description

IBM Z, is the home to mission critical applications as it offers unparalleled quality of services including security, availably, reliability and scalability. DevOps technologies can be used with IBM Z including Continuous Integration (CI), Continuous Deployment (CD) and automated testing.  Like any platform, you can integrate enterprise tools like Git, Jenkins, SonarQube, Artifactory to create a DevOps pipeline for applications which run on z/OS.

Open source based Ansible automation is one of the tools in the DevOps toolchain that can simplify a variety of things including application deployments, middleware provisioning, orchestration and much more. All these can be accomplished using Ansible playbooks, a simple and easy to read script, written in YAML, which can be version controlled.  Ansible employs an agentless architecture, typically consisting of a x86 Linux based control node with a number of managed nodes that span a variety of platforms like Linux/Unix/Windows (LUW) and IBM Z. Ansible runs playbooks on the control node to automate and bring managed nodes to a desired state. With the introduction of [Red Hat® Certified Ansible Content for IBM Z](https://www.ibm.com/support/z-content-solutions/ansible/), you can accelerate your adoption of Ansible for IBM Z to bring in additional efficiencies in your mainframe DevOps pipelines.

For ease of discussion, consider a simple CICS-COBOL-DB2 application. Typical steps to deploy such a mainframe application include: 

- Backup load modules and DBRMs for rollback actions as needed
- Copy updated load modules to application library in CICS DFHRPL DD concatenation  
- Bind updated DB2 DBRMs/Packages to DB2 plan
- Do CICS refresh (New Copy) to pick up updated load modules  
- In the event of failure, rollback to old load modules and DBRMs

We will perform these actions on z/OS using Ansible below.

## Flow

![06_Ansible_Deployment_Flow.PNG](./Images/06_Ansible_Deployment_Flow.png)

## Related Links

- Read more on Ansible here - [Ansible Documentation](https://docs.ansible.com/).
- Read on Ansible collections for z/OS here - [Ansible Galaxy](https://galaxy.ansible.com/search?deprecated=false&keywords=zos&order_by=-relevance&page=1).

## Next Steps

Watch out this space for new Ansible collections for z/OS - [Ansible Galaxy](https://galaxy.ansible.com/search?deprecated=false&keywords=zos&order_by=-relevance&page=1). 

## License

This code pattern is licensed under the Apache License, Version 2. Separate third-party code objects invoked within this code pattern are licensed by their respective providers pursuant to their own separate licenses. Contributions are subject to the [Developer Certificate of Origin, Version 1.1](https://developercertificate.org/) and the [Apache License, Version 2](https://www.apache.org/licenses/LICENSE-2.0.txt).

[Apache License FAQ](https://www.apache.org/foundation/license-faq.html#WhatDoesItMEAN)