# Seedance Video Prompt Skill

A Codex skill for creating, optimizing, and diagnosing structured prompts for Seedance 2.0 / Jimeng / 即梦 AI video generation.

This skill turns rough ideas, scripts, product briefs, image/video/audio references, or existing prompts into copy-ready video prompts. It focuses on practical prompt patterns for multimodal Seedance workflows, including `@图片`, `@视频`, and `@音频` reference usage.

## What It Covers

- General Seedance 2.0 prompt writing
- Text-to-video and image-to-video prompts
- Camera, action, effect, and rhythm reference transfer
- Video extension and video editing prompts
- Timecoded storyboards for 10-15s clips
- Short drama and dialogue prompts
- Product, e-commerce, and TikTok/Reels ad prompts
- Realistic UGC, documentary, phone-shot, DV, VHS, CCTV, and anti-AI-looking prompts
- Compliance-aware rewrites for public figures, copyrighted IP, brands, claims, and sensitive topics

## Install

Copy this folder into your Codex skills directory:

```bash
mkdir -p ~/.codex/skills
cp -R seedance-video-prompt ~/.codex/skills/
```

Then invoke it in Codex with:

```text
Use $seedance-video-prompt to turn my video idea into a Seedance 2.0 prompt.
```

You can also trigger it naturally by asking for Seedance / 即梦 / AI video prompt help.

## Example Requests

```text
帮我写一个 15 秒 Seedance 产品广告提示词，竖屏，主体是 @图片1 里的香水瓶。
```

```text
Use $seedance-video-prompt to make this phone-shot skincare UGC prompt feel less AI-generated.
```

```text
我有 @图片1 角色图和 @视频1 运镜参考，帮我写一条动作复刻提示词。
```

```text
将 @视频1 向后延长 10 秒，保持原来的光线、角色和镜头运动。
```

## Skill Structure

```text
seedance-video-prompt/
├── SKILL.md
├── agents/
│   └── openai.yaml
├── references/
│   ├── core-patterns.md
│   ├── realism.md
│   ├── commerce.md
│   ├── compliance.md
│   └── source-attribution.md
└── LICENSE
```

## Reference Files

- `references/core-patterns.md` - Core Seedance prompt structures, reference roles, timed storyboards, extension, editing, beat sync, and camera language.
- `references/realism.md` - Realistic footage identity, device aesthetics, anti-AI imperfections, human micro-behavior, and environment realism.
- `references/commerce.md` - Product showcase, UGC ads, before/after, unboxing, problem-solution, premium, food/beverage, and e-commerce conversion patterns.
- `references/compliance.md` - Safe rewrite patterns for public figures, copyrighted characters, third-party brands, sensitive content, and regulated claims.
- `references/source-attribution.md` - Reviewed source repositories, licenses, and publication guidance.

## Design Philosophy

The skill is intentionally compact at the entry point. `SKILL.md` decides which workflow applies, then loads only the relevant reference file. This keeps Codex responsive while preserving deeper prompt engineering guidance for specialized cases.

The content is synthesized and rewritten from public Seedance prompt resources. It keeps reusable methods and removes redundant examples, installation clutter, platform promotion, and large prompt dumps.

## License

MIT. See `LICENSE`.

## Attribution

This project was synthesized from a review of public Seedance prompt repositories. See `references/source-attribution.md` for source links and license notes.
