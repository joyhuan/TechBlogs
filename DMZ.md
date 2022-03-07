# DMZ

## What is a DMZ Network?
A DMZ Network is a perimeter network that protects and adds an extra layer of security to an organization’s internal local-area network from untrusted traffic. A common DMZ is a subnetwork that sits between the public internet and private networks.

The end goal of a DMZ is to allow an organization to access untrusted networks, such as the internet, while ensuring its private network or LAN remains secure. Organizations typically store external-facing services and resources, as well as servers for the Domain Name System (DNS), File Transfer Protocol (FTP), mail, proxy, Voice over Internet Protocol (VoIP), and web servers, in the DMZ. 

These servers and resources are isolated and given limited access to the LAN to ensure they can be accessed via the internet but the internal LAN cannot. As a result, a DMZ approach makes it more difficult for a hacker to gain direct access to an organization’s data and internal servers via the internet.

## How Does a DMZ Network Work?
Businesses with a public website that customers use must make their web server accessible from the internet. Doing so means putting their entire internal network at high risk. To prevent this, an organization could pay a hosting firm to host the website or their public servers on a firewall, but this would affect performance. So instead, the public servers are hosted on a network that is separate and isolated.

A DMZ network provides a buffer between the internet and an organization’s private network. The DMZ is isolated by a security gateway, such as a firewall, that filters traffic between the DMZ and a LAN. The default DMZ server is protected by another security gateway that filters traffic coming in from external networks.

It is ideally located between two firewalls, and the DMZ firewall setup ensures incoming network packets are observed by a firewall—or other security tools—before they make it through to the servers hosted in the DMZ. This means that even if a sophisticated attacker is able to get past the first firewall, they must also access the hardened services in the DMZ before they can do damage to a business.

If an attacker is able to penetrate the external firewall and compromise a system in the DMZ, they then also have to get past an internal firewall before gaining access to sensitive corporate data. A highly skilled bad actor may well be able to breach a secure DMZ, but the resources within it should sound alarms that provide plenty of warning that a breach is in progress.

Organizations that need to comply with regulations, such as the Health Insurance Portability and Accountability Act (HIPAA), will sometimes install a proxy server in the DMZ. This enables them to simplify the monitoring and recording of user activity, centralize web content filtering, and ensure employees use the system to gain access to the internet.

## Benefits of Using a DMZ
The main benefit of a DMZ is to provide an internal network with an advanced security layer by restricting access to sensitive data and servers. A DMZ enables website visitors to obtain certain services while providing a buffer between them and the organization’s private network. As a result, the DMZ also offers additional security benefits, such as:
1. Enabling access control: Businesses can provide users with access to services outside the perimeters of their network through the public internet. The DMZ enables access to these services while implementing network segmentation to make it more difficult for an unauthorized user to reach the private network. A DMZ may also include a proxy server, which centralizes internal traffic flow and simplifies the monitoring and recording of that traffic.
2. Preventing network reconnaissance: By providing a buffer between the internet and a private network, a DMZ prevents attackers from performing the reconnaissance work they carry out the search for potential targets. Servers within the DMZ are exposed publicly but are offered another layer of security by a firewall that prevents an attacker from seeing inside the internal network. Even if a DMZ system gets compromised, the internal firewall separates the private network from the DMZ to keep it secure and make external reconnaissance difficult.
3. Blocking Internet Protocol (IP) spoofing: Attackers attempt to find ways to gain access to systems by spoofing an IP address and impersonating an approved device signed in to a network. A DMZ can discover and stall such spoofing attempts as another service verifies the legitimacy of the IP address. The DMZ also provides network segmentation to create a space for traffic to be organized and public services to be accessed away from the internal private network.

Services of a DMZ include:
1. DNS servers
2. FTP servers
3. Mail servers
4. Proxy servers
5. Web servers

## DMZ Design and Architecture
A DMZ is a “wide-open network," but there are several design and architecture approaches that protect it. A DMZ can be designed in several ways, from a single-firewall approach to having dual and multiple firewalls. The majority of modern DMZ architectures use dual firewalls that can be expanded to develop more complex systems.

1. Single firewall: A DMZ with a single-firewall design requires three or more network interfaces. The first is the external network, which connects the public internet connection to the firewall. The second forms the internal network, while the third is connected to the DMZ. Various rules monitor and control traffic that is allowed to access the DMZ and limit connectivity to the internal network.
2. Dual firewall: Deploying two firewalls with a DMZ between them is generally a more secure option. The first firewall only allows external traffic to the DMZ, and the second only allows traffic that goes from the DMZ into the internal network. An attacker would have to compromise both firewalls to gain access to an organization’s LAN.
Organizations can also fine-tune security controls for various network segments. This means that an intrusion detection system (IDS) or intrusion prevention system (IPS) within a DMZ could be configured to block any traffic other than Hypertext Transfer Protocol Secure (HTTPS) requests to the Transmission Control Protocol (TCP) port 443.

## The Importance of DMZ Networks: How Are They Used?
DMZ networks have been central to securing global enterprise networks since the introduction of firewalls. They protect organizations’ sensitive data, systems, and resources by keeping internal networks separate from systems that could be targeted by attackers. DMZs also enable organizations to control and reduce access levels to sensitive systems.

Enterprises are increasingly using containers and virtual machines (VMs) to isolate their networks or particular applications from the rest of their systems. The growth of the cloud means many businesses no longer need internal web servers. They have also migrated much of their external infrastructure to the cloud by using Software-as-a-Service (SaaS) applications. 

For example, a cloud service like Microsoft Azure allows an organization that runs applications on-premises and on virtual private networks (VPNs) to use a hybrid approach with the DMZ sitting between both. This method can also be used when outgoing traffic needs auditing or to control traffic between an on-premises data center and virtual networks.

Further, DMZs are proving useful in countering the security risks posed by new technology such as Internet-of-Things (IoT) devices and operational technology (OT) systems, which make production and manufacturing smarter but create a vast threat surface. That is because OT equipment has not been designed to cope with or recover from cyberattacks the way that IoT digital devices have been, which presents a substantial risk to organizations’ critical data and resources. A DMZ provides network segmentation to lower the risk of an attack that can cause damage to industrial infrastructure.

## FAQs
### Is a DMZ safe?
The DMZ network itself is not safe. It enables hosts and systems stored within it to be accessible from untrusted external networks, such as the internet, while keeping other hosts and systems on private networks isolated.

### What is the benefit of DMZ?
A DMZ provides an extra layer of security to an internal network. It restricts access to sensitive data, resources, and servers by placing a buffer between external users and a private network. Other benefits include access control, preventing attackers from carrying out reconnaissance of potential targets, and protecting organizations from being attacked through IP spoofing.

### Should you use a DMZ on your router?
A DMZ can be used on a router in a home network. The DMZ router becomes a LAN, with computers and other devices connecting to it. Some home routers also have a DMZ host feature that allocates a device to operate outside the firewall and act as the DMZ. All other devices sit inside the firewall within the home network. A gaming console is often a good option to use as a DMZ host. It ensures the firewall does not affect gaming performance, and it is likely to contain less sensitive data than a laptop or PC.

