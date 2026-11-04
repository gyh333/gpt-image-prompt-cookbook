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
| 07 | [Style Upgrade Report](07-AI%E7%A9%BF%E6%90%AD-%E8%A1%A3%E5%93%81%E5%8D%87%E7%BA%A7%E6%94%B9%E9%80%A0%E6%8A%A5%E5%91%8A/提示词.md) | Portrait → before/after style proposal board | 4 |
| 08 | [Hairstyle Upgrade Report](08-AI%E5%8F%91%E5%9E%8B%E7%BE%8E%E5%AD%A6%E5%8D%87%E7%BA%A7%E6%8A%A5%E5%91%8A/提示词.md) | Front portrait → haircut proposal + avoid list | 3 |
| 09 | [Personal Color Diagnosis](09-AI%E4%B8%AA%E4%BA%BA%E8%89%B2%E5%BD%A9%E8%AF%8A%E6%96%AD%E6%8A%A5%E5%91%8A/提示词.md) | Portrait → three-image diagnosis series | 3 |
| 10 | [Glasses Style Matching Report](10-AI%E7%9C%BC%E9%95%9C%E9%A3%8E%E6%A0%BC%E9%80%82%E9%85%8D%E6%8A%A5%E5%91%8A/提示词.md) | Front portrait → frame matching proposal | 4 |
| 11 | [Facial Aesthetic Upgrade Report](11-AI%E4%BA%94%E5%AE%98%E7%BE%8E%E5%AD%A6%E5%8D%87%E7%BA%A7%E6%8A%A5%E5%91%8A/提示词.md) | Front portrait → six-zone notes + priority matrix | 2 |
| 12 | [Minimal Geometric Poster](12-%E6%9E%81%E7%AE%80%E5%87%A0%E4%BD%95%E6%B5%B7%E6%8A%A5/提示词.md) | Product → geometric-installation key visual | 5 |
| 13 | [Restaurant Brand VI Kit](13-%E9%A4%90%E9%A5%AE%E5%93%81%E7%89%8C%E5%85%A8%E5%A5%97VI/提示词.md) | Brand name + category → touchpoint matrix board | 5 |

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

## 07 · AI Style Upgrade Report

A landscape 4:3 before/after proposal board: the same person on both sides — original outfit left, a visibly sharper and more stylish version right — ringed by style direction, palette, materials, silhouette strategy and three outfit looks.

<img src="07-AI%E7%A9%BF%E6%90%AD-%E8%A1%A3%E5%93%81%E5%8D%87%E7%BA%A7%E6%94%B9%E9%80%A0%E6%8A%A5%E5%91%8A/%E6%A1%88%E4%BE%8B/1.jpg" width="380" alt="Style upgrade report sample">

**Prompt moves**
- Pins the aesthetic first (Korean clean street / Clean Fit / City Boy / relaxed HK cool), then lists what to avoid line by line: no business wear, no middle-aged office look, no insurance-salesman styling. Negatives do more work here than positives.
- Allocates explicit visual weight to the before/after pair (55–60%) and lets the After figure sit slightly larger — that size difference is what sells the transformation.
- Defines the layout as "magazine spread + consultant proposal board", with a hard ban on Excel sheets, PPT templates and e-commerce collages.
- Nine content modules (direction / key upgrades / palette / materials / silhouette / looks / key pieces / detail notes / summary) are all forced into short labels so the model can't drift into paragraphs.

## 08 · AI Hairstyle Upgrade Report

Hair only, face untouched: original hairstyle left, recommended cut right, four "best options" cards, three "less flattering" cards and an execution guide below.

<img src="08-AI%E5%8F%91%E5%9E%8B%E7%BE%8E%E5%AD%A6%E5%8D%87%E7%BA%A7%E6%8A%A5%E5%91%8A/%E6%A1%88%E4%BE%8B/1.jpg" width="380" alt="Hairstyle upgrade report sample">

**Prompt moves**
- Narrows the variable to exactly one thing: hair. Explicit bans on changing the face, features, skin smoothing, outfit or makeup — without them, the model will "improve" the face as a bonus.
- Requires the Before shot to stay honestly bad: flat roots, messy volume, rough ends. Soften it and the comparison stops persuading anyone.
- Three-tier structure with green checks and red crosses; the avoid zone is allowed a little humor, but never mockery or deliberate ugliness.
- Six annotation points locked to bangs, crown, sides, layers, ends and color, each with numbering, arrows and detail crops so it reads like a real consultant's markup.

## 09 · AI Personal Color Diagnosis

Three separate finished images, not one long strip: an overall diagnosis page, a color-draping × styling page, and a makeup × hair × detail page — same person, same season conclusion throughout.

<img src="09-AI%E4%B8%AA%E4%BA%BA%E8%89%B2%E5%BD%A9%E8%AF%8A%E6%96%AD%E6%8A%A5%E5%91%8A/%E6%A1%88%E4%BE%8B/1_1.jpg" width="380" alt="Personal color diagnosis sample">

**Prompt moves**
- The strongest constraint is a prohibition: no preset season, no preset color names, no fixed lipstick or hair-color codes. Diagnose from the photo first. Skip this and the model slides straight into soft-autumn / milk-tea / dusty-rose defaults.
- Colors come in three layers instead of one answer — core palette, stretch palette, use-with-caution. That's what makes the report feel bounded but still full of choices.
- The diagnosis must carry a reasoning chain (skin, lips, eyes, hair, contrast → why this season), not just a verdict.
- Requires three standalone images that still read as one series — same visual language, same conclusion carried through.

## 10 · AI Glasses Style Matching Report

A frame-matching proposal: Before (no glasses) and After (the recommended pair) in the center, surrounded by four best matches, two or three worth trying, and three to avoid.

<img src="10-AI%E7%9C%BC%E9%95%9C%E9%A3%8E%E6%A0%BC%E9%80%82%E9%85%8D%E6%8A%A5%E5%91%8A/%E6%A1%88%E4%BE%8B/1.jpg" width="380" alt="Glasses matching report sample">

**Prompt moves**
- Another single-variable case: swap the glasses only, lock face, makeup, outfit and lighting. Otherwise the model fakes improvement with retouching and wardrobe changes.
- Three tiers beat a single recommendation — and the avoid tier has to explain itself: too narrow widens the face, too thick buries the features, too round flattens the jawline.
- The six annotation dimensions follow a real optician's decision chain: frame shape, width, bridge fit, thickness, color, style mood.
- Ends with something actionable: best shape, best width, material feel, colors, plus a list of avoid keywords.

## 11 · AI Facial Aesthetic Upgrade Report

Two faces, six annotated zones, one priority matrix: the After face aims for "natural refinement" rather than surgery, and the bottom splits into priority / optional / evaluate / high-caution tiers.

<img src="11-AI%E4%BA%94%E5%AE%98%E7%BE%8E%E5%AD%A6%E5%8D%87%E7%BA%A7%E6%8A%A5%E5%91%8A/%E6%A1%88%E4%BE%8B/1.jpg" width="380" alt="Facial aesthetic report sample">

**Prompt moves**
- Frames the goal as "naturally better looking, naturally more refined", then closes every plastic-surgery tell one by one: no oversized double eyelids, no epicanthoplasty, no high bridge, no pointed tip, no V-line, no lip filler.
- Bans improving the result through wardrobe — this prompt type drifts into a style report if you let it.
- Demands real skin texture, explicitly avoiding plastic and wax-figure looks, the most common failure in AI portraits.
- The priority matrix adds tiers and a disclaimer (bone-level procedures are a consultation direction only), which keeps it professional without overstepping.

## 12 · Minimal Geometric Poster

Product, packaging and ingredient slices as one visual chain, staged on cylinders, blocks and rings under high-key white light with generous negative space.

<img src="12-%E6%9E%81%E7%AE%80%E5%87%A0%E4%BD%95%E6%B5%B7%E6%8A%A5/%E6%A1%88%E4%BE%8B/1.jpg" width="380" alt="Minimal geometric poster sample">

**Prompt moves**
- Hard-codes the trio: product, packaging, and raw material or component. Drop one and the image collapses back into an ordinary e-commerce studio shot.
- Palette is derived from the product rather than fixed, which stops every poster from turning the same shade of cream.
- Geometric props are limited to support and rhythm; they may not compete with the subject. Material notes are itemized (acrylic, frosted, paper labels, fruit texture).
- Two explicit paths — use the supplied product photo, or design the packaging from scratch — because the results diverge sharply.

## 13 · Restaurant Brand VI Kit

Brand name plus category in, a full touchpoint matrix out: tote bags, cups, boxes, menus, table cards, stickers and cutlery, mixed at large, medium and small scale.

<img src="13-%E9%A4%90%E9%A5%AE%E5%93%81%E7%89%8C%E5%85%A8%E5%A5%97VI/%E6%A1%88%E4%BE%8B/1-%E5%B1%B1%E9%87%8E%E8%8C%B6%E4%BA%8B%EF%BC%88%E5%9B%BD%E6%BD%AE%E4%B8%9C%E6%96%B9%EF%BC%89.jpg" width="380" alt="Restaurant brand VI sample">

**Prompt moves**
- Only two required inputs; everything else — tone, palette, hero product, tagline, price band, material types — is derived by an explicit auto-completion rule set.
- The material list is itemized rather than described as "a packaging set". Naming cup sleeves, seals and hang tags is what produces a system instead of a pile of boxes.
- Layout rule: large items anchor, medium items inform, small items complete. That's what keeps a mockup board from falling apart.
- Every item must carry the same logo, color block and tagline; without that instruction the output reads as unrelated packaging photos.

---

## How to use

1. Open a recipe's `提示词.md` and read it whole — the negative constraints at the end matter as much as the positives.
2. Attach your own reference photo (01, 02, 03, 04, 06, 07, 08, 09, 10, 11 require one; 05, 12, 13 only need a topic or brand brief).
3. Replace the topic / parameters, keep the structure. Deleting the "avoid" section is the fastest way to get generic output.
4. Expect 1–3 retries on text-heavy recipes (01, 04, 05 and the report series 07–11) — small typos are normal.

## Notes

- All samples are AI-generated. People in them are not real, and no third-party photos are included.
- Recipes 07–11 are the "image consultant report" series, and every one of them insists on preserving the subject's identity instead of swapping the face. Use these templates on your own photos only.
- Prompts are written in Chinese. That is deliberate: for typography- and layout-heavy constraints, Chinese phrasing tends to be more precise than a translated English prompt.
- Fonts and handwritten text are the least reliable part of current models — check every label before publishing.
