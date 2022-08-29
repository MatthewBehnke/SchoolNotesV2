# Implementation Of UDP and TCP

## User Datagram Protocol (UDP)

- Goal 
	- Provide application to application communication 
- Idea: Concept of port 
	- Each connection links to a specific port 
		- (srcIP, srcPort, dstIP, dstPort) uniquely identifies each connection 
- Interface 
	- UDP_Send(destIP, buf, port)
	- UDP_Recv(buf, port)
- Service 
	- Send datagram from (srcIP, secPort) to (destIP, destPort)
	- Service is unreliable, but error detection possible 

## UDP Send

- UDP_Send(destIP, buff, port)
	1. Prepare header
		1. source port (usually any available port)
		2. destination port
		3. UDP length
		4. UDP checksum
	2. IP_Send(dstIP, header+buf)

Header: 8 bytes 

## UDP Receive

- UDP_Rece(buf, port)
	1. IP_recv(buf)
	2. Get port information from the udp header encoded in buf
	3. Any listener on port
		1. Yes, drop the payload to the message queue of the listener and wake it up (if it is waiting) 
		2. No, discard the packet 

## Problems of Port 

- Each connection links to a specific port
	- (srcIP, srcPort, dstIP, dstPort) uniquely identifies each connection 
- Totally there are 65535 ports
	- Well known ports (0 -1023)L everyone agrees which services run on these ports
		- ssh:22, http:80, dns:53
		- Access to these ports requires admin privileges 
- Emhemeral ports (most 1024 - 65535) 

## Transmission Control Protocol (TCP)

- Design Goals 
	- Provide app to app communication 
	- messages can be of arbitrary length 
	- provide reliable and in order delivery 
	- provide congestion control and avoidance 
- Basic idea to address reliability 
	- Using timer: sending a packet and waiting for an acknowledgement form the receiver 
		- If the ACK is received within a given time period, the packet is received 
		- otherwise, the packet is assumed to be lost 

## TCP Header 

- Sequence number, ack and advertused window 
- Flags
	- SYN - establishing a TCP connection 
	- FIN - terminating a TCP connection 
	- ACK - set when ack field if valid 
	- URG - urgent data; Urgent pointer says where non-urgent data starts 
	- PUSH - don't wait to fill segment 
	- RESET - abort connection 

## TCP Implementation 

- Start a connection 
- Reliable byte stream delivery from (srcIP, srcPort) to (dstIP, dstPort)
	- Indication if connection fails: rest
- Terminate the connection 


## Connection: 3-Way Handshake 

- Three messages (I.e syn, syn-ack, ack) are exchanged before data transmission 
- Exchange sequence number, total buffer size and the size of the largest segment that can be handled at each side. 


## Why 3WH? 

- Three-way handshake adds 1RTT delay 
	- expensive for small connections such as RPC
- WHY?
	- Congestion control SYN (40 bytes) acts as cheap probe 
		- Both synder and receiver has now has one round trip, which tells some information such as their distance 
	- Protect against delayed packets form other connection (would confuse receiver) 


## DoS: TCP SYN Flooding 

- How it works: exhausting system resources
	- Using a faked IP address
	- Initiates a TCP connection to a server with a faked IP address
		- Sends a SYN message
		- The server responds with a SYN-ACK
		- Since the address does not exist, the server needs to wait until time out 
			- The server never receives the ACK (the final stage of the TCP connection) 
	- Repeat with a new faked IP address 
		- Repeat at a pace faster than the TCP timeouts release the resources 
		- All resources will be used and no more incoming connection requests can be accepted 
- Some common ways to present 
	- Install a firewall
	- Close all ports not in use 
	- Deny requests from unusual IP addresses 

## Termination: 4-Way Handshake 

- Four messages(FIN, ACK, FIN, ACK) are exchanged to terminate a connection
	- FIN from B to A
		- B does not transmit any new data, but is still responsible for any corrupted data 
	- ACK form A to B
	- FIN from A to B
		- After reading all of the bytes from B, A sends FIN to B
	- ACK from B to A 
		- The connection is formally closed 

## Exchange: Stop and Wait

- Send; wait for ack
- if timeout, re-transmit; else repeat 

## Exchange: Go-Back-n (GBN)

- Sliding Window Protocol
	- Trnasmit ip to n unacknowledged packets / bytes 
	- If timeout for ACK(k) retransmit k, k + 1


### Observations 

- Pros:
	- It is possible to fully utilize a link, provided the sliding window size, is large enough. The throughput is $\sim$  (w/RTT)
	- Stop and wait is like w = 1
- Cons:
	- Sender has to buffer all unack packets, because they may require re transmission 
	- Receiver may be able to accept out of order packets, but only up to its buffer limits 


	- 
## Sliding Window Size 

- What size should the window be? 
	- Too small:
		- inefficient, degenerated to S&W when w = 1
	- Too large:
		- more buffer required for both sender and receiver 
		- Transmitting too fast requests in network congestion and packet lost 
- Congestion control 
	- Slow start phase 
		- Initially set to be 1 or 2
		- Increase the window by 1 for each ACK received (this results in multiplicative increase) 
	- Congestion-avoidance phase 
		- The window is increased by only 1 at a time after it is larger than the slow start threshold 
	- In the base a packet is lost, the window is decreased by half  (window / 2)

## Timer 

- The sender needs to set timers in order to know when to re transmit a packet that may have been lost 
- How  to set the timer for? 
	- Too short: may re transmit before data or ACK has arrived, creating duplicates 
	- Too long: if a packet is lost, will take a ling time to recover (inefficient)

## Adaptation 

