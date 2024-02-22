# Edit Anything by Segment-Anything

[![HuggingFace space](https://img.shields.io/badge/🤗-HuggingFace%20Space-cyan.svg)](https://huggingface.co/spaces/shgao/EditAnything)

This is an ongoing project aims to **Edit and Generate Anything** in an image,
powered by [Segment Anything](https://github.com/facebookresearch/segment-anything), [ControlNet](https://github.com/lllyasviel/ControlNet),
[BLIP2](https://github.com/salesforce/LAVIS/tree/main/projects/blip2), [Stable Diffusion](https://huggingface.co/spaces/stabilityai/stable-diffusion), etc.

Any forms of contribution and suggestion
are very welcomed!

# News🔥
2023/08/09 - Revise UI and code, fixed multiple known issues.

2023/07/25 - EditAnything is accepted by the ACM MM demo track.

<details>
  <summary> More update logs. </summary>
2023/05/01 - Models V0.4 based on Stable Diffusion 1.5/2.1 are released. New models are trained with more data and iterations.[Model Zoo](https://github.com/sail-sg/EditAnything#model-zoo)

2023/04/20 - We support the Customized editing with DreamBooth.
</details>

# Features

**Try our [![HuggingFace DEMO](https://img.shields.io/badge/🤗-HuggingFace%20Space-cyan.svg)](https://huggingface.co/spaces/shgao/EditAnything)🔥🔥🔥**
## Unleash creative fusion: Cross-image region drag and merge!🔥
<img width="1268" alt="image" src="https://github.com/sail-sg/EditAnything/assets/20515144/7f997db8-d2ea-4341-a7d7-dfe8ac5dd338">
<img width="1283" alt="image" src="https://github.com/sail-sg/EditAnything/assets/20515144/da34126c-d0fc-4020-85b6-1d99bed806e1">

## Clothes editing!🔥
<img width="1357" alt="image" src="https://github.com/sail-sg/EditAnything/assets/20515144/03452a0f-83ae-4257-995c-f3d8b71d4f1d">

## Haircut editing!🔥
<img width="1406" alt="image" src="https://github.com/sail-sg/EditAnything/assets/20515144/9091e3c9-c7e1-485d-bfe6-de5b21e83814">

## Draw your Sketch and Generate your Image!🔥
prompt: "a paint of  a  tree in the ground with a river."
<div>
<img width="250" alt="image" src="images/sk1.png">
<img width="250" alt="image" src="images/sk1_ex1.png">
<img width="250" alt="image" src="images/sk1_ex2.png">
</div>

## Edit Specific Thing by Text-Grounding and Segment-Anything
### Editing by Text-guided Part Mask
Text Grounding: "dog head"

Human Prompt: "cute dog"
![p](images/sample_dog_head.jpg)

<details>
  <summary> More demos. </summary>
    
Text Grounding: "cat eye"

Human Prompt: "A cute small humanoid cat"
![p](images/sample_cat_eye.jpg)
    
</details>

1) The human prompt and BLIP2 generated prompt build the text instruction.
2) The SAM model segment the input image to generate segmentation mask without category.
3) The segmentation mask and text instruction guide the image generation.

## Generate semantic labels for each SAM mask.
![p](images/sample_semantic.jpg)
```
python sam2semantic.py

```

Highlight features:
- Pretrained ControlNet with SAM mask as condition enables the image generation with fine-grained control.
- category-unrelated SAM mask enables more forms of editing and generation.
- BLIP2 text generation enables text guidance-free control.

# Model Zoo

| Model | Features | Download Path |
|-------|----------|---------------|
|SAM Pretrained(v0-1) | Good Nature Sense | [shgao/edit-anything-v0-1-1](https://huggingface.co/shgao/edit-anything-v0-1-1) |
|LAION Pretrained(v0-3) | Good Face        | [shgao/edit-anything-v0-3](https://huggingface.co/shgao/edit-anything-v0-3)
|LAION Pretrained(v0-4) | Support StableDiffusion 1.5/2.1, More training data and iterations, Good Face        | [shgao/edit-anything-v0-4-sd15](https://huggingface.co/shgao/edit-anything-v0-4-sd15) [shgao/edit-anything-v0-4-sd21](https://huggingface.co/shgao/edit-anything-v0-4-sd21)
