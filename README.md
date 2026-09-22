# GPT Image (OpenAI)

GPT Image is OpenAI's image model behind ChatGPT Images, known for accurate text rendering and precise instruction-following edits.

> **Try GPT Image online →** [https://image-gpt.net](https://image-gpt.net?utm_source=github&utm_medium=ugc&utm_campaign=gptimage-official&utm_content=readme-top&utm_term=tier-b)

GPT Image is the name OpenAI uses for the image generation models that power ChatGPT Images and the Images API. The line began in March 2025 when OpenAI switched ChatGPT from DALL-E 3 to native image generation inside GPT-4o, a release that spread quickly because of how well it handled legible text, coherent layouts and edits of uploaded photos. The same model reached developers a month later as gpt-image-1, followed by a cheaper gpt-image-1-mini, an improved gpt-image-1.5 in December 2025, and the current ChatGPT Images 2.0 generation.

Unlike most competitors, GPT Image is not a standalone diffusion model bolted onto a chat interface. It is built on the same multimodal transformer as the GPT models, which is why it can read a long instruction, keep a dozen constraints in mind, render multi-line text correctly and edit an image conversationally across several turns. The trade-off is speed: high-quality outputs typically take longer than diffusion models such as Flux, and pricing is per output token rather than per image.

In the market GPT Image competes most directly with Google's Nano Banana models (Gemini 2.5 Flash Image and Gemini 3 Pro Image), Black Forest Labs' Flux family, ByteDance Seedream and Midjourney. It is generally the reference point for text rendering, infographics, UI mockups and instruction-heavy edits, while Midjourney and Flux keep an edge on pure aesthetic stills and Nano Banana on speed and cost.

## Contents

- [What GPT Image (OpenAI) can do](#what-gpt-image-openai-can-do)
- [Versions](#versions)
- [How to access GPT Image (OpenAI)](#how-to-access-gpt-image-openai)
- [Prompt examples](#prompt-examples)
- [GPT Image (OpenAI) vs alternatives](#gpt-image-openai-vs-alternatives)
- [Pricing](#pricing)
- [FAQ](#faq)
- [Links](#links)

## What GPT Image (OpenAI) can do

- Text-to-image at 1024x1024, 1024x1536 and 1536x1024 with low, medium and high quality settings; later versions extend the size and fidelity range.
- Natural-language editing of uploaded images: change one element, restyle, relight, remove or add objects, or merge several photos into one scene.
- Masked inpainting through the edits endpoint, so only the transparent region of a mask is regenerated.
- Multiple reference images in a single request (up to 16 in the API) for products, characters and styles.
- Text rendering that stays legible across signs, packaging, posters, charts, menus, multi-line paragraphs and UI mockups.
- Transparent backgrounds (PNG or WebP), JPEG/WebP output compression control and streaming of partial images while a generation is in progress.
- High input fidelity mode that preserves faces, logos and fine details from the reference image during edits.
- Multi-turn generation in ChatGPT and in the Responses API image_generation tool, where each follow-up edit builds on the previous output.

Known limitations: high-quality generations are slow compared with diffusion models, often taking well over half a minute; every output is billed per token, so large or high-quality images cost noticeably more; edits regenerate the whole image rather than touching only the requested region, so exact pixel preservation is not guaranteed even with high input fidelity; very small text, dense tables and precise numeric charts still contain errors; the moderation layer refuses requests involving real people, many copyrighted characters and explicit content; and there is no video or animation output. All outputs carry C2PA provenance metadata.

## Versions

| Version | Released | Notes |
|---|---|---|
| GPT-4o image generation (ChatGPT Images) | 2025-03 | First native image generation in ChatGPT; replaced DALL-E 3 as the default and became known for text rendering and photo edits |
| gpt-image-1 | 2025-04 | API release through the Images API: generations, edits, masks, transparency, quality tiers and up to 16 reference images |
| gpt-image-1-mini | 2025-10 | Smaller, faster and much cheaper variant for high-volume workloads |
| gpt-image-1.5 (ChatGPT Images 1.5) | 2025-12 | Faster generation, stronger instruction following and better preservation of reference details during edits |
| ChatGPT Images 2.0 (gpt-image-2) | — | Current generation; higher fidelity, improved text and layout accuracy and more precise edits |

## How to access GPT Image (OpenAI)

GPT Image is a closed, hosted model. The official ways to use it are:

- ChatGPT, where image generation is available on Free (with daily limits), Plus, Pro, Team and Enterprise plans; edits and multi-turn refinement happen in the same conversation.
- The OpenAI API: the Images API (generations and edits endpoints) with the gpt-image-1, gpt-image-1-mini and gpt-image-1.5 model IDs, and the Responses API image_generation tool for multi-turn workflows. New organisations may need to complete identity verification before the image models are enabled.
- Microsoft Azure AI Foundry and Microsoft Copilot, which host the same models under Microsoft's terms.
- Partner integrations such as Adobe Firefly, Figma and Canva, which license the model as one of several image engines.

ChatGPT image generation is available in every region where ChatGPT operates; the API is available wherever OpenAI provides API access, with the usual exclusions. If you only want to generate or edit a few images without a ChatGPT subscription or API setup, [GPT Image](https://image-gpt.net) offers pay-per-generation access in the browser with no waitlist.

**Fastest way to try it:** [Try GPT Image online](https://image-gpt.net?utm_source=github&utm_medium=ugc&utm_campaign=gptimage-official&utm_content=readme-access&utm_term=tier-b) — no waitlist, runs in the browser.

## Prompt examples

**Packaging with readable text**

```text
A photorealistic product shot of a matte white coffee bag on a light oak table, front label reads 'MORNING RIDGE' in bold black serif type with 'Single Origin Ethiopia, Medium Roast, 340 g' underneath in smaller text, soft window light from the left, shallow depth of field, a few scattered coffee beans in the foreground
```

**Infographic**

```text
A clean vertical infographic titled 'How a Heat Pump Works' with four numbered steps, each step has a simple flat-style icon and one short sentence, cool blue and warm orange colour scheme on an off-white background, sans-serif typography, all text spelled correctly and fully legible
```

**UI mockup**

```text
A mobile app screen for a habit tracker in light mode: top bar with the title 'Today', a circular progress ring showing 4 of 6 habits done, a list of habit rows with checkboxes and labels Water, Stretch, Read 20 min, Walk, Journal, Sleep by 11, a floating plus button bottom right, iOS style, crisp and realistic
```

**Editorial illustration**

```text
A hand-drawn editorial illustration in the style of a 1960s magazine, a tiny person climbing a staircase made of oversized books, muted mustard, teal and cream palette, visible ink texture, generous negative space on the left for a headline
```

**Edit instruction**

```text
Using the uploaded photo of the living room, replace the grey sofa with a green velvet three-seater, keep the rug, lamp, window light and everything else exactly as they are, match the shadows to the existing lighting
```

## GPT Image (OpenAI) vs alternatives

| Model | Max resolution | Text rendering | Editing and reference support | Access | Price tier |
|---|---|---|---|---|---|
| GPT Image (OpenAI) | 1536x1024 in gpt-image-1; higher in later versions | Excellent | Instruction edits, masks, up to 16 references, multi-turn | ChatGPT, OpenAI API, Azure, partners | Mid to high |
| Nano Banana Pro (Gemini 3 Pro Image) | Up to 4K | Very good | Conversational edits, multi-image blending, character consistency | Gemini app, Gemini API, Vertex AI | Mid |
| Flux.1 Kontext / Flux 2 | Up to about 2K (4K in Flux 2) | Good | Instruction edits, reference images; open-weight variants | BFL API, fal.ai, Replicate, self-hosted | Low to mid |
| Midjourney v7 | Up to about 2K with upscaling | Weak | Style and character references, editor, retexture | Midjourney web and Discord, subscription only | Mid |
| Seedream 4.0 (ByteDance) | Up to 4K | Good | Multi-image reference, batch generation, edits | Dreamina, Volcano Engine API, fal.ai | Low |

GPT Image is the model to reach for when the picture has to say something specific: labels, diagrams, interfaces, ads with copy, or a photo that must be changed in exactly one way. Nano Banana Pro is its closest rival on edits and beats it on speed and native resolution, Flux and Seedream are cheaper and faster for volume, and Midjourney still leads on painterly aesthetics. Where GPT Image loses is latency and cost per image, which matters for large batches.

## Pricing

In ChatGPT, image generation is included in the Free plan with a small daily allowance and in Plus, Pro, Team and Enterprise with progressively higher limits; there is no separate image add-on.

API pricing is per token rather than per image. As of the last public information, a 1024x1024 image from gpt-image-1 costs roughly $0.02 at low quality, $0.07 at medium and $0.19 at high, with larger sizes costing proportionally more and input images and prompt text billed separately at much lower rates. gpt-image-1-mini is priced several times lower, and gpt-image-1.5 and the current generation sit near the gpt-image-1 rates. The OpenAI pricing page is the only authoritative source and rates change with each release. For occasional use without an API account, pay-per-generation access such as the [GPT Image](https://image-gpt.net) link on this page avoids both the subscription and the token maths.

## FAQ

**What is GPT Image?**

GPT Image is OpenAI's image generation model family, introduced in ChatGPT in March 2025 and offered to developers as gpt-image-1 and its successors. It generates and edits images from natural-language instructions and is especially strong at rendering readable text and following detailed layout requirements.

**Is GPT Image free?**

ChatGPT's Free plan includes a small daily allowance of image generations; paid ChatGPT plans raise the limit. The API is pay-per-use with no free tier beyond any trial credits OpenAI grants a new account.

**Is there a GPT Image API?**

Yes. The OpenAI Images API exposes gpt-image-1, gpt-image-1-mini and gpt-image-1.5 for generation and editing, and the Responses API includes an image_generation tool for multi-turn workflows. Microsoft also hosts the models on Azure AI Foundry.

**Does GPT Image have an official GitHub repository?**

No. GPT Image is a closed model; OpenAI publishes API documentation and SDKs but not the model itself. This page is an independent collection of publicly available information about it.

**How do I try GPT Image online?**

Open ChatGPT and ask it to generate or edit an image, or use the OpenAI API with an API key. For a quick test without an account or subscription, https://image-gpt.net offers pay-per-generation access in the browser.

**What are the limits?**

Output sizes are 1024x1024, 1024x1536 and 1536x1024 in gpt-image-1, with larger options in later versions. High-quality images can take well over thirty seconds, edits regenerate the whole picture, tiny text and dense charts still contain errors, and the moderation layer refuses real people, many copyrighted characters and explicit content.

**Is GPT Image the same as DALL-E?**

No. DALL-E 2 and DALL-E 3 were separate diffusion models. GPT Image is built into the GPT multimodal transformer itself, which is why it handles text and detailed instructions far better; it replaced DALL-E 3 as the default in ChatGPT in March 2025.

## Links

- [Introducing ChatGPT Images 2.0 (OpenAI)](https://openai.com/index/introducing-chatgpt-images-2-0/)
- [Introducing 4o Image Generation (OpenAI)](https://openai.com/index/introducing-4o-image-generation/)
- [OpenAI image generation guide](https://platform.openai.com/docs/guides/image-generation)
- [Try GPT Image online](https://image-gpt.net)

---

*This is an independent, community-maintained information repository about GPT Image (OpenAI). It is not affiliated with, endorsed by, or sponsored by OpenAI. All trademarks belong to their respective owners. Corrections welcome via issues.*

_Last reviewed: 2026-09-22_
