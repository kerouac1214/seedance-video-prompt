# Core Seedance Prompt Patterns

Use this file for general Seedance 2.0 prompt writing, including text-to-video, image/video/audio references, extension, editing, storyboards, short drama, action, effects, and beat sync.

## Prompt Anatomy

Use this order unless the user's task suggests a smaller form:

```text
[Goal / format / duration / aspect]
[Reference roles: @图片 / @视频 / @音频]
[Subject or product anchors]
[Scene and time]
[Action or story progression]
[Camera movement and shot sizes]
[Timing or fluent sequence]
[Transitions / effects]
[Audio: dialogue, ambience, music, sound effects]
[Look / lighting / texture]
[Embedded constraints]
```

High-signal formula: `Subject + Camera + Effect/Emotion + Light/Look + Audio`.

Prefer concrete cinematic verbs:

- Subject: visible identity, clothing, material, product shape, pose, state.
- Camera: push in, pull back, handheld follow, orbit, overhead, low angle, whip pan, focus pull, one-take.
- Effect or emotion: describe what appears on screen, such as sparks, condensation, dust, fabric movement, reflected light, micro-expression progression.
- Light/look: natural light, neon spill, side backlight, overcast softness, film grain, phone HDR, low-light noise.
- Audio: environment, impact, voice, music rhythm, product sounds.

## @ Reference Roles

Always assign a job to every reference.

| Reference use | Prompt phrase |
|---|---|
| First frame | `@图片1作为首帧` |
| Last frame | `@图片2作为尾帧` |
| Character/product identity | `主体外观严格参考@图片1` |
| Outfit/material | `服装和材质参考@图片2` |
| Scene/background | `场景氛围参考@图片3` |
| Camera movement | `参考@视频1的运镜` |
| Action choreography | `动作节奏参考@视频1` |
| Effects/transition | `特效和转场参考@视频1` |
| Beat/rhythm | `画面切换节奏参考@视频1或@音频1` |
| Voice/tone | `声音/语气参考@音频1` |
| Sound design | `音效参考@视频1中的现场声音` |

For multi-reference prompts, keep roles orthogonal: one reference for identity, one for motion, one for rhythm, one for scene. Do not let two references fight over the same property unless the user asks for a blend.

## Structure Choice

Use fluent narration when:

- The clip is short.
- The model can infer natural continuity.
- The user asks for atmosphere, action, product beauty, or a single continuous moment.

Use timestamps when:

- Dialogue, reveal order, or beat sync matters.
- The video has multiple story beats.
- The user wants precise control.

Template:

```text
15秒，9:16，风格...
0-3秒：镜头/主体/动作/环境/声音。
3-7秒：...
7-12秒：...
12-15秒：收束画面，声音渐弱或落版。
```

## Common Task Patterns

### Text to Video

Turn the idea into:

```text
[duration/aspect/style]。主体是[visible subject]，位于[scene]。
镜头[primary camera movement]，主体[main action]，[environment reaction]。
[effect details]，[lighting/look]。
音效：[specific ambience and key sounds]。
```

### Image to Video / Consistency

```text
@图片1中的主体作为全片唯一主体，保持身份、服装、发型、产品外观和比例一致。
[action progression]，镜头从[shot size]到[shot size]，[scene details]。
```

For multiple images, state priority: identity > product shape > scene > style > decorative details.

### Camera or Action Replication

```text
主体外观参考@图片1，场景参考@图片2。
完整参考@视频1的运镜节奏和主体动作，但将原主体替换为@图片1中的主体。
保持镜头连贯，不改变@视频1的主要运动路径。
```

### Effects or Creative Template Replication

```text
参考@视频1的特效逻辑和转场节奏，将其中的[old element]替换为@图片1中的[new element]。
特效表现为[visible physical detail]，不要只写"炫酷"或"高级"。
```

### Video Extension

```text
将@视频1延长X秒，生成时长选择X秒。
延续原视频的主体、光线、色调、镜头运动和声音环境。
0-X秒：[new action that starts from the ending frame]。
结尾：[clear stopping image].
```

For reverse extension:

```text
向前延长X秒，生成时长选择X秒。新增内容自然衔接到@视频1开头...
```

### Video Editing

```text
基于@视频1进行定向修改。
保留：原场景、主体站位、运镜节奏、整体光线。
修改：[specific element/action/expression/object].
要求：只在指定位置改变，不新增无关角色或字幕。
```

### Music Beat-Matching

```text
画面节奏参考@音频1 / @视频1的鼓点和段落变化。
每个节拍切换[pose/outfit/scene/product angle]，关键重拍出现[reveal/action].
保持主体一致，切换要干净、卡点明确。
```

### One-Take / Continuous Scene

```text
一镜到底，无切镜。镜头从[opening]开始，[path and transitions]，依次经过[scene beats]，最后停在[ending].
用遮挡、转身、经过门框、光线变化或主体靠近镜头完成自然转场。
```

### Short Drama / Dialogue

Keep dialogue short. Pair every line with emotion and action.

```text
9:16，15秒短剧。
角色A：[visual anchor]。角色B：[visual anchor]。
0-5秒：[conflict action]。台词A（语气）："..."
5-10秒：[reveal/action]。台词B（语气）："..."
10-15秒：[reversal/end pose]。台词A（语气）："..."
字幕与口型逐句对应，背景声音匹配场景。
```

### Storyboard / Grid Reference

When using a storyboard image:

```text
@图片1是一张分镜图。严格按照从左到右、从上到下的顺序生成连贯视频。
每个格子对应一个镜头段落，保持主体一致，镜头之间用自然动作或遮挡过渡。
```

If order precision matters, list each grid cell's role explicitly.

## Camera Cheat Sheet

| Need | Useful language |
|---|---|
| Establish scale | wide establishing shot, overhead, crane rise, slow pull back |
| Emphasize product/face/detail | macro close-up, focus pull, slow push in |
| Tension | handheld follow, shallow depth, off-center framing, quick pan |
| Hero reveal | low angle, backlight, orbit, slow motion cloth/material movement |
| Speed | side tracking, hood/POV mount, motion blur, whip pan |
| Premium product | controlled turntable, macro texture, specular highlight sweep |
| UGC realism | imperfect handheld, small exposure shifts, casual reframing |

## Quality Checklist

- Does every reference have a role?
- Is the subject visually stable across shots?
- Are camera movements named and motivated?
- Are effects described as visible physical details?
- Does audio reinforce the image instead of floating separately?
- Is the ending deliberate: cut to black, hold, product hero, exit, or text/logo if appropriate?
