# Stable Diffusion Prompts for Image Generation 📝

A comprehensive guide to crafting effective prompts in Stable Diffusion.

## Table of Contents

1. [Introduction](#introduction)
2. [Prompt Crafting Principles](#prompt-crafting-principles)
3. [Techniques for Generating Detailed Prompts](#techniques-for-generating-detailed-prompts)
4. [Handling Common Issues with Prompts](#handling-common-issues-with-prompts)
5. [CLIP and DeepDanbooru for Image Tagging](#clip-and-deepdanbooru-for-image-tagging)
6. [Negative Prompting with Embeddings](#negative-prompting-with-embeddings)
7. [Advanced Tips and Tricks](#advanced-tips-and-tricks)
8. [Prompt Examples](#prompt-examples)

## Introduction

Stable Diffusion is a powerful technique for generating high-quality images using ML models. Crafting effective prompts is crucial to achieving desired results. This guide will provide you with deep insights and recommendations for creating prompts.

## Prompt Crafting Principles

Effective prompt design for stable diffusion follows these principles:

- **Simplicity**: Start with basic prompts that describe the core concept you want to generate.
- **Style**: Incorporate elements that define the desired style, such as artist names or specific art styles.
- **Negative Prompts**: Employ standard negative prompts to guide the model's generation process away from undesirable outcomes.
- **Sampler Selection**: Choose the appropriate sampler for your desired image quality and details.


## Techniques for Generating Detailed Prompts

- **Keyword Combinations**: Combine relevant keywords that describe the scene, objects, and colors you want to include in the generated image.
- **Explicit Descriptions**: Specify details explicitly, such as textures, lighting, and the position of objects within the scene.
- **Reference Images**: Use reference images or links to help guide the model in generating images that match your desired style or content.
- **Iterative Refinement**: Refine the prompt iteratively, making adjustments based on the outcomes of previous generations.

## Handling Common Issues with Prompts

Address common issues that may arise during the prompt design process:

- **Soft or Fuzzy Textures**: Experiment with different samplers, moving away from the `euler` family to achieve more interesting and realistic textures.
- **Lack of Detail**: Add specific keywords to emphasize desired details, such as `freckles, skin pores, detailed skin, goosebumps` for skin textures.
- **Inconsistent Outcomes**: Limit the dimensions of the generated image to avoid consistency issues, and consider upscaling the image as needed.

## CLIP and DeepDanbooru for Image Tagging

In this section, we will discuss two image tagging systems, CLIP and DeepDanbooru, and provide a few simple examples of image tagging with each.

### CLIP

CLIP (Contrastive Language-Image Pretraining) is an image tagging and zero-shot learning model. It is trained on a vast dataset of images and text captions, enabling it to understand and generate a wide variety of tags for images. CLIP can be used to create detailed prompts for stable diffusion models by providing relevant tags that describe the content of an image.

**Example 1**: An image of a beautiful sunset at the beach might be tagged by CLIP as:
```
ocean, beach, sunset, waves, sand, palm trees, golden sky
```

**Example 2**: An image of a cat sitting on a windowsill might be tagged by CLIP as:
```
cat, windowsill, sitting, whiskers, fluffy, indoor, looking outside
```

### DeepDanbooru

DeepDanbooru is an image tagging system that uses deep learning to automatically assign tags to images, primarily focusing on anime-style and any type of cartoon image. It is trained on a large dataset of images with associated tags, allowing it to recognize a wide range of attributes, characters, and styles.

**Example 1**: An image of a character with blue hair and and white armor in a forest:
```
1girl, blue_hair, white_armor, smiling, long_hair, ribbon, solo, forest
```

**Example 2**: An image ofa landscape with a cherry blossom tree:
```
cherry_blossoms, no_humans, landscape, tree, sky, petals, scenic
```

Both CLIP and DeepDanbooru can be used to generate tags for images, which can then be utilized as prompts for stable diffusion models. By employing these tagging systems, you can guide the image generation process more effectively, ensuring that the generated images closely match your desired content and style.

## Negative Prompting with embeddings

Negative prompting is an approach that uses textual inversions or contrasting terms in the prompts to encourage a language model to generate better responses or predictions. This technique can be beneficial when addressing issues like hand-fixing in generated outputs.

One example of negative prompting is the use of EasyNegative embedding, which can be found at [CivitAI](https://civitai.com/models/7808/easynegative) and [Hugging Face](https://huggingface.co/datasets/gsdf/EasyNegative). By incorporating EasyNegative in a negative prompt, it can help improve the quality of generated responses. An example of using EasyNegative in a negative prompt is as follows:

```
(EasyNegative:1.2), (monochrome:1.1), (greyscale),
```

![xyz_grid-0039-b644d850c9-3912355876.jpeg](https://imagecache.civitai.com/xG1nkqKTMzGDvpLrqFT7WA/8c1de243-daf4-413e-386e-d5b8a33e7e00/width=4096/xyz_grid-0039-b644d850c9-3912355876.jpeg)


Another approach to negative prompting is using bad_prompt_v2, a textual inversion that can be employed to correct hand-fixing issues in generated outputs. More information about bad_prompt_v2 can be found on the [Hugging Face page](https://huggingface.co/datasets/Nerfgun3/bad_prompt).

An example of utilizing bad_prompt_v2 in a negative prompt:

```
(bad_prompt_version2:0.8), (worst quality:1.4), (low quality:1.4) , (monochrome:1.1)
```

By utilizing resources like EasyNegative and bad_prompt_v2, it is possible to create more accurate and reliable generated responses.

![bad_prompt_showcase.jpg](https://huggingface.co/datasets/Nerfgun3/bad_prompt/resolve/main/bad_prompt_showcase.jpg)


## Advanced Tips and Tricks

Employ advanced techniques to optimize your prompts for stable diffusion:

- **Fine-Tuning the Sampler**: Adjust the DPM++2M Karras sampler steps to find the optimal balance between graininess and photorealism.
- **Resolution Management**: Generate images at smaller resolutions, and perform an SD upscale to save time while maintaining quality.
- **Multiple Upscales**: If necessary, perform upscaling multiple times to achieve the desired image quality.
- **Hires Fix**: Use the Hires fix option for generating numerous images without manual tweaking, but be mindful that it reduces the level of human selection.

By following these guidelines and recommendations, you can craft effective prompts that drive stable diffusion to produce high-quality images that match your desired style and content.

## Prompt Examples

A collection of prompt examples to inspire and guide the creation of effective prompts.

1. **Cyberpunk Cityscape**

   ```
   neon-lit cyberpunk city at night, futuristic skyscrapers, flying cars, crowded streets, by Syd Mead
   ```

2. **Mystical Forest**

   ```
   enchanting forest, glowing trees, magical creatures, dense fog, moonlit night, by Brian Froud
   ```

3. **Renaissance-Inspired Portrait**

   ```
   Renaissance-style portrait, woman wearing a pearl necklace, soft lighting, elegant attire, by Leonardo da Vinci
   ```

4. **Vintage Travel Poster**

   ```
   vintage travel poster, tropical beach, palm trees, golden sunset, art deco style, by A.M. Cassandre
   ```

5. **Sci-Fi Space Scene**

   ```
   epic sci-fi space battle, spaceships, laser beams, distant planets, vibrant colors, by Chris Foss
   ```

6. **Wildlife Illustration**

   ```
   realistic wildlife illustration, lion family resting in the grass, African savanna, golden hour, by Robert Bateman
   ```

7. **Fantasy Landscape**

   ```
   dreamy fantasy landscape, floating islands, waterfalls, dragons soaring in the sky, by Roger Dean
   ```

8. **Abstract Art**

   ```
   abstract expressionist painting, bold colors, dynamic brush strokes, intense emotion, by Jackson Pollock
   ```

9. **Forest Guardian Warrior**

   ```
   A majestic forest guardian warrior, with hair flowing in the wind and piercing blue eyes, stands near a rainforest with a cascading waterfall in the background. She wears gleaming gold and white armor, adorned with big hoop gold earrings and a tiara. A battle axe and broad sword hang from her belt, ready for battle. This should be a lifelike, super highly detailed, professional digital painting with HD quality and 8k resolution, in the style of Artgerm, Greg Rutkowski, and Loish.
   ```

10. **Medieval Knight Warrior**

   ```
   A noble and chivalrous medieval knight warrior, with hair flowing in the wind and piercing blue eyes, stands in front of a castle with a clear blue sky in the background. She wears gleaming gold and white armor, adorned with big hoop gold earrings and a tiara. A battle axe and broad sword hang from her belt, ready for battle. This should be a lifelike, super highly detailed, professional digital painting with HD quality and 8k resolution, in the style of Alphonse Mucha, Artgerm, and Greg Rutkowski.
   ```

11. **Futuristic Space Warrior**

   ```
   A fierce and futuristic space warrior, with hair flowing in the wind and piercing blue eyes, stands on the bridge of a spaceship with stars and galaxies in the background. She wears gleaming gold and white armor, adorned with big hoop gold earrings and a tiara. A laser sword and plasma blaster hang from her belt, ready for battle. This should be a lifelike, super highly detailed, professional digital painting with HD quality and 8k resolution, in the style of WLOP, Artgerm, and Greg Rutkowski.
   ```

12. **Mythical Sea Warrior**

   ```
   A mythical sea warrior, with hair flowing in the wind and piercing blue eyes, stands on the rocky shore of an island with a stormy sea in the background. She wears gleaming gold and white armor, adorned with big hoop gold earrings and a tiara. A trident and harpoon hang from her belt, ready for battle. This should be a lifelike, super highly detailed, professional digital painting with HD quality and 8k resolution, in the style of Alphonse Mucha, Loish, and Artgerm.
   ```

These prompt examples showcase how to effectively combine scene descriptions, specific objects, artistic styles, and artist names to guide stable diffusion in generating the desired images.
