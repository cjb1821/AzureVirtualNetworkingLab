

<h1>Azure Virtual Networking Lab</h1>

<h2>Description/Objectives</h2>
- Create a virtual network with subnets
<br>
- Create a virtual network and subnets using a template
<br>
- Implement an Application Security Group (ASG) and a Network Security Group (NSG)
<br>
- Configure public and private Azure DNS Zones
<br>
<br>


<h2>Utilities Used</h2>

- <b>Azure</b>
<br>
<h2>Lab walk-through:</h2>

<p align="left">

Created an address space for the CoreServices virtual network through the portal <br>
<img src="https://imgur.com/vJwUKWC.png" height="80%" width="80%" alt=""/>
<br />
<br />
<br />
Created two separate subnets within the address space that are designated for their own purposes <br>
<img src="https://imgur.com/EXZdAoN.png" height="80%" width="80%" alt=""/>
<br />
<br />
<br />
Created the Manufacturing Virtual Network through an ARM Template
<img src="https://imgur.com/mqg90xU.png" height="80%" width="80%" alt=""/>
<br />
<br />
<br />
The subnets for the Manufacturing VNet were also created through an ARM Template
<img src="https://imgur.com/TkcWQN6.png" height="80%" width="80%" alt=""/>
<br />
<br />
<br />
An NSG was created to be associated with the CoreServices VNet and its VMs
<img src="https://imgur.com/GMKA9vu.png" height="80%" width="80%" alt=""/>
<br />
<br />
<br />
An inbound rule was created within the NSG to allow ASG traffic to flow through it. The Application Security Group (ASG) was created behind the scenes. The Application Security Group was created to have the capability to reuse security policies with scale compared to hardcoding IP addresses in the NSG rules.  
<br />
<img src="https://imgur.com/4CVZhSP.png" height="80%" width="80%" alt=""/>
<br />
<br />
<br />
This outbound rule prevents any traffic from the virtual network and its VMs to go outbound toward the internet. 
<img src="https://imgur.com/5Q9dOEa.png" height="80%" width="80%" alt=""/>
<br />
<br />
<br />
Created a public DNS Zone to resolve hostnames in my public domain. 
<img src="https://imgur.com/NHeU5v8.png" height="80%" width="80%" alt=""/>
<br />
<br />
<br />
Created an A record behind the scenes for my public domain. This picture proves the hostname contosocbressler resolves to the IP address 10.1.1.4 I provided.
<br />
<img src="https://imgur.com/v5wOgaS.png" height="80%" width="80%" alt=""/>
<br />
<br />
<br />
Created a private DNS Zone for name resolution services within my virtual networks. I created an A record as well.
<br />
<img src="https://imgur.com/MTzKcXS.png" height="80%" width="80%" alt=""/>
