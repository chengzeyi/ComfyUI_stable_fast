# ComfyUI_stable_fast

Experimental usage of [stable-fast](https://github.com/chengzeyi/stable-fast).

# Installation

```
git clone https://github.com/gameltb/ComfyUI_stable_fast custom_nodes/ComfyUI_stable_fast
```

[stable-fast installation](https://github.com/chengzeyi/stable-fast?tab=readme-ov-file#installation)

## Usage

It can work with Lora, ControlNet and lcm. SD1.5, SDXL, and SSD-1B are supported.  
Run ComfyUI with `--disable-cuda-malloc` may be possible to optimize the speed further.

> [!NOTE]
> 
> - If you are using WSL, please do not install Triton for the time being due to bugs. 
> - stable fast not work well with accelerate, So this node has no effect when the vram is low. For example: 6G vram card run SDXL.  

![sd1.5](asset/scr.png)
![ssd-1b](asset/scr1.png)

> [!NOTE]
>
> - stable fast will optimize the speed when generating images using the same model for the second time. if you switch models or Lora frequently, please consider bypass it temporarily.
> - stable fast should be directly connected to ksampler, and it is better not to have other nodes between them.
