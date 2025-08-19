# Edge Computing for Conservation

*A curated, community-maintained hub for **edge computing** and **edge AI** methods, tools, datasets, and deployments in conservation.*

This survey is intended to consolidate projects and resources for deploying edge AI for conservation. This page is maintained by [Jenna Kline](https://jennamk14.github.io/). Contributions are welcome! Please submit additions or corrections as Github pull requests.


## Table of Contents

* [Why this repo?](#why-this-repo)
* [Scope & taxonomy](#scope--taxonomy)
* [Resources](#resources)
  * [Cyberinfrastructure for Edge AI](#cyberinfrastructure-for-edge-ai)
    * [Edge platforms & devices](#edge-platforms--devices)
    * [Smart Sensors/Platforms](#smart-sensorsplatforms)
    * [AI Models for Edge](#ai-models-for-edge)
  * [Projects](#projects)
  * [Papers](#papers)
    * [What is edge AI?](#what-is-edge-ai)
    * [Acoustics](#acoustics)
    * [Biologgers](#biologgers)
    * [Drones (Aerial and Marine)](#drones-aerial-and-marine)
    * [Camera traps](#camera-traps)
* [Contributing](#contributing)
* [Maintainers](#maintainers)
* [License](#license)


## Why this repo?

Edge AI is transforming wildlife monitoring and ecosystem science by running perception, decision-making, and data analysis on-device and in the field . 
Relevant projects, tools, and papers, span multiple subfields (computer systems, AI, robotics, acoustics, ecology). 
This repo aggregates references and resources: what to use, how to deploy, and where to learn from real-world efforts.
This repo is intended to be a **living document** that evolves with the field.

### How this repo relates to prior work

This project is inspired by excellent modality-specific surveys, including 
[Everything I know about ML and camera traps](https://agentmorris.github.io/camera-trap-ml-survey/) maintained by Dan Morris 
and [Computer Vision and Aerial Imagery for Wildlife Conservation](https://bkellenb.github.io/cv-for-wildlife-aerial-imagery/)
maintained by Dan Morris and Benjamin Kellenberger. This repo aims to broaden to **multi-modal edge AI for conservation** 
with a consistent taxonomy, runnable examples, and deployment-first guidance.



## Scope & taxonomy

This project prioritizes:

* **On-device AI** (Raspberry Pi/CM, Jetson, microcontrollers; phones/laptops as edge devices).
* **Conservation sensing modalities:** drones/UAS, camera traps, bioacoustics, GPS/biologgers, ect.
* **Pipelines & operations:** data curation, training, optimization, evaluation, deployment, monitoring, and governance.
* **Cross-modality**: how to integrate data across sensors and modalities (e.g., camera trap + drone + bioacoustics).
* **Distributed edge systems**: how to deploy and manage edge AI in remote or low-connectivity environments.
* **Optimization for the edge**: quantization, pruning, distillation, and other techniques to improve model performance on edge devices.

> Out of scope: purely cloud-only analytics without an edge component.

## Resources

### Cyberinfrastructure for Edge AI

#### Edge platforms & Devices

| Platform                         | What it is                                         | Links                                                                                                                                                                                |
| -------------------------------- | -------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| NVIDIA Jetson (Nano / Orin Nano) | Embedded GPU modules for on-device AI              | [Jetson Nano](https://developer.nvidia.com/embedded/jetson-nano), [Orin Nano](https://developer.nvidia.com/embedded/learn/get-started-jetson-orin-nano-devkit)                       |
| Raspberry Pi                     | Single-board computers for far‑edge deployments    | [raspberrypi.com](https://www.raspberrypi.com/)                                                                                                                                      |
| Google Coral                     | Edge TPU accelerators and dev boards               | [coral.ai](https://coral.ai/), [Docs](https://coral.ai/docs/)                                                                                                                        |
| Seeed Studio LoRaWAN Dev Kit     | LoRaWAN gateway/dev kit for LPWAN edge sensing     | [Product](https://www.seeedstudio.com/Seeed-Studio-LoRaWAN-Dev-Kit-p-5370.html)                                                                                                      |
| Edge Impulse                     | Edge ML platform (data→model→deploy; MCUs & Linux) | [edgeimpulse.com](https://edgeimpulse.com/)                                                                                                                                          |
| Conservation X Labs              | Conservation tech and open innovation ecosystem    | [conservationxlabs.com](https://conservationxlabs.com/)   |
| Animl                            | Camera trap platform - see 'Lessons learned from deploying and managing wireless camera trap networks in remote environments' for edge AI specific guidelines                     | [animl.camera](https://guides.animl.camera/) [YouTube](https://youtu.be/oF-8bnVymv8)    [Report](https://bioone.org/journals/western-north-american-naturalist/volume-85/issue-2/064.085.0220/Real-Time-Island-Biosecurity-Surveillance--Evaluating-a-Wireless-Camera/10.3398/064.085.0220.short)                                                                                                                                     |       

#### Smart Sensors & Platforms
| Sensor Type                      | What it is                                         | Links                                                                                                                                                                                |
| -------------------------------- | -------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| BirdWeather                      | AI powered bioacoustics platform                   | https://www.birdweather.com/                                                                                                                                                         |
| WildWing                         | Open-source drone for animal behavior monitoring | [WildWing Project](https://imageomics.github.io/wildwing/)                                                                                                                                |
| Sentinel Hub                    | Smart camera trap plaform, democratizing AI for wildlife and disease monitoring             | [Sentinel Project](https://sentinel.conservationxlabs.com/)                                                                                                     |
| Mini AI Wildlife Monitor with Raspberry Pi AI Camera| AI edge compute based wildlife detection | [Discussion Post](https://wildlabs.net/discussion/mini-ai-wildlife-monitor) [YouTube Video](https://www.youtube.com/watch?v=rA1S0aAPw5U&embeds_referring_euri=https%3A%2F%2Fwildlabs.net%2F)

#### AI Models for Edge
| Model                            | What it is                                         | Links                                                                                                                                                                                |
| -------------------------------- | -------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| BirdNET-Pi                       | A realtime acoustic bird classification system for the Raspberry Pi 5, 4B 3B+ 0W2 and more | https://www.birdweather.com/birdnetpi |
| YOLO                             | Small, real‑time models for detection and classification | https://docs.ultralytics.com/ |
| MobileSAM                        | Segment Anything Model optimized for edge | https://github.com/ChaoningZhang/MobileSAM |    
| WL-YOLO                          | Designed for lightweight wildlife for real-time detection in complex forest environments    | [Paper](https://doi.org/10.3390/rs16081350) |




### Projects
| Project                          | What it is                                         | Links                                                                                                                                                                                |
| -------------------------------- | -------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Wild Edge (WildLabs Group)       | Community for edge AI in conservation              | [wildlabs.net](https://wildlabs.net/)                                                                                                                                                 |
| Microsoft Project SPARROW        | Biodiversity edge‑AI initiative/platform           | [Announcement](https://blogs.microsoft.com/on-the-issues/2024/12/18/announcing-sparrow-a-breakthrough-ai-tool-to-measure-and-protect-earths-biodiversity-in-the-most-remote-places/) |                                                                                                                                       |
| SmartWilds                       | Edge AI for animal land use patterns, species ID | [Project Page](https://imageomics.github.io/naturelab/)                                                                                                                                |
| Robinson Crusoe Island Project                                 | Delivering edge computing on Robinson Crusoe Island (Chile) | [Article](https://wildlabs.net/article/video-delivering-edge-computing-robinson-crusoe-island-chile-preserve-biodiversity)                                                                 |           


### Papers

#### Overviews
____

**Edge computing in wildlife behavior and ecology** — *Trends in Ecology & Evolution* 39(2):128–130, 2024. *Yu, H., et al.* [Paper](https://pubmed.ncbi.nlm.nih.gov)

**Characterizing and Modeling AI-Driven Animal Ecology Studies at the Edge** — 2024 IEEE/ACM Symposium on Edge Computing (SEC), Rome, Italy. *J. Kline, A. O’Quinn, T. Berger‑Wolf, C. Stewart*. [Paper](https://ieeexplore.ieee.org/document/10818207/)

**Environment-Aware Dynamic Pruning for Pipelined Edge Inference** — arXiv preprint (2025). O’Quinn, Snedeker, Zhang, Kline. [Paper](https://arxiv.org/abs/2503.03070)

**ML Field Planner: Analyzing and Optimizing ML Pipelines for Field Research** — PEARC ’25: Practice and Experience in Advanced Research Computing, 2025. *Stubbs, J., Balasubramaniam, S., Khuvis, S., Withana, S., Vallabhajosyula, M. S., Cardone, R., Garcia, C., Freeman, N., Guzman, C., Plale, B., Ramnath, R., & Berger-Wolf, T.* [Paper](https://doi.org/10.1145/3708035.3736013)

#### Acoustics
____

**acoupi: An Open-Source Python Framework for Deploying Bioacoustic AI Models on Edge Devices** - arXiv preprint arXiv:2501.17841., *Vuilliomenet, A., Balvanera, S. M., Mac Aodha, O., Jones, K. E., & Wilson, D.* [Paper](https://arxiv.org/abs/2501.17841) [Repo](https://github.com/acoupi/acoupi) [Docs](https://acoupi.github.io/acoupi/)


#### Biologgers
____
**Wildlife Monitoring on the Edge: A Performance Evaluation of Embedded Neural Networks on Microcontrollers for Animal Behavior Classification** — *Sensors* 21(9):2975, 2021. *Dominguez‑Morales, J. P., Duran‑Lopez, L., Gutierrez‑Galan, D., Rios‑Navarro, A., Linares‑Barranco, A., & Jimenez‑Fernandez, A.* [Paper](https://www.mdpi.com/1424-8220/21/9/2975)

#### Drones (Aerial and Marine)
____
**Building of an edge-enabled drone network ecosystem for bird species identification** — *Ecological Informatics* 2022. *Das, N., et al.* [Paper](https://ouci.dntb.gov.ua/)

**WildWing: An open-source, autonomous and affordable UAS for animal behaviour video monitoring** — *Methods in Ecology and Evolution*, 2025. *Kline, J., Zhong, A., Irizarry, K., Stewart, C. V., Stewart, C., Rubenstein, D. I., & Berger‑Wolf, T.* [Project Page](https://imageomics.github.io/wildwing/) [Paper](https://besjournals.onlinelibrary.wiley.com/doi/10.1111/2041-210X.70018)

**WildLive: Near Real-time Visual Wildlife Tracking onboard UAVs** - *CV4Animals Workshop at CVPR* 2025. *Dat NN, Richardson T, Watson M, Meier K, Kline J, Reid S, Maalouf G, Hine D, Mirmehdi M, Burghardt T.* [Paper](https://doi.org/10.48550/arXiv.2504.10165)

**Semi-supervised Visual Tracking of Marine Animals Using Autonomous Underwater Vehicles** - *Int J Comput Vis 131*, 2023. Cai, L., McGuire, N.E., Hanlon, R. et al. [Paper](https://doi.org/10.1007/s11263-023-01762-5)

#### Camera traps
____
**AI-Driven Real-Time Monitoring of Ground-Nesting Birds: A Case Study on Curlew Detection Using YOLOv10** — arXiv preprint arXiv:2411.15263. *Chalmers, C., Fergus, P., Wich, S., Longmore, S. N., Walsh, N. D., Oliver, L., Warrington, J., Quinlan, J., & Appleby, K.* [Paper](http://arxiv.org/abs/2411.15263)

**An IoT System Using Deep Learning to Classify Camera Trap Images on the Edge** — *Computers*, 2022. *Zualkernan, I., Dhou, S., Judas, J., Sajun, A. R., Gomez, B. R., & Alhaj Hussain, L.* [Paper](https://www.mdpi.com/2073-431X/11/1/13)

**Energy-Efficient Audio Processing at the Edge for Biologging Applications** — *Journal of Low Power Electronics and Applications*, 2023. *Miquel, J., Latorre, L., & Chamaillé‑Jammes, S.* [Paper](https://www.mdpi.com/2079-9268/13/2/30)

**Real-time alerts from AI-enabled camera traps using the Iridium satellite network: A case-study in Gabon, Central Africa** — *Methods in Ecology and Evolution*, 2023. *Whytock, R. C., et al.* [Paper](https://onlinelibrary.wiley.com/doi/abs/10.1111/2041-210X.14036)

**Reliable and efficient integration of AI into camera traps for smart wildlife monitoring (with on-device continual learning)** — *Ecological Informatics*, 2024. *Velasco‑Montero, D., Fernández‑Berni, J., Carmona‑Galán, R., Sanglas, A., & Palomares, F.* [Paper](https://www.sciencedirect.com/science/article/pii/S1574954124003571) 

**Towards a standardized framework for AI-assisted, image-based monitoring of nocturnal insects** — *Philosophical Transactions of the Royal Society B* , 2024. *Roy, D. B., Alison, J., August, T. A., et al.* [Paper](https://royalsocietypublishing.org/doi/full/10.1098/rstb.2023.0108)

**Towards scalable insect monitoring: Ultra-lightweight CNNs as on-device triggers for insect camera traps** — *Methods in Ecology and Evolution*, 2025. *Gardiner, R. J., Rowlands, S., & Simmons, B. I.* [Paper](https://onlinelibrary.wiley.com/doi/abs/10.1111/2041-210X.70098)

**Assessment of technological developments for camera-traps: a wireless network and advanced image recognition** — *Wildlife Society Bulletin*, 2022. *Meek, P., et al.* [Paper](https://wildlife.onlinelibrary.wiley.com)

**A computer vision enhanced IoT system for koala monitoring and recognition** - *Internet of Things*, 2025. *Trevathan, J., Tan, W.L., Xing, W., Holzner, D., Kerlin, D., Zhou, J. and Castley, G.,* [Paper](https://doi.org/10.1016/j.iot.2024.101474)

## Contributing

We welcome issues and PRs for:

* New resources, corrections, or re-organizations
* Field notes and deployment postmortems
* Minimal working examples (scripts, configs)

## License

MIT — see [LICENSE](LICENSE).

