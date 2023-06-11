The User Datagram Protocol, or UDP, is a communication protocol used across the Internet for especially time-sensitive transmissions such as video playback or [DNS](https://www.cloudflare.com/learning/dns/what-is-dns/) lookups. It speeds up communications by not formally establishing a connection before data is transferred. This allows data to be transferred very quickly, but it can also cause [packets](https://www.cloudflare.com/learning/network-layer/what-is-a-packet/) to become lost in transit — and create opportunities for exploitation in the form of [DDoS attacks](https://www.cloudflare.com/learning/ddos/what-is-a-ddos-attack/).

![[Pasted image 20221023103513.png]]


UDP is faster but less reliable than [TCP](https://www.cloudflare.com/learning/ddos/glossary/tcp-ip/), another common transport protocol. In a TCP communication, the two computers begin by establishing a connection via an automated process called a ‘handshake.’ Only once this handshake has been completed will one computer actually transfer data packets to the other.

UDP communications do not go through this process. Instead, one computer can simply begin sending data to the other: