# Google Cloud Interconnect

[Google Cloud Interconnect](https://cloud.google.com/interconnect/) provides options to connect your networks together using Dedicated Interconnect, Partner Interconnect, IPsec VPN, Direct Peering, or Carrier Peering.

|        | Dedicated              |           | Shared               |
|--------|------------------------|-----------|----------------------|
| Layer3 | Direct Peering         | Cloud VPN | Carrier Peering      |
| Layer2 | Dedicated Interconnect |           | Partner Interconnect |

Excluding IPsec VPN, by peering with Google you get the benefits of low latency, high throughput connections. This enables fast high volume data transfers or supports latency sensitive applications.

## Explanation

The Internet is a collection of separate and distinct networks referred to as autonomous systems, each one operating under a common framework of globally unique IP addressing and global BGP routing.

The relationships between these networks are generally described by one of the following three categories:

* Transit (or pay) – The network operator pays money (or settlement) to another network for Internet access (or transit).
* Peer (or swap) – Two networks exchange traffic between their users freely, and for mutual benefit.
* Customer (or sell) – A network pays another network money to be provided with Internet access.

Following are the options for interconnecting with Google:

* Dedicated Interconnect:
  * Category: Peer
  * Private IP Support: True
  * Directly connect your on-premises network to your GCP VPC.
  * Require a common point-of-presence with Google.
  * Router requirements must be met.
  * 99.9 or 99.99 SLA with Google
* Partner Interconnect
  * Category: Transit
  * Private IP Support: True
  * SLA is with the service provider
* IPsec VPN:
  * Category: Transit
  * Private IP Support: True
  * Connects your on-premises network to your GCP VPC through an IPsec VPN.
* Direct Peering:
  * Category: Peer
  * Private IP Support: False
  * Uses BGP with public AS numbers.
  * Connect directly to Google to save on egress fees.
  * No SLA
  * Reach all of Google Services
* Carrier Peering:
  * Category: Transit
  * Private IP Support: False
  * Uses BGP with public AS numbers.
  * No SLA
  * Reach all of Google Services
  * If you do not meet the requirements for Direct Peering you can connect with a Carrier Peering partner.

| Connection       | Provides                                              | Capacity                | Requirements   | Access Type |
|------------------|-------------------------------------------------------|-------------------------|----------------|-------------|
| IPSec VPN Tunnel | Encryption Tunnel to VPC Network thru public Internet | 1.5 to 3Mbps per tunnel | On-Prem VPN GW | Internal IP Addresses |
| Dedicated Interconnect | Dedicated Direct connection to VPC Network | 10Gbps per link | Connection in Colo Facility | Internal IP Addresses |
| Partner Interconnect | Dedicated BW connection to VPC Network thru a Service Provider | 50Mbps - 10Gbps per connection | Service Provider | Internal IP Addresses |
| Direct Peering | Dedicated Direct connection to Google's Network | 10Gbps per link | Connection in GCP POP | Exteranl IP Addresses |
| Carrier Peering | Peer thru Service Provider to Google's Public Network | Various based on Service Provider Offering | Service Provider | Exteranl IP Addresses |

__Note:__  
Interconnect - Direct access to RFC1918 IP Addresses in your VPC with SLA.  
Peering - Access to Google public IP Addresses only without SLA. i.e. API, G-Suite
