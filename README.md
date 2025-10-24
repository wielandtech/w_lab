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
| **Access Point** | UniFi U7-Pro-Wall | $210.94* |
| **Switch A** | UniFi USW-Pro-XG-8-PoE | $528.94* |
| **Switch B** | UniFi USW-Ultra | $136.74* |
| **Patch Cables** | Assorted UniFi Patch Cables | $68.86* |
| **Patch Cables** | Assorted Monoprice Patch Cables | $87.92* |
| **Patch Panel A** | DeskPi 12 Port CAT6 Network Patch Panel | $24.37* |
| **Patch Panel B** | Rapink Mini 12 Port Cat6A Patch Panel | $29.68* |
| **Compute**	| 3x Dell OptiPlex 7060 (i5 i5-8500T CPU, 16GB RAM, 2.5GbE NIC) | $340.45 |
| **NAS** | Synology DS923+ (2x Seagate IronWolf 8TB RAID1, 2x 500GB WD Red SN700 NVMe, 10GbE NIC) | $1,255* |
| **UPS**	| Tripp Lite 600VA 300W UPS - BC600RNC | $155.09* |
| **PDU**	| 4 Outlet PDU | $14.30* |
| **USB Power**	| 300 W USB‑C charging station | $24.78* |
| **USB C Cables**	| 3x 60W USB-C to USB-C Cables | $10.59* |
| **Misc. Devices** | Philips Hue Bridge | included with lights |
| **Misc. Devices** | Raspberry Pi 2 B | no longer sold |
| **Misc. Devices** | HDHomeRun EXTEND | no longer sold |
| **Mini‑rack** | DeskPi RackMate T2 (10″ 12U) | $195.03* |
| **Mini-rack Accessories** | T2 Metal Shelf, 0.5U Brush Cable Management, 1U Blank, 2x 2U Blank, Mounting Hardware | $94.51* |
| Total | One bad ass closet that'll actually fit in a closet| $3472.94* |



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
| **Database** | CloudNativePG + Redis | Production-ready PostgreSQL operator + caching layer |
| **Monitoring** | Prometheus + Grafana + Netdata | Metrics collection, visualization, and AI-powered troubleshooting |
| **Automation** | Renovate + n8n | Dependency updates and workflow automation |

## ⚡ Applications & Services
The cluster hosts a variety of self-hosted applications:

**Media & Entertainment:**
- **<img src="https://cdn.jsdelivr.net/gh/walkxcode/dashboard-icons/svg/plex.svg" width="16" height="16"> [Plex Media Server](https://www.plex.tv/)** - Streaming with Intel QuickSync hardware transcoding ([Install Guide](https://support.plex.tv/articles/200264746-quick-start-step-by-step-guides/))
- **<img src="https://cdn.jsdelivr.net/gh/walkxcode/dashboard-icons/svg/radarr.svg" width="16" height="16"> [Radarr](https://radarr.video/)** - Movie collection manager and downloader ([GitHub](https://github.com/Radarr/Radarr))
- **<img src="https://cdn.jsdelivr.net/gh/walkxcode/dashboard-icons/svg/sonarr.svg" width="16" height="16"> [Sonarr](https://sonarr.tv/)** - TV series collection manager and downloader ([GitHub](https://github.com/Sonarr/Sonarr))
- **<img src="https://cdn.jsdelivr.net/gh/walkxcode/dashboard-icons/svg/lidarr.svg" width="16" height="16"> [Lidarr](https://lidarr.audio/)** - Music collection manager and downloader ([GitHub](https://github.com/Lidarr/Lidarr))
- **<img src="https://cdn.jsdelivr.net/gh/walkxcode/dashboard-icons/svg/bazarr.svg" width="16" height="16"> [Bazarr](https://www.bazarr.media/)** - Subtitle management for movies and TV shows ([GitHub](https://github.com/morpheus65535/bazarr))
- **<img src="https://cdn.jsdelivr.net/gh/walkxcode/dashboard-icons/svg/ombi.svg" width="16" height="16"> [Ombi](https://ombi.io/)** - Media request management system ([GitHub](https://github.com/Ombi-app/Ombi))
- **<img src="https://cdn.jsdelivr.net/gh/homarr-labs/dashboard-icons/svg/commafeed.svg" width="16" height="16"> [CommaFeed](https://www.commafeed.com/)** - Self-hosted RSS reader and aggregator ([GitHub](https://github.com/Athou/commafeed))

**Home Automation:**
- **<img src="https://cdn.jsdelivr.net/gh/walkxcode/dashboard-icons/svg/home-assistant.svg" width="16" height="16"> [Home Assistant](https://www.home-assistant.io/)** - Complete home automation platform ([Installation Guide](https://www.home-assistant.io/installation/) | [GitHub](https://github.com/home-assistant/core))

**Monitoring & Observability:**
- **<img src="https://cdn.jsdelivr.net/gh/walkxcode/dashboard-icons/svg/prometheus.svg" width="16" height="16"> [Prometheus](https://prometheus.io/)** - Metrics collection and alerting with 30-day retention ([Installation Guide](https://prometheus.io/docs/prometheus/latest/installation/) | [GitHub](https://github.com/prometheus/prometheus))
- **<img src="https://cdn.jsdelivr.net/gh/walkxcode/dashboard-icons/svg/grafana.svg" width="16" height="16"> [Grafana](https://grafana.com/)** - Visualization dashboards with persistent storage ([Installation Guide](https://grafana.com/docs/grafana/latest/setup-grafana/installation/) | [GitHub](https://github.com/grafana/grafana))
- **<img src="https://cdn.jsdelivr.net/gh/walkxcode/dashboard-icons/svg/prometheus.svg" width="16" height="16"> [AlertManager](https://prometheus.io/docs/alerting/latest/alertmanager/)** - Alert routing and management ([GitHub](https://github.com/prometheus/alertmanager))
- **<img src="https://cdn.jsdelivr.net/gh/walkxcode/dashboard-icons/svg/prometheus.svg" width="16" height="16"> [Blackbox Exporter](https://prometheus.io/docs/guides/multi-target-exporter/)** - External endpoint monitoring and health checks ([GitHub](https://github.com/prometheus/blackbox_exporter))
- **<img src="https://cdn.jsdelivr.net/gh/walkxcode/dashboard-icons/svg/netdata.svg" width="16" height="16"> [Netdata](https://www.netdata.cloud/)** - Real-time monitoring with AI-powered troubleshooting and per-second metrics collection ([Installation Guide](https://learn.netdata.cloud/docs/agent/packaging/installer/) | [GitHub](https://github.com/netdata/netdata))

**Dashboard & Management:**
- **🏠 [Homepage](https://gethomepage.dev/)** - Unified dashboard with service integrations and widgets ([GitHub](https://github.com/gethomepage/homepage))
- **<img src="https://cdn.jsdelivr.net/gh/walkxcode/dashboard-icons/svg/n8n.svg" width="16" height="16"> [n8n](https://n8n.io/)** - Workflow automation platform with 400+ integrations ([Installation Guide](https://docs.n8n.io/hosting/) | [GitHub](https://github.com/n8n-io/n8n))

**Infrastructure & DevOps:**
- **<img src="https://cdn.jsdelivr.net/gh/walkxcode/dashboard-icons/svg/postgresql.svg" width="16" height="16"> [PostgreSQL](https://www.postgresql.org/)** - Production-ready database clusters with CloudNativePG ([Installation Guide](https://www.postgresql.org/docs/current/installation.html) | [GitHub](https://github.com/postgres/postgres))
- **<img src="https://cdn.jsdelivr.net/gh/walkxcode/dashboard-icons/svg/redis.svg" width="16" height="16"> [Redis](https://redis.io/)** - In-memory data store for caching and sessions ([Installation Guide](https://redis.io/docs/getting-started/installation/) | [GitHub](https://github.com/redis/redis))
- **<img src="https://cdn.jsdelivr.net/gh/walkxcode/dashboard-icons/svg/renovate.svg" width="16" height="16"> [Renovate](https://renovatebot.com/)** - Automated dependency updates and security patches ([Documentation](https://docs.renovatebot.com/) | [GitHub](https://github.com/renovatebot/renovate))

**Web Services:**
- **<img src="https://cdn.jsdelivr.net/gh/walkxcode/dashboard-icons/svg/python.svg" width="16" height="16"> [WielandTech Website](https://wielandtech.com/)** - Personal portfolio and blog self-hosted on the homelab cluster ([GitHub](https://github.com/wielandtech/w_tech))

## 🔗 Repository Links
- **🔧 Infrastructure Code**: [w_homelab](https://github.com/wielandtech/w_homelab) - Private GitOps repository with Kubernetes manifests
- **📸 Documentation**: [w_lab](https://github.com/wielandtech/w_lab) - Public documentation and photos
- **🌐 Personal Website**: [wielandtech.com](https://wielandtech.com/) - Self-hosted portfolio and blog ([Source Code](https://github.com/wielandtech/w_tech))

## 🙏 Special Thanks
* [**Jeff Geerling**](https://github.com/geerlingguy) — ["Project Mini Rack"](https://github.com/geerlingguy/mini-rack) for inspiring my shopping list.
* [**Mischa van den Burg**](https://github.com/mischavandenburg) — ["K8S Homelab"](https://github.com/mischavandenburg/homelab) for inspiring my stack.

### 🖨️ 3D Print Files
* [**Mauker**](https://www.printables.com/@Mauker_) — [Unifi USW-Ultra 10-inch Rack Mount](https://www.printables.com/model/963100-unifi-usw-ultra-10-inch-rack-mount), [Unifi UCG-Fiber 10-inch Rack Mount](https://www.printables.com/model/1235928-unifi-ucg-fiber-10-inch-rack-mount), [10-inch 1U Keystone Patchpanel x8 ports](https://www.printables.com/model/1180979-10-inch-12u-keystone-patchpanel-x8-ports)
* [**TimPrints**](https://www.printables.com/@TimPrints_686384) — [Dell OptiPlex 7060 MicroPC 10 Inch Rack Mount](https://www.printables.com/model/980541-dell-optiplex-7060-micropc-10-inch-rack-mount)

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
