# Related Works (Previous Research)

---

## 1. Leaf Only SAM

**Paper:** [Leaf Only SAM: A Segment Anything Pipeline for Zero-Shot Automated Leaf Segmentation](https://www.researchgate.net/publication/382611063_Leaf_Only_SAM_A_Segment_Anything_Pipeline_for_Zero-Shot_Automated_Leaf_Segmentation)

**Summary:** Uses the Segment Anything Model (SAM) combined with post-processing to segment potato leaves with zero training data.

**Relevance:** This is similar to Stage 1 of the proposed approach, where large pre trained segmentation models are used to generate masks without manual labeling. It demonstrates the feasibility of zero shot segmentation for plant leaves, though SAM's performance is expected to degrade in indoor and hydroponic environments.

---

## 2. Faster Segment Anything (MobileSAM)

**Paper:** [Faster Segment Anything: Towards Lightweight SAM for Mobile Applications](https://arxiv.org/abs/2306.14289)

**Summary:** Distills SAM's heavy encoder into a lightweight encoder that is 66x smaller. However, it distills the encoder directly rather than generating synthetic training data with it.

**Relevance:** This work offers an alternative path to model compression. The proposal notes that their approach could also explore generating synthetic training data with the distilled model, which is a different strategy than direct encoder distillation.

---

## 3. FastSAM

**Paper:** [Fast Segment Anything](https://arxiv.org/abs/2306.12156)

**Summary:** Replaces SAM's ViT backbone entirely with a YOLOv8 seg architecture trained on SAM generated data.

**Relevance:** This is exactly what the project is trying to do: use SAM generated data to train a lighter, faster segmentation model. FastSAM serves as a direct precedent and proof of concept for the Stage 1 approach.

---

## 4. Zero Shot Instance Segmentation for Plant Phenotyping in Vertical Farming

**Paper:** [Zero-shot instance segmentation for plant phenotyping in vertical farming with foundation models and VC-NMS](https://www.frontiersin.org/journals/plant-science/articles/10.3389/fpls.2025.1536226/full)

**Summary:** Applies SAM to indoor and hydroponic plant segmentation, explicitly noting that SAM's zero shot performance degrades under the uneven lighting and complex backgrounds typical of vertical farms.

**Relevance:** This is a strong framing citation for why indoor environments need more than zero shot SAM. It directly motivates the project's Stage 1 goal of fine tuning a model on environment specific data to overcome these limitations.

---

## 5. Reducing the Side Effects of Oscillations in Training of Quantized YOLO Networks

**Paper:** [Reducing the Side-Effects of Oscillations in Training of Quantized YOLO Networks (WACV 2024)](https://arxiv.org/abs/2311.05109)

**Summary:** Shows that 4 bit and lower quantization aware training (QAT) is genuinely difficult for YOLO detection and segmentation models due to weight oscillation. It proposes an EMA + single epoch correction fix.

**Relevance:** If the project pursues model compression for deployment on edge hardware (e.g., drones), this paper provides important insights into the challenges of quantizing YOLO based segmentation models and a potential solution.

---

## 6. LeafTrackNet

**Paper:** [LeafTrackNet: A Deep Learning Framework for Robust Leaf Tracking in Top-Down Plant Phenotyping](https://arxiv.org/abs/2512.13130)

**Summary:** Uses an embedding based approach where cutouts of leaves within a plant are matched to similar leaves, enabling tracking of individual leaves over time with consistent IDs.

**Relevance:** This is the core method for Stage 2 of the project (tracking). Traditional tracking methods like SLAM may not work with discontinuous image feeds, making an embedding based approach necessary. Alternatively, a shape estimator algorithm could match similar leaf shapes and colors, but this is prone to error since plants change leaf shape and color frequently.
