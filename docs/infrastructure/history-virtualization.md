---
title: From Mainframes to Serverless: The Evolution of Virtualization and Containerization
layout: page
parent: infrastructure
---

# From Mainframes to Serverless: The Evolution of Virtualization and Containerization

## Contents

1. [The Dawn of Computing: Mainframes](#the-dawn-of-computing-mainframes)
2. [The Birth of Virtualization: Virtual Machines](#the-birth-of-virtualization-virtual-machines)
3. [Lightweight and Portable: Containers](#lightweight-and-portable-containers)
4. [From Static to Dynamic: Elastic Services](#from-static-to-dynamic-elastic-services)
5. [The Future is Serverless: GCP, AWS, and Azure Services](#the-future-is-serverless-gcp-aws-and-azure-services)

Join me on a journey through the history and evolution of virtualization and containerization!

## The Dawn of Computing: Mainframes

Our journey begins in the era of mainframes. A mainframe was a large computer that could support multiple users, each running their own tasks. However, they were not utilized efficiently, as one user's task could not use another user's allocated resources, even if they were idle.

> Think of mainframes as apartment buildings. Each tenant (user) had their own apartment (resources), but if one tenant was out of town (idle), no other tenant could use their apartment.

## The Birth of Virtualization: Virtual Machines

The advent of virtual machines (VMs) addressed this inefficiency. A VM is a software emulation of a computer that runs on a host computer. With VMs, a single physical server can run multiple different virtual servers, maximizing resource utilization.

VMs allowed multiple operating systems to run simultaneously on a single machine, isolating the applications and preventing one application's problems from affecting others. This was akin to having several virtual computers operating independently within one physical computer.

> Imagine a building with flexible walls. The rooms (VMs) can be resized or reconfigured according to the needs of the tenants (applications), maximizing the use of space (resources).

## Lightweight and Portable: Containers

Containers took the concept of virtualization one step further. Unlike a VM, which includes a full copy of an operating system plus the application and its dependencies, a container includes only the application and its dependencies. This makes containers more lightweight and faster to start than VMs.

Just like shipping containers, which revolutionized the transport industry due to their standard size and portability, software containers brought similar benefits to software development. They ensure that applications run the same, regardless of where they are deployed.

> Picture a container ship. Each container (application) can be loaded and unloaded efficiently, moved from ship to ship, or from ship to truck, and it will always fit because all containers share a standard size and form.

## From Static to Dynamic: Elastic Services

In the era of cloud computing, the need for infrastructure to scale with use became evident. Elastic services, which can automatically adjust resources based on demand, were the answer to this need. 

For example, a retail website might have average traffic most of the year, but during the holiday shopping season, traffic could spike dramatically. With elastic services, the website can scale up resources during the holiday season and scale back down when it's over, ensuring optimal performance while keeping costs under control.

## The Future is Serverless: GCP, AWS, and Azure Services

The latest step in this evolution is serverless computing, where developers build and run applications without thinking about servers. 

In serverless computing, cloud providers dynamically manage the allocation of machine resources. This allows developers to focus on their code, and the cloud provider takes care of the rest.

Here are some examples from leading cloud service providers:

- **Google Cloud Platform (GCP)**: Google Cloud Functions is a serverless execution environment for building and connecting cloud services.
- **Amazon Web Services (AWS)**: AWS Lambda lets you run your code without provisioning or managing servers.
- **Microsoft Azure**: Azure Functions is a serverless solution that allows you to write less code, maintain less infrastructure, and save on costs by only paying for what you use.

Joining the serverless revolution allows businesses to increase their agility, focus on their core products, and significantly reduce operational costs. This is the future of development - welcome aboard!