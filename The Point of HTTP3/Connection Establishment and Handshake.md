2. **Connection Establishment and Handshake Overhead**: Establishing a secure connection using TCP and TLS requires multiple round-trips between the client and the server. This added latency, especially when a new connection was required. QUIC, on which HTTP/3 is built, provides a faster handshake process and supports zero round-trip time (0-RTT) resumption.

0-RTT 
![[Pasted image 20230922155558.png]]

Without 0-RTT
![[Pasted image 20230922155531.png]]


https://blog.cloudflare.com/even-faster-connection-establishment-with-quic-0-rtt-resumption/
https://blog.cloudflare.com/the-road-to-quic/#builtinsecurityandperformance

https://medium.com/codavel-blog/quic-vs-tcp-tls-and-why-quic-is-not-the-next-big-thing-d4ef59143efd

https://www.smashingmagazine.com/2021/08/http3-performance-improvements-part2/