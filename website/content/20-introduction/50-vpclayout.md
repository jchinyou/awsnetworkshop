+++
title = "VPC Layout"
chapter = false
weight = 50
+++

![Speficy Details Screenshot](../images/hybrid-vpcs-diagram.png)

There are lots of choices for VPC and Account Architectures, but this is mostly out-of-scope for this workshop. Take a look at what Androski Spicer presented at re:Invent 2018 in his [From One to Many: Evolving VPC Design](https://www.youtube.com/watch?v=8K7GZFff_V0 "youtube video") session if you'd like to learn more on this topic.
In our case, we are going to provide three types of VPCs:

1. **Non-production VPCs**: We might create several of these to house our training, development, and QA/test resources.
1. **Production VPCs**: This is for our live production systems.
1. **Shared Resources**: For resources and services that we want shared across all VPCs.

