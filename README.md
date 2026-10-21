# Awesome-DNS-Network-Security

# Top DNS & Network Security Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on DNS Filtering, Secure Web Gateways & Zero Trust Network Access*  
**Last updated: October 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **DNS & Network Security**. These tools enable organizations to filter malicious domains, block trackers and ads, enforce acceptable use policies, and secure outbound traffic—from cloud-delivered secure web gateways to self-hosted DNS sinkholes that protect every device on a network without per-device configuration.

**Examples** include Cisco Umbrella, Cloudflare Zero Trust, Zscaler Internet Access, Palo Alto Prisma Access, DNSFilter, NextDNS, Akamai Enterprise Threat Protector, Infoblox BloxOne, Forcepoint, and Barracuda Content Shield (the category leaders).

**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, encrypted DNS, and open network filtering—ideal for privacy-conscious users, homelab enthusiasts, and organizations seeking transparent, vendor-independent DNS security.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[Cisco Umbrella](https://umbrella.cisco.com/)**  
  **Cloud-delivered secure web gateway** with DNS-layer security, SSL inspection, and firewall. **Pricing**: **Standard at $4/month** per user (annualized $48/year); no free tier available . **Best for**: enterprises wanting Cisco-integrated DNS security.

- **[Cloudflare Zero Trust (Gateway)](https://www.cloudflare.com/zero-trust/)**  
  **SASE platform with DNS filtering, secure web gateway, and ZTNA**. **Pricing**: **Free plan** for up to **50 users** with DNS filtering and basic policies; paid plans from **$7/user/month**. **Best for**: teams wanting a generous free tier with enterprise-grade infrastructure.

- **[Zscaler Internet Access](https://www.zscaler.com/)**  
  **Cloud-native secure web gateway** with SSL inspection, DLP, and sandboxing. **Pricing**: Quote-only enterprise contracts; no free tier. **Best for**: large enterprises needing comprehensive SASE.

- **[Palo Alto Prisma Access](https://www.paloaltonetworks.com/prisma/access)**  
  **Cloud-delivered SASE** combining ZTNA, CASB, and threat prevention. **Pricing**: Quote-only; no free tier. **Best for**: Palo Alto ecosystem organizations.

- **[DNSFilter](https://www.dnsfilter.com/)**  
  **DNS-layer threat protection** with content filtering and roaming client. **Pricing**: **Free plan** for 1 user/1 network; paid from **$1/user/month**. **Best for**: MSPs and small businesses wanting affordable DNS filtering.

- **[NextDNS](https://nextdns.io/)**  
  **Cloud-based DNS filtering** with ad blocking, parental controls, and encrypted DNS. **Pricing**: **Free tier** includes **300,000 queries/month** with unlimited devices . Paid plans from **~$1.99/month** for unlimited queries. **Best for**: individuals and families wanting privacy-focused DNS filtering.

- **[Akamai Enterprise Threat Protector](https://www.akamai.com/)**  
  **Cloud-based DNS security** with threat intelligence from Akamai's global network. **Pricing**: Quote-only; no free tier. **Best for**: enterprises already on Akamai CDN.

- **[Infoblox BloxOne Threat Defense](https://www.infoblox.com/)**  
  **DNS security platform** combining on-prem and cloud with DDI integration. **Pricing**: Quote-only; no free tier. **Best for**: enterprises needing DNS infrastructure and security together.

- **[Forcepoint](https://www.forcepoint.com/)**  
  **Cloud and on-prem secure web gateway** with behavioral analytics. **Pricing**: Quote-only; no free tier. **Best for**: government and defense organizations.

- **[Barracuda Content Shield](https://www.barracuda.com/)**  
  **DNS filtering and content security** for schools and businesses. **Pricing**: Quote-only; no free tier. **Best for**: education and SMB markets.

## Open-Source GitHub Projects

- **[AdGuard Home](https://github.com/AdguardTeam/AdGuardHome)**  
  **Network-wide ads & trackers blocking DNS server** (GPL-3.0) — **the most widely adopted open-source DNS filter** with **~34,800 GitHub stars** . **Native DoH/DoT/DoQ support**—encrypted DNS without sidecar services . **Features**: **per-client filtering rules**, **parental controls + Safe Search enforcement**, **DHCP server**, **DNS rewrites**, and **low resource usage (~60-80 MB RAM)** . **The reference implementation for open-source DNS filtering**—choose when you want the most complete self-hosted solution with native encrypted DNS.

- **[Pi-hole](https://github.com/pi-hole/pi-hole)**  
  **Network-wide ad blocker and DNS sinkhole** (EUPL) — **the original and most widely known DNS sinkhole** with **50,000+ GitHub stars** . **Blocks ads on every device** including smart TVs, game consoles, and IoT—no browser extension required . **Gravity database** processes millions of blocked domain patterns across hundreds of community blocklists . **Built-in DHCP server** simplifies network configuration . **The trade-offs**: **no native DoH/DoT**—requires Unbound or cloudflared sidecar for encrypted upstream queries ; **higher resource usage than AdGuard Home** . **Best for**: teams wanting the largest community and most battle-tested sinkhole.

- **[Blocky](https://github.com/0xERR0R/blocky)**  
  **Fast and lightweight DNS proxy as ad-blocker for local network** (Apache-2.0) — **the config-as-code choice** . **~10-30 MB RAM**—the lightest option available. **YAML configuration**—version-control friendly. **Native DoH/DoT** without sidecars. **Built-in DNSSEC validation**, **Prometheus metrics**, and **multi-instance sync via Redis**. **The trade-off**: **no web UI**—API only . **Best for**: infrastructure-as-code practitioners and resource-constrained hardware.

- **[Technitium DNS Server](https://github.com/TechnitiumSoftware/DnsServer)**  
  **Authoritative and recursive DNS server with built-in blocking** (GPL-3.0) — **the all-in-one DNS choice** . **Version 14** adds **clustering** (manage multiple DNS servers from one console) and **TOTP 2FA** . **Recursive resolver, sinkhole with blocklists, and authoritative zone server all in one process** . **Features**: **DoH/DoT/DoQ**, **DNSSEC**, **multi-network DHCP**, **clustering**, and **apps for DNS64, DNS Rebinding Protection, and Advanced Forwarding** . **Best for**: teams wanting DNS sinkholing, recursive resolution, and zone hosting in one tool.

- **[Unbound](https://github.com/NLnetLabs/unbound)**  
  **Validating, recursive, and caching DNS resolver** (BSD-3-Clause) — **the DNSSEC-first choice** . **Built-in DNSSEC validation** and **modern DNS features** for security and speed . **Often paired with Pi-hole** as the upstream resolver for encrypted queries . **Best for**: teams wanting a secure recursive resolver as the foundation for their filtering stack.

- **[dnscrypt-proxy](https://github.com/DNSCrypt/dnscrypt-proxy)**  
  **Flexible DNS proxy with support for encrypted DNS protocols** (ISC) — **the protocol-flexibility choice** . **Supports DNSCrypt, DoH, and ODoH**—encrypts DNS queries between the client and resolver. **Best for**: teams wanting protocol flexibility and anonymized DNS.

- **[Stubby](https://github.com/getdnsapi/stubby)**  
  **Local DNS Privacy stub resolver** (BSD-3-Clause) — **the DNS-over-TLS specialist** . **Encrypts DNS queries sent from the local machine to a DNS Privacy resolver** using DNS-over-TLS . **Strict Privacy mode** with certificate pinning. **Best for**: technical users wanting simple DoT encryption without a full filtering server.

- **[modDNS (IVPN)](https://github.com/ivpn/moddns)**  
  **Full-stack DNS security platform** (GPL-3.0) — **the audited, feature-rich choice** . **Features**: **DoH, DoT, DoQ**, **built-in blocklists** (AdGuard, Hagezi, OISD, StevenBlack), **custom allow/deny rules per profile**, **DNS rebinding protection**, **MFA (TOTP and WebAuthn)**, **near real-time query logging**, and **Prometheus metrics** . **Microservices architecture** (Go, MongoDB, Redis, React) . **Best for**: teams wanting a production-grade, auditable DNS security platform with multi-profile support.

### Additional Strong Open-Source Options

- **CoreDNS** — DNS server with plugin architecture (Apache-2.0). **Best for**: Kubernetes-native DNS service discovery.
- **dnsmasq** — Lightweight DNS forwarder and DHCP server (GPL-2.0). **Best for**: simple local network DNS and DHCP.
- **BIND 9** — The original DNS server (MPL-2.0). **Best for**: authoritative DNS hosting with DNSSEC.
- **Grafana** — Dashboards for DNS query analytics (AGPL-3.0). **Best for**: visualizing Pi-hole or AdGuard Home metrics.
- Community **n8n** workflows for DNS query alerting and blocklist update automation.

**Frameworks for building custom systems**: Combine **AdGuard Home** for all-in-one DNS filtering with **Unbound** for DNSSEC-validating recursion, **Blocky** for config-as-code deployments, **Technitium** for clustering and zone hosting, and **modDNS** for audited enterprise-grade security—creating a comprehensive open-source DNS security stack.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- DNS security tools handling network traffic must comply with privacy regulations (GDPR, CCPA, etc.) and organizational acceptable use policies.
- **The "cloud SWG vs. self-hosted sinkhole" distinction matters.** **Cisco Umbrella, Zscaler, and Cloudflare Gateway** provide cloud-delivered protection for roaming devices—no local infrastructure, but traffic routes through the vendor . **AdGuard Home, Pi-hole, and Blocky** protect devices on your local network—no traffic leaves your infrastructure, but **remote devices require a VPN** to benefit . **Choose based on whether you need roaming protection or network-level control.**
- **AdGuard Home is the best all-around open-source choice for most teams.** **Native DoH/DoT/DoQ** without sidecars, **parental controls**, **per-client rules**, and **~34,800 GitHub stars** . **Pi-hole's larger community** (50,000+ stars) comes with **no native encrypted DNS**—you need Unbound or cloudflared .
- **Pi-hole's limitation is real.** **No native DoH/DoT** means you either run it without encrypted upstream queries or add a sidecar service . **AdGuard Home solves this out of the box** .
- **Blocky is for config-as-code teams.** **YAML configuration, no web UI, ~10-30 MB RAM**—**the lightest option** . **Choose when you want DNS filtering managed like infrastructure, not like an appliance.**
- **Technitium's clustering is a genuine enterprise feature.** **Version 14** lets you manage multiple DNS servers from one console . **If you're running DNS at multiple sites, Technitium avoids per-site management overhead.**
- Self-hosted open-source solutions require proper network configuration (router DNS settings), blocklist maintenance, and ongoing monitoring. **DNS is your first line of network defense**—misconfiguration can break connectivity or leave gaps.

---

**Made for security engineers, network administrators, and organizations building transparent DNS security solutions.**  
Let's make DNS & Network Security more open, data-driven, and resilient.
