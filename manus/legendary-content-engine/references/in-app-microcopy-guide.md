# In-App Microcopy Guide

UI copy for buttons, errors, onboarding, tooltips, empty states, loading states,
and all in-product text. Every word inside the product carries the brand voice.

## Table of Contents

1. [Microcopy Principles](#1-microcopy-principles)
2. [Buttons and CTAs](#2-buttons-and-ctas)
3. [Onboarding Flow](#3-onboarding-flow)
4. [Error States](#4-error-states)
5. [Loading and Progress States](#5-loading-and-progress-states)
6. [Empty States](#6-empty-states)
7. [Tooltips and Help Text](#7-tooltips-and-help-text)
8. [Notifications and Alerts](#8-notifications-and-alerts)

---

## 1. Microcopy Principles

### Voice in Product

The brand voice inside the product is the same voice as marketing, but at
lower intensity. Think of it as the brand speaking quietly in a focused room
rather than across a crowded space.

### Rules
- Clarity over cleverness (always)
- Outcome-based language over mechanic-based language
- Respect the user's time and intelligence
- Never condescend, never over-explain
- {{MICROCOPY_RULE_1}}
- {{MICROCOPY_RULE_2}}

---

## 2. Buttons and CTAs

### Primary Actions

| Action | Wrong | Right |
|--------|-------|-------|
| Start the process | "Submit" | "{{CTA_START}}" |
| View results | "View Results" | "{{CTA_VIEW_RESULTS}}" |
| Upgrade | "Upgrade Now" | "{{CTA_UPGRADE}}" |
| Share | "Share" | "{{CTA_SHARE}}" |
| Save | "Save" | "{{CTA_SAVE}}" |

> Examples:
> - Start: "See my colors" instead of "Submit"
> - View: "See what your colors mean" instead of "View Results"
> - Upgrade: "See everything" instead of "Upgrade Now"

### Button Copy Rules
- Use first person ("my" not "your") for primary actions
- Describe the outcome, not the mechanic
- 2-4 words maximum
- No exclamation marks

---

## 3. Onboarding Flow

### Welcome Screen

```
Headline: "{{ONBOARDING_HEADLINE}}"
Subhead: "{{ONBOARDING_SUBHEAD}}"
CTA: "{{ONBOARDING_CTA}}"
```

> Example:
> Headline: "Let us find your colors."
> Subhead: "It takes about two minutes. You will need a photo in natural light."
> CTA: "Get started"

### Step Indicators

Use progress language that builds anticipation:

```
Step 1: "{{STEP_1_LABEL}}"
Step 2: "{{STEP_2_LABEL}}"
Step 3: "{{STEP_3_LABEL}}"
```

> Example:
> Step 1: "Your photo"
> Step 2: "Your analysis"
> Step 3: "Your colors"

### Photo Upload Screen

```
Headline: "{{UPLOAD_HEADLINE}}"
Instructions: "{{UPLOAD_INSTRUCTIONS}}"
```

> Example:
> Headline: "Show us you."
> Instructions: "Natural light. No filters. Face the camera directly."

---

## 4. Error States

### Principles
- Name what happened without blame
- Tell them what to do next
- Keep the brand voice even in errors

### Error Messages

| Error Type | Wrong | Right |
|-----------|-------|-------|
| Upload failed | "Error: Upload failed" | "{{ERROR_UPLOAD}}" |
| Bad photo quality | "Invalid image" | "{{ERROR_PHOTO_QUALITY}}" |
| Network error | "Network error" | "{{ERROR_NETWORK}}" |
| Payment failed | "Payment declined" | "{{ERROR_PAYMENT}}" |
| Generic error | "Something went wrong" | "{{ERROR_GENERIC}}" |

> Examples:
> - Upload: "That did not work. Try again with a different photo."
> - Photo quality: "We need a bit more light. Try a photo near a window."
> - Network: "Lost connection. We will try again in a moment."
> - Payment: "That did not go through. Check your card details and try again."

---

## 5. Loading and Progress States

### Analysis in Progress

```
State 1: "{{LOADING_STATE_1}}"
State 2: "{{LOADING_STATE_2}}"
State 3: "{{LOADING_STATE_3}}"
Complete: "{{LOADING_COMPLETE}}"
```

> Example:
> State 1: "Looking at your photo..."
> State 2: "Analyzing your coloring..."
> State 3: "Building your palette..."
> Complete: "Your colors are ready."

### Rules
- Never use generic spinners with no text
- Each state should feel like progress, not waiting
- The final state should feel like arrival

---

## 6. Empty States

### No Results Yet

```
Headline: "{{EMPTY_NO_RESULTS}}"
CTA: "{{EMPTY_CTA}}"
```

> Example:
> Headline: "Nothing here yet. Let us change that."
> CTA: "Get started"

### No Saved Items

```
Headline: "{{EMPTY_NO_SAVED}}"
```

> Example: "You have not saved anything yet. Your favorites will appear here."

---

## 7. Tooltips and Help Text

### Principles
- One sentence maximum
- Answer the question "What does this do?" or "Why is this here?"
- Use plain language, no jargon

### Examples

{{TOOLTIP_EXAMPLES}}

> Example tooltips:
> - "Your undertone is the base color beneath your skin. It determines which colors harmonize with you."
> - "Contrast measures the difference between your lightest and darkest features."
> - "These are the colors that will make you look most like yourself."

---

## 8. Notifications and Alerts

### Push Notification Templates

```
[RESULTS READY]
"{{NOTIFICATION_RESULTS}}"
> Example: "Your colors are ready. Take a look."

[NEW FEATURE]
"{{NOTIFICATION_FEATURE}}"
> Example: "Something new: see how your colors work in outfits."

[REMINDER]
"{{NOTIFICATION_REMINDER}}"
> Example: "Your palette is waiting. Pick up where you left off."
```

### Notification Rules
- Never use urgency language in notifications
- One notification per event, never batched
- Respect notification preferences absolutely
- {{NOTIFICATION_RULE}}
