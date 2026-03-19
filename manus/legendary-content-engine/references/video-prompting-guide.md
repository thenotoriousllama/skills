# Video Prompting Guide

How to write AI video generation prompts using VEO 3.1, Sora, Runway Gen-3 Alpha,
and similar models. Grounded in research on cinematic video generation and adapted
to your brand voice and visual system.

## Table of Contents

1. [Video vs. Image Prompting](#1-video-vs-image-prompting)
2. [The 5-Part Video Prompt Architecture](#2-the-5-part-video-prompt-architecture)
3. [VEO 3.1 Specifics](#3-veo-31-specifics)
4. [Camera Movement Vocabulary](#4-camera-movement-vocabulary)
5. [Temporal Control](#5-temporal-control)
6. [Subject Consistency](#6-subject-consistency)
7. [Short-Form Social Video](#7-short-form-social-video)
8. [Example Prompts](#8-example-prompts)

---

## 1. Video vs. Image Prompting

Video prompts require everything an image prompt needs plus three additional
dimensions that image prompts do not:

- **Temporal progression**: What happens over time, not just what exists
- **Camera movement**: How the viewer's perspective changes through space
- **Action and pacing**: What subjects do, at what speed, in what sequence

An image prompt that says "a woman in a flowing dress" produces a static moment.
A video prompt must specify: what she does, how the camera reveals her, how long
each action takes, and how the scene evolves across the full duration.

---

## 2. The 5-Part Video Prompt Architecture

Every brand video prompt follows a 5-part structure. This ordering ensures the
model prioritizes spatial and temporal relationships before rendering specific content.

### Part 1: Cinematography

Specify camera movement, framing, and lens before anything else.

"Slow dolly-in from medium shot to close-up, shot on 85mm lens with shallow
depth of field."

This establishes: how the camera moves (dolly-in), the framing transition
(medium to close-up), the lens character (85mm portrait compression), and
the focus behavior (shallow DOF).

### Part 2: Subject

Identify the primary focal point with permanent visual characteristics.
Keep subject description concise in video prompts. Use reference images
for character consistency when possible.

Separate subject appearance from action. Do not combine "a woman looking
worried while picking up her phone" into one clause. Split them.

### Part 3: Action

Describe what the subject does with explicit temporal beats and observable motion.

"She walks to the window in three steps, pauses for two seconds, then turns
back to face camera with a subtle shift in expression."

Action rules:
- Use measurable descriptions: "three steps," "two seconds," "turns 90 degrees"
- Match action duration to video duration
- Describe gesture through physical movement, not emotional labels
- Sequence multiple actions with explicit timing

### Part 4: Context

Establish environment with spatial relationships described relative to the
subject and camera.

Context rules:
- Specify spatial positions: "on the left," "behind," "eight feet away"
- Describe only what is visible from the camera position
- Include enough detail for visual coherence but not so much that the model
  generates competing focal points

### Part 5: Style and Ambiance

Specify lighting, color grading, mood, and any post-production aesthetic.

Style rules:
- Name the color palette: "warm amber and terracotta," "cool blue-grey"
- Specify lighting direction and quality (not just "cinematic")
- Reference the mood through observable qualities, not abstract emotions
- Include grain or texture preferences

---

## 3. VEO 3.1 Specifics

### Timestamp Prompting

VEO 3.1 supports timestamp-based prompts that assign specific actions to
exact temporal positions:

```
[00:00-00:03] Wide establishing shot, slow pan across the scene.
[00:03-00:07] Medium tracking shot following subject.
[00:07-00:12] Close-up of key action. Camera holds steady.
[00:12-00:15] Medium shot resolution. Subtle expression change.
```

### Reference Images

VEO 3.1 allows combining multiple reference images (character, setting,
style reference) with a text prompt. When using this feature:

- Let reference images handle visual appearance
- Focus text prompt on action, timing, camera movement, and mood
- Do not repeat visual details already present in reference images

### Duration Control

VEO 3.1 supports 4, 6, or 8 seconds per generation on Replicate.
For longer content, plan multi-shot sequences where each shot is generated separately.

Always state duration explicitly: "In an 8-second clip, the subject walks
for 3 seconds, pauses for 3 seconds, and turns for the final 2 seconds."

### Audio Generation

VEO 3.1 generates synchronized native audio automatically. Guide it by describing
desired sounds in your prompt: "with bird songs and wind rustling" or
"accompanied by upbeat music."

### Resolution and Aspect Ratio

- 720p or 1080p at 24 FPS
- Landscape (16:9) or portrait (9:16)
- Use 9:16 for TikTok, Reels, and Shorts
- Use 16:9 for YouTube, website, and ads

---

## 4. Camera Movement Vocabulary

### Dolly
Camera moves toward or away from the subject through physical space.
Use for: intimate reveals, building emotional connection.
"Slow dolly-in from medium shot to close-up over 8 seconds."

### Tracking
Camera follows a moving subject, maintaining constant framing.
Use for: following subjects through space, energy and motion.

### Crane
Camera moves vertically, often starting low and rising to reveal context.
Use for: revelation, establishing scope, dramatic openings.

### Orbit
Camera circles around a stationary subject while maintaining focus.
Use for: product showcase, establishing presence, dramatic emphasis.

### Pan
Camera rotates horizontally from a fixed position.
Use for: establishing shots, environmental reveal, transition.

### Static
Camera does not move. Subject action and internal composition carry the moment.
Use for: intimate moments, product close-ups, letting emotion breathe.

---

## 5. Temporal Control

### Beat Structures

```
Beat 1 (0-3s): Establishing. Slow. Wide. Let the viewer orient.
Beat 2 (3-7s): Development. Moderate pace. Subject engages with environment.
Beat 3 (7-11s): Climactic moment. Close-up. Emotional peak.
Beat 4 (11-15s): Resolution. Pull back or hold. Let the moment settle.
```

### Pacing as Emotional Tool

- Slow pacing (slow camera, held shots): calm, reverence, intimacy
- Moderate pacing (steady movement, deliberate action): confidence, purpose
- Fast pacing (quick cuts, dynamic movement): energy, excitement, urgency

{{BRAND_NAME}} defaults to {{DEFAULT_PACING}} pacing. Adjust per platform norms.

### Duration Specification

Always state explicitly how long each action takes. Without explicit timing,
the model distributes action unpredictably.

### Smooth Transitions

For loops: "The end frame should match the beginning frame in subject
position and camera angle, allowing seamless looping."

---

## 6. Subject Consistency

### Reference Images
- Use clear, well-lit frontal or three-quarter angle shots
- Simple, uncluttered backgrounds
- Consistent, even studio lighting
- Multiple angles of the same subject improve consistency

### Wardrobe Anchoring
Restate key wardrobe details in every prompt for multi-shot sequences.

### Multi-Shot Sequences
- Maintain consistent lighting language across all shots
- Use the same style/ambiance section for all shots in a sequence
- Explicitly reference previous shots

---

## 7. Short-Form Social Video

### TikTok and Instagram Reels (9:16, 15-60 seconds)

- 3-second hook imperative: the first action must visually arrest the viewer
- Vertical composition: keep subjects centered in the frame
- Fast initial reveal, then slow for emotional landing
- On-screen text space: leave room in upper and lower thirds for captions

Hook strategies for {{BRAND_NAME}}:
{{VIDEO_HOOK_STRATEGIES}}

> Example hook strategies:
> - Transformation reveal: subject holds wrong item, then switches to right item
> - Identity disruption visual: subject surrounded by wrong choices, then stepping into aligned choices
> - Product reveal: close-up of result, then slow pull back to show full context

### YouTube Shorts (9:16 or 1:1, up to 3 minutes)

- More narrative development allowed than TikTok
- Structure: problem establishment (15s), insight/demonstration (30s), result (15s)
- Can include founder voice-over with educational content

### Facebook Reels (9:16, 15-60 seconds)

- Retention-focused: maintain visual interest throughout
- Less hook-dependent than TikTok but still needs strong opening
- Pairs well with longer-form Facebook post for context

---

## 8. Example Prompts

### Example 1: Brand Reveal

```
Slow crane shot starting at ground level, ascending over 10 seconds.

The {{BRAND_NAME}} {{BRAND_VISUAL_ELEMENT}} sits at center frame. As the
camera rises, {{BRAND_SIGNATURE_MOTION}} begins.

Background is {{VIDEO_BACKGROUND}}. Lighting is {{VIDEO_LIGHTING}}.

{{BRAND_REVEAL_ACTION}}

The mood is confident, beautiful, and inevitable. The viewer should feel
that something meaningful is arriving.

Style: editorial quality, {{BRAND_COLOR_GRADE}}, subtle film grain.
Duration: 10 seconds.
```

### Example 2: Product Feature Demonstration

```
[00:00-00:03] Static close-up of {{PRODUCT_CLOSE_UP}}.
Warm studio lighting, shallow depth of field.

[00:03-00:07] Slow pull back to medium shot revealing the subject.
{{PRODUCT_DEMO_SUBJECT}}

[00:07-00:11] {{PRODUCT_DEMO_ACTION}}

[00:11-00:15] Subject looks at camera with a subtle, knowing expression.
Hold on this frame. The moment should feel like quiet confidence.

Style: clean, editorial, {{BRAND_COLOR_GRADE}}, film grain. Duration: 15 seconds.
```

### Example 3: Social Short-Form Hook

```
Fast opening: static close-up for 1 second.

{{SHORT_FORM_HOOK_VISUAL}}

Quick cut at 1 second to same subject, same framing.

{{SHORT_FORM_REVEAL_VISUAL}}

Hold on this comparison for 3 seconds. Camera remains static.

Then slow dolly-out to medium shot over 3 seconds revealing
{{PRODUCT_REVEAL_ELEMENT}}.

Background: clean white studio. Lighting: bright, even studio.
Style: crisp, high-contrast, immediate. Duration: 7 seconds.
Aspect ratio: 9:16 (vertical for TikTok/Reels).
```
