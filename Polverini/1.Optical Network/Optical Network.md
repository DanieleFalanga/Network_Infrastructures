Optical Network connects users with optical fiber cables. 
First generation of optical networks are called Passive optical Network because it is composed by passive component like passive splitter. 

Another big difference between first generations of optical network is that the routing, switching and other intelligent function are handled by electronics. 

In the *second generations* of optical network, called WDM-PON, this functions are handled in the optical layer. 

There are two ways to increase the transmission capacity on a fiber:

1) **Time division Multiplexing (TDM):** Assign time slots to users data packet. This type of technology is used mainly in first generation of Optical Network. 
2) **Wavelength Division Multiplexing (WDM):** Divide the traffic in wavelengths, each users has yours. This technique allows the transmission of data simultaneously.

![[Pasted image 20240126094356.png]]

---

# Second Generation of Optical Networks


![[Pasted image 20240126094756.png]]

The main idea is to incorporate all the intelligent function in the optical domain. 

Another important characteristics is that wavelength can be converted from one wavelength to another.

## Components of a Optical Networks

### OLT (Optical Line Terminals)

Optical line terminals are used at the end of a point-to-point link to multiplex and demultiplex wavelenghts. 

It is composed by three functional elements:
- Transponder (O/E/O): 
- Wavelength multiplexers 
- Optical amplifiers

Transponder adapts the signal coming from a client of the optical network and vice versa. 
1) Convert the signal into a wavelength that is suited in the optical network. 
2) Adds OTN overhead
3) Monitors the bit error rate
It is constitute the bulk of the cost of an optical network. 

![[Pasted image 20240126095614.png]]

### OADM (Optical Add/Drop Multiplexers)


![[Pasted image 20240126100639.png | 400]]

Optical add/drop multiplexers (OADMs) provide a cost-effective means for handling pass through traffic in both metro and long-haul networks.

### OXC (Optical Crossconnects)

![[Pasted image 20240126101152.png]]

In general, OXCs enables reconfigurable optical networks, where lightpaths can be set up and taken down as needed. 

It provides several key functions in a large network: 
- **Service provisioning:** provisioning of the lightpaths in a large network in automated manner. It is able to reconfigure lightpaths to respond to traffic change. 
- **Protection:** Detect failure and rapidly re-route the failed lightpath
- **Wavelength conversion:** Change the wavelength of an incoming signal before transmitting it

## Electronics in Optical Networks

Electronics plays a crucial role in performing the intelligent control and management functions. It is required at the **edge of the network** in order to adapt the signal entering in the optical domain and in the **core network** in order to **regenerate** the signal and perform wavelength conversion. 

There are three types of eletronic regeneration: 
▶ 1R: regeneration (can be seen as an Optical Amplifier) 
	PRO: supports analog signals 
	CONS: poor performance 
▶ 2R - regeneration with reshaping 
	PRO: offers transparency to bit rates 
	CONS: limits the number of regeneration steps allowed due to the accumulated jitter 
▶ 3R - regeneration with retiming and reshaping 
	PRO: produces a “fresh” copy of the signal 
	CONS: it eliminates transparency to bit rates and the framing protocols

# Control and Management

## Management Framework

Most functions of the network are implemented in a centralized manner by a hierarchy of management systems. 

Due to latency, some management functions are performed in a decentralized manner like: responding to failures and setting up/taking down connetions)

During lightpath setup client layers can specify to the optical layer the following services: 
- The endpoints to interconnect
- The amount of bandwidth that is required 
- It can specify if an adaption function is needed
- the BER 
- The level of protection against failure

All of this services requires a control management interface between the optical layer and the client layer.

Is useful to subdivide the optical layer into several sublayers:

![[Pasted image 20240126122235.png]]
- **Optical Channel layer (OCh):** Takes care of end to end routing of the lightpaths
- **Optical multiplex Section Layer (OMS):** Each link between OLTs ot OADMs represents an optical multiplex section carrying multiple wavelenghts. 
- **Optical transimission Sections layer (OTS):** Link between two optical amplifier stages
--- 
- **Optical channel transport unit (OTU):** 
	- provide identification of the optical connection
	- monitor bit error rate (BER)
	- carry alarms indicators to signal failures
	- provide communication channel between the end points of the optical connection
- **Optical channel data unit (ODU):** 
	- as OTU but at higer layer
	- includes the Optical channel Payload Unit (OPU) sublayer that adapts client signal to the OTN frames

Each of this component adds overhead to the packet

![[Pasted image 20240126122313.png]]

