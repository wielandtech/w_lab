### 🏠 w_lab
My Kubernetes homelab: more expensive and less reliable than the cloud, but way more fun!

![Image](https://raw.githubusercontent.com/wielandtech/w_lab/main/w_lab_front.jpg)
![Image](https://raw.githubusercontent.com/wielandtech/w_lab/main/w_lab_back.jpg)

#### Motivation
The goal of this project is to give all of my networking toys a home that fits in the attic crawl-space or on a self in the basement.

Eventually, this project will culminate with my own private cloud and self-hosted kubernetes cluster, so I would like to keep performance and upgradability in mind. Going to start with k3s with the eventual goal of Talos.

#### Hardware
| Piece	| What it is | Cost, as of May 1st, 2025, (*including 6% sales tax) |
|-------|------------| --------------------------|
|**Mini‑rack** |DeskPi RackMate T2 (10″ 12U) | $195.03* |
|**Router**	| Amazon Eero Pro 6E | $199, or free with Frontier ISP |
| **Cellular Failover Router** | NETGEAR Nighthawk M1 | no longer sold |
| **Patch Panel** | Rapink Mini 12 Port Cat6A Patch Panel | $28 |
| **Switch** | TP-Link TL-SG108 8 Port Gigabit Switch | $20 |
| **Compute**	| ???? You Decide ???? | $300-$600 |
| **NAS** | Synology DS923+ (2x Seagate IronWolf 8TB RAID1, 2x 500GB WD Red SN700 NVMe) | $1,138.41* |
| **UPS**	| Tripp Lite 600VA 300W UPS - BC600R | $105.99* |
| **USB Power**	| 300 W USB‑C charging station | $24.78* |
| **Misc. Devices** | Philips Hue Bridge | included with lights |
| Total | One bad ass closet that'll actually fit in a closet| $1512.21 |

Really happy that I pulled the trigged when I did. The RackMate T2 is now ~$300 with "shipping" and the tariffs. The Seagate drives jumped $20/ea between when I ordered them on Friday and when they shipped on Monday.

All that really remains now is to decide what sort of compute should I put inside? I have 4.5U open in my T2. I would like to run multi-nodal k8s to mimic a modern cloud devops environment. I don't have any problem with RaspberryPis, but I was thinking that some refurbished enterprise Tiny/Mini/Micro machines might be a better bang per buck given the tariffs. 

I was thinking of starting out with 2x Dell Optiplex 7070 Micro, with i7, 16g RAM, 128 SSD? Anyone else have any suggestions, on either new or used compute to power this rack?

#### Special Thanks 🙌
* **Jeff Geerling** — “Project Mini Rack” for inspiring my Amazon shopping list.
