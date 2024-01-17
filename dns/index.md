# Mutualized Oblivious DNS

## About

This is a web site introducing a new concept of anonymized DNS, called **Mutualized Oblivious DNS** (μODNS). Our implementation, public servers and their detailed information are given below."

---

## Publication

### Research articles

- Extended journal paper:
  > Jun Kurihara, Toshiaki Tanaka, and Takeshi Kubo, "μODNS: A Distributed Approach to DNS Anonymization with Collusion Resistance," *Computer Networks*, Elsevier, vol. 237, p. 110078, Dec. 2023. [Online] Available at [https://doi.org/10.1016/j.comnet.2023.110078](https://doi.org/10.1016/j.comnet.2023.110078).

- Initial concept paper:
  > Jun Kurihara and Takeshi Kubo, "Mutualized oblivious DNS (μODNS): Hiding a tree in the wild forest," [https://arxiv.org/abs/2104.13785v3](https://arxiv.org/abs/2104.13785v3), Jun. 2021

### Presentation slides

- Initial &mu;ODNS concept.
  > Jun Kurihara and Takeshi Kubo, "Mutualized Oblivious DNS (μODNS): Hiding a tree in the wild forest", IEICE NS, Jul. 2021. (in Japanese) [[Slideshare]](https://www.slideshare.net/JunKurihara2/mutualized-oblivious-dns-odns-hiding-a-tree-in-the-wild-forest-249693576)

---

## Implementation as an extension of Oblivious DNS over HTTPS (Being actively developed on GitHub)

We sometimes call this ODoH-based protocol and implementation by **μODoH** or **MODoH**.

### Do53 - μODoH translation proxy written in Rust

- (Source) [https://github.com/junkurihara/doh-auth-proxy](https://github.com/junkurihara/doh-auth-proxy)
- (Docker) [https://hub.docker.com/r/jqtype/doh-auth-proxy](https://hub.docker.com/r/jqtype/doh-auth-proxy)

### μODoH relays and target servers with authentication and access control

- (Source) [https://github.com/junkurihara/modoh-server](https://github.com/junkurihara/modoh-server)
- (Docker) [https://hub.docker.com/r/jqtype/modoh-server](https://hub.docker.com/r/jqtype/modoh-server)

(Replaced [fork of `doh-server`](https://github.com/junkurihara/doh-server))

To protect DNS servers and relays from DoS attacks, authentication is introduced at the first hop relay. So, in addition to the above relay/target, authentication server is needed as below.

- (Source) [https://github.com/junkurihara/rust-token-server](https://github.com/junkurihara/rust-token-server)
- (Docker) [https://hub.docker.com/r/jqtype/id-token-server](https://hub.docker.com/r/jqtype/id-token-server)

### Public relays and servers

Currently we are testing its feasibility.

### Acknowledment
The work on this extension of ODoH to MoDoH is partially supported by NICT22401, JSPS KAKENHI Grant Number JP22K11994, JP21H03442, and KDDI Foundation Research Grant.

---

## PoC implementation based on `Dnscrypt` protocol

### Do53 - μODNS translation proxy (fork of `dnscrypt-proxy`)

- (Source) [https://github.com/junkurihara/dnscrypt-proxy-modns](https://github.com/junkurihara/dnscrypt-proxy-modns)

- (Docker) [https://hub.docker.com/r/jqtype/dnscrypt-proxy-modns](https://hub.docker.com/r/jqtype/dnscrypt-proxy-modns)

### μODNS servers based on `encrypted-dns-server`

- (Source) [https://github.com/junkurihara/encrypted-dns-server-modns](https://github.com/junkurihara/encrypted-dns-server-modns)

- (Docker) [https://hub.docker.com/r/jqtype/encrypted-dns-server-modns](https://hub.docker.com/r/jqtype/encrypted-dns-server-modns)

- (Docker with `unbound` resolver) [https://hub.docker.com/r/jqtype/dnscrypt-server-modns](https://hub.docker.com/r/jqtype/dnscrypt-server-modns)

### Public resolvers and relays

- [https://github.com/junkurihara/experimental-resolvers](https://github.com/junkurihara/experimental-resolvers)

---

## Public DoH Server as an Entry of μODNS

If you want to just check if it works, you can try our DoH-μODNS translator from Chrome and Firefox browsers without using our [dedicated client](https://github.com/junkurihara/dnscrypt-proxy-modns).

This translator converts DoH queries to PoC μODNS queries. It first works as the 'first-hop' relay of μODNS, and randomly choose subsequent (up to 2) relays from listed relays for user anonymity in DNS queries. The DoH address is:

> [https://dns.secarchlab.net/dns-query](https://dns.secarchlab.net/dns-query)

Target full-service resolvers are ones listed in this repo and Quad9 servers of no-filters.

NOTE: Although our experimental resolvers and relays are ones with no log and no filter, the DoH-μODNS filters some content by using public ad lists and logs blocking histories.

Please use this translator only for testing at your own risk, and do not use this translator for your private activity. From the concept of μODNS, you should build your dedicated relay. Also note that it is not guaranteed that our translator works 24/365.

**[[Back to top]](../)**
