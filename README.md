# Prompts

Prompts for AI artwork developed by 3Games.

- [Tips](#tips)
- [F222 Model](#f222-model)
- [TrinArt V1 Model](#trinartv1)
- [Mo Di Diffusion Model](#mo-di-diffusion)
- [Samdoesart Model](#samdoesart)
- [Default model](#default-model)
- [Pickle Scanners](#pickle-scanners)
- [Good Reading](#good-reading)

## Tips

- Use simple prompts: "rainy neon cyberpunk mega city, scyscraper, cars, people" or "high mountain lake, aquamarine blue, clear sky, evil mage tower" initally to start iterating.

- The artist, for example: "by alexi zaitsev, by Antoine Blanchard, by Brent Heighton, by Jeremy Mann" is the important part for the style, add some favourites like "masterpiece, intricate, 8k".

- negative prompts: Use a [standard negative prompt](#improved-shared-negative-prompt)

-  **DPM++2M Karras** sampler between 50-80 steps gives an ideal amount of grain for photorealistic surfaces.

- Move away from the ```euler``` family of samplers if you want more interesting skin texture. I prefer ```k heun``` at around 20 - 75 steps.

- Euler makes most things soft and fuzzy/airbrush by default comparison
 
- Skin look too soft: Try freckles, skin pores, detailed skin or goosebumps.


If you want to generate results faster, make a batch at a smaller res (360x512), select the best and do an SD upscale. It's the same but I can then do the upscale on only the one I prefer and maybe try some seeds to get the best result.

**Hires fix** is for the one that want to leave the generation running for a lot of images without having to tweak things, but it remove a lot of the human selection that's so important with SD.

You can upscale 2 times if you want.

I generally use higher dimensions (512x760) but some images will have consistency problems at these resolutions. If you use a max size of 512 it avoid that problem.

Also I should add that I do SD upscale but still change the dimensions to do only one render (so I put 680x1024) for the first upscale with a medium strength, and then do another upscale with the same dims or just a bit more, so it do 4 render with a very low strength (like 0.2)

If Version < SD 2.0 = max height == **768**

If Version > SD 2.0 = mas height == **higher than 768**


### Improved shared negative prompt:

```lowres, bad hands, text, error, missing fingers, extra digit, fewer digits, cropped, worst quality, low quality, normal quality, jpeg artifacts, signature, watermark, username, blurry, ((ugly)), ((duplicate)), ((morbid)), ((mutilated)), out of frame, extra fingers, mutated hands, ((poorly drawn hands)), ((poorly drawn face)), (((mutation))), (((deformed))), ((bad anatomy)), (((bad proportions))), ((extra limbs)), cloned face, (((disfigured))), extra limbs, gross proportions, (malformed limbs), ((missing arms)), ((missing legs)), (((extra arms))), (((extra legs))), mutated hands, (fused fingers), (too many fingers), (((long neck)))```

  
## F222 model
https://ai.zeipher.com/

Originally this Model was created for anatomically correct images of females in their "birthday suite", but you can do so much more with that.  F222 model can often use a low step count:

**Example**: 20 steps with Euler A are often already enough for perfect results.
F222 is good at it and additionally go with a higher resolution.

Another Example Prompt:

```highly detailed photography, spring, portrait of beautiful blonde woman standing in a park, ((top and miniskirt)), perfect face, perfect body, large breasts, slightly thin skin, ((sharp focus)), photo by Annie Leibovitz, intricate, natural lighting, high quality, 4k, cover photo```

negative:

``` ((out of focus body)), ((out of focus face)), ((((ugly)))), (((duplicate))), ((morbid)), ((mutilated)), [out of frame], extra fingers, mutated hands, ((poorly drawn hands)), ((poorly drawn face)), (((mutation))), (((deformed))), ((ugly)), blurry, ((bad anatomy)), (((bad proportions))), ((extra limbs)), cloned face, (((disfigured))), out of frame, ugly, extra limbs, (bad anatomy), gross proportions, (malformed limbs), ((missing arms)), ((missing legs)), (((extra arms))), (((extra legs))), mutated hands, (fused fingers), (too many fingers), (((long neck)))```

Scroll down to f222 entry.
https://rentry.org/sdmodels
**Warning**, most of the models on the page listed are nsfw.

**Additional Example**:

```"a woman in liminal space, portrait, soft diffused light, soft focus, matte, pastel colors, [[[polaroid]]], canon eos r3, f/1.8, Wolfgang Tillmans, neon haze aesthetic"```

**Negative**: 
```"(child:1.5), ugly, deformed face, disfigured, deformed, (watermarked:1.2)" ```

**Settings**:
- 768x768, 
- 20 steps, 
- DPM2 a Karras, 
- CFG scale: 9.5, 
- using Restore Faces and Highres.fix 
- Size: 512 x 512.

**More Examples**:

```highly detailed photography, spring, portrait of beautiful blonde woman standing in a park, ((top and miniskirt)), perfect face, perfect body, large breasts, slightly thin skin, ((sharp focus)), photo by Annie Leibovitz, intricate, natural lighting, high quality, 4k, cover photo```

**Negative prompt**: 

```((out of focus body)), ((out of focus face)), ((((ugly)))), (((duplicate))), ((morbid)), ((mutilated)), [out of frame], extra fingers, mutated hands, ((poorly drawn hands)), ((poorly drawn face)), (((mutation))), (((deformed))), ((ugly)), blurry, ((bad anatomy)), (((bad proportions))), ((extra limbs)), cloned face, (((disfigured))), out of frame, ugly, extra limbs, (bad anatomy), gross proportions, (malformed limbs), ((missing arms)), ((missing legs)), (((extra arms))), (((extra legs))), mutated hands, (fused fingers), (too many fingers), (((long neck)))```

- Steps: 20, 
- Sampler: DPM++ 2M Karras, 
- CFG scale: 10, 
- Seed: 2115941735, 
- Size: 512x512, 
- Model hash: 44bf0551

**Example**:

```Perfectly-centered portrait-photograph of a real life godly dragon creature with shining scales descending from heaven, lifelike, super highly detailed, professional digital painting, artstation, concept art, Unreal Engine 5, Photorealism, HD quality, 8k resolution, cinema 4d, 3D, beautiful, cinematic, art by artgerm and greg rutkowski and alphonse mucha and loish and WLOP```

**Negative**:  

```((((ugly)))), (((duplicate))), ((morbid)), ((mutilated)), [out of frame], extra fingers, mutated hands, ((poorly drawn hands)), ((poorly drawn face)), (((mutation))), (((deformed))), ((ugly)), blurry, ((bad anatomy)), (((bad proportions))), ((extra limbs)), cloned face, (((disfigured))). out of frame, ugly, extra limbs, (bad anatomy), gross proportions, (malformed limbs), ((missing arms)), ((missing legs)), (((extra arms))), (((extra legs))), mutated hands, (fused fingers), (too many fingers), (((long neck)))```

```wide shot, best quality lapis erebcir highres 1girl bangs black gloves brown hair closed mouth hair between eyes looking at viewer male focus bald beard blue eyes```

##  TrinArtv1

trinart_characters_19.2m_stable_diffusion_v1 is a stable diffusion v1-based model trained by roughly 19.2M anime/manga style images (pre-rolled augmented images included) plus final finetuning by about 50,000 images. This model seeks for a sweet spot between artistic style versatility and anatomical quality within the given model spec of SDv1.

https://huggingface.co/naclbit/trinart_characters_19.2m_stable_diffusion_v1

### Config

TrinArt 2022 Artstyle preset negative prompts:  **retro style, 1980s, 1990s, 2000s, 2005 2006 2007 2008 2009 2010 2011 2012 2013 2014 2015 2016 2017 2018 2019**

TrinArt More Details preset negative prompts:  **flat color, flat shading**

We recommend to add known sets of negative prompts in order to stabilize the anatomy such as: bad hands, fewer digits, etc.

**Example prompts**

```wide shot, high quality, htgngg animal arm rest brown hair merry chair cup dress flower from above jacket on shoulders long hair sitting solo sugar bowl fantasy adventurer's inn table teacup teapot landscape miniature (2022 Artstyle preset)```

```highres wide shot bangs bare shoulders water bird cage terrarium detached sleeves frilled frilled legwear frills hair ornament hair ribbon hood long hair medium breasts ribbon thighhighs (2019 Artstyle preset)```

```1girl standing holding sword hizzrd arm up bangs bare shoulders boots bow breasts bright pupils choker detached sleeves diamond (shape) floating floating hair footwear bow from side full body gloves leg up long hair looking at viewer open mouth outstretched arm solo streaked hair swept bangs two tone hair very long hair::4 angry::1 (2022 Artstyle preset)```

```1boy male focus standing hizzrd holding sword arm up bow bright pupils cape coat diamond (shape) floating floating hair fold-over boots footwear bow from side full body gloves leg up long sleeves looking at viewer open mouth outstretched arm open coat open clothes solo swept two tone hair thigh boots::4 angry::1.25 (2022 Artstyle preset)```

```cathedral 1girl schoolgirl momoko school uniform cats particles beautiful shooting stars detailed cathedral jacket open mouth glasses cats (2022 Artstyle preset)```

```highres 2girls yuri wide shot bangs bare shoulders water bird cage terrarium detached sleeves frilled frilled legwear frills hair ornament hair ribbon hood long hair medium breasts ribbon thighhighs (More Details preset)```

```wide shot, best quality lapis erebcir highres 1boy bangs black gloves brown hair closed mouth gloves hair between eyes looking at viewer male focus flowers green eyes (More Details preset)```

## Mo Di Diffusion

This is the fine-tuned Stable Diffusion model trained on screenshots from a popular animation studio. Use the tokens **_modern disney style_** in your prompts for the effect.

https://huggingface.co/nitrosocke/mo-di-diffusion

```modern disney lara croft```

- Steps: 50, 
- Sampler: Euler a, 
- CFG scale: 7, 
- Seed: 3940025417, 
- Size: 512x768

```modern disney (baby lion) Negative prompt: person human```

- Steps: 50, 
- Sampler: Euler a, 
- CFG scale: 7, 
- Seed: 1355059992, 
- Size: 512x512

## samdoesart

https://anonfiles.com/85B2H9Hfy9/samdoesarts_v2_ckpt
https://rentry.org/2oz58

```platinum blonde girl, samdoesart```
 
 - Steps: 35, 
 - Sampler: Euler a, 
 - CFG scale: 7, 
 - Seed: 3428273302, 
 - Size: 512x512, 
 - Model hash: e516b6bd

Note: remember to use the .vae file

Prompt: ```redhead, samdoesart```

- vae-ft-mse-840000-ema-pruned enabled, but apart from that, everything is default.
- euler a, 
- 50 steps,
-  cfg 7, 
- prompt: ```samdoesarts cyberpunk portrait```


```Dinosaurs complaining about asteroid entering Earth's atmosphere```


## Default model

**Old photography example**:

```photo, a black and white photo of an old women in a vintage dress and brim hat, people walking around her, very detailed eyes, very detailed skin, very detailed nose, inspired by Bert Hardy, pexels contest winner, inspired by Vivian Maier, people on the streets, flickr, 1940s street scene, high quality photo, afp```

### Husky

```Close-up polaroid photo, of a husky, soft lighting, outdoors, 24mm Nikon Z FX```

### Oil painting

```detailed oil painting of a cute bunyip-30000 by greg rutkowski makoto shinkai takashi takeuch with a ((pretty face)), smiling lips, and fire, (sharp eyes and focus), lit by a ((strong rim light))```

#### Negative prompt:

```((blurry)), out of frame, ((ugly)), (((bad anatomy))), gross proportions, ((cloned arms)), ((cloned hands)), ((cross eyed)), (malformed limbs), ((fused fingers)), ((too many fingers)), (poorly drawn hands), (poorly drawn face), jpeg, ((fat))```


- Steps: 50
- Sampler: Euler a
- CFG scale: 12
- Seed: 1515817498
- Size: 512x768
- Model hash: 45dee52b
- Batch size: 6
- Batch pos: 0

**Example**: 
  
```close-up photo of a natural ((young)) european woman as (beautiful farmer's daughter) , headshot, textured skin, (((skin pores))), birthmark, blonde hair, blue eyes, in the (bottom of the garden), ((vegetable harvest)),```

**Negative prompt**: 

```make up, ugly, hands, blurry, low resolution, animated, cartoonSteps: 30, Sampler: Euler a, CFG scale: 7, Size: 768x768, Model: 768-v-ema```

## Pickle Scanners

Malicious code can be executed in these any model.  These models evaluate code using ```eval``` which will execute any code regardless as there is no validation.  Some models rely on libraries outside of their scope.  These are called Pickles.  Some pickles can be bad.  Use these scanners to check for bad actors in your models:

- https://github.com/zxix/stable-diffusion-pickle-scanner

## Good Reading

- https://web.stanford.edu/class/cs81n/command.txt



