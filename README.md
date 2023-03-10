## Abstract
Existing video inpainting methods mainly recover the missing content by retrieving similar patches from known regions. However, due to the temporal correlation of videos, the intermediate predictions (i.e., inpainted frames) can also supply rich cues about the missing region. Motivated by this, we present a new video inpainting model with a dynamic memory bank to employ previous inpainted frames as space-time memory, which aims to dig into the valuable information from both known regions and the intermediate prediction of unknown ones. Specifically, we customize a Context-aware Memory Read (CMR) module to integrate spatio-temporal contextual cues for memory reading, ensuring discriminative features being precisely loaded. Besides, we allow the transformer inpainter to distinguish tokens by their sources via our proposed Mask-Guided Self-Attention (MGSA) mechanism, where the calculation of self-attention is guided by leveraging the mask information. With the progress of inpainting, the mask is dynamically updated to gradually enable more tokens to be utilized. Experimental results on DAVIS and Youtube-VOS datasets demonstrate our superior performances over the state-of-the-art video inpainting approaches in generating temporally-consistent content and synthesizing fine-grained details.

## Demo

![teaser](./figs/teaser.gif)

## Overview
![overall_structure](./figs/overview.png)

### :rocket: Highlights:
- **SOTA performance**: Our memory-based solution achieves significant improvements on all quantitative metrics in comparison with SOTA methods.
- **Highly effiency**: Our method processes 432 × 240 videos at 0.12 seconds per frame on a Titan XP GPU, which is nearly 15× faster than previous flow-based methods. Besides, our method has the lowest FLOPs among all compared SOTA
methods.
