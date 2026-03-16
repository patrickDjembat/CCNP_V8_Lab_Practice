# OSPF_V8_Lab_Practice
![Lab Topology](./Topology/OSPF_lab_Topology.png)

## Purpose
Hello network! 👋

While preparing for my CCNP ENARSI exam, I decided to build custom labs to solidify my understanding of each concept. What started as a study exercise has evolved into this project!The goal of this repository is to bridge the gap between theory and practice through hands-on examples, fueled by my 10+ years of experience in the field. Whether you’re also studying for the CCNP or just want to sharpen your skills, I hope you find this helpful.I’d love to hear your thoughts! Feel free to reach out here on LinkedIn if you have any questions or suggestions.

## Getting started

### Images Used
- IOSv Version 15.8(3)M2
- VPCS built in images
  
### Description
Don’t just trust the documentation—verify it. 🛠️

You can use the provided topology to map out the connections in this lab, but I encourage you to double-check every detail. Why? Because in a production environment, documentation is rarely up-to-date. Relying solely on a diagram without verifying it yourself can be a costly mistake.

#### Lab Specs:
- 13 Routers 
- 6 Hosts.
- Protocols: OSPF, RIP, and EIGRP.
- Troubleshooting: 8 active tickets are available now, with more on the way!

[Follow me on LinkedIn](https://www.linkedin.com/in/djembto/) for updates as I add new scenarios.

#### Addressing Table

| Router | Router ID | Interface | OSPF Area | IP Address / Network |
|------|------|------|------|------|
| R01 | 1.1.1.1 | Gi0/0 | Area 1 | 10.1.11.1/24 |
|  |  | Gi0/1 | Area 1 | 10.1.12.1/24 |
| R02 | 2.2.2.2 | Gi0/0 | Area 1 | 10.1.12.2/24 |
|  | | Gi0/1 | Area 0 | 10.1.23.1/24 |
| R03 | 3.3.3.3 | Gi0/1 | Area 0 | 10.1.23.2/24 |
|  |  | Gi0/3 | Area 0 | 10.1.34.1/24 |
|  |  | Gi0/0 | Area 0 | 10.1.36.1/24 |
|  |  | Gi0/2 | Area 0 | 192.168.33.1/24 |
|  |  | Gi0/4 | Area 0 | 10.1.35.1/24 |
|  |  | Gi0/5 | Area 0 | 10.1.101.1/24 |
| R04 | 4.4.4.4 | Gi0/1 | Area 0 | 10.1.34.2/24 |
|  |  | Gi0/0 | Area 0 | 192.168.42.1/24 |
|  | | Gi0/2 | Area 0 | 192.168.46.1/24 |
| R05 | 5.5.5.5 | Gi0/1 | Area 0 | 10.1.35.2/24 |
|  |  | Gi0/0 | Area 4 (NSSA) | 10.1.58.1/24 |
| R06 | 6.6.6.6 | Gi0/0 | Area 0 | 10.1.36.2/24 |
|  |  | Gi0/1 | Area 2 | 10.1.67.1/24 |
| R07 | 7.7.7.7 | Gi0/0 | Area 2 | 10.1.67.2/24 |
|  |  | Gi0/1 | Area 2 | 10.1.79.1/24 |
| R08 | 8.8.8.8 | Gi0/0 | Area 4 (NSSA) | 10.1.58.2/24 |
|  |  | Gi0/1 | Area 4 (NSSA) | 192.168.85.1/24 |
|  |  | Gi0/2 | EIGRP Domain | 192.168.81.1/24 |
| R09 | 9.9.9.9 | Gi0/0 | Area 2 | 10.1.79.2/24 |
|  |  | Gi0/1 | Area 3 | 192.168.94.1/24 |
| R10 | 10.10.10.10 | Gi0/0 | EIGRP Domain | 192.168.81.2/24 |
| R11 | 11.11.11.11 | Gi0/0 | Area 0 | 10.1.101.2/24 |
|  |  | Gi0/1 | Area 4 (Totally NSSA) | 10.1.112.1/24 |
| R12 | 12.12.12.12 | Gi0/0 | Area 4 (Totally NSSA) | 10.1.112.2/24 |
|  |  | Gi0/1 | RIP Domain | 10.1.123.1/24 |
| R13 | 13.13.13.13 | Gi0/0 | RIP Domain | 10.1.123.2/24 |

## Project Structure
```bash
│
├── README.md
├── Topology/
│   ├── OSPF_lab_topology.png
│
├── configs/
│   ├── initial-working-config/
│       ├── R01.cfg
│       ├── R02.cfg
│       ├── R03.cfg
│       ├── R04.cfg
│       ├── R05.cfg
│       ├── R06.cfg
│       ├── R07.cfg
│       ├── R08.cfg
│       ├── R09.cfg
│       ├── R10.cfg
│       ├── R11.cfg
│       ├── R12.cfg
│       └── R13.cfg
│
├── trouble-ticket-1/
│   ├── lab-guide.md
│   ├── running-config/
│   │   ├── R01.cfg
│   │   ├── R02.cfg
│   │   ├── R03.cfg
│   └── troubleshooting-walkthrough.md
│
├── trouble-ticket-2/
├── trouble-ticket-3/
├── trouble-ticket-4/
├── trouble-ticket-5/
├── trouble-ticket-6/
├── trouble-ticket-7/
├── trouble-ticket-8/
└── eve-ng/
    └── lab.unl
```

Under each trouble ticket, you will find the configuration for the devices which were changed for this specific scenario.

### Disclaimer
- This is a lab topology and is in no shape and form representative of the topology with my current or formers employers.
- Before Using anything discuss here, please review with your team before applying it on a live network as each and every network behaves differently.
- This is Network Engineering, and there is no single way to achieve a goal. Our goal is to learn while developping an optimal way to achieve the same objectif.
