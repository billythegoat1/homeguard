# Installation Guide

## Prerequisites
- Raspberry Pi 4 (4GB RAM recommended)
- Raspberry Pi OS installed
- Internet connection

## Step 1: Set Static IP
```bash
sudo nmcli connection modify "Wired connection 1" \
  ipv4.addresses 192.168.0.101/24 \
  ipv4.gateway 192.168.0.1 \
  ipv4.dns "8.8.8.8" \
  ipv4.method manual
```

## Step 2: Install Pi-hole
```bash
curl -sSL https://install.pi-hole.net | bash
```

## Step 3: Install UFW
```bash
sudo apt update
sudo apt install ufw -y
sudo ufw allow 22/tcp
sudo ufw allow 53/tcp
sudo ufw allow 53/udp
sudo ufw allow 80/tcp
sudo ufw allow 3000/tcp
sudo ufw default deny incoming
sudo ufw enable
```

## Step 4: Install Prometheus
```bash
sudo apt install prometheus -y
sudo systemctl start prometheus
sudo systemctl enable prometheus
```

## Step 5: Install Pi-hole Exporter
```bash
sudo docker run -d -p 9617:9617 \
  -e PIHOLE_HOSTNAME=192.168.0.101 \
  -e PIHOLE_PASSWORD='your_password' \
  ekofr/pihole-exporter:latest
```

## Step 6: Install Grafana
```bash
wget -q -O - https://packages.grafana.com/gpg.key | \
  sudo gpg --dearmor -o /usr/share/keyrings/grafana.gpg
echo "deb [signed-by=/usr/share/keyrings/grafana.gpg] https://packages.grafana.com/oss/deb stable main" | \
  sudo tee /etc/apt/sources.list.d/grafana.list
sudo apt update
sudo apt install grafana -y
sudo systemctl start grafana-server
```

## Access
- Pi-hole: http://192.168.0.101/admin
- Grafana: http://192.168.0.101:3000
- Prometheus: http://192.168.0.101:9090
