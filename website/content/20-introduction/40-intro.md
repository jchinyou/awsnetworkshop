+++
title = "Overview"
menutitle = "Overview"
chapter = false
weight = 40
+++

## Considerations

When building a multi-VPC and/or multi-account architecture, there are several services that we need to consider to provide seamless integration.
Foundationally we need to provide robust connectivity and routing between all of the VPCs, but we also need to provide and control routing between those VPCs. For example, we may have a 'Shared Services' VPC that every other VPC needs access to and in which we place common resources that everyone needs, such as a NAT Gateway service to access the internet. At the same time, we don't want just any VPC talking to any other VPC. In particular, we don't want our 'Non-Production' VPCs talking to our 'Production' VPCs.

## The Connectivity

In the past, customers used third-party solutions and/or transit VPCs that they built and managed on their own. In order to remove much of that undifferentiated heavy lifting, we will use the **AWS Transit Gateway** Service to provide this connectivity and routing. **AWS Transit Gateway** is a service that enables customers to connect their Amazon Virtual Private Clouds (VPCs) and their on-premise networks to a highly-available gateway. **AWS Transit Gateway** provides easier connectivity, better visibility, more control, and on-demand bandwidth.

## Inter-Region

After we have established connectivity and routing, we may need to provide seamless connectivity between our Datacenter to the VPCs. To do this we will use **Inter-Region Peering**. **Inter-Region Peering** is the ability to peer Transit Gateways between different AWS Regions, enabling customers to extend this connectivity and build global networks spanning multiple AWS Regions. Traffic using inter-region Transit Gateway peering always stays on the AWS global network and never traverses the public internet, thereby reducing threat vectors, such as common exploits and DDoS attacks. Inter-region Transit Gateway peering encrypts inter-region traffic with no single point of failure.
