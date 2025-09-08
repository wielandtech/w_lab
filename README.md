### 🏠 w_lab
My Kubernetes homelab: more expensive and less reliable than the cloud, but way more fun!


## 🤖 Motivation
The goal of this project is to give all of my networking toys a home that fits in the attic crawl-space or on a self in the basement.

Eventually, this project will culminate with my own private cloud and self-hosted kubernetes cluster, so I would like to keep performance and upgradability in mind. Going to start with k3s with the eventual goal of Talos.

## 🔧 Hardware
| Piece	| What it is | Cost, as of May 1st, 2025, (*including 6% sales tax) |
|-------|------------| --------------------------|
| **Router/Firewall** | UniFi UCG-Fiber | $295.74* |
| **Cellular Failover Router** | NETGEAR Nighthawk M1 | no longer sold |
| **Access Point** | UniFi U7-Pro-Wall | $199 |
| **Switch A** | UniFi USW-Pro-XG-8-PoE | $528.94* |
| **Switch B** | UniFi USW-Ultra | $136.74* |
| **Patch Cables** | Assorted UniFi Patch Cables | $68.86 |
| **Patch Cables** | Assorted Monoprice Patch Cables | $87.92 |
| **Patch Panel A** | DeskPi 12 Port CAT6 Network Patch Panel | $24.37* |
| **Patch Panel B** | Rapink Mini 12 Port Cat6A Patch Panel | $28 |
| **Compute**	| 3x Dell OptiPlex 7060 (i5 i5-8500T CPU, 16GB RAM, 2.5GbE NIC) | $340.45 |
| **NAS** | Synology DS923+ (2x Seagate IronWolf 8TB RAID1, 2x 500GB WD Red SN700 NVMe, 10GbE NIC) | $1,255* |
| **UPS**	| Tripp Lite 600VA 300W UPS - BC600RNC | $155.09* |
| **UPS**	| 4 Outlet PDU | $14.30* |
| **USB Power**	| 300 W USB‑C charging station | $24.78* |
| **USB C Cables**	| 3x 60W USB-C to USB-C Cables | $10.59* |
| **Misc. Devices** | Philips Hue Bridge | included with lights |
| **Misc. Devices** | Raspberry Pi 2 B | no longer sold |
| **Misc. Devices** | HDHomeRun EXTEND | no longer sold |
| **Mini‑rack** | DeskPi RackMate T2 (10″ 12U) | $195.03* |
| **Mini-rack Accessories** | T2 Metal Shelf, 0.5U Brush Cable Management, 1U Blank, 2x 2U Blank, Mounting Hardware | $94.51* |
| Total | One bad ass closet that'll actually fit in a closet| $3459.32 |



## 🧠 Software Stack
This homelab runs a complete Kubernetes infrastructure with GitOps automation:

| Component | Technology | Purpose |
|-----------|------------|---------|
| **Kubernetes** | K3s | Lightweight Kubernetes distribution |
| **GitOps** | Flux v2 | Automated deployment and configuration management |
| **Ingress** | Traefik | HTTP/HTTPS routing and load balancing |
| **LoadBalancer** | MetalLB | LoadBalancer implementation for bare metal |
| **Storage** | Synology CSI | Integration with NAS for persistent storage |
| **Certificates** | cert-manager | Automated TLS certificate management |
| **Secrets** | Sealed Secrets | Encrypted secrets management for GitOps |

## ⚡ Applications & Services
The cluster hosts a variety of self-hosted applications:

**Media & Entertainment:**
- **<img src="https://cdn.jsdelivr.net/gh/walkxcode/dashboard-icons/svg/plex.svg" width="16" height="16"> Plex Media Server** - Streaming with Intel QuickSync hardware transcoding

**Home Automation:**
- **<img src="https://cdn.jsdelivr.net/gh/walkxcode/dashboard-icons/svg/home-assistant.svg" width="16" height="16"> Home Assistant** - Complete home automation platform

**Monitoring & Observability:**
- **<img src="https://cdn.jsdelivr.net/gh/walkxcode/dashboard-icons/svg/prometheus.svg" width="16" height="16"> Prometheus** - Metrics collection and alerting
- **<img src="https://cdn.jsdelivr.net/gh/walkxcode/dashboard-icons/svg/grafana.svg" width="16" height="16"> Grafana** - Visualization dashboards
- **<img src="https://cdn.jsdelivr.net/gh/walkxcode/dashboard-icons/svg/prometheus.svg" width="16" height="16"> AlertManager** - Alert routing and management

**Dashboard:**
- **🏠 Homepage** - Unified dashboard with service integrations and widgets

## 🔗 Repository Links
- **🔧 Infrastructure Code**: [w_homelab](https://github.com/wielandtech/w_homelab) - Private GitOps repository with Kubernetes manifests
- **📸 Documentation**: [w_lab](https://github.com/wielandtech/w_lab) - Public documentation and photos

## 🙏 Special Thanks
* [**Jeff Geerling**](https://github.com/geerlingguy) — ["Project Mini Rack"](https://github.com/geerlingguy/mini-rack) for inspiring my shopping list.
* [**Mischa van den Burg**](https://github.com/mischavandenburg) — ["K8S Homelab"](https://github.com/mischavandenburg/homelab) for inspiring my stack.

## 📸 Gallery
<table>
  <tr>
    <td align="center" width="50%">
      <a href="https://raw.githubusercontent.com/wielandtech/w_lab/main/w_homelab_front.jpg" target="_blank">
        <img src="https://raw.githubusercontent.com/wielandtech/w_lab/main/w_homelab_front.jpg" alt="Homelab Front View" width="400" style="max-width: 100%; height: auto;">
      </a>
      <br><em>Front View</em>
    </td>
    <td align="center" width="50%">
      <a href="https://raw.githubusercontent.com/wielandtech/w_lab/main/w_homelab_back.jpg" target="_blank">
        <img src="https://raw.githubusercontent.com/wielandtech/w_lab/main/w_homelab_back.jpg" alt="Homelab Back View" width="400" style="max-width: 100%; height: auto;">
      </a>
      <br><em>Back View</em>
    </td>
  </tr>
  <tr>
    <td align="center" width="50%">
      <a href="https://raw.githubusercontent.com/wielandtech/w_lab/main/w_homelab_left.jpg" target="_blank">
        <img src="https://raw.githubusercontent.com/wielandtech/w_lab/main/w_homelab_left.jpg" alt="Homelab Left Side View" width="400" style="max-width: 100%; height: auto;">
      </a>
      <br><em>Left Side View</em>
    </td>
    <td align="center" width="50%">
      <a href="https://raw.githubusercontent.com/wielandtech/w_lab/main/w_homelab_right.jpg" target="_blank">
        <img src="https://raw.githubusercontent.com/wielandtech/w_lab/main/w_homelab_right.jpg" alt="Homelab Right Side View" width="400" style="max-width: 100%; height: auto;">
      </a>
      <br><em>Right Side View</em>
    </td>
  </tr>
</table>
