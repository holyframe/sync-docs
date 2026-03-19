# Meeting Script: Sharing Our Current Design System with the Hogan Team

## Topic 2: Shared Design System

### Intro

> **Say:** "The second thing I want to cover today is how we can share the design structure we already have with the Hogan team. The goal here is to show the design system we have in place today, how it’s structured, and how it could serve as a shared foundation for both HoganX and CoreIgnite."

---

## 1. Shared Design Foundation

> **Say:** “Let me start with the foundation of the design system.”

**Show:** `packages/ui/src/styles/globals.css`

> **Say:** “In this file, we define our core design tokens using CSS custom properties. These tokens cover colors, spacing, border radius, typography, and other base styling values. So instead of each team making styling decisions separately, we can all work from the same shared visual system.”

→ **Point:** CSS custom property definitions in `globals.css`

→ **Point:** `--surface-primary` for background surfaces

→ **Point:** `--content-primary` for primary text color

→ **Point:** `--accent` for primary actions and emphasis

> **Say:** “These tokens give us a single source of truth for the visual language of the product. At a high level, this is what helps us stay consistent across screens, components, and teams.”

---

## 2. Tailwind Integration

> **Say:** “On top of that, we also map those shared tokens into Tailwind so they’re easy to use in development.”

**Show:** `tailwind.config.ts`

> **Say:** “In the Tailwind config, especially in the colors section, we map the CSS variables into utility classes.”

→ **Point:** `colors` section in `tailwind.config.ts`

> **Say:** “That means developers don’t need to hardcode hex values directly in the UI. Instead, we can use shared utility classes that already reflect the design system.”

→ **Point:** `bg-surface-primary`

→ **Point:** `text-content-primary`

→ **Point:** `bg-accent`

> **Say:** “That keeps the code cleaner, and it also makes the design system a lot easier to scale.So from both a design and engineering perspective, this gives us consistency without adding extra complexity.”

---

## 3. Shared Components

> **Say:** “Then on top of the tokens, we have shared components.”

**Show:** `packages/ui/src/components/`

> **Say:** “This is where we define reusable UI components built on top of the same shared foundation.The benefit here is that the components already inherit the same tokens, the same styling rules, and the same visual language. For example, let’s look at the Button component.”

**Show:** `packages/ui/src/components/Button.tsx`

> **Say:** “This is a good example of how the shared design system becomes something practical and reusable.”

→ **Point:** `variants` definition in `Button.tsx`

> **Say:** “Here you can see how the button variants map back to the design system.”

→ **Point:** `primary` uses the accent style for primary actions

→ **Point:** `secondary` uses border and content styling for secondary actions

→ **Point:** `danger` uses destructive styling for warning or critical actions

> **Say:** “So this is really the key point: the tokens are not just abstract values in a file. They’re actually being applied through shared components that teams can reuse directly.”

---

## Closing Summary

> **Say:** “So overall, this is the design system architecture we have today. At the foundation, we have shared tokens. On top of that, we have Tailwind mappings and shared components. And then for product-specific needs, we can handle those through brand configuration. My proposal is to use this shared design system so HoganX and CoreIgnite can stay visually consistent, easier to scale, and easier to maintain over time. By aligning on shared tokens, shared components, and shared brand configuration, we can create a much more consistent experience across both products. So yeah, that’s the design system architecture I wanted to walk through today, and how I think it can support better consistency with Hogan.”

---

