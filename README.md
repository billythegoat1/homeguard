# HomeGuard

Network security platform for home networks using Raspberry Pi 4.

## What does HomeGuard do ?

- Blocks malicious domains with Pi-hole DNS filtering
- Enforces firewall rules with UFW
- Monitors network activity via Grafana dashboard

## How does it work ?

All devices on your network use the Pi as their DNS server. Pi-hole blocks bad domains. UFW blocks unauthorized connections. Prometheus collects the data. Grafana shows you what's happening.

## Hardware

- Raspberry Pi 4 (4GB)
- 32GB microSD card
- Ethernet cable


## Stack

- Pi-hole - DNS filtering
- UFW - Firewall
- Prometheus - Metrics
- Grafana - Dashboard
- Docker - Exporters

## Status

✅ Pi-hole running and blocking threats
✅ UFW firewall active
✅ Prometheus collecting metrics
✅ Grafana dashboard live

🚧 UFW log integration
🚧 Email alerts

## Screenshots

[Coming soon]

## Author

Billy Baptiste Nitunga
