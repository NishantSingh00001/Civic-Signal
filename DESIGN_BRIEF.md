# Visual quality brief

This project must not use generic dashboard composition, default component-library styling, or decorative animation without a job to do.

## Preferred visual stack

- **GSAP** for deliberate page entrances, scroll sequences, text reveals, and timeline orchestration.
- **Lenis** when a scroll-led page needs smoother physical scrolling.
- **Three.js** when a standalone interactive 3D object adds real value.
- **Framer Motion** for React or Next.js views that need layout transitions and interaction physics.
- **Tailwind** and bespoke primitives for an implementation that moves to React or Next.js.

## Quality rules

1. Start each project with a unique visual thesis and composition.
2. Make the main content object, scene, map, model, or product the dominant visual element.
3. Tie motion to a user action, a data state, or the story being told.
4. Use generous, readable type and intentional hierarchy.
5. Build desktop and mobile as distinct compositions, then test both.
6. Verify that maps, 3D scenes, controls, and page navigation actually load before presenting a preview.
7. Avoid unsupported live metrics. Clearly label samples, demos, and planned integrations.
