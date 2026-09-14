# Federated Low-Rank Adaptation: A Survey

**Federated Low-Rank Adaptation: A Survey of Methods, Systems, Security, and Research Directions**

Tuan Nguyen · Minh-Duong Nguyen · Khoa D. Doan · Kok-Seng Wong

[Field overview](#field-overview) · [Paper collection](#paper-collection) · [Research directions](#research-directions) · [Citation](#citation-and-corrections)

Federated low-rank adaptation uses compact, trainable adapters to adapt models collaboratively while keeping training data local. This survey follows what clients upload, how their contributions are combined, what they receive, and which state they retain for later training and prediction. These choices connect aggregation and personalization to system costs, protection mechanisms, and the evidence needed to compare methods.

The catalogue contains the survey's **231 included studies through July 2026**. It follows the manuscript's primary topic assignments; each study appears once. Background references are outside this catalogue. Venue and status labels follow the cited sources, with preprints and submissions distinguished from published proceedings.

## Field overview

| Design question | Main takeaway |
| --- | --- |
| How should updates be combined and returned? | Equal immediate aggregates can lead to different subsequent training when the returned factors, base model, or retained state differ. |
| What should be shared across different clients? | Rank compatibility, device capacity, and the need for a personal predictor are distinct design decisions. |
| Which resource limits useful training? | Compare communication, memory, and time to the same quality target, including frozen-model computation and return traffic. |
| What must be protected, and from whom? | The adversary and exposed state determine which privacy, confidentiality, and robustness mechanisms can work together. |
| Which results support a design choice? | Match the task, protocol, prediction state, and measured costs before comparing outcomes. |

## Paper collection

Expand a topic to browse its papers, ordered by cited-source year (newest first), then title. A primary placement is a navigation choice; many papers address several topics. A submission label does not imply acceptance.

### Aggregation and adapter states

<details>
<summary>Browse 48 studies</summary>

- <a id="yan2026breakingstandalone"></a>**2026** · [1+1&lt;1? Breaking the Standalone Barrier in Federated Fine-Tuning of Multimodal Large Language Models under Non-IID Data](https://openreview.net/forum?id=BI0QjdL8PX) · ICLR submission.
- <a id="zhang2025alternating"></a>**2026** · [Alternating Aggregation Low-Rank Adaptation Approach for Federated Large Models](https://doi.org/10.1007/978-981-95-3453-1_31) · Adv. Data Min. Appl.
- <a id="ali2026alzfedxai"></a>**2026** · [Alz-Fed-XAI: A dynamic federated transformer for multimodal Alzheimer’s classification, fuzzy explainable reasoning and smart decision support](https://doi.org/10.1016/j.asoc.2026.115716) · Appl. Soft Comput.
- <a id="fang2026feddrlora"></a>**2026** · [Decoupled Low-Rank Adaptation for Robust Federated Fine-Tuning](https://openreview.net/forum?id=eNcIILpv8F) · ICML.
- <a id="thompson2026dpflogtinyllm"></a>**2026** · [DP-FlogTinyLLM: Differentially private federated log anomaly detection using Tiny LLMs](https://arxiv.org/abs/2604.19118) · arXiv preprint.
- <a id="yang2026dynamicrank"></a>**2026** · [Dynamic Rank-Aware Aggregation with Graph Contrastive Learning for Federated Foundation Model Fine-Tuning](https://doi.org/10.23919/date69613.2026.11539341) · Des., Autom. Test Eur. Conf. (DATE).
- <a id="singhal2026fedsb"></a>**2026** · [Fed-SB: A Silver Bullet for Extreme Communication Efficiency and Performance in (Private) Federated LoRA Fine-Tuning](https://arxiv.org/abs/2502.15436v2) · Transact. Mach. Learn. Res.
- <a id="chen2026fedotab"></a>**2026** · [Federated LoRA Fine-Tuning of LLMs with Only Transmitting Matrix A or B](https://doi.org/10.1109/TMC.2026.3696859) · IEEE Trans. Mob. Comput.
- <a id="kaur2026fedllmtraffic"></a>**2026** · [FedLLM: A Privacy-Preserving Federated Large Language Model for Explainable Traffic Flow Prediction](https://doi.org/10.2139/ssrn.7086750) · SSRN preprint.
- <a id="li2026fedpla"></a>**2026** · [FedPLA: Prototype-Aligned Low-Rank Adaptation for Multimodal Federated Learning](https://doi.org/10.1109/icassp55912.2026.11461621) · IEEE Int. Conf. Acoust., Speech Signal Process. (ICASSP).
- <a id="ren2026fedsdr"></a>**2026** · [FedSDR: Federated Self-Distillation with Rectification](https://arxiv.org/abs/2605.18028v1) · ICML.
- <a id="cruz2026fltflow"></a>**2026** · [FL-TFlow: Benign-Only Federated LoRA Tuning of SLMs for Edge Ransomware Detection](https://doi.org/10.5753/wgrs.2026.24104) · An. Workshop de Gerência e Operação de Redes e Serviços (WGRS).
- <a id="nayak2026pubswap"></a>**2026** · [PubSwap: Public-Data Off-Policy Coordination for Federated RLVR](https://arxiv.org/abs/2604.12160v1) · ICML Workshop on Decision-Making from Offline Datasets to Online Adaptation: Black-Box Optimization to Reinforcement Learning.
- <a id="li2026rethinkingaggregation"></a>**2026** · [Rethinking LoRA Aggregation for Federated Fine-tuning of Foundation Models](https://openreview.net/forum?id=k5SgTEKdA2) · ICLR submission.
- <a id="liu2026shelora"></a>**2026** · [SHE-LoRA: Selective Homomorphic Encryption for Federated Tuning with Heterogeneous LoRA](https://openreview.net/forum?id=PWChrnrw7Z) · ICLR.
- <a id="huang2026stabilized"></a>**2026** · [Stabilized Fine-Tuning with LoRA in Federated Learning: Mitigating the Side Effect of Client Size and Rank via the Scaling Factor](https://arxiv.org/abs/2603.08058) · arXiv preprint.
- <a id="liang2026uniflow"></a>**2026** · [UniFLoW: Universal Multi-Modal Federated LoRA Fine-Tuning Framework with Analytical Aggregation](https://openreview.net/forum?id=TNARYxc9YF) · ICML.
- <a id="liu2024adaptive"></a>**2025** · [Adaptive Parameter-Efficient Federated Fine-Tuning on Heterogeneous Devices](https://doi.org/10.1109/tmc.2025.3586644) · IEEE Trans. Mob. Comput.
- <a id="salami2025closedform"></a>**2025** · [Closed-Form Merging of Parameter-Efficient Modules for Federated Continual Learning](https://openreview.net/forum?id=ROpY0qRUXL) · ICLR.
- <a id="chen2025aggregationbroadcast"></a>**2025** · [Convergence Analysis of Aggregation-Broadcast in LoRA-Enabled Distributed Fine-Tuning](https://arxiv.org/abs/2508.01348v2) · arXiv preprint.
- <a id="zhu2025deer"></a>**2025** · [DEeR: Deviation Eliminating and Noise Regulating for Privacy-Preserving Federated Low-Rank Adaptation](https://doi.org/10.1109/tmi.2024.3518539) · IEEE Trans. Med. Imaging.
- <a id="xu2025dpfedlora"></a>**2025** · [DP-FedLoRA: Privacy-Enhanced Federated Fine-Tuning for On-Device Large Language Models](https://doi.org/10.1109/icdm65498.2025.00089) · IEEE Int. Conf. Data Min. (ICDM).
- <a id="chen2025intelligent"></a>**2025** · [Federated Fine-Tuning of Large Language Models for Intelligent Automotive Systems with Low-Rank Adaptation](https://doi.org/10.1109/vtc2025-spring65109.2025.11174441) · IEEE Veh. Technol. Conf. (VTC-Spring).
- <a id="ning2025heterogeneous"></a>**2025** · [Federated Fine-Tuning on Heterogeneous LoRAs With Error-Compensated Aggregation](https://doi.org/10.1109/tnnls.2025.3586545) · IEEE Trans. Neural Netw. Learn. Syst.
- <a id="yan2025residual"></a>**2025** · [Federated Residual Low-Rank Adaptation of Large Language Models](https://openreview.net/forum?id=e0rQRMUhs7) · ICLR.
- <a id="singhal2025fedexlora"></a>**2025** · [FedEx-LoRA: Exact Aggregation for Federated and Efficient Fine-Tuning of Large Language Models](https://doi.org/10.18653/v1/2025.acl-long.67) · ACL (Long Papers).
- <a id="peng2025fedhl"></a>**2025** · [FedHL: Federated Learning for Heterogeneous Low-Rank Adaptation via Unbiased Aggregation](https://arxiv.org/abs/2505.18494) · arXiv preprint.
- <a id="jhunjhunwala2025fedrpca"></a>**2025** · [FedRPCA: Enhancing Federated LoRA Aggregation Using Robust PCA](https://arxiv.org/abs/2506.01194) · arXiv preprint.
- <a id="nguyen2026florana"></a>**2025** · [FLoRA-NA: Nearly Accurate Aggregation for Federated Low-Rank Adaptation](https://arxiv.org/abs/2509.26399) · arXiv preprint.
- <a id="zhang2025incentive"></a>**2025** · [Incentive mechanism of foundation model enabled cross-silo federated learning](https://doi.org/10.1038/s41598-025-10195-8) · Sci. Rep.
- <a id="bian2025lorafair"></a>**2025** · [LoRA-FAIR: Federated LoRA Fine-Tuning with Aggregation and Initialization Refinement](https://doi.org/10.1109/iccv51701.2025.00356) · ICCV.
- <a id="elbakary2025mira"></a>**2025** · [MIRA: A Method of Federated Multi-Task Learning for Large Language Models](https://doi.org/10.1109/lnet.2025.3539810) · IEEE Netw. Lett.
- <a id="malinovsky2025randomized"></a>**2025** · [Randomized Asymmetric Chain of LoRA: The First Meaningful Theoretical Framework for Low-Rank Adaptation for Federated Learning](https://openreview.net/forum?id=xIxawIhmgO) · ICML Workshop: Tiny Titans: The Next Wave of On-Device Learning for Foundation Models (TTODLer-FM).
- <a id="he2025ratemylora"></a>**2025** · [Rate-My-LoRA: EFFICIENT AND ADAPTIVE FEDERATED MODEL TUNING FOR CARDIAC MRI SEGMENTATION](https://doi.org/10.1109/isbi60581.2025.10980762) · IEEE Int. Symp. Biomed. Imaging (ISBI).
- <a id="chen2024rbla"></a>**2025** · [RBLA: Rank-Based-LoRA-Aggregation for Fine-Tuning Heterogeneous Models in FLaaS](https://doi.org/10.1007/978-3-031-77072-2_4) · ICWS 2024 proceedings.
- <a id="chen2025robust"></a>**2025** · [Robust Federated Finetuning of LLMs via Alternating Optimization of LoRA](https://doi.org/10.52202/085713-4009) · NeurIPS.
- <a id="guo2025selective"></a>**2025** · [Selective Aggregation for Low-Rank Adaptation in Federated Learning](https://proceedings.iclr.cc/paper_files/paper/2025/hash/f53a37f820d5be5930415d964f4a0187-Abstract-Conference.html) · ICLR.
- <a id="yu2025task"></a>**2025** · [Task-agnostic Low-rank Residual Adaptation for Efficient Federated Continual Fine-Tuning](https://arxiv.org/abs/2505.12318) · arXiv preprint.
- <a id="fang2025robust"></a>**2025** · [Towards Robust Parameter-Efficient Fine-Tuning for Federated Learning](https://doi.org/10.52202/085713-4740) · NeurIPS.
- <a id="chen2025truncate"></a>**2025** · [Truncate without Fear: Module Aggregation and Redistribution in Federated Low-Rank Adaptation](https://iclr.cc/virtual/2025/33999) · ICLR Workshop: Modular, Collaborative and Decentralized Deep Learning.
- <a id="trautmann2024aggregating"></a>**2024** · [Aggregating Low Rank Adapters in Federated Fine-Tuning](https://doi.org/10.1109/flta63145.2024.10840125) · Int. Conf. Federated Learn. Technol. Appl. (FLTA).
- <a id="cai2024fcodellm"></a>**2024** · [F-CodeLLM: A Federated Learning Framework for Adapting Large Language Models to Practical Software Development](https://doi.org/10.1145/3639478.3643533) · Companion Proc. IEEE/ACM Int. Conf. Softw. Eng. (ICSE).
- <a id="nguyen2024flora"></a>**2024** · [FLoRA: Enhancing Vision-Language Models with Parameter-Efficient Federated Learning](https://doi.org/10.48550/arxiv.2404.15182) · arXiv preprint.
- <a id="he2024flora"></a>**2024** · [FLoRA: Federated Fine-Tuning Large Language Models with Heterogeneous Low-Rank Adaptations](https://doi.org/10.52202/079017-0708) · NeurIPS.
- <a id="sun2024improving"></a>**2024** · [Improving LoRA in Privacy-preserving Federated Learning](https://proceedings.iclr.cc/paper_files/paper/2024/hash/4e243e95c913b367775d71d7182b99d9-Abstract-Conference.html) · ICLR.
- <a id="jiang2024lpfl"></a>**2024** · [Low-Parameter Federated Learning with Large Language Models](https://doi.org/10.1007/978-981-97-7707-5_28) · Web Inf. Syst. Appl.
- <a id="nguyen2024communication"></a>**2024** · [Towards Efficient Communication and Secure Federated Recommendation System via Low-rank Training](https://doi.org/10.1145/3589334.3645702) · The Web Conference (WWW).
- <a id="kim2023efficientadapter"></a>**2023** · [Efficient Federated Learning with Pre-Trained Large Language Model Using Several Adapter Mechanisms](https://doi.org/10.3390/math11214479) · Mathematics.

</details>

### Heterogeneity and personalization

<details>
<summary>Browse 69 studies</summary>

- <a id="sang2026lomofed"></a>**2026** · [A communication-efficient personalized federated learning framework driven by parameter decoupling](https://doi.org/10.1016/j.neucom.2026.133790) · Neurocomputing.
- <a id="gupta2026hyperlora"></a>**2026** · [Amortizing Federated Adaptation: Hypernetwork Driven LoRA for Personalized Foundation Models](https://doi.org/10.48550/arXiv.2606.06154) · arXiv preprint.
- <a id="chen2026glora"></a>**2026** · [Beyond Factor Aggregation: Gauge-Aware Low-Rank Server Representations for Federated LoRA](https://arxiv.org/abs/2605.06733) · arXiv preprint.
- <a id="cheng2026cfedlad"></a>**2026** · [cFedLAD: A Clustered Additive LoRA Framework for Robust and Personalized Federated Learning](https://doi.org/10.1007/978-981-95-4969-6_28) · AI 2025 proceedings.
- <a id="cheng2025cfedlora"></a>**2026** · [cFedLoRA: Clustered Aggregation for Federated LoRA](https://doi.org/10.1007/978-981-95-3453-1_13) · Adv. Data Min. Appl.
- <a id="li2025communication"></a>**2026** · [Communication-Efficient and Personalized Federated Foundation Model Fine-Tuning via Tri-Matrix Adaptation](https://doi.org/10.1109/tmm.2026.3703316) · IEEE Trans. Multimed.
- <a id="gu2026dlora"></a>**2026** · [D-LoRA: A Dual Low-Rank Adaptation Framework for Cost-Efficient Personalized Federated Learning](https://doi.org/10.1109/ICASSP55912.2026.11461534) · IEEE Int. Conf. Acoust., Speech Signal Process. (ICASSP).
- <a id="yang2026dphm2f"></a>**2026** · [DP-HM2F: Data-driven LoRA with dual-projection representation for heterogeneous multimodal federated fine-tuning](https://doi.org/10.1016/j.eswa.2026.131287) · Expert Syst. Appl.
- <a id="song2026explanation"></a>**2026** · [Explanation-Enhanced Federated Fine-Tuning of Large Language Models for Photovoltaic Power Forecasting](https://doi.org/10.1109/tste.2026.3655809) · IEEE Trans. Sustain. Energy.
- <a id="wang2025fedpisa"></a>**2026** · [FED-PISA: Federated Voice Cloning Via Personalized Identity-Style Adaptation](https://doi.org/10.1109/icassp55912.2026.11461787) · IEEE Int. Conf. Acoust., Speech Signal Process. (ICASSP).
- <a id="bian2026fedalt"></a>**2026** · [FedALT: Federated Fine-Tuning Through Adaptive Local Training with Rest-of-World LoRA](https://doi.org/10.1609/aaai.v40i24.39054) · AAAI.
- <a id="yan2024federa"></a>**2026** · [FeDeRA: Efficient Fine-tuning of Language Models in Federated Learning Leveraging Weight Decomposition](https://arxiv.org/abs/2404.18848v3) · AAAI Workshop on Machine Learning for Wireless Communication and Networks (ML4Wireless).
- <a id="he2026clair"></a>**2026** · [Federated LoRA Fine-Tuning for LLMs via Collaborative Alignment](https://arxiv.org/abs/2605.21217) · arXiv preprint.
- <a id="liu2026fixedbasis"></a>**2026** · [Federated LoRA with Fixed Orthogonal Basis and Dimension-wise Aggregation](https://doi.org/10.1109/ISCAS66217.2026.11562992) · IEEE Int. Symp. Circuits Syst. (ISCAS).
- <a id="yang2025fedilora"></a>**2026** · [FediLoRA: Practical Federated Fine-Tuning of Foundation Models Under Missing-Modality Constraints](https://arxiv.org/abs/2509.06984) · Int. Jt. Conf. Artif. Intell./Eur. Conf. Artif. Intell. (IJCAI-ECAI), Special Track on AI and Health.
- <a id="pham2026fedkls"></a>**2026** · [FedKLS: Federated KL-Driven Low-rank SVD Adaptation in Non-IID Data Distributions](https://openreview.net/forum?id=gxKvAhqhmT) · ICLR submission.
- <a id="yan2026fedmomentum"></a>**2026** · [FedMomentum: Preserving LoRA Training Momentum in Federated Fine-Tuning](https://arxiv.org/abs/2603.08014) · arXiv preprint.
- <a id="he2026fedpissa"></a>**2026** · [FedPissa: Towards Federated Personalized Adaptation of Foundation Models via LoRA Subspace Mapping](https://openreview.net/forum?id=ZEWN40uNEh) · ICML.
- <a id="zhang2026fedrotlora"></a>**2026** · [FedRot-LoRA: Mitigating Rotational Misalignment in Federated LoRA](https://arxiv.org/abs/2602.23638) · ICML.
- <a id="wang2026fedsmoothlora"></a>**2026** · [FedSmoothLoRA: Toward Smoother and Faster Convergence in Federated Low-Rank Adaptation](https://arxiv.org/abs/2605.29460) · arXiv preprint.
- <a id="bian2026fedtreelora"></a>**2026** · [FedTreeLoRA: Reconciling Statistical and Functional Heterogeneity in Federated LoRA Fine-Tuning](https://arxiv.org/abs/2603.13282v2) · ICML.
- <a id="meng2026florg"></a>**2026** · [FLoRG: Federated Fine-tuning with Low-rank Gram Matrices and Procrustes Alignment](https://arxiv.org/abs/2602.17095) · ICLR.
- <a id="ramesh2025florist"></a>**2026** · [FLoRIST: Singular Value Thresholding for Efficient and Accurate Federated Fine-Tuning of Large Language Models](https://arxiv.org/abs/2506.09199) · MLSys.
- <a id="zhang2026heterogeneous"></a>**2026** · [Heterogeneous Federated Fine-Tuning with Parallel One-Rank Adaptation](https://iclr.cc/virtual/2026/poster/10007044) · ICLR.
- <a id="peng2026hilora"></a>**2026** · [HiLoRA: Hierarchical Low-Rank Adaptation for Personalized Federated Learning](https://arxiv.org/abs/2603.02785) · CVPR.
- <a id="tran2026fedpower"></a>**2026** · [Improving Parameter-Efficient Federated Learning with Differentially Private Refactorization](https://arxiv.org/abs/2605.08443) · arXiv preprint.
- <a id="rahimi2026persia"></a>**2026** · [Low-Rank Aggregation via Optimal Right-Space Projection](https://openreview.net/forum?id=2hNK26yQee) · OpenReview manuscript.
- <a id="llussa2026medduallora"></a>**2026** · [Med-DualLoRA: Local Adaptation of Foundation Models for 3D Cardiac MRI](https://arxiv.org/abs/2603.10967) · arXiv preprint.
- <a id="chen2026perfedlora"></a>**2026** · [Per-FedLoRA: Personalized Federated LoRA Fine-Tuning for Multi-Task Large Language Models](https://doi.org/10.1109/iwcmc69287.2026.11580063) · Int. Wirel. Commun. Mob. Comput. Conf. (IWCMC).
- <a id="hao2026pf2lora"></a>**2026** · [Personalized Federated Fine-tuning for Heterogeneous Data: An Automatic Rank Learning Approach via Two-Level LoRA](https://openreview.net/forum?id=X7ITc8NmSv) · ICLR submission.
- <a id="yi2026pfedlora"></a>**2026** · [pFedLoRA: Model-Heterogeneous Personalized Federated Learning with Homogeneous Low-Rank Adapter Sharing on Mobile Edge Devices](https://doi.org/10.1109/tmc.2026.3674996) · IEEE Trans. Mob. Comput.
- <a id="waseem2026prelort"></a>**2026** · [PreLort: Prefix-Nested LoRA for Federated Fine-Tuning under Rank Heterogeneity](https://arxiv.org/abs/2606.15963) · arXiv preprint.
- <a id="wu2026preventing"></a>**2026** · [Preventing Rank Collapse in Federated Low-Rank Adaptation with Client Heterogeneity](https://arxiv.org/abs/2602.13486) · arXiv preprint.
- <a id="wu2026prism"></a>**2026** · [PRISM: Exposing and Resolving Spurious Isolation in Federated Multimodal Continual Learning](https://arxiv.org/abs/2605.01061) · arXiv preprint.
- <a id="ali2026multimodalalz"></a>**2026** · [Privacy-preserving multimodal fusion for Alzheimer’s staging: A federated vision transformer framework with explainable AI](https://doi.org/10.1016/j.compmedimag.2026.102730) · Comput. Med. Imaging Graph.
- <a id="liu2026proreslora"></a>**2026** · [ProRes-LoRA: Bridging the Rank Gap via Progressive Orthogonal Residual Decomposition for Heterogeneous Federated Fine-tuning](https://doi.org/10.1109/cscwd68734.2026.11581708) · Int. Conf. Comput. Support. Coop. Work Des. (CSCWD).
- <a id="ha2026rblora"></a>**2026** · [RB-LoRA: Rank-Balanced Aggregation for Low-Rank Adaptation with Federated Fine-Tuning](https://doi.org/10.18653/v1/2026.findings-eacl.88) · Findings of EACL.
- <a id="ban2025llm"></a>**2026** · [Rethinking Parameter Sharing for LLM Fine-Tuning with Multiple LoRAs](https://doi.org/10.18653/v1/2026.findings-acl.625) · Findings of ACL.
- <a id="shen2026sdflora"></a>**2026** · [SDFLoRA: Selective Decoupled Federated LoRA for Privacy-preserving Fine-tuning with Heterogeneous Clients](https://arxiv.org/abs/2601.11219) · Int. Jt. Conf. Artif. Intell./Eur. Conf. Artif. Intell. (IJCAI-ECAI), Main Track.
- <a id="zhao2026iat"></a>**2026** · [Shift-Dependent Asymmetry: Orthogonal Inverse Low-Rank Adaptation for Federated Medical Segmentation](https://arxiv.org/abs/2606.08687) · ICML.
- <a id="senarath2026subspace"></a>**2026** · [Subspace-Constrained Federated Learning with Low-Rank Adaptation](https://arxiv.org/abs/2606.22724) · arXiv preprint.
- <a id="xiao2026vehicle"></a>**2026** · [Vehicle Profiling-Aware Personalized Federated Low-Rank Adaptation in IoVs](https://doi.org/10.1109/lcomm.2025.3633387) · IEEE Commun. Lett.
- <a id="suresh2025fedperlorahealth"></a>**2025** · [A personalized communication efficient federated learning framework with low rank adaptation for intelligent leukemia diagnosis](https://doi.org/10.1038/s41598-025-29672-1) · Sci. Rep.
- <a id="nguyen2025fedglad"></a>**2025** · [Adaptive Federated Distillation with Dual-LoRA for Personalized Representation Learning](https://doi.org/10.1145/3769102.3770624) · Proc. ACM/IEEE Symp. Edge Comput. (SEC).
- <a id="wang2025adaptive"></a>**2025** · [Adaptive LoRA Experts Allocation and Selection for Federated Fine-Tuning](https://doi.org/10.52202/085713-2553) · NeurIPS.
- <a id="almansoori2025floral"></a>**2025** · [Collaborative and Efficient Personalization with Mixtures of Adaptors](https://proceedings.mlr.press/v280/almansoori25a.html) · Conf. Parsimony Learn.
- <a id="wen2025differentially"></a>**2025** · [Differentially Private Federated Low Rank Adaptation Beyond Fixed-Matrix](https://doi.org/10.52202/085713-3825) · NeurIPS.
- <a id="wang2025ealora"></a>**2025** · [EA-Lora:Error Aggregation for Federated Learning and Efficient Fine-Tuning of Foundation Models Via SVD Decomposition](https://doi.org/10.1109/mlnlp66797.2025.11388943) · Int. Conf. Mach. Learn. Nat. Lang. Process. (MLNLP).
- <a id="yi2025fedalora"></a>**2025** · [FedALoRA: Adaptive Local LoRA Aggregation for Personalized Federated Learning in LLM](https://doi.org/10.1109/jiot.2025.3582427) · IEEE Internet Things J.
- <a id="zhao2025fedloraoptimizer"></a>**2025** · [FedLoRA-Optimizer: Federated LoRA Fine-Tuning with Global and Local Optimization in Heterogeneous Data Scenarios](https://doi.org/10.48550/arxiv.2510.11274) · arXiv preprint.
- <a id="flink2025fedloraswitch"></a>**2025** · [FedLoRASwitch: Efficient Federated Learning via LoRA Expert Hotswapping and Routing](https://doi.org/10.1109/flta67013.2025.11336447) · Int. Conf. Federated Learn. Technol. Appl. (FLTA).
- <a id="lee2025fedsvd"></a>**2025** · [FedSVD: Adaptive Orthogonalization for Private Federated Learning with LoRA](https://doi.org/10.52202/085713-3998) · NeurIPS.
- <a id="mitra2025fedvlm"></a>**2025** · [FedVLM: Scalable Personalized Vision-Language Models Through Federated Learning](https://doi.org/10.3233/faia251319) · ECAI 2025.
- <a id="fan2025helora"></a>**2025** · [HeLoRA: LoRA-heterogeneous Federated Fine-tuning for Foundation Models](https://doi.org/10.1145/3723877) · ACM Trans. Internet Technol.
- <a id="zhou2025ilora"></a>**2025** · [ILoRA: Federated Learning with Low-Rank Adaptation for Heterogeneous Client Aggregation](https://arxiv.org/abs/2511.16069) · arXiv preprint.
- <a id="li2025multilingual"></a>**2025** · [Multilingual Federated Low-Rank Adaptation for Collaborative Content Anomaly Detection across Multilingual Social Media Participants](https://doi.org/10.18653/v1/2025.emnlp-main.770) · EMNLP.
- <a id="shen2025pfedgpt"></a>**2025** · [pFedGPT: Hierarchically Optimizing LoRA Aggregation Weights for Personalized Federated GPT Models](https://doi.org/10.18653/v1/2025.emnlp-main.239) · EMNLP.
- <a id="guo2024pilora"></a>**2025** · [PILoRA: Prototype Guided Incremental LoRA for Federated Class-Incremental Learning](https://doi.org/10.1007/978-3-031-73650-6_9) · ECCV 2024 proceedings.
- <a id="raje2025ravan"></a>**2025** · [Ravan: Multi-Head Low-Rank Adaptation for Federated Fine-Tuning](https://doi.org/10.52202/085713-1622) · NeurIPS.
- <a id="li2025tensor"></a>**2025** · [Tensor-aggregated LoRA in Federated Fine-tuning](https://doi.org/10.1109/iccv51701.2025.00106) · ICCV.
- <a id="byun2025heterogeneity"></a>**2025** · [Towards Federated Low-Rank Adaptation of Language Models with Rank Heterogeneity](https://doi.org/10.18653/v1/2025.naacl-short.30) · NAACL (Short Papers).
- <a id="du2024speech"></a>**2024** · [Communication-Efficient Personalized Federated Learning for Speech-to-Text Tasks](https://doi.org/10.1109/icassp48485.2024.10447662) · IEEE Int. Conf. Acoust., Speech Signal Process. (ICASSP).
- <a id="qi2024fdlora"></a>**2024** · [FDLoRA: Personalized Federated Learning of Large Language Model via Dual LoRA Tuning](https://doi.org/10.48550/arXiv.2406.07925) · arXiv preprint.
- <a id="bai2024heterogeneous"></a>**2024** · [Federated Fine-tuning of Large Language Models under Heterogeneous Tasks and Client Resources](https://doi.org/10.52202/079017-0461) · NeurIPS.
- <a id="guo2024fedhlt"></a>**2024** · [FedHLT: Efficient Federated Low-Rank Adaption with Hierarchical Language Tree for Multilingual Modeling](https://doi.org/10.1145/3589335.3651933) · The Web Conference (WWW) Companion.
- <a id="guo2024fedlfc"></a>**2024** · [FedLFC: Towards Efficient Federated Multilingual Modeling with LoRA-based Language Family Clustering](https://doi.org/10.18653/v1/2024.findings-naacl.98) · Findings of NAACL.
- <a id="liu2024fisher"></a>**2024** · [Fisher Information-based Efficient Curriculum Federated Learning with Large Language Models](https://doi.org/10.18653/v1/2024.emnlp-main.587) · EMNLP.
- <a id="ping2024fltac"></a>**2024** · [FL-TAC: Enhanced Fine-Tuning in Federated Learning via Low-Rank, Task-Specific Adapter Clustering](https://openreview.net/forum?id=JDmAymuFFQ) · ICLR Workshop on Large Language Model (LLM) Agents.
- <a id="cho2024heterogeneous"></a>**2024** · [Heterogeneous LoRA for Federated Fine-tuning of On-Device Foundation Models](https://doi.org/10.18653/v1/2024.emnlp-main.717) · EMNLP.

</details>

### Architectures and training protocols

<details>
<summary>Browse 13 studies</summary>

- <a id="wang2026alignfed"></a>**2026** · [AlignFed: Alignment-Aware Asynchronous Federated Fine-Tuning for Large Language Models in Heterogeneous Edge Environments](https://arxiv.org/abs/2606.08197) · arXiv preprint.
- <a id="zhou2026cpsfl"></a>**2026** · [Communication-Pipelined Split Federated Learning for Foundation Model Fine-Tuning in UAV Networks](https://doi.org/10.1109/TMC.2026.3697889) · IEEE Trans. Mob. Comput.
- <a id="saadati2025decaf"></a>**2026** · [DeCAF: Decentralized consensus-and-factorization for low-rank adaptation of foundation models](https://doi.org/10.1016/j.neunet.2026.108992) · Neural Netw.
- <a id="chang2026adaptivelorafl"></a>**2026** · [Enhancing Aggregation Efficiency and Training Stability in Heterogeneous Federated Learning Using the Adaptive LoRA FL Framework](https://doi.org/10.12720/jait.17.4.678-695) · J. Adv. Inf. Technol.
- <a id="fu2026heterogeneous"></a>**2026** · [Federated fine-tuning on heterogeneous data with alternating device-to-device collaboration](https://doi.org/10.1016/j.comnet.2025.111931) · Comput. Netw.
- <a id="yang2026priority"></a>**2026** · [Priority-Aware Learning-Unlearning Correction for Dynamic Decentralized LoRA Fine-Tuning](https://arxiv.org/abs/2606.22878) · arXiv preprint.
- <a id="wang2026tadlora"></a>**2026** · [Stabilizing Decentralized Federated Fine-Tuning via Topology-Aware Alternating LoRA](https://arxiv.org/abs/2602.00451) · arXiv preprint.
- <a id="wang2025cafe"></a>**2025** · [CAFE AU LAIT: Compute-Aware Federated Augmented Low-Rank AI Training](https://doi.org/10.1145/3732775.3733580) · Proc. Platf. Adv. Sci. Comput. Conf.
- <a id="ghiasvand2025decentralized"></a>**2025** · [Decentralized Low-Rank Fine-Tuning of Large Language Models](https://doi.org/10.18653/v1/2025.realm-1.24) · Proc. Workshop for Research on Agent Language Models (REALM).
- <a id="xu2025you"></a>**2025** · [You Only Communicate Once: One-shot Federated Low-Rank Adaptation of MLLM](https://doi.org/10.52202/085713-2060) · NeurIPS.
- <a id="wang2024feditd"></a>**2024** · [FedITD: A Federated Parameter-Efficient Tuning With Pre-Trained Large Language Models and Transfer Learning Framework for Insider Threat Detection](https://doi.org/10.1109/access.2024.3482988) · IEEE Access.
- <a id="lin2024splitlora"></a>**2024** · [SplitLoRA: A Split Parameter-Efficient Fine-Tuning Framework for Large Language Models](https://arxiv.org/abs/2407.00952) · arXiv preprint.
- <a id="babakniya2023slora"></a>**2023** · [SLoRA: Federated Parameter Efficient Fine-Tuning of Language Models](https://arxiv.org/abs/2308.06522) · arXiv preprint.

</details>

### Communication and compression

<details>
<summary>Browse 32 studies</summary>

- <a id="zhu2026enhanced"></a>**2026** · [An enhanced low-rank fine-tuning framework for federated large language models](https://doi.org/10.1016/j.neucom.2025.132475) · Neurocomputing.
- <a id="song2026bitlora"></a>**2026** · [BitLoRA: Quantization-Compatible Adapter Tuning for 1.58-bit LLM in Federated On-Device AI-Agent](https://doi.org/10.1016/j.eswa.2026.131397) · Expert Syst. Appl.
- <a id="li2026fedfstq"></a>**2026** · [Fed-FSTQ: Fisher-Guided Token Quantization for Communication-Efficient Federated Fine-Tuning of LLMs on Edge Devices](https://doi.org/10.1109/TMC.2026.3711494) · IEEE Trans. Mob. Comput.
- <a id="wang2026iflora"></a>**2026** · [Federated LoRA Fine-Tuning with Pipelined Error-Mitigated Aggregation and Matrix-Wise Freezing](https://doi.org/10.18653/v1/2026.findings-acl.284) · Findings of ACL.
- <a id="fang2025sketching"></a>**2026** · [Federated Sketching LoRA: A Flexible Framework for Heterogeneous Collaborative Fine-Tuning of LLMs](https://arxiv.org/abs/2501.19389v4) · ICML.
- <a id="xie2026fedlodrop"></a>**2026** · [FedLoDrop: Federated LoRA With Dropout for Generalized LLM Fine-Tuning](https://doi.org/10.1109/JSAC.2026.3660935) · IEEE J. Sel. Areas Commun.
- <a id="li2025fedquad"></a>**2026** · [FedQuad: Adaptive Layer-Wise LoRA Deployment and Activation Quantization for Federated Fine-Tuning](https://doi.org/10.1109/tmc.2025.3637064) · IEEE Trans. Mob. Comput.
- <a id="yan2025fedsrd"></a>**2026** · [FedSRD: Sparsify-Reconstruct-Decompose for Communication-Efficient Federated Large Language Models Fine-Tuning](https://doi.org/10.1145/3774904.3792144) · The Web Conference (WWW).
- <a id="xudong2026fedtlrec"></a>**2026** · [FedTLRec: Federated Recommendation with Transformer-based Parameter Aggregation and LoRA Compression](https://doi.org/10.62762/TMI.2025.882476) · ICCK Trans. Mach. Intell.
- <a id="kuo2026flasc"></a>**2026** · [FLASC: Federated LoRA with Sparse Communication](https://doi.org/10.1145/3786335.3813151) · Proc. ACM Conf. AI Agentic Syst.
- <a id="la2026force"></a>**2026** · [FORCE: Federated Orthogonality-aware low-Rank adaptation for Communication-Efficient fine-tuning](https://doi.org/10.1109/LNET.2026.3706755) · IEEE Netw. Lett.
- <a id="huang2026gmfl"></a>**2026** · [GMFL: Efficient Global Masking for Federated LLM Fine-tuning](https://doi.org/10.18653/v1/2026.acl-long.1160) · ACL (Long Papers).
- <a id="alzahrani2026privlora"></a>**2026** · [PrivLoRA: Enhancing Privacy in LoRA-Based Fine-Tuning of Large Language Models for Federated Learning](https://doi.org/10.1109/icnc68183.2026.11416880) · Int. Conf. Comput., Netw. Commun. (ICNC).
- <a id="jiang2026resourcesplit"></a>**2026** · [Resource-Aware Split Federated Low-Rank Fine-Tuning: Joint Communication and Privacy Optimization for Lightweight Large Language Models in Heterogeneous IoT](https://doi.org/10.1109/ainit70033.2026.11558056) · Int. Semin. Artif. Intell., Netw. Inf. Technol. (AINIT).
- <a id="qiang2026tsflora"></a>**2026** · [TSFLora: Token-Compressed Split Fine-Tuning for Wireless Edge Networks](https://arxiv.org/abs/2605.23988) · arXiv preprint.
- <a id="tran2026ubsmoe"></a>**2026** · [UB-SMoE: Universally Balanced Sparse Mixture-of-Experts for Resource-adaptive Federated Fine-tuning of Foundation Models](https://arxiv.org/abs/2605.16690) · ICML.
- <a id="pathak2025democratizing"></a>**2025** · [Democratizing Instruction-Tuned LLMs with Federated LoRA: A Scalable Framework for Low-Resource Institutions](https://doi.org/10.1109/temsmet65536.2025.11467304) · IEEE Int. Conf. Technol., Eng., Manag. Soc. Impact Using Mark., Entrepreneurship Talent (TEMSMET).
- <a id="liu2025ecolora"></a>**2025** · [EcoLoRA: Communication-Efficient Federated Fine-Tuning of Large Language Models](https://doi.org/10.18653/v1/2025.emnlp-main.1046) · EMNLP.
- <a id="venkatesh2025edgefit"></a>**2025** · [Edge-FIT: Federated Instruction Tuning of Quantized LLMs for Privacy-Preserving Smart Home Environments](https://doi.org/10.1109/iemcon67450.2025.11381090) · IEEE Inf. Technol., Electron. Mob. Commun. Conf. (IEMCON).
- <a id="zhang2025fedhello"></a>**2025** · [Fed-HeLLo: Efficient Federated Foundation Model Fine-Tuning With Heterogeneous LoRA Allocation](https://doi.org/10.1109/tnnls.2025.3580495) · IEEE Trans. Neural Netw. Learn. Syst.
- <a id="zhou2025fedpelad"></a>**2025** · [Fed-PELAD: Communication-Efficient Federated Learning for Massive MIMO CSI Feedback with Personalized Encoders and a LoRA-Adapted Shared Decoder](https://arxiv.org/abs/2510.25181) · arXiv preprint.
- <a id="gao2025adaptive"></a>**2025** · [Federated Adaptive Fine-Tuning of Large Language Models with Heterogeneous Quantization and LoRA](https://doi.org/10.1109/infocom55648.2025.11044641) · IEEE Conf. Comput. Commun. (INFOCOM).
- <a id="liang2025non"></a>**2025** · [Federated Fine-Tuning Large Language Models with LoRA and Non-Orthogonal Transmission](https://doi.org/10.1109/globecom59602.2025.11432233) · IEEE Global Commun. Conf. (GLOBECOM).
- <a id="wang2025fedqlora"></a>**2025** · [Federated Fine-Tuning on Heterogeneous Devices with Adaptive Quantization and LoRA Depths](https://doi.org/10.1109/icpads67057.2025.11323139) · IEEE Int. Conf. Parallel Distrib. Syst. (ICPADS).
- <a id="su2025llms"></a>**2025** · [Federated LLMs Fine-Tuned with Adaptive Importance-Aware LoRA](https://doi.org/10.1109/icc52391.2025.11161447) · IEEE ICC.
- <a id="li2025federatedtransfer"></a>**2025** · [Federated Transfer Learning for On-Device LLMs Efficient Fine Tuning Optimization](https://doi.org/10.26599/bdma.2024.9020068) · Big Data Min. Anal.
- <a id="koo2025robust"></a>**2025** · [Towards Robust and Efficient Federated Low-Rank Adaptation with Heterogeneous Clients](https://doi.org/10.18653/v1/2025.acl-long.19) · ACL (Long Papers).
- <a id="wu2024fedbiot"></a>**2024** · [FedBiOT: LLM Local Fine-tuning in Federated Learning without Full Model](https://doi.org/10.1145/3637528.3671897) · KDD.
- <a id="deng2024smartgrid"></a>**2024** · [Federated Large Language Models for Smart Grid: A Communication Efficient LoRA Approach](https://doi.org/10.1109/iccasit62299.2024.10827901) · IEEE Int. Conf. Civ. Aviat. Saf. Inf. Technol. (ICCASIT).
- <a id="wu2024fedfmsl"></a>**2024** · [FedFMSL: Federated Learning of Foundation Models With Sparsely Activated LoRA](https://doi.org/10.1109/tmc.2024.3454634) · IEEE Trans. Mob. Comput.
- <a id="ribeiro2024flocora"></a>**2024** · [FLoCoRA: Federated Learning Compression with Low-Rank Adaptation](https://doi.org/10.23919/eusipco63174.2024.10715461) · Eur. Signal Process. Conf. (EUSIPCO).
- <a id="zhu2024promoting"></a>**2024** · [Promoting Data and Model Privacy in Federated Learning through Quantized LoRA](https://doi.org/10.18653/v1/2024.findings-emnlp.615) · Findings of EMNLP.

</details>

### Resource costs and optimization

<details>
<summary>Browse 30 studies</summary>

- <a id="wu2026adaptive"></a>**2026** · [Adaptive Rank Allocation for Federated Parameter-Efficient Fine-Tuning of Language Models](https://doi.org/10.1109/tc.2026.3655161) · IEEE Trans. Comput.
- <a id="yu2026adaptivefedlora"></a>**2026** · [AdaptiveFedLoRA: Drift-Aware Adaptive LoRA Rank Scheduling for Federated Medical Small Language Models](https://doi.org/10.64898/2026.01.18.26344237) · medRxiv preprint.
- <a id="choi2026adasplitlora"></a>**2026** · [AdaSplitLoRA: Adaptive Split Federated Learning for Efficient LLM Fine-Tuning in Wireless Networks](https://doi.org/10.1109/LWC.2026.3711276) · IEEE Wirel. Commun. Lett.
- <a id="fang2026fedpipe"></a>**2026** · [Automated Federated Pipeline for Parameter-Efficient Fine-Tuning of Large Language Models](https://doi.org/10.1109/TMC.2025.3649881) · IEEE Trans. Mob. Comput.
- <a id="dermagpt2026"></a>**2026** · [DermaGPT a federated multimodal framework with a meta learned trust function for interpretable dermatology diagnostics](https://doi.org/10.1038/s41598-026-38715-0) · Sci. Rep.
- <a id="jones2026parameter"></a>**2026** · [Federated Parameter-Efficient Adaptation for Interference Mitigation at the Wireless Edge](https://arxiv.org/abs/2604.15936) · arXiv preprint.
- <a id="lee2026fedp2eft"></a>**2026** · [FedP²EFT: Federated Learning to Personalize PEFT for Multilingual LLMs](https://doi.org/10.1609/aaai.v40i27.39443) · AAAI.
- <a id="lin2026hsplitlora"></a>**2026** · [HSplitLoRA: A Heterogeneous Split Parameter-Efficient Fine-Tuning Framework for Large Language Models](https://doi.org/10.1109/TMC.2026.3680521) · IEEE Trans. Mob. Comput.
- <a id="zou2025joint"></a>**2026** · [Joint Rank Optimization and Bandwidth Allocation for Heterogeneous Federated LoRA Fine-Tuning](https://doi.org/10.1109/tvt.2025.3623104) · IEEE Trans. Veh. Technol.
- <a id="baccour2026qualityaware"></a>**2026** · [Quality-Aware Dynamic Client-Rank Selection for Resource-Constrained Federated LoRA](https://doi.org/10.1109/iwcmc69287.2026.11580045) · Int. Wirel. Commun. Mob. Comput. Conf. (IWCMC).
- <a id="wu2026relief"></a>**2026** · [RELIEF: Turning Missing Modalities into Training Acceleration for Federated Learning on Heterogeneous IoT Edge](https://doi.org/10.1109/JIOT.2026.3725593) · IEEE Internet Things J.
- <a id="qiang2026semantic"></a>**2026** · [Semantic-aware Token Selection and Resource Optimization for Communication-efficient Split Federated Fine-tuning in Edge Intelligence](https://arxiv.org/abs/2605.26120) · arXiv preprint.
- <a id="yang2026wirelessmultitask"></a>**2026** · [Wireless Federated Multi-Task LLM Fine-Tuning via Sparse-and-Orthogonal LoRA](https://arxiv.org/abs/2602.20492) · arXiv preprint.
- <a id="wang2025wirelessparadigm"></a>**2025** · [A Federated Fine-Tuning Paradigm of Foundation Models in Heterogenous Wireless Networks](https://doi.org/10.1109/GLOBECOM59602.2025.11432417) · IEEE Global Commun. Conf. (GLOBECOM).
- <a id="hou2025adaptivewireless"></a>**2025** · [Adaptive Federated LoRA in Heterogeneous Wireless Networks with Independent Sampling](https://arxiv.org/abs/2505.23555) · arXiv preprint.
- <a id="zhou2025aflora"></a>**2025** · [AFLoRA: Adaptive Federated Fine-Tuning of Large Language Models with Resource-Aware Low-Rank Adaption](https://arxiv.org/abs/2505.24773) · arXiv preprint.
- <a id="hou2025bifdr"></a>**2025** · [BiFDR: Brain-Inspired Federated Diffusion Transformer with Reinforcement for privacy-preserving molecular generation](https://doi.org/10.1016/j.jbi.2025.104910) · J. Biomed. Inform.
- <a id="zhou2025convergence"></a>**2025** · [Convergence and Optimization of Wireless Federated Low-Rank Adaptation with Imperfect CSI](https://doi.org/10.1109/pimrc62392.2025.11275356) · IEEE Int. Symp. Pers., Indoor Mob. Radio Commun. (PIMRC).
- <a id="wang2025wirelessfinetuning"></a>**2025** · [Federated Fine-Tuning for Pre-Trained Foundation Models Over Wireless Networks](https://doi.org/10.1109/TWC.2025.3531128) · IEEE Trans. Wirel. Commun.
- <a id="hannaan2025lowrank"></a>**2025** · [Federated Learning of Low-Rank One-Shot Image Detection Models in Edge Devices with Scalable Accuracy and Compute Complexity](https://doi.org/10.1109/iwcmc65282.2025.11059568) · Int. Wirel. Commun. Mob. Comput. Conf. (IWCMC).
- <a id="sun2025wireless"></a>**2025** · [Federated Low-Rank Adaptation for Large Models Fine-Tuning Over Wireless Networks](https://doi.org/10.1109/twc.2024.3497998) · IEEE Trans. Wirel. Commun.
- <a id="saadati2025fedmeft"></a>**2025** · [Foundation Model Efficient Fine-Tuning in Centralized and Federated Settings](https://doi.org/10.1109/bigdata66926.2025.11400875) · IEEE Int. Conf. Big Data (BigData).
- <a id="thuau2025frugalfederatedviolence"></a>**2025** · [Frugal Federated Learning for Violence Detection: A Comparison of LoRA-Tuned VLMs and Personalized CNNs](https://doi.org/10.1109/flta67013.2025.11336730) · Int. Conf. Federated Learn. Technol. Appl. (FLTA).
- <a id="solat2025optimizing"></a>**2025** · [Optimizing Client Participation in Communication-Constrained Federated LLM Adaptation with LoRA](https://doi.org/10.3390/s25216538) · Sensors.
- <a id="song2025optimizingcommunication"></a>**2025** · [Optimizing Communication and Performance in Federated Learning for Large Language Models](https://doi.org/10.1109/icaiic64266.2025.10920742) · Int. Conf. Artif. Intell. Inf. Commun. (ICAIIC).
- <a id="keerthika2025pneumonia"></a>**2025** · [Proximal guided hybrid federated learning approach with parameter efficient adaptive intelligence for pneumonia diagnosis](https://doi.org/10.1038/s41598-025-32286-2) · Sci. Rep.
- <a id="zhao2025sfllm"></a>**2025** · [SflLLM: Efficient Split Federated Learning for Large Language Model over Wireless Networks](https://doi.org/10.1109/GLOBECOM59602.2025.11432069) · IEEE Global Commun. Conf. (GLOBECOM).
- <a id="kim2025two"></a>**2025** · [Two-Stage Wireless Federated LoRA Fine-Tuning with Sparsified Orthogonal Updates](https://arxiv.org/abs/2505.00333v2) · arXiv preprint.
- <a id="jiang2024personalizedwireless"></a>**2024** · [Personalized Wireless Federated Learning for Large Language Models](https://doi.org/10.48550/arxiv.2404.13238) · arXiv preprint.
- <a id="wen2023fednaspet"></a>**2023** · [When Neural Network Architecture Search Meets Federated Learning Parameter Efficient Fine Tuning](https://doi.org/10.1109/icc59986.2023.10421429) · Int. Conf. Intell. Commun. Comput. (ICC).

</details>

### Security, privacy, and robustness

<details>
<summary>Browse 22 studies</summary>

- <a id="kim2026aslora"></a>**2026** · [Adaptive Selection of LoRA Components in Privacy-Preserving Federated Learning](https://arxiv.org/abs/2605.05769v1) · arXiv preprint.
- <a id="liang2026dpfvit"></a>**2026** · [DP-FViT: Differentially private federated vision transformer with LoRA for secure and accurate medical image classification](https://doi.org/10.1016/j.bspc.2025.109388) · Biomed. Signal Process. Control.
- <a id="chen2026fedgraph"></a>**2026** · [FedGraph: Defending Federated Large Language Model Fine-Tuning Against Backdoor Attacks via Graph-Based Aggregation](https://openreview.net/forum?id=PUFCmGuuXg) · ICLR Workshop: Principled Design for Trustworthy AI: Interpretability, Robustness, and Safety across Modalities.
- <a id="zhang2026flaguard"></a>**2026** · [FLAGuard: Efficient Verifiable Federated LoRA of Large Language Models](https://doi.org/10.1109/TMC.2025.3641570) · IEEE Trans. Mob. Comput.
- <a id="dong2026lowsecurity"></a>**2026** · [Low Rank Comes with Low Security: Gradient Assembly Poisoning Attacks against Distributed LoRA-based LLM Systems](https://arxiv.org/abs/2601.00566) · arXiv preprint.
- <a id="bossy2026memorization"></a>**2026** · [Mitigating Unintended Memorization with LoRA in Federated Learning for LLMs](https://openreview.net/forum?id=WKPyZnLIW4) · Transact. Mach. Learn. Res.
- <a id="liu2026rethinking"></a>**2026** · [Rethinking LoRA for Privacy-Preserving Federated Learning in Large Models](https://openreview.net/forum?id=BPzSV4uw0x) · ICLR.
- <a id="yu2026rfdlora"></a>**2026** · [RFD-LoRA: Robust Federated Distillation for LoRA Fine-Tuning under Heterogeneous and Adversarial Clients](https://openreview.net/forum?id=srLqdXZHR0) · ICLR submission.
- <a id="tao2026safefedllm"></a>**2026** · [Safe-FedLLM: Delving into the Safety of Federated Large Language Models](https://doi.org/10.18653/v1/2026.acl-long.1120) · ACL (Long Papers).
- <a id="shaaban2026securegate"></a>**2026** · [SecureGate: Learning When to Reveal PII Safely via Token-Gated Dual-Adapters for Federated LLMs](https://doi.org/10.18653/v1/2026.acl-long.1972) · ACL (Long Papers).
- <a id="li2026sketched"></a>**2026** · [Sketched Gaussian Mechanism on Matrix for Private Federated LoRA](https://openreview.net/forum?id=4xzpNtnowK) · ICLR submission.
- <a id="zhu2026aggregator"></a>**2026** · [When the Aggregator Cheats: Data-Free Backdoors in Federated LLM-based QA Systems](https://www.usenix.org/conference/usenixsecurity26/presentation/zhu-chenqing) · USENIX Security.
- <a id="kou2026winflora"></a>**2026** · [WinFLoRA: Incentivizing Client-Adaptive Aggregation in Federated LoRA under Privacy Heterogeneity](https://doi.org/10.1145/3774904.3792295) · The Web Conference (WWW).
- <a id="liu2025differentially"></a>**2025** · [Differentially Private Low-Rank Adaptation of Large Language Model Using Federated Learning](https://doi.org/10.1145/3682068) · ACM Trans. Manag. Inf. Syst.
- <a id="miyata2025enhancing"></a>**2025** · [Enhancing Privacy and Communication Efficiency in Federated Learning Through Selective Low-Rank Adaptation and Differential Privacy](https://doi.org/10.3390/app152413102) · Appl. Sci.
- <a id="park2025fedrand"></a>**2025** · [FedRand: Enhancing Privacy in Federated Learning with Randomized LoRA Subparameter Updates](https://arxiv.org/abs/2503.07216) · arXiv preprint.
- <a id="mia2025fedshieldllm"></a>**2025** · [FedShield-LLM: A Secure and Scalable Federated Fine-Tuned Large Language Model](https://arxiv.org/abs/2506.05640) · arXiv preprint.
- <a id="li2025fop"></a>**2025** · [FOP: A Personalized Federated Learning Framework for CLIP Integrating LoRA and Differential Privacy](https://doi.org/10.1109/aibdf67964.2025.11440775) · Int. Symp. Artif. Intell. Big Data (AIBDF).
- <a id="pass2025llmbased"></a>**2025** · [Synchronizing LLM-based semantic knowledge bases via secure federated fine-tuning in semantic communication](https://doi.org/10.3389/frai.2025.1690950) · Front. Artif. Intell.
- <a id="huang2024fast"></a>**2024** · [A Fast, Performant, Secure Distributed Training Framework For LLM](https://doi.org/10.1109/icassp48485.2024.10446717) · IEEE Int. Conf. Acoust., Speech Signal Process. (ICASSP).
- <a id="xu2024dpdylora"></a>**2024** · [DP-DyLoRA: Fine-Tuning Transformer-Based Models On-Device under Differentially Private Federated Learning using Dynamic Low-Rank Adaptation](https://doi.org/10.48550/arxiv.2405.06368) · arXiv preprint.
- <a id="li2024peftattack"></a>**2024** · [PEFT-as-an-Attack! Jailbreaking Language Models during Federated Parameter-Efficient Fine-Tuning](https://doi.org/10.48550/arxiv.2411.19335) · arXiv preprint.

</details>

### Evaluation and benchmarks

<details>
<summary>Browse 11 studies</summary>

- <a id="confidence2026fedgraph"></a>**2026** · [Confidence-calibrated federated graph attention for internet of things agents under latency SLOs](https://doi.org/10.1038/s41598-026-45662-3) · Sci. Rep.
- <a id="su2026fedumm"></a>**2026** · [FedUMM: A General Framework for Federated Learning with Unified Multimodal Models](https://doi.org/10.1145/3774905.3796623) · The Web Conference (WWW) Companion.
- <a id="xiong2026medqafora"></a>**2026** · [MedQA-FoRA-MultiHospital: A Non-IID Multihospital Benchmark and Adaptive Federated Low-Rank Framework for Privacy-Preserving Medical Question Answering and Clinical Report Generation](https://doi.org/10.71448/bcds2671-5) · Bull. Comput. Data Sci.
- <a id="gutierrez2026next"></a>**2026** · [Towards the Next Frontier of LLMs, Training on Private Data: A Cross-Domain Benchmark for Federated Fine-Tuning](https://arxiv.org/abs/2605.13936) · arXiv preprint.
- <a id="naseer2026when"></a>**2026** · [When More Parameters Hurt: Foundation Model Priors Amplify Worst-Client Disparity Under Extreme Federated Heterogeneity](https://arxiv.org/abs/2605.08992) · arXiv preprint.
- <a id="chen2025federal"></a>**2025** · [Federal parameter-efficient fine-tuning for speech emotion recognition](https://doi.org/10.1016/j.eswa.2025.128154) · Expert Syst. Appl.
- <a id="kuang2023federatedscopellm"></a>**2024** · [FederatedScope-LLM: A Comprehensive Package for Fine-tuning Large Language Models in Federated Learning](https://doi.org/10.1145/3637528.3671573) · KDD.
- <a id="ye2024fedllmbench"></a>**2024** · [FedLLM-Bench: Realistic Benchmarks for Federated Learning of Large Language Models](https://doi.org/10.52202/079017-3528) · NeurIPS.
- <a id="zhang2024building"></a>**2024** · [Towards Building The Federatedgpt: Federated Instruction Tuning](https://doi.org/10.1109/icassp48485.2024.10447454) · IEEE Int. Conf. Acoust., Speech Signal Process. (ICASSP).
- <a id="fan2023fatellm"></a>**2023** · [FATE-LLM: A Industrial Grade Federated Learning Framework for Large Language Models](https://doi.org/10.48550/arxiv.2310.10049) · arXiv preprint.
- <a id="zhang2023fedpetuning"></a>**2023** · [FedPETuning: When Federated Learning Meets the Parameter-Efficient Tuning Methods of Pre-trained Language Models](https://doi.org/10.18653/v1/2023.findings-acl.632) · Findings of ACL.

</details>

### Applications

<details>
<summary>Browse 6 studies</summary>

- <a id="borno2025decentralized"></a>**2026** · [Decentralized LoRA augmented transformer with multi-scale feature learning for secured eye diagnosis](https://doi.org/10.1016/j.knosys.2026.115948) · Knowl.-Based Syst.
- <a id="zeng2026modality"></a>**2026** · [Modality augmentation and task-aware dual-modal LoRAs for multi-task multimodal federated learning](https://doi.org/10.1016/j.ipm.2025.104601) · Inf. Process. Manag.
- <a id="kalimuthu2026fedlora"></a>**2026** · [Small Language Models and Neuro-Symbolic AI in Zonal Architectures: Federated Low-Rank Adaptation (Fed-LoRA) for Regional Behavior Modeling](https://doi.org/10.63282/3050-9262.ijaidsml-v7i1p138) · Int. J. Artif. Intell. Data Sci. Mach. Learn.
- <a id="alkhunaizi2025federatedpeft"></a>**2025** · [Probing the Efficacy of Federated Parameter-Efficient Fine-Tuning of Vision Transformers for Medical Image Classification](https://doi.org/10.1007/978-3-031-77610-6_22) · MICCAI 2024 Workshops.
- <a id="chen2025clinically"></a>**2025** · [Towards Clinically Applicable Large-Model-Based Privacy-Preserving Polyp Segmentation: A Federated LoRA Approach to Colonoscopy](https://doi.org/10.1109/jbhi.2025.3639279) · IEEE J. Biomed. Health Inform.
- <a id="kim2025xflora"></a>**2025** · [X-FLoRA: Cross-modal Federated Learning with Modality-expert LoRA for Medical VQA](https://doi.org/10.18653/v1/2025.emnlp-main.422) · EMNLP.

</details>

## Research directions

- **Returned state:** At a fixed client storage budget, can joint choices of return rank and initialization improve training beyond minimizing immediate aggregation error?
- **Resource allocation:** Can measured computation, traffic in both directions, and link delay guide resource decisions better than trainable parameter count?
- **Combined protections:** At a fixed total privacy budget, can private screening improve robustness and model quality over releasing only a protected aggregate?
- **Recovery:** At a fixed checkpoint budget, which allocation to personal model state and optimizer history best supports recovery after a restart?

## Citation and corrections

To cite the survey manuscript:

```bibtex
@misc{nguyen2026fedlorasurvey,
  title  = {Federated Low-Rank Adaptation: A Survey of Methods, Systems, Security, and Research Directions},
  author = {Nguyen, Tuan and Nguyen, Minh-Duong and Doan, Khoa D. and Wong, Kok-Seng},
  year   = {2026},
  note   = {Manuscript},
  url    = {https://github.com/sail-research/fedlora-survey}
}
```

For metadata corrections or paper suggestions, [open an issue](https://github.com/sail-research/fedlora-survey/issues) with the paper link and the proposed change.
