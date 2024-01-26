Optical Network connects users with optical fiber cables. 
First generation of optical networks are called Passive optical Network because it is composed by passive component like passive splitter. 

Another big difference between first generations of optical network is that the routing, switching and other intelligent function are handled by electronics. 

In the *second generations* of optical network, called WDM-PON, this functions are handled in the optical layer. 

There are two ways to increase the transmission capacity on a fiber:

1) Time division Multiplexing (TDM): Assign time slots to users data packet. This type of technology is used mainly in first generation of Optical Network. 
2) Wavelength Division Multiplexing (WDM): Divide the traffic in wavelengths, each users has yours. This technique allows the transmission of data simultaneously.

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
- 