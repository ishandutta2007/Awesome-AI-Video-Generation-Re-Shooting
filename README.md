# Awesome-AI-Video-Generation-Re-Shooting

<div align="center">

# 🎬 Awesome AI Video Generation & Re-Shooting
### Top AI Video Generation Re Shooting (Opensource) 🌟 Star if you like it! 🌟

[![Awesome](https://awesome.re)](https://awesome.re)
[![PRs Welcome](https://shields.io)](http://makeapullrequest.com)
[![License: CC0-1.0](https://shields.io)](http://creativecommons.org)

*A curated directory of open-source AI video generation models, shot-transfer / re-shooting pipelines, motion control frameworks, and commercial SaaS platforms.*

</div>

---

## 📋 Table of Contents

- [📖 Overview](#-overview)
- [🟢 Open-Source Ecosystem (Primary Focus)](#-open-source-ecosystem-primary-focus)
  - [🎥 Video Re-Shooting, Shot-Transfer & Motion Control](#-video-re-shooting-shot-transfer--motion-control)
  - [🧠 Foundation Video Generation Models (T2V / I2V)](#-foundation-video-generation-models-t2v--i2v)
  - [🎨 Node-Based UIs, Studios & Production Pipelines](#-node-based-uis-studios--production-pipelines)
  - [🎭 Character Animation, Lip-Sync & Portrait Re-Shooting](#-character-animation-lip-sync--portrait-re-shooting)
- [☁️ SaaS / Hosted Platforms](#️-saas--hosted-platforms)
  - [📊 Commercial Platform Comparison](#-commercial-platform-comparison)
- [🔄 Open-Source vs. SaaS Equivalent Matrix](#-open-source-vs-saas-equivalent-matrix)
- [🤝 Contributing](#-contributing)

---

## 📖 Overview

**AI Video Generation & Re-Shooting** covers two core pillars of modern generative filmmaking:
1. **Video Generation (T2V / I2V):** Synthesizing coherent video clips from text prompts, reference images, or first/last keyframes.
2. **Video Re-Shooting & Control (V2V / ControlNet):** Extracting camera trajectories, depth maps, optical flow, or human pose skeletons from an existing reference shot to re-render the scene with new actors, environments, or artistic styles ("copy the shot, not the actors").

---

## 🟢 Open-Source Ecosystem (Primary Focus)

### 🎥 Video Re-Shooting, Shot-Transfer & Motion Control

Tools dedicated to extracting camera choreography, depth, pose, and motion from reference videos to re-shoot scenes cleanly.

* **[maosika-ai/reshot](https://github.com/maosika-ai/reshot)** *(Apache-2.0)* — **ReShot ("Copy the shot, not the actors")**: Extracts clean depth maps, OpenPose skeletons, and Canny edge videos from reference footage to drive Seedance, MiniMax H3 ControlNet, and Wan VACE without leaking original actor identities. Includes a local Web UI and CLI.
* **[maosika-ai/ComfyUI-ReShot](https://github.com)** *(Apache-2.0)* — Native ComfyUI nodes for the ReShot pipeline, enabling seamless shot choreography and camera motion transfer directly inside node graphs.
* **[Wan-Video/Wan2.1 (VACE)](https://github.com/Wan-Video/Wan2.1)** *(Apache-2.0)* — **Video All-in-One Creation and Editing (VACE)**: Supports reference-to-video, video-to-video repainting, mask-based re-shooting, depth/pose/flow conditioning, and First-Last-Frame-to-Video (FLF2V) interpolation.
* **[guoyww/AnimateDiff](https://github.com)** *(Apache-2.0)* — Plug-and-play motion module for Stable Diffusion that pairs with ControlNet (Depth, OpenPose, Lineart) and SparseCtrl for controllable video-to-video re-shooting.
* **[hao-ai-lab/FastVideo](https://github.com/yepicaiaaron/awesome-realtime-video-generation)** *(Apache-2.0)* — Unified inference and post-training acceleration framework featuring progressive distillation for low-latency video generation and controllable workflows across HunyuanVideo and CogVideoX.

---

### 🧠 Foundation Video Generation Models (T2V / I2V)

Open-weight base models serving as open-source alternatives to Runway Gen-3, Kling AI, and Luma Dream Machine.

* **[Wan-Video/Wan2.2](https://github.com/Wan-Video/Wan2.2)** *(Apache-2.0)* — State-of-the-art Mixture-of-Experts (MoE) video generation suite (`T2V-A14B`, `I2V-A14B`, `TI2V-5B`, `Animate-14B`) delivering cinematic aesthetics and strong physics adherence on consumer and multi-GPU setups.
* **[Tencent-Hunyuan/HunyuanVideo](https://github.com)** *(Tencent Open License)* — Large-scale open video foundation model (13B parameters) renowned for realistic motion physics, lighting consistency, and native spatial-temporal VAE compression.
* **[Lightricks/LTX-Video](https://github.com)** *(Apache-2.0 / LTX Open License)* — Real-time DiT-based video generation model optimized for rapid inference speeds, low VRAM footprints, and high-FPS output.
* **[THUDM/CogVideoX](https://github.com)** *(Apache-2.0)* — Expert transformer text-to-video and image-to-video model series (`CogVideoX-2B` / `5B`) with strong prompt alignment and ecosystem tooling.
* **[Stability-AI/generative-models (Stable Video Diffusion)](https://github.com)** *(SVD Community License)* — Foundational open-weight image-to-video (`SVD` / `SVD-XT`) latent diffusion models for turning single frames into smooth multi-view or motion clips.
* **[hpcaitech/Open-Sora](https://github.com/hpcaitech/Open-sora)** *(Apache-2.0)* — Full open-source video generation pipeline providing data preprocessing, training scripts, and model weights for variable-resolution and variable-aspect-ratio generation.
* **[genmoai/mochi](https://github.com)** *(Apache-2.0)* — Asymmetric Diffusion Transformer (AsymmDiT) architecture (`Mochi 1`) focused on fluid human motion and strict prompt adherence.
* **[meituan-longcat/LongCat-Video](https://github.com/meituan-longcat/LongCat-Video)** *(MIT)* — Foundational video generation model supporting long-horizon video continuation and audio-driven generation.

---

### 🎨 Node-Based UIs, Studios & Production Pipelines

Local-first interfaces and agentic workflows for chaining generation, re-shooting, storyboarding, and timeline editing.

* **[comfyanonymous/ComfyUI](https://github.com)** *(GPL-3.0)* — The standard node-based orchestration engine for running Wan2.2, HunyuanVideo, LTX-Video, CogVideoX, SVD, and ReShot ControlNet pipelines locally.
* **[Anil-matcha/Open-Generative-AI](https://github.com/anil-matcha/open-generative-ai)** *(MIT)* — Self-hosted multi-model image and video studio supporting 600+ workflows, multi-image reference inputs, and local/remote GPU offloading.
* **[LudwigKienle/ai-video-production-editor](https://github.com/LudwigKienle/ai-video-production-editor)** *(Open-Source)* — Local-first Electron + React film production workstation uniting scriptwriting, storyboarding, ComfyUI open-weight video generation, and multi-track timeline editing.
* **[HBAI-Ltd/Toonflow-app](https://github.com/topics/video-generation)** *(Open-Source)* — Infinite-canvas AI short-drama and motion-comic production studio with asset consistency, storyboarding, and local model deployment.
* **[lcy362/agnes-video-generator](https://github.com/lcy362/agnes-video-generator)** *(MIT)* — Self-hosted multi-scene video generator supporting text-to-video, keyframe animation, narration, and subtitles via Web UI.
* **[OpenMontageInc/OpenMontage](https://github.com/OpenMontageInc/OpenMontage)** *(Open-Source)* — Agentic video production pipeline that plans, retrieves footage, and assembles multi-shot timelines automatically.
* **[openfilm/openfilm](https://github.com/openfilm/openfilm)** *(Open-Source)* — Open-source AI video agent and timeline editor allowing natural-language shot-by-shot revisions and manual element manipulation.

---

### 🎭 Character Animation, Lip-Sync & Portrait Re-Shooting

Open-source replacements for Viggle AI, HeyGen, and character motion-transfer tools.

* **[KlingAIResearch/LivePortrait](https://github.com)** *(MIT)* — High-speed portrait animation and expression re-targeting from driving videos, ideal for re-shooting facial performances.
* **[HumanAIGC/AnimateAnyone](https://github.com)** *(Research / Open Ecosystem)* — Pose-guided character image-to-video synthesis enabling full-body dance and action transfer onto reference characters (open implementations via Moore-AnimateAnyone & Open-AnimateAnyone).
* **[ZJUI/MimicMotion](https://github.com)** *(Open-Source)* — High-quality human motion transfer framework using confidence-aware pose guidance for smooth, artifact-free character re-shooting.
* **[duixcom/Duix-Avatar](https://github.com/topics/video-generation)** *(Open-Source)* — Offline digital human and AI avatar toolkit for voice-driven video synthesis and character cloning.

---

## ☁️ SaaS / Hosted Platforms

Proprietary cloud platforms offering web interfaces, APIs, and commercial video generation/stylization suites.

* **[Runway (Gen-3 Alpha / Gen-4)](https://runwayml.com)** — Industry-standard generative video suite featuring Text-to-Video, Image-to-Video, **Video-to-Video**, **Act-One** (performance capture), and camera motion controls.
* **[Kling AI](https://klingai.com)** — High-fidelity video generation model by Kuaishou offering **Motion Brush**, camera control, lip-sync, and 1080p cinematic generation.
* **[Luma Dream Machine](https://lumalabs.ai)** — Fast generative video engine featuring **Keyframe interpolation**, **Modify Video** (re-shooting/re-texturing), and camera trajectory presets.
* **[Pika Labs (Pika Art)](https://pika.art)** — Creative video platform known for **Pikaffects**, **Modify Region** (inpainting video elements), and lip-sync capabilities.
* **[Haiper AI](https://haiper.ai)** — Perceptual foundation model platform supporting Text-to-Video, Image-to-Video, and **Video Repainting** (re-shooting styles and textures).
* **[Kaiber](https://kaiber.ai)** — Artist-focused generative studio specializing in **Video-to-Video style transfer**, audio-reactive animations, and storyboard canvases.
