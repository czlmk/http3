http structures
![[Pasted image 20230922092305.png]]
QUIC Packet
![[Pasted image 20230922092456.png]]
* EG.
	QUIC IETF  
	QUIC Connection information  
	[Packet Length: 1350]  
	1... .... = Header Form: Long Header (1)  
	.1.. .... = Fixed Bit: True  
	..00 .... = Packet Type: Initial (0)  
	.... 00.. = Reserved: 0  
	.... ..00 = Packet Number Length: 1 bytes (0)  
	Version: draft-29 (0xff00001d)  
	Destination Connection ID Length: 8  
	Destination Connection ID: 45fb5955dfaa8914  
	Source Connection ID Length: 0  
	Token Length: 0  
	Length: 1332  
	Packet Number: 1  
	Payload: 5a99e5b29413627619ca3b5add4cf8b6ce348355b1c1a2be9874c7961e7996a24aeec860…  
	TLSv1.3 Record Layer: Handshake Protocol: Client Hello  
	PADDING Length: 997
	QUIC Frames
![[Pasted image 20230922092809.png]]
* EG.
	TLSv1.3 Record Layer: Handshake Protocol: Client Hello  
	Frame Type: CRYPTO (0x0000000000000006)  
	Offset: 0  
	Length: 314  
	Crypto Data  
	Handshake Protocol: Client Hello

HTTP/3 Frame
![[Pasted image 20230922093142.png]]
UDP Packet
![[Pasted image 20230922141034.png]]