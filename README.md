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
### Pi-Hole
<img width="2096" height="1098" alt="Screenshot From 2026-03-10 15-37-00" src="https://github.com/user-attachments/assets/d06b2605-a97a-4ab1-aa60-4f2d54395640" />

### Grafana
<img width="2548" height="1181" alt="Screenshot From 2026-03-10 15-39-12" src="https://github.com/user-attachments/assets/f20b5c64-75a2-4301-907a-e467fa8b2455" />



## Author

Billy Baptiste Nitunga
