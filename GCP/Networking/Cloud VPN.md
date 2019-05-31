# Google Cloud Virtual Private Network

[Google Cloud VPN](https://cloud.google.com/vpn/docs/concepts/overview) securely connects your on-premises network to your Google Cloud Platform (GCP) Virtual Private Cloud (VPC) network through an IPsec VPN connection.

## Features

* 99.9% availability.
* Site-to-site VPN (star topology).
* Routing via static or dynamic routes using Cloud Router.
* Supports IKE V1 & V2 pre-shared keys.
* Uses Encapsulated Security Payload (ESP) in tunnel mode with authentication.
* Maximum MTU 1460 bytes

__Note:__ ESP Authentication Headers (AH) or ESP in Transport mode are not supported.

## Performance

* Each VPN has a maximum throughput of 3Gbps.
* Use Equal-Cost Multipath (ECMP) routing over multiple VPNs to achieve greater overall throughput.

## When to Use

* When you have a dedicated client side VPN gateway.
* Point-to-site VPN is not supported.
* Useful for low volume data connections
