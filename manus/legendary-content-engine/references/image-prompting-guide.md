# Image Prompting Guide

How to write AI image generation prompts for your brand using Nano Banana Pro,
Flux, and similar diffusion models. Derived from research on commercial-grade
image generation and adapted to your brand's visual system.

## Table of Contents

1. [The 7-Layer Prompt Architecture](#1-the-7-layer-prompt-architecture)
2. [Nano Banana Pro Specifics](#2-nano-banana-pro-specifics)
3. [Human Portrait Realism](#3-human-portrait-realism)
4. [Multi-Subject Composition](#4-multi-subject-composition)
5. [Brand Visual Consistency at Scale](#5-brand-visual-consistency-at-scale)
6. [Material and Texture Language Bank](#6-material-and-texture-language-bank)
7. [Negative Constraint Library](#7-negative-constraint-library)
8. [Example Prompts](#8-example-prompts)

---

## 1. The 7-Layer Prompt Architecture

Every brand image prompt follows a 7-layer structure. The layers are ordered
by priority: information placed earlier in the prompt carries more weight with the model.

### Layer 1: Creative Intent and Brand Reference

Open with what you are making and why. Anchor the model to the creative concept.

"I want you to create a {{IMAGE_TYPE}} using the {{BRAND_NAME}} {{BRAND_VISUAL_ELEMENT}}
in the style of {{BRAND_STYLE_REFERENCE}}."

> Example: "I want you to create a beautiful social image using the Color Clarity logo in the style of the paint graphic."

### Layer 2: Technical Cinematic Frame

Specify the camera and composition before the subject.

Key specifications:
- Lens: 35mm (environmental), 50mm (natural), 85mm (portrait), 135mm (compressed)
- Composition style: editorial, movie poster, magazine cover, product hero
- Aspect ratio when relevant: 16:9 (cinematic), 4:5 (Instagram), 9:16 (stories/reels)

### Layer 3: Environment and Background

Specify the background with precision. Vague backgrounds produce vague results.

Options:
- Clean studio (default for product and social imagery)
- Soft gradient (for editorial variation)
- Environmental context (for lifestyle shots, specify location precisely)

Always specify depth of field behavior with the background.

### Layer 4: Lighting and Post-Production Direction

Lighting shapes mood more than any other element. Use directional, specific language.

Effective lighting specifications:
- Direction: "soft directional from camera left at 45 degrees"
- Quality: "diffused," "hard with defined shadows," "backlit with rim separation"
- Color temperature: "warm golden hour," "cool blue-grey," "neutral studio"
- Post-production: "film grain," "high-end retouching," "editorial color grade"

Avoid vague terms: "good lighting," "cinematic lighting," "dramatic lighting."

### Layer 5: Subject Description

Describe subjects left-to-right with extraordinary specificity. Each subject gets:
ethnicity, hair, eyes, complexion, body type, exact pose direction, gesture semantics.

Subject description rules:
- Always specify ethnicity explicitly for accurate representation
- Describe body angle in degrees: "turned approximately 30 degrees to the left"
- Describe arm/hand/finger position precisely
- Describe gesture semantics: "as if she is pointing at someone"
- Each subject should have distinct body type, proportions, and pose
- Specify expression through observable behavior, not emotional labels

### Layer 6: Material, Texture, and Metaphor Language

Materials and textures separate professional output from generic results.
Describe optical properties, not just names.

Material language should specify:
- How light interacts with the surface (sheen, matte, reflective, translucent)
- How the material moves (flowing, rigid, draped, liquid, cascading)
- Metaphor connections ({{BRAND_MATERIAL_METAPHOR}})

> Example metaphor: "paint as fabric, color as liquid, texture as emotion"

### Layer 7: Emotional Viewer Directive + CRITICAL DIRECTIVES

Close with two components: the emotional impact on the viewer, and explicit
negative constraints.

**Emotional directive:**
"{{EMOTIONAL_DIRECTIVE}}"

> Example: "The image should evoke desire and emotion. The viewer should be able to imagine themselves standing in front of the scene where the classical beauty makes them speechless."

**CRITICAL DIRECTIVES (always include):**
```
CRITICAL DIRECTIVES:
- Do not include: {{NEGATIVE_ELEMENTS}}
- No stock photos
- No appearance of AI generation
- {{BRAND_SPECIFIC_DIRECTIVE_1}}
- {{BRAND_SPECIFIC_DIRECTIVE_2}}
```

> Example directives:
> - Do not include: robots, cyborgs, circuit boards, futuristic neon, AI brain imagery
> - Women must be hyper realistic
> - Women must be ethnically accurate in body type, complexion, and hair style

---

## 2. Nano Banana Pro Specifics

Nano Banana Pro emphasizes logical coherence and precise instruction-following:

- **Prioritize precision over atmosphere.** Clear numerical specifications
  ("3 subjects," "30 degrees," "85mm lens") outperform vague atmospheric language.
- **Use the full 7-layer structure.** The model responds well to hierarchical,
  organized prompts where each layer builds on the previous.
- **CFG scale guidance:** For photorealistic output, keep CFG in the 5-8 range.
- **Sampling steps:** 25-40 steps for production work. Diminishing returns above 50.
- **Seed management:** Fix seeds for approved compositions, then vary targeted
  prompt elements while maintaining the seed for controlled iteration.

---

## 3. Human Portrait Realism

### Skin Texture
Always specify: "natural skin texture with visible pores, fine lines appropriate
to age, subtle irregularities and micro-variations in skin tone, soft luminosity
without airbrushed appearance."

### Eyes
Specify: "bright, natural eye reflection with multiple catch lights suggesting
appropriate lighting direction, moist eye surface with subtle glistening, eyes
conveying genuine emotion rather than blank stare."

### Facial Asymmetry
Specify: "naturally asymmetrical facial features without appearing disfigured,
with subtle variation in cheekbone prominence and slight variation in eye size."

### Hands
Specify: "hands with correct digit count, natural proportion, anatomically
plausible joint structure, no webbing or malformation between digits."

### Micro-Expressions
Use FACS-informed language: "slight cheek raiser creating natural eye crinkles
combined with subtle lip corner puller for genuine warmth" rather than generic
"happy expression."

---

## 4. Multi-Subject Composition

### Spatial Arrangement
Describe positions relative to stable anchors: "three women positioned side by side,
center figure facing camera directly, left and right figures angled approximately
30 degrees inward."

### Left-to-Right Sequencing
Always describe subjects in reading order for unambiguous spatial assignment.

### Pose Mirroring and Variation
Use deliberate mirroring for compositional balance with variation in body type.

### Diversity
Always specify: "all subjects must be well proportioned with an emphasis on not
being of identical body type."

---

## 5. Brand Visual Consistency at Scale

### Seed-Based Workflow
1. Generate baseline image with specific seed
2. Get creative team approval
3. Generate variants by modifying targeted prompt elements while preserving seed
4. Maintain approved seeds in a reference library

### Template Prompt System
Use fixed elements with bracketed variables:

```
[CREATIVE INTENT: {{BRAND_NAME}} {{IMAGE_TYPE}} for {platform}]
[FRAME: cinematic portrait, {lens}mm lens, {composition} composition]
[BACKGROUND: {background_type}, no depth of field]
[LIGHTING: {lighting_setup}, film grain, high-end professional photography]
[SUBJECTS: {subject_descriptions}]
[MATERIALS: {material_descriptions}]
[EMOTIONAL DIRECTIVE: {viewer_impact}]
[CRITICAL DIRECTIVES: standard {{BRAND_NAME}} block]
```

### Batch Quality Gates
When generating 10+ images, review at 25% intervals. If quality degrades,
stop and adjust parameters before completing the batch.

---

## 6. Material and Texture Language Bank

### Fabric and Clothing
- Liquid flow: "fabric appears to be liquid flowing over the body"
- Structured: "tailored wool with defined edges and crisp silhouette"
- Metallic: "metallic fabric catching light with shifting color reflections"

### Skin and Body
- Natural: "natural skin texture with visible pores and micro-variations"
- Luminous: "soft luminosity with subtle micro-highlights on cheekbones"
- Warm: "warm undertones visible in natural light, healthy glow without filter"

### Brand Signature Materials
{{BRAND_MATERIAL_BANK}}

> Example (paint-based brand):
> - Flowing: "multicolored paint flowing and cascading, liquid texture, perfectly blended"
> - Splash: "paint splash with dynamic movement, vibrant droplets"
> - Gradient: "harmonious color gradient transitioning smoothly across the surface"

### Environment
- Studio: "clean white studio backdrop with controlled lighting, no texture"
- Soft: "soft gradient background transitioning from white to subtle warm tone"
- Atmospheric: "gentle atmospheric haze creating depth separation"

---

## 7. Negative Constraint Library

### Standard Block (Include in Every Prompt)

```
CRITICAL DIRECTIVES:
- Do not include: {{NEGATIVE_ELEMENTS}}
- No stock photos
- No appearance of AI generation
- All human subjects must be hyper realistic
- No identical body types across subjects
```

### Portrait-Specific Additions
```
- No airbrushed or plastic skin texture
- No symmetrically perfect faces
- No blank or vacant stare
- No anatomically incorrect hands or fingers
```

### Social Media Additions
```
- No text overlays (add in post-production)
- No watermarks or borders
- Compose with safe zones for platform cropping
```

---

## 8. Example Prompts

### Example 1: Hero Social Image

```
I want you to create a beautiful social image using the {{BRAND_NAME}}
{{BRAND_VISUAL_ELEMENT}} in the style of {{BRAND_STYLE_REFERENCE}}.

This is a cinematic portrait shot on 85mm lens, movie poster composition.

The background is white, no depth of field.

White studio lighting, film grain, high-end intentional professional
photography and editing.

{{HERO_SUBJECT_DESCRIPTION}}

{{HERO_MATERIAL_DESCRIPTION}}

{{HERO_EMOTIONAL_DIRECTIVE}}

CRITICAL DIRECTIVES:
{{HERO_CRITICAL_DIRECTIVES}}
```

> See the voice-and-emotion-guide for emotional directive methodology.

### Example 2: Product Feature Visualization

```
Create a {{BRAND_NAME}} product visualization image.

Shot on 50mm lens, clean product photography composition with editorial quality.

Background is a soft warm gradient from white to pale blush, no depth of field.

Soft directional studio lighting from camera left at 45 degrees, warm color
temperature, film grain, high-end retouching.

{{PRODUCT_SUBJECT_DESCRIPTION}}

The image conveys {{PRODUCT_EMOTIONAL_QUALITY}}.

CRITICAL DIRECTIVES:
- No appearance of AI generation
- Hyper realistic skin texture with natural pores and variations
- Ethnically accurate proportions
- Anatomically correct hands with proper digit count
- No stock photo aesthetic
```

### Example 3: Founder Portrait

```
Create a founder portrait for {{BRAND_NAME}} brand storytelling.

Cinematic portrait on 85mm lens, editorial magazine quality.

Background is a naturally blurred interior environment suggesting a creative
workspace. Warm tones, depth of field separating subject from background.

Soft natural window light from camera right combined with subtle fill light,
warm color temperature, minimal film grain, high-end editorial retouching.

{{FOUNDER_PORTRAIT_DESCRIPTION}}

The viewer should feel they are looking at someone who sees what others miss.

CRITICAL DIRECTIVES:
- No appearance of AI generation
- Hyper realistic, editorial photography quality
- No stock photo aesthetic
- Natural facial asymmetry for authenticity
- No glamour or beauty campaign styling
```
