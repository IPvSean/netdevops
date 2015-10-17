# NetDevops
Using Ansible as a SDN controller to automate several pieces of a modern data center network in a leaf spine configuration.  This demonstration was used at All Things Open talk "Using Devops Tools For Modern Data Centers" by Sean Cavanaugh on October 19, 2015.  

##Topology
Here is the topology for the demonstration:

![Topology](https://raw.githubusercontent.com/seanx820/netdevops/master/topology.png)

##Playbook descriptions
- playbook.yml - this playbook is used to provision the network with [OSPF Unnumbered](http://docs.cumulusnetworks.com/display/CL25/Open+Shortest+Path+First+-+OSPF+-+Protocol).  Each node is given a single IP address instead of burning (using up) an IP address per link.
- playbook-fan.yml - this playbook runs when spine2 (4.4.4.4) has been identified to have a bad fan
- playbook-check.yml - this playbook runs to check that spine2 (4.4.4.4) has been removed from the routing table gracefully

all other playbooks are just for provisioning part of the network, or are just tests sean is playing with while he makes this demo better and better

##Contributing
Make pull requests at any time, just leave descriptions... this is more of a sandbox.  Please email me at sean @ cumulusnetworks.com if you want more information or demos to play with.  We have heaps on our [Demo Website](https://support.cumulusnetworks.com/hc/en-us/sections/200398866)

***

![Cumulus icon](http://cumulusnetworks.com/static/cumulus/img/logo_2014.png)

### Cumulus Linux

Cumulus Linux is a software distribution that runs on top of industry standard 
networking hardware. It enables the latest Linux applications and automation 
tools on networking gear while delivering new levels of innovation and 
ﬂexibility to the data center.

For further details please see: [cumulusnetworks.com](http://www.cumulusnetworks.com)
