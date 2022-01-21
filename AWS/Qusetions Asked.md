**Q1. What is VPC and Why should I use VPC?**

Ans:- VPC
A virtual Private Cloud is a Virtual Networking that closely Resembles a traditional Networking that you operate in your own data center,with the Benefits of using the Scalable Infrastructure of Aws. 

Amazon VPC enables you to build a virtual network in the AWS cloud - no VPNs, hardware, or physical datacenters required. You can define your own network space, and control how your network and the Amazon EC2 resources inside your network are exposed to the Internet. You can also leverage the enhanced security options in Amazon VPC to provide more granular access to and from the Amazon EC2 instances in your virtual network. 

**Q2.what is cidr and why is it used?**
Ans:-CIDR, which stands for Classless Inter-Domain Routing, is an IP addressing scheme that improves the allocation of IP addresses. It replaces the old system based on classes A, B, and C. This scheme also helped greatly extend the life of IPv4 as well as slow the growth of routing tables.

CIDR is an alternative to IP subnetting. It organizes IP addresses into subnetworks independent of the value of the addresses themselves. CIDR is also known as supernetting because it effectively allows several subnets to be grouped together for network routing. 

**Q3. What is Internet Gateway and Nat Gateway?**
Ans:- An Internet Gateway (IGW) is a logical connection between an Amazon VPC and the Internet. It is not a physical device. Only one can be associated with each VPC. 
A NAT gateway is a Network Address Translation (NAT) service. You can use a NAT gateway so that instances in a private subnet can connect to services outside your VPC but external services cannot initiate a connection with those instances. A NAT device forwards traffic from the instances in the private subnet to the internet or other AWS services, and then sends the response back to the instances while Internet Gateway is used to allow resources in your VPC to access internet.

