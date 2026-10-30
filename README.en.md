# GPT-Image Prompt Cookbook

Battle-tested prompt recipes for image generation models — each one ships with the full prompt, real output samples, and the constraints that keep results stable across retries.

**English** · [简体中文](README.md)

---

## What's inside

| # | Recipe | From → To | Samples |
| :-: | --- | --- | :-: |
| 01 | [Chibi Sticker Diary Photo](01-Q%E7%89%88%E5%88%86%E8%BA%AB%E6%89%8B%E8%B4%A6%E7%85%A7/提示词.md) | Everyday photo → scrapbook page with chibi stickers | 5 |
| 02 | [Chinese Shadow Puppetry × Photography](02-%E4%B8%AD%E5%BC%8F%E4%BC%A0%E7%BB%9F%E7%9A%AE%E5%BD%B1%E6%88%8F%20x%20%E7%9C%9F%E4%BA%BA%E6%91%84%E5%BD%B1/提示词.md) | Portrait photo → split-screen fine-art poster | 5 |
| 03 | [Real Photo → Acrylic Keychain](03-%E7%9C%9F%E4%BA%BA%E7%85%A7%E7%89%87%E8%BD%AC%E4%BA%9A%E5%85%8B%E5%8A%9B%E9%92%A5%E5%8C%99%E6%89%A3%E5%8D%A1%E9%80%9A%E9%A3%8E/提示词.md) | Real photo → anime acrylic charm product shot | 1 |
| 04 | [Photo Vocabulary Scrapbook](04-%E7%9C%8B%E5%9B%BE%E5%AD%A6%E5%8D%95%E8%AF%8D%E6%89%8B%E8%B4%A6/提示词.md) | Daily-life photo → English vocabulary notes | 4 |
| 05 | [Illustrated Encyclopedia Card](05-%E7%A7%91%E6%99%AE%E7%99%BE%E7%A7%91%E5%9B%BE/提示词.md) | Any topic → modular infographic card | 7 |
| 06 | [Mirror World](06-%E9%95%9C%E5%83%8F%E4%B8%96%E7%95%8C/提示词.md) | Any subject → mirrored fine-art photography | 5 |

---

## 01 · Chibi Sticker Diary Photo

A real lifestyle photo becomes a diary page: the same person reappears 5–8 times as die-cut chibi stickers, surrounded by hand-drawn doodles and handwritten captions.

<img src="01-Q%E7%89%88%E5%88%86%E8%BA%AB%E6%89%8B%E8%B4%A6%E7%85%A7/%E6%A1%88%E4%BE%8B/1.jpg" width="380" alt="Chibi sticker diary photo sample">

**Prompt moves**
- Requires the model to infer the theme (commute / café / gym / travel / wedding) from the photo first, then match every sticker pose and caption to it — no random poses.
- Sticker treatment is spelled out: white outline, soft shadow, slight lift, die-cut edge.
- Hard rule: keep the original face, lighting and background untouched; the chibi versions must read as the same person at a glance.
- Explicit anti-list at the end (garbled text, inconsistent style, crowded layout, cheap collage feel).

## 02 · Chinese Shadow Puppetry × Photography

A 3:4 poster split exactly 50/50: real photography on top, a traditional hand-carved shadow puppet of the same moment below.

<img src="02-%E4%B8%AD%E5%BC%8F%E4%BC%A0%E7%BB%9F%E7%9A%AE%E5%BD%B1%E6%88%8F%20x%20%E7%9C%9F%E4%BA%BA%E6%91%84%E5%BD%B1/%E6%A1%88%E4%BE%8B/1.jpg" width="380" alt="Shadow puppetry poster sample">

**Prompt moves**
- Locks the geometry up front: 3:4, 1:1 vertical split, 50% each — the single biggest failure mode of split posters.
- The puppet half is described physically (carved translucent leather, articulated joints, metal rivets, bamboo control rods, rice-paper screen, backlight) so the model can't regress into a flat illustration or a silhouette.
- Pose correspondence is enforced: if the couple makes a heart with their hands above, the puppet does the same below.
- Negatives carry equal weight — no collage, no 3D plastic, no neon, no filling the frame (negative space is part of the composition).

## 03 · Real Photo → Acrylic Keychain

Turns a real photo into a product shot of a transparent acrylic charm: anime-styled character, rounded die-cut outline following the silhouette, metal ring, lanyard, clean white studio background.

<img src="03-%E7%9C%9F%E4%BA%BA%E7%85%A7%E7%89%87%E8%BD%AC%E4%BA%9A%E5%85%8B%E5%8A%9B%E9%92%A5%E5%8C%99%E6%89%A3%E5%8D%A1%E9%80%9A%E9%A3%8E/%E6%A1%88%E4%BE%8B/1.png" width="380" alt="Acrylic keychain sample">

**Prompt moves**
- The hard part is *preserving* the pose — the prompt insists on keeping limb positions, body proportions, outfit and the one key prop, then simplifies the background down to just that prop.
- Explicitly bans chibi proportions, short legs, head-too-big, and "stuffing the whole scene into the keychain".

## 04 · Photo Vocabulary Scrapbook

A daily-life photo becomes an English learning card: 5–6 common objects circled with white hand-drawn lines, each tagged with a word and one A1–A2 example sentence.

<img src="04-%E7%9C%8B%E5%9B%BE%E5%AD%A6%E5%8D%95%E8%AF%8D%E6%89%8B%E8%B4%A6/%E6%A1%88%E4%BE%8B/1.jpg" width="380" alt="Photo vocabulary scrapbook sample">

**Prompt moves**
- Object selection is filtered three ways (everyday, clear, easy noun) and allowed to drop from 6 to 5 rather than pad the list.
- Sentence difficulty is pinned to a CEFR band and a word count, which is what stops the model from writing literary prose.
- One optional chibi study buddy, with conditions: only if a person or pet exists in the photo, only one, only in a corner, never overlapping a label.

## 05 · Illustrated Encyclopedia Card

A topic in, a museum-atlas style vertical card out: hero visual, magnified detail callouts, lettered modules (profile / features / care / risks / rating card), and a Top-5 summary band.

<img src="05-%E7%A7%91%E6%99%AE%E7%99%BE%E7%A7%91%E5%9B%BE/%E6%A1%88%E4%BE%8B/1.jpg" width="380" alt="Encyclopedia card sample">

**Prompt moves**
- Supplies a module *menu* instead of a fixed layout, so the model can choose what fits the topic while the visual grammar stays consistent.
- Names the target genre precisely — natural-history atlas, not advertisement — which is the difference between an information card and a poster.
- Demands scoring cards and Top-5 blocks: concrete structures are what make a generated infographic look designed.

## 06 · Mirror World

Any subject dropped onto a vast, flawless mirror floor, so the real scene and its reflection read as two halves of the same image.

<img src="06-%E9%95%9C%E5%83%8F%E4%B8%96%E7%95%8C/%E6%A1%88%E4%BE%8B/1.png" width="380" alt="Mirror world sample">

**Prompt moves**
- Defines "a real mirror" as testable physics — accurate contact points, continuous silhouette, exact proportion and perspective match. Without it, models default to puddles, frosted glass, or a semi-transparent overlay pasted in post.
- Names the failure modes explicit negatives rarely cover: double subjects, misaligned reflections, broken mirror lines, floating weightlessness.
- Adds a dedicated finger-and-toe count block and requires the reflection to match digit for digit — the single most common breakdown in mirror images.
- Leaves aspect ratio to the model, prioritizing a complete subject plus a complete reflection.

---

## How to use

1. Open a recipe's `提示词.md` and read it whole — the negative constraints at the end matter as much as the positives.
2. Attach your own reference photo (recipes 01, 02, 03, 04, 06 require one; 05 only needs a topic).
3. Replace the topic / parameters, keep the structure. Deleting the "avoid" section is the fastest way to get generic output.
4. Expect 1–3 retries on text-heavy recipes (01, 04, 05) — small typos are normal.

## Notes

- All samples are AI-generated. People in them are not real, and no third-party photos are included.
- Prompts are written in Chinese. That is deliberate: for typography- and layout-heavy constraints, Chinese phrasing tends to be more precise than a translated English prompt.
- Fonts and handwritten text are the least reliable part of current models — check every label before publishing.
