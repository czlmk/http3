1. **TCP Head-of-Line Blocking**: Even though HTTP/2 introduced multiplexing (multiple requests and responses over a single connection), it was still susceptible to head-of-line blocking at the TCP level. If a single packet was lost, it would block all streams, even if the packet was only relevant to one of them. 
![[Pasted image 20230922092126.png]]

https://cabulous.medium.com/http-3-quic-and-how-it-works-c5ffdb6735b4

2. As TCP, employed by HTTP/2, considers every request (including multiplexed ones) as a single byte stream. This approach employed by TCP is usually the cause of HOL issues during multiplexed streaming in HTTP/2. In HTTP/3, the issue is addressed via implementation of UDP’s out-of-order delivery, where each byte stream is transported independently over the network.