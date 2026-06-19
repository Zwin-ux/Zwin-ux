# Work-Ready UI And Agent Workflow Brain

This is the operating standard for public-facing project cleanup and new product UI work.

It exists to prevent the recurring failures that make software feel unfinished: generic SaaS layouts, decorative motion, cluttered cards, weak mobile states, vague copy, and agent sessions that burn context reading the wrong things.

## Source References

- Animate UI: https://animate-ui.com
- Animate UI accessibility guidance: https://animate-ui.com/docs/accessibility
- Animate UI MCP/shadcn guidance: https://animate-ui.com/docs/mcp
- Token Savior: https://github.com/Mibayy/token-savior

These are references, not claims about this account's benchmarks or implementation.

## UI Rules

1. Start with the actual product screen. Do not default to a landing page.
2. One visual identity per product. Do not mix arcade, glass, enterprise, and neon styles on the same screen.
3. Motion must explain state, focus attention, or make a control feel responsive. No motion as decoration.
4. If Animate UI or Motion is used, add reduced-motion support at the app root:

```tsx
import { MotionConfig } from "motion/react";

export function AppShell({ children }: { children: React.ReactNode }) {
  return <MotionConfig reducedMotion="user">{children}</MotionConfig>;
}
```

5. Use Animate UI selectively: buttons, tabs, dialogs, sheets, tooltips, menus, previews, and small state transitions. Do not rebuild the whole app around animation.
6. Avoid looping backgrounds, parallax, large transform movement, and auto-playing effects unless the product itself needs them.
7. Every screen needs a mobile layout before it is called done.
8. Cards are for repeated items, modals, and framed tools. Do not build card-inside-card page sections.
9. Copy should name what the product actually does. Remove vague phrases, badges, and inflated claims.
10. A public demo link must load before it goes into a repo homepage or profile README.

## Common UI Issues To Replace

| Weak pattern | Replace with |
| --- | --- |
| Hero, subcopy, dual CTA, floating mockup | The working product surface as the first screen |
| Feature-card grid | A short proof section tied to real workflows |
| Glowing gradient panels | Clear layout, typography, and restrained color |
| Too many badges | One status line or none |
| Decorative animation | Stateful motion with reduced-motion support |
| Desktop-only polish | Mobile-first constraints and overflow checks |
| "AI-powered" filler | The exact model, mode, artifact, or limitation |

## Agent Workflow Rules

Token Savior is useful as a reference because it pushes three habits that matter here:

1. Navigate structurally before reading full files.
2. Compact command output so the next decision is not buried in noise.
3. Preserve durable project memory instead of rediscovering the same constraints.

For this workspace:

- Search with `rg` before opening files.
- Prefer targeted reads over full-file dumps.
- Use porcelain, JSON, quiet, or no-pretty flags when a command supports them.
- Save triage outputs when they become decision records.
- Keep public copy tied to repo evidence, live URLs, and test results.
- If a deployed site is broken, remove the public homepage link or fix the deployment before calling it portfolio-ready.

## Acceptance Criteria

A repo or site is employer-ready only when:

- The README says what it is, what is real, how to run it, and what is still prototype.
- The GitHub description is specific and not inflated.
- The homepage link returns a real page.
- The first viewport is the product, not generic marketing filler.
- Mobile does not overflow or hide the main action.
- Motion respects reduced-motion preferences.
- The strongest projects are pinned first.
