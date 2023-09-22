1. **TCP Head-of-Line Blocking**: Even though HTTP/2 introduced multiplexing (multiple requests and responses over a single connection), it was still susceptible to head-of-line blocking at the TCP level. If a single packet was lost, it would block all streams, even if the packet was only relevant to one of them. 
 ![[Pasted image 20230922092126.png]]
2. **Connection Establishment and Handshake Overhead**: Establishing a secure connection using TCP and TLS requires multiple round-trips between the client and the server. This added latency, especially when a new connection was required. QUIC, on which HTTP/3 is built, provides a faster handshake process and supports zero round-trip time (0-RTT) resumption.
![[Pasted image 20230922095438.png]]![[Pasted image 20230922100447.png]]
   
3. **Connection Interruptions Due to Mobility**: When a user's IP address changes, such as when switching between Wi-Fi and cellular data, TCP connections would get terminated. QUIC is designed to handle such IP address or port changes, ensuring smoother transitions and reducing disruptions.
   
4. **Inefficient Connection Migration**: QUIC provides better support for connection migration, which is essential in an increasingly mobile world where users might switch networks or face other connection alterations.
   
5. **Incorporate Advancements in TLS**: HTTP/3 mandates the use of TLS 1.3, the latest version of the Transport Layer Security protocol. TLS 1.3 offers enhanced security and performance over its predecessors.
   
6. **TCP and Congestion Control**: Multiple TCP connections (as is common with HTTP/1.1) independently manage congestion control, which can be inefficient. While HTTP/2 reduced the number of connections, it still faced TCP's head-of-line blocking. QUIC provides a unified approach to congestion control without the head-of-line blocking problem.