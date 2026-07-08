---
name: seedance-video-prompt
description: Create, optimize, diagnose, or rewrite prompts for Seedance 2.0 / Jimeng / 即梦 AI video generation. Use when the user mentions Seedance, 即梦, AI video, video prompt, 文生视频, 图生视频, 多模态视频, @图片/@视频/@音频 references, video extension, video editing, camera/action/effect replication, music beat-matching, storyboards, short drama, UGC/TikTok/Reels ads, product/e-commerce commercials, realistic documentary-style video, or wants to turn an idea/image/video/audio reference into a copy-ready video generation prompt.
---

# Seedance Video Prompt

Generate copy-ready Seedance 2.0 prompts from vague ideas, assets, scripts, product briefs, or existing prompts. Keep the answer practical: ask only for missing information that changes the prompt, otherwise infer sensible defaults and produce the prompt.

## Language

Respond in the user's language unless they request another language. For final prompts, offer English when the user wants maximum model compatibility or international ad usage.

## Workflow

1. Classify the task.
   - General Seedance prompt, storyboard, extension, editing, reference transfer, or music sync: read `references/core-patterns.md`.
   - Realistic, UGC, TikTok/Reels, phone-shot, DV, surveillance, documentary, "not AI-looking": also read `references/realism.md`.
   - Product, e-commerce, ad, brand, landing product video, sales/conversion: also read `references/commerce.md`.
   - Real people, public figures, IP characters, brands/logos, politics, violence, sexuality, minors, medical/financial claims, or policy-sensitive content: read `references/compliance.md`.

2. Collect only blocking details.
   - Must know or infer: goal, duration, aspect ratio, available references, subject/product/scene, and desired style.
   - Defaults when unspecified: 10-15s; `9:16` for social ads/UGC, `16:9` for cinematic/story, `1:1` for product loops; natural audio unless the user requests silence or music.
   - If the user supplies assets, use Seedance references explicitly: `@图片1`, `@视频1`, `@音频1`; do not invent unprovided files.

3. Build the prompt using the smallest effective structure.
   - For simple 4-8s clips, use one dense paragraph.
   - For 10-15s videos, use timed segments if timing matters; otherwise use fluent cinematic narration.
   - For long videos, split into <=15s segments and chain later segments with `将@视频1延长Xs`.
   - For reference transfer, state exactly what each reference controls: appearance, scene, motion, camera, rhythm, audio, first frame, or last frame.

4. Run a quiet quality check before answering.
   - Every important subject has stable visual anchors.
   - The camera language is specific, not generic.
   - Effects are visible physical phenomena, not vague adjectives.
   - The audio matches the scene.
   - Constraints do not fight the desired style.
   - Any risky real person, IP, brand, or claim has been safely rewritten or declined.

## Output Rules

- If the user asks for a usable prompt, output the prompt first with minimal explanation.
- If optimizing an existing prompt, give a short diagnosis and a rewritten prompt.
- If multiple good directions exist, provide 2 variants maximum unless the user asks for more.
- Do not include long theory, installation instructions, or unrelated platform commentary.
- Do not output a separate "negative prompt" block for Seedance unless it helps the user; embed constraints naturally.

## Seedance Reference Basics

Common working assumptions for Seedance 2.0 style workflows:

- Images: up to 9 references for first/last frame, character, product, outfit, scene, composition, or visual style.
- Videos: up to 3 references for camera motion, action, effects, transitions, rhythm, or audio feel.
- Audio: up to 3 references for music, voice, rhythm, or sound design.
- Generated clips are usually planned in the 4-15s range; longer videos should be segmented.
- Avoid clear realistic human face uploads when the target platform blocks them; use original virtual characters or non-identifying descriptions.

## Maintenance

When editing or publishing this skill, read `references/source-attribution.md` so attribution and license notes stay intact.
