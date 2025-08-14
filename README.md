# Edge AI for Conservation

*A curated, community-maintained hub for **edge AI** methods, tools, datasets, and deployments in conservation.*

This survey is intended to consolidate projects and resources for deploying edge AI for conservation. This page is maintained by [Jenna Kline](https://jennamk14.github.io/). Contributions are welcome! Please submit additions or corrections as Github pull requests.

---

## Table of Contents

* [Why this repo?](#why-this-repo)
* [Scope & taxonomy](#scope--taxonomy)
* [Quick start: top entry points](#quick-start-top-entry-points)
* [Curated resources](#curated-resources)

  * [Projects & papers](#projects--papers-edge-ai-for-conservation)
    * [General edge AI for conservation](#general-edge-ai-for-conservation)
    * [Acoustics](#acoustics)
    * [Biologgers](#biologgers)
    * [Drones](#drones)
    * [Camera traps](#camera-traps)

  * [Cyberinfrastructure (edge platforms & SDKs)](#cyberinfrastructure-edge-platforms--sdks)
  * [Sensors (smart sensors & deployments)](#sensors-smart-sensors--deployments)
  * [AI models & toolchains](#ai-models--toolchains)
  * [Optimization for the edge (quantization, pruning, distillation)](#optimization-for-the-edge-quantization-pruning-distillation)
  * [Multimodal fusion & digital twins](#multimodal-fusion--digital-twins)
  * [Datasets — help wanted](#datasets--help-wanted)
  * [Ethics, permitting, & community guidelines — help wanted](#ethics-permitting--community-guidelines--help-wanted)
* [Case studies & deployments](#case-studies--deployments)
* [Contributing](#contributing)
* [Roadmap](#roadmap)
* [Maintainers](#maintainers)
* [License](#license)

---

## Why this repo?

Edge AI—running perception, decision-making, and data triage **on-device**—is transforming wildlife monitoring and ecosystem science. The literature and tooling are fragmented across subfields (CV, robotics, acoustics, ecology). This repo aggregates **practical** references: what to use, how to deploy, and where to learn from real-world efforts.

## Scope & taxonomy

This project prioritizes:

* **On-device AI** (Raspberry Pi/CM, Jetson, Coral, microcontrollers; phones as edge devices).
* **Conservation sensing modalities:** drones/UAS, camera traps, bioacoustics, GPS/biologgers, eDNA, and environmental sensors.
* **Pipelines & operations:** data curation, training, optimization, evaluation, deployment, monitoring, and governance.

> Out of scope: purely cloud-only analytics without an edge component.

## Quick start: top entry points

* **What’s here today:** curated tables for **Cyberinfrastructure**, **Sensors**, and **AI models** with links.
* **Coming soon (help wanted):** **Starter kits**, **Benchmarks**, and **Field‑ops checklists**. If you have a minimal working example or checklist, please open a PR.

---

## Curated resources

### Projects & papers (edge AI for conservation)

#### General edge AI for conservation
**Edge computing in wildlife behavior and ecology** — *Trends in Ecology & Evolution* 39(2):128–130, 2024. *Yu, H., et al.* [PubMed](https://pubmed.ncbi.nlm.nih.gov)

**Characterizing and Modeling AI-Driven Animal Ecology Studies at the Edge** — 2024 IEEE/ACM Symposium on Edge Computing (SEC), Rome, Italy. *J. Kline, A. O’Quinn, T. Berger‑Wolf, C. Stewart*. DOI: 10.1109/SEC62691.2024.00025. [Paper](https://ieeexplore.ieee.org/document/10818207/)

**Environment-Aware Dynamic Pruning for Pipelined Edge Inference** — arXiv preprint (2025). O’Quinn, Snedeker, Zhang, Kline. [Paper](https://arxiv.org/abs/2503.03070)

**Analyzing and Optimizing ML Pipelines for Field Research** — PEARC ’25. [Paper](https://dl.acm.org/doi/full/10.1145/3708035.3736013)

#### Acoustics

**acoupi: An Open-Source Python Framework for Deploying Bioacoustic AI Models on Edge Devices** - arXiv preprint arXiv:2501.17841., *Vuilliomenet, A., Balvanera, S. M., Mac Aodha, O., Jones, K. E., & Wilson, D.* [Paper](https://arxiv.org/abs/2501.17841) [Repo](https://github.com/acoupi/acoupi) [Docs](https://acoupi.github.io/acoupi/)

#### Biologgers
**Wildlife Monitoring on the Edge: A Performance Evaluation of Embedded Neural Networks on Microcontrollers for Animal Behavior Classification** — *Sensors* 21(9):2975, 2021. *Dominguez‑Morales, J. P., Duran‑Lopez, L., Gutierrez‑Galan, D., Rios‑Navarro, A., Linares‑Barranco, A., & Jimenez‑Fernandez, A.* [Paper](https://www.mdpi.com/1424-8220/21/9/2975)

#### Drones
**Building of an edge-enabled drone network ecosystem for bird species identification** — *Ecological Informatics* 68:101540, 2022. *Das, N., et al.* [Paper](https://ouci.dntb.gov.ua/)
**WildWing: An open‑source, autonomous and affordable UAS for animal behaviour video monitoring** [Project Page](https://imageomics.github.io/wildwing/) [Paper](https://besjournals.onlinelibrary.wiley.com/doi/10.1111/2041-210X.70018)

#### Camera traps
**AI-Driven Real-Time Monitoring of Ground-Nesting Birds: A Case Study on Curlew Detection Using YOLOv10** — arXiv preprint arXiv:2411.15263. *Chalmers, C., Fergus, P., Wich, S., Longmore, S. N., Walsh, N. D., Oliver, L., Warrington, J., Quinlan, J., & Appleby, K.* [Paper](http://arxiv.org/abs/2411.15263)

**An IoT System Using Deep Learning to Classify Camera Trap Images on the Edge** — *Computers* 11(1):13, 2022. *Zualkernan, I., Dhou, S., Judas, J., Sajun, A. R., Gomez, B. R., & Alhaj Hussain, L.* [Paper](https://www.mdpi.com/2073-431X/11/1/13)

**Energy-Efficient Audio Processing at the Edge for Biologging Applications** — *Journal of Low Power Electronics and Applications* 13(2):30, 2023. *Miquel, J., Latorre, L., & Chamaillé‑Jammes, S.* [Paper](https://www.mdpi.com/2079-9268/13/2/30)

**Real-time alerts from AI-enabled camera traps using the Iridium satellite network: A case-study in Gabon, Central Africa** — *Methods in Ecology and Evolution* 14(3):867–874, 2023. *Whytock, R. C., et al.* [Paper](https://onlinelibrary.wiley.com/doi/abs/10.1111/2041-210X.14036)

**Reliable and efficient integration of AI into camera traps for smart wildlife monitoring (with on-device continual learning)** — *Ecological Informatics* 83:102815, 2024. *Velasco‑Montero, D., Fernández‑Berni, J., Carmona‑Galán, R., Sanglas, A., & Palomares, F.* [Paper](https://www.sciencedirect.com/science/article/pii/S1574954124003571) [WILDLABS](https://wildlabs.net)

**Towards a standardized framework for AI-assisted, image-based monitoring of nocturnal insects** — *Philosophical Transactions of the Royal Society B* 379:20230108, 2024. *Roy, D. B., Alison, J., August, T. A., et al.* [Paper](https://royalsocietypublishing.org/doi/full/10.1098/rstb.2023.0108)

**Towards scalable insect monitoring: Ultra-lightweight CNNs as on-device triggers for insect camera traps** — *Methods in Ecology and Evolution*, 2025. *Gardiner, R. J., Rowlands, S., & Simmons, B. I.* [Paper](https://onlinelibrary.wiley.com/doi/abs/10.1111/2041-210X.70098)

**Assessment of technological developments for camera-traps: a wireless network and advanced image recognition** — *Wildlife Society Bulletin*, 2022. *Meek, P., et al.* [Paper](https://wildlife.onlinelibrary.wiley.com)

### Cyberinfrastructure (edge platforms & SDKs)

**Edge platforms & devices**

| Platform                         | What it is                                         | Links                                                                                                                                                                                |
| -------------------------------- | -------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| NVIDIA Jetson (Nano / Orin Nano) | Embedded GPU modules for on-device AI              | [Jetson Nano](https://developer.nvidia.com/embedded/jetson-nano), [Orin Nano](https://developer.nvidia.com/embedded/learn/get-started-jetson-orin-nano-devkit)                       |
| Raspberry Pi                     | Single-board computers for far‑edge deployments    | [raspberrypi.com](https://www.raspberrypi.com/)                                                                                                                                      |
| Google Coral                     | Edge TPU accelerators and dev boards               | [coral.ai](https://coral.ai/), [Docs](https://coral.ai/docs/)                                                                                                                        |
| Seeed Studio LoRaWAN Dev Kit     | LoRaWAN gateway/dev kit for LPWAN edge sensing     | [Product](https://www.seeedstudio.com/Seeed-Studio-LoRaWAN-Dev-Kit-p-5370.html)                                                                                                      |
| Edge Impulse                     | Edge ML platform (data→model→deploy; MCUs & Linux) | [edgeimpulse.com](https://edgeimpulse.com/)                                                                                                                                          |
| Conservation X Labs              | Conservation tech and open innovation ecosystem    | [conservationxlabs.com](https://conservationxlabs.com/)                                                                                                                              |
| Microsoft Project SPARROW        | Biodiversity edge‑AI initiative/platform           | [Announcement](https://blogs.microsoft.com/on-the-issues/2024/12/18/announcing-sparrow-a-breakthrough-ai-tool-to-measure-and-protect-earths-biodiversity-in-the-most-remote-places/) |

**SDKs & compilers**

| SDK                      | Purpose                                                     | Link                                                                                                                   |
| ------------------------ | ----------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| TensorRT                 | NVIDIA inference optimizer/runtime for high‑throughput edge | [docs](https://docs.nvidia.com/deeplearning/tensorrt/latest/index.html)                                                |
| OpenVINO                 | Intel toolkit for optimized inference on CPUs/VPUs/GPUs     | [docs](https://docs.openvino.ai/)                                                                                      |
| Apache TVM               | Compiler stack to optimize models across hardware           | [tvm.apache.org](https://tvm.apache.org/)                                                                              |
| Core ML Tools            | Convert/train/export models for Apple devices               | [coremltools](https://github.com/apple/coremltools)                                                                    |
| Arm NN & Compute Library | Inference SDKs for Arm CPUs/GPUs/NPUs                       | [Arm NN](https://www.arm.com/products/silicon-ip-cpu/ethos/arm-nn), [ACL](https://arm-software.github.io/armnn/24.02/) |

### Sensors (smart sensors & deployments)

| Modality         | Key tools/projects                                             | Notes                                          | Links                                                                                                                                                                                                                      |
| ---------------- | -------------------------------------------------------------- | ---------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Drones & aerial  | PX4, ArduPilot, Pixhawk, WildWing                              | Open FC stacks; behavior‑aware UAS             | [PX4](https://px4.io/), [ArduPilot](https://www.ardupilot.org/), [Pixhawk](https://pixhawk.org/), [WildWing](https://imageomics.github.io/wildwing/)                                                                       |
| Camera traps     | CameraTraps/PyTorch‑Wildlife, MegaDetector, CVAT, Label Studio | E2E pipelines; annotation; on‑device filtering | [CameraTraps](https://microsoft.github.io/CameraTraps/), [MegaDetector](https://github.com/agentmorris/MegaDetector), [CVAT](https://github.com/cvat-ai/cvat), [Label Studio](https://github.com/HumanSignal/label-studio) |
| Bioacoustics     | ACOUPI, BirdNET‑Analyzer, BirdNET‑Pi                           | Edge acoustic detection & stations             | [ACOUPI](https://github.com/acoupi/acoupi), [BirdNET‑Analyzer](https://github.com/birdnet-team/BirdNET-Analyzer), [BirdNET‑Pi](https://github.com/Nachtzuster/BirdNET-Pi)                                                  |
| GPS / biologging | OpenCollar, Movebank                                           | Low‑power collars and shared data platform     | [OpenCollar](https://www.smartparks.org/opencollar-io/), [Movebank](https://www.movebank.org/)                                                                                                                             |
| eDNA / other     | —                                                              | Seeking stable kits & SOPs (PRs welcome)       | —                                                                                                                                                                                                                          |

### AI models & toolchains

| Task                       | Tool/Model                  | Why edge‑relevant                                                      | Link(s)                                                                                                                                           |
| -------------------------- | --------------------------- | ---------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| Detection / classification | YOLO, RT‑DETR               | Small, real‑time models; quantizable; export to ONNX/TensorRT/TFLite   | [Ultralytics YOLO](https://github.com/ultralytics/ultralytics), [RT‑DETR](https://github.com/lyuwenyu/RT-DETR)                                    |
| Segmentation               | MobileSAM                   | Fast SAM variants; lightweight ROI extraction on mid‑tier edge GPUs    | [MobileSAM](https://github.com/ChaoningZhang/MobileSAM)                                                                                           |
| Tracking & re‑ID           | DeepSORT, OC‑SORT, BoT‑SORT | Maintains identity on‑device; reduces bandwidth & post‑hoc association | [DeepSORT](https://github.com/nwojke/deep_sort), [OC‑SORT](https://github.com/noahcao/OC_SORT), [BoT‑SORT](https://github.com/NirAharon/BoT-SORT) |
| Pose / keypoints (animal)  | DeepLabCut, SLEAP           | Enables behavior inference; export options for deployment              | [DeepLabCut](https://github.com/DeepLabCut/DeepLabCut), [SLEAP](https://github.com/talmolab/sleap)                                                |


### Datasets — help wanted

We haven’t seeded this section yet. **Please contribute** curated datasets via PRs using this format:
**Name | Modality | Tasks (det/reID/behav/multimodal) | Size | License | Link**. Include a short justification (why useful for **edge** deployment) and confirm license terms.

### Ethics, permitting, & community guidelines — help wanted

We’re compiling durable, reusable guidance: UAV & wildlife guidelines, acoustic recording ethics, camera‑trap human privacy, Indigenous data sovereignty, and data sensitivity classification. If you can contribute a **stable, citable resource** (policy, handbook, standard), please open a PR.


### Community & discussions from [WILDLABS](https://wildlabs.net/) — organized by **cyberinfrastructure** topics

#### 1) Cyberinfrastructure: edge platforms & tooling
* Proposal for new Wild Edge group - [https://wildlabs.net/discussion/exploring-wild-edge-proposal-new-wildlabs-group](https://wildlabs.net/discussion/exploring-wild-edge-proposal-new-wildlabs-group)
* Edge Impulse joins 1% for the Planet — [https://wildlabs.net/article/edge-impulse-becomes-first-ai-company-join-1-planet](https://wildlabs.net/article/edge-impulse-becomes-first-ai-company-join-1-planet)
* MegaDetector on edge devices — [https://wildlabs.net/discussion/megadetector-edge-devices](https://wildlabs.net/discussion/megadetector-edge-devices)
* ML at the edge — [https://wildlabs.net/discussion/ml-edge](https://wildlabs.net/discussion/ml-edge)

#### 2) Distributed computing techniques & system operations

* Video: Delivering edge computing on Robinson Crusoe Island (Chile) — [https://wildlabs.net/article/video-delivering-edge-computing-robinson-crusoe-island-chile-preserve-biodiversity](https://wildlabs.net/article/video-delivering-edge-computing-robinson-crusoe-island-chile-preserve-biodiversity)
* AI for Conservation — Office Hours 2023 review — [https://wildlabs.net/article/ai-conservation-office-hours-2023-review](https://wildlabs.net/article/ai-conservation-office-hours-2023-review)
* Discussion: Questions for biologists on acoustic system requirements — [https://wildlabs.net/discussion/questions-biologists-relating-system-requirements-acoustic-research#comment-10765](https://wildlabs.net/discussion/questions-biologists-relating-system-requirements-acoustic-research#comment-10765)

#### 3) AI for the edge (models, training, deployment)

* Discussion: AI animal identification models — [https://wildlabs.net/discussion/ai-animal-identification-models](https://wildlabs.net/discussion/ai-animal-identification-models)
* Link: **ACOUPI** — Python framework for deploying bioacoustic AI on edge devices — [https://wildlabs.net/link/acoupi-open-source-python-framework-deploying-bioacoustic-ai-models-edge-devices](https://wildlabs.net/link/acoupi-open-source-python-framework-deploying-bioacoustic-ai-models-edge-devices)
* Discussion: AI & edge‑compute‑based wildlife detection — [https://wildlabs.net/discussion/ai-edge-compute-based-wildlife-detection](https://wildlabs.net/discussion/ai-edge-compute-based-wildlife-detection)
* Discussion: Mini AI wildlife monitor — [https://wildlabs.net/discussion/mini-ai-wildlife-monitor](https://wildlabs.net/discussion/mini-ai-wildlife-monitor)

#### 4) Smart sensors & deployments (drones, camera traps, bioacoustics)

* Article: Announcement — Project SPARROW — [https://wildlabs.net/article/announcement-project-sparrow](https://wildlabs.net/article/announcement-project-sparrow)
* Project update: GreenCrossingAI — [https://wildlabs.net/discussion/greencrossingai-project-update](https://wildlabs.net/discussion/greencrossingai-project-update)

---

## Case studies & deployments

Short, actionable write-ups:

* **Title (site/country)** — goals, sensors, edge stack, models, evaluation metrics, lessons learned, links/code.

---

## Contributing

We welcome issues and PRs for:

* New resources, corrections, or re-organizations
* Field notes and deployment postmortems
* Minimal working examples (scripts, configs)

#### Help wanted right now

* **Seed the Datasets section** with stable, licensed benchmarks.
* **Seed the Ethics/Permitting/Community Guidelines section** with durable guidelines and standards.

**How to contribute:**

1. Open an issue describing the change.
2. For lists, follow alphabetical order within subsections.
3. Prefer **official sources** and **open licenses**; add a one-line description and a short justification (why useful for edge deployment).
4. When adding datasets, confirm license/usage terms and include citation.

We use **awesome-lint** and a link checker in CI; see `.github/workflows/` for details.

---

## Roadmap

* [ ] Seed the repo with initial cross-modality resources
* [ ] Add a **Datasets** table (CSV + Markdown view)
* [ ] Add **Starter kits** directory with runnable examples for Pi/Jetson/Coral
* [ ] Case studies: write up deployments and field notes from the community
* [ ] Add **Multimodal fusion & digital twins** for integrating data across sensors
* [ ] Add **Optimization for the edge techniques** for edge AI models in conservation

---

## Maintainers

* [Jenna Kline](https://jennamk14.github.io/) (@jennamk14) — edge AI & autonomous systems for ecology
* Looking for co-maintainers across modalities (camera traps, acoustics, bio, drones)

## License

MIT — see [LICENSE](LICENSE).

---

### How this repo relates to prior work

This project is inspired by excellent modality-specific surveys, including [Everything I know about ML and camera traps](https://agentmorris.github.io/camera-trap-ml-survey/) maintained by Dan Morris and [Computer Vision and Aerial Imagery for Wildlife Conservation](https://bkellenb.github.io/cv-for-wildlife-aerial-imagery/) maintained by Dan Morris and Benjamin Kellenberger.
This repo aims to broaden to **multi-modal edge AI for conservation** with a consistent taxonomy, runnable examples, and deployment-first guidance.
