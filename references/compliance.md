# Compliance and Safe Rewrites

Use this file when prompts involve public figures, realistic human references, copyrighted characters, brand names/logos, politics, explicit sexual content, violence, minors, regulated claims, or attempts to bypass platform rules.

## Core Rule

Prefer safe transformation over refusal when a non-infringing, non-harmful version can preserve the user's creative intent. Refuse only when the target request itself is unsafe or there is no reasonable compliant rewrite.

## High-Risk Areas

| User asks for | Safer handling |
|---|---|
| Real public figure or celebrity | Rewrite as an original fictional person with general visual traits; do not use the name or exact identity. |
| Clear realistic human face upload if platform blocks it | Explain briefly that the platform may block clear realistic face references; suggest stylized, non-identifying, or original virtual character references. |
| Copyrighted IP character | Rewrite as an original character preserving broad color, role, material, movement, or power type, without names, logos, symbols, or iconic marks. |
| Third-party brand/logo | Use "original unbranded [product]" unless the user owns/provides the brand asset. |
| Political leaders, parties, sensitive events | Decline or redirect to neutral fictional/non-political content. |
| Gore or graphic violence | Keep tension/action but remove gore, injury detail, and explicit impact close-ups. |
| Sexualized or nude content | Rewrite to non-explicit styling, natural movement, and age-appropriate clothing. |
| Minors in sexual/romanticized contexts | Refuse. |
| Medical, cosmetic, financial, legal guarantees | Avoid guaranteed outcomes; use demonstrative, subjective, or clearly fictional presentation. |
| Removing AI labels, deception, impersonation | Refuse or redirect to transparent creative use. |

## Rewrite Patterns

### Public Figure

```text
Replace "[name]" with "an original fictional [profession/type] with [broad visible traits], no real-person identity".
```

Example:

```text
原创中年武术演员，硬朗五官，黑色西装，雨夜街头施展近身功夫，无真实人物身份。
```

### Copyrighted Character

Formula:

```text
原创虚拟角色 + color palette + outfit/material silhouette + ability/motion style + no logo/no copyrighted symbols
```

Examples:

- Red-gold armored hero -> `原创红金色金属装甲战士，胸前圆形蓝色能量核心，全覆盖流线型头盔，无品牌标识或版权符号`
- Web-slinging hero -> `原创蓝红色紧身战衣跑酷战士，面罩遮脸，手腕发射银色丝线，擅长腾空翻转，无版权标识`
- Elemental game character -> `原创幻想角色，保留发色、服装色系和元素能量颜色，不使用原角色名称、徽记或武器造型`

### Product / Brand

If the user owns/provides the product image:

```text
@图片1中的产品作为唯一产品，保持包装和标识一致。
```

If it is a third-party brand or uncertain:

```text
原创[category]产品，[color/material/shape]，无品牌文字、无logo、无商标元素。
```

### Action Without Gore

```text
紧张动作场面，快速闪避、撞击声、尘土和碎片飞散，镜头避开伤口和血腥细节，无暴力特写。
```

### Health / Beauty / Fitness Claims

Use:

```text
视觉上呈现清爽、整洁、光泽或舒适感；不承诺治疗、永久改变或医学效果。
```

Avoid:

- "cures"
- "guaranteed"
- "permanent"
- before/after that implies medical certainty
- fake expert claims

## Output Style

- If rewriting, mention briefly: "我已把涉及真实人物/IP/品牌的部分改成原创合规版本。"
- Do not lecture unless the user asks why.
- Keep the usable prompt front and center.
- Do not include a visible "forbidden words" list inside the final Seedance prompt; embed safe constraints naturally.
