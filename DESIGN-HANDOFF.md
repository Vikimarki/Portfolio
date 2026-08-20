# f9cd5cd9-2951-48cc-9ca4-a52167440f97 implementation handoff

This archive is the source of truth for turning the design into production code. Start from `assets.html`, then preserve the visual system, responsive behavior, and interactions found in the exported files.

## Implementation target
- Build production UI from the exported design, not a loose reinterpretation.
- Preserve typography scale, spacing rhythm, color tokens, border radii, shadows, motion timing, and component states.
- Replace static placeholders only when the target app has real data or functional equivalents.
- Keep generated product UI free of Open Design chrome, preview labels, or design-process annotations.
- Treat this handoff as a visual contract: if implementation choices conflict, match the exported pixels and behavior first, then refactor internals.

## Source map
- Primary entry: `assets.html`
- HTML screens detected: 13
- Stylesheets detected: 0
- Script/component files detected: 0
- Supporting assets detected: 200

## Responsive contract
Validate the implementation across this 2025–2026 viewport matrix:
- Mobile compact: 360×800
- Mobile standard: 390×844
- Mobile large: 430×932
- Foldable / small tablet: 600×960
- Tablet portrait: 820×1180
- Tablet landscape: 1024×768
- Laptop: 1366×768
- Desktop: 1440×900
- Wide desktop: 1920×1080

For responsive web exports, treat these as a modern breakpoint system for one adaptive web experience, not three fixed screenshots. Do not split responsive web into unrelated native app screens unless the project explicitly includes native targets. Use semantic layout thresholds, fluid `clamp()` type/spacing, and container queries where component width matters more than viewport width. Preserve any CSS media queries, container queries, fluid `clamp()` scales, and layout changes already present in the exported files.

## Design fidelity contract
- Extract reusable tokens before writing components: background, surface, foreground, muted text, border, accent, radius, shadow, spacing, type scale, and motion duration/easing.
- Map product screens, in-app modules/components, optional landing page, and optional OS widget surfaces before coding. Keep these surfaces separate in the target architecture.
- Match layout geometry: max-widths, gutters, grid columns, card proportions, sticky/fixed elements, and viewport-specific navigation.
- Preserve real copy, labels, and data shown in the export. Do not replace specific text with generic marketing filler.
- Preserve interactive affordances: hover, focus, pressed, disabled, loading, validation, copy/share, tab/accordion, modal/sheet, and keyboard states where present.
- Preserve accessibility semantics when converting: headings stay hierarchical, controls remain buttons/links/inputs, focus states stay visible.
- Do not keep prototype-only annotations, frame labels, or Open Design chrome in the production UI.

## CJX-ready UX contract
- Use `DESIGN-MANIFEST.json` as the machine-readable map for screens, app modules, OS widgets, landing pages, tokens, interactions, and viewport checks.
- Screen-file-first: when multiple user-facing surfaces exist, implement each HTML screen as its own route/file. Treat `index.html` as a launcher/overview when the manifest marks it that way, not as a combined final UI.
- If `landing.html`, app screens, platform screens, or OS widget files exist, preserve those boundaries in the target app instead of merging them into one page.
- A single self-contained `assets.html` is acceptable only when the export truly contains one user-facing screen and its CSS/JS are structured enough to extract tokens, components, states, and behavior.
- If separate `css/` or `js/` files exist, treat them as source of truth for token/component/interactions before porting to React, Vue, SwiftUI, Compose, or another target stack.
- In-app modules/components are product UI blocks inside the app. OS widgets are home-screen/lock-screen/quick-access surfaces outside the app. Do not merge those concepts.

## Color and brand contract
- Use the exported design tokens and product/domain context as the color source of truth.
- Do not introduce warm beige / cream / peach / pink / orange-brown background washes unless they are already explicit brand/reference colors in the export.
- No obvious token stylesheet was detected; sample colors from the entry file and convert them into named tokens before coding.

## Implementation sequence for AI coding tools
1. Open `assets.html` and `DESIGN-MANIFEST.json`; identify every screen file, launcher/overview file, app module, and interaction before coding.
2. If multiple HTML screens exist, map them to separate routes/surfaces first; do not merge `landing.html`, product app screens, platform screens, or OS widgets into one route.
3. Extract a token table from CSS/root styles and inline styles before building framework components.
4. Build product screens and domain-specific in-app modules from largest layout regions down to controls; avoid starting with isolated atoms that lose spatial intent.
5. Port responsive behavior across the modern viewport matrix and test each semantic breakpoint before cleanup.
6. Port interactions and states, then replace static placeholders only with real app data or functional equivalents.
7. Keep optional landing page and OS widget surfaces as separate surfaces if present.
8. Compare final screenshots against the export at 360×800, 390×844, 430×932, 820×1180, 1024×768, 1366×768, 1440×900, and 1920×1080 before declaring done.

## Entry points
- `assets.html`
- `cars.html`
- `cities.html`
- `contact.html`
- `hk-aerial.html`
- `index.html`
- `robots.html`
- `rune-sword.html`
- `sci-fi-weapon.html`
- `stone-sword-v2.html`
- `stone-sword.html`
- `work-v2.html`
- `work.html`

## Styles
- None detected

## Scripts/components
- None detected

## Assets and supporting files
- `0524.png`
- `1-1.png`
- `1-2.png`
- `1-3.png`
- `1-4.png`
- `1-5.png`
- `1.png`
- `1.png0150.png`
- `2-1.png`
- `2-2.png`
- `2-3.png`
- `2-4.png`
- `2-5.png`
- `2-6.png`
- `2-7.png`
- `2.png`
- `2ntitled-1.png`
- `2ntitled.png`
- `3-1.png`
- `3-2.png`
- `3-3.png`
- `3.png`
- `4-1.png`
- `4.png`
- `5.png`
- `assets-preview.png`
- `assets.jpeg`
- `assets/assets/overview.jpg`
- `assets/cars/nightshade-solid.jpg`
- `assets/cars/nightshade-textured.jpg`
- `assets/cars/nocturne-solid.jpg`
- `assets/cars/nocturne-textured.jpg`
- `assets/cities/environment-01.jpg`
- `assets/cities/environment-02.jpg`
- `assets/cities/environment-03.jpg`
- `assets/cities/trailer-poster.jpg`
- `assets/hk-aerial/clay-01.jpg`
- `assets/hk-aerial/clay-02.jpg`
- `assets/hk-aerial/clay-03.jpg`
- `assets/hk-aerial/clay-04.jpg`
- `assets/hk-aerial/textured-01.jpg`
- `assets/hk-aerial/textured-02.jpg`
- `assets/hk-aerial/textured-03.jpg`
- `assets/hk-aerial/textured-04.jpg`
- `assets/hk-aerial/wireframe-01.jpg`
- `assets/hk-aerial/wireframe-02.jpg`
- `assets/hk-aerial/wireframe-03.jpg`
- `assets/hk-aerial/wireframe-04.jpg`
- `assets/portrait.jpg`
- `assets/portrait.png`
- `assets/robots/clay-01.jpg`
- `assets/robots/textured-01.jpg`
- `assets/robots/textured-02.jpg`
- `assets/robots/textured-03.jpg`
- `assets/robots/wireframe-01.jpg`
- `assets/rune-sword/rune-sword-01.jpg`
- `assets/rune-sword/rune-sword-02.jpg`
- `assets/rune-sword/rune-sword-03.jpg`
- `assets/rune-sword/rune-sword-04.jpg`
- `assets/rune-sword/rune-sword-05.jpg`
- `assets/scene.jpg`
- `assets/sci-fi-weapon/assault-rifle-01.jpg`
- `assets/sci-fi-weapon/assault-rifle-02.jpg`
- `assets/sci-fi-weapon/guard-weapon-01.jpg`
- `assets/sci-fi-weapon/guard-weapon-02.jpg`
- `assets/sci-fi-weapon/lmg-01.jpg`
- `assets/sci-fi-weapon/lmg-02.jpg`
- `assets/sci-fi-weapon/sniper-01.jpg`
- `assets/sci-fi-weapon/sniper-02.jpg`
- `assets/stone-sword/clay-01.jpg`
- `assets/stone-sword/clay-02.jpg`
- `assets/stone-sword/clay-03.jpg`
- `assets/stone-sword/clay-04.jpg`
- `assets/stone-sword/clay-05.jpg`
- `assets/stone-sword/clay-06.jpg`
- `assets/stone-sword/clay-07.jpg`
- `assets/stone-sword/clay-08.jpg`
- `assets/stone-sword/clay-09.jpg`
- `assets/stone-sword/clay-10.jpg`
- `assets/stone-sword/mat-ao.jpg`
- `assets/stone-sword/mat-base-color.jpg`
- `assets/stone-sword/mat-height.jpg`
- `assets/stone-sword/mat-metalness.jpg`
- `assets/stone-sword/mat-normal-opengl.jpg`
- `assets/stone-sword/mat-normal.jpg`
- `assets/stone-sword/mat-roughness.jpg`
- `assets/stone-sword/stone-sword-01.jpg`
- `assets/stone-sword/stone-sword-02.jpg`
- `assets/stone-sword/stone-sword-03.jpg`
- `assets/stone-sword/stone-sword-04.jpg`
- `assets/stone-sword/stone-sword-05.jpg`
- `assets/stone-sword/stone-sword-06.jpg`
- `assets/stone-sword/wire-01.jpg`
- `assets/stone-sword/wire-02.jpg`
- `assets/stone-sword/wire-03.jpg`
- `assets/stone-sword/wire-04.jpg`
- `assets/stone-sword/wire-05.jpg`
- `assets/work/cars-cover.jpg`
- `assets/work/environment-01.jpg`
- `assets/work/environment-02.jpg`
- `assets/work/hk-aerial-cover.jpg`
- `assets/work/sword-01.jpg`
- `assets/work/sword-02.jpg`
- `assets/work/sword-03.jpg`
- `assets/work/sword-render-03.jpg`
- `assets/work/sword-render-04.jpg`
- `b_door_DefaultMaterial_BaseColor.1001.png`
- `b_door_DefaultMaterial_Normal.1001.png`
- `b_door_DefaultMaterial_OcclusionRoughnessMetallic.1001.png`
- `b_top_DefaultMaterial_BaseColor.1001.png`
- `b_top_DefaultMaterial_Normal.1001.png`
- `b_top_DefaultMaterial_OcclusionRoughnessMetallic.1001.png`
- `brand-spec.md`
- `car_camera.mp4`
- `cars_in_city_1.mp4`
- `cars_in_city_2.mp4`
- `cars-preview.png`
- `cities-preview.png`
- `contact-preview.png`
- `ez.mp4`
- `final_render_sword_3-1.png`
- `final_render_sword_3.png`
- `final_render_sword_4-1.png`
- `final_render_sword_4.png`
- `HK_Body_low_defaultMat_BaseColor.1001.png`
- `HK_Body_low_defaultMat_Normal.1001.png`
- `HK_Body_low_defaultMat_OcclusionRoughnessMetallic.1001.png`
- `hk_cam_low_defaultMat_BaseColor.1001.png`
- `hk_cam_low_defaultMat_Normal.1001.png`
- `hk_cam_low_defaultMat_OcclusionRoughnessMetallic.1001.png`
- `HK_front_small_wing_left_low_defaultMat_BaseColor.1001.png`
- `HK_front_small_wing_left_low_defaultMat_Normal.1001.png`
- `HK_front_small_wing_left_low_defaultMat_OcclusionRoughnessMetallic.1001.png`
- `HK_front_small_wing_low_defaultMat_BaseColor.1001.png`
- `HK_front_small_wing_low_defaultMat_Normal.1001.png`
- `HK_front_small_wing_low_defaultMat_OcclusionRoughnessMetallic.1001.png`
- `HK_Main_big_armor_low_defaultMat_BaseColor.1001.png`
- `HK_Main_big_armor_low_defaultMat_Normal.1001.png`
- `HK_Main_big_armor_low_defaultMat_OcclusionRoughnessMetallic.1001.png`
- `hk-aerial-preview.png`
- `low_blade_1.png`
- `low_blade_2.png`
- `low_blade.png`
- `low_blade2.png`
- `low_guard-1.png`
- `low_guard.png`
- `low_handle-1.png`
- `low_handle.png`
- `low_ring-1.png`
- `low_ring.png`
- `mark_yes-1.png`
- `mark_yes.png`
- `preview.png`
- `robots-preview.png`
- `sci-fi-weapon-preview.png`
- `Screenshot-2026-08-19-203754.png`
- `stone-sword-preview.png`
- `sword_1-1.png`
- `sword_1.png`
- `sword_2-1.png`
- `sword_2.png`
- `sword_3-1.png`
- `sword_3.png`
- `Sword_Mat_Base_color_1001.png`
- `Sword_Mat_Base_metalness_1001.png`
- `Sword_Mat_Height_1001.png`
- `Sword_Mat_Mixed_AO_1001.png`
- `Sword_Mat_Normal_1001.png`
- `Sword_Mat_Normal_OpenGL_1001.png`
- `Sword_Mat_Specular_roughness_1001.png`
- `Terminator_scene.mp4`
- `test_ofy2_DefaultMaterial_BaseColor.1001-1.png`
- `test_ofy2_DefaultMaterial_BaseColor.1001.png`
- `test_ofy2_DefaultMaterial_Normal.1001-1.png`
- `test_ofy2_DefaultMaterial_Normal.1001.png`
- `test_ofy2_DefaultMaterial_OcclusionRoughnessMetallic.1001-1.png`
- `test_ofy2_DefaultMaterial_OcclusionRoughnessMetallic.1001.png`
- `texture_1.png`
- `texture_2.jpeg`
- `texture_3.jpeg`
- `texture_4.jpeg`
- `Untitled-1.png`
- `Untitled-2.png`
- `Untitled-3.png`
- `Untitled-4.png`
- `Untitled-5.png`
- `Untitled.png`
- `varos.png`
- `varos2.png`
- `w_1.png`
- `w_2.png`
- `w_3.png`
- `w_4.png`
- `w_light.png`
- `wire_2.png`
- `wire_3.png`
- `wire_4.png`
- `wire_5.png`
- `wire.png`
- `work-preview.png`

## Coding checklist for AI tools
1. Inspect `assets.html` and `DESIGN-MANIFEST.json` first and identify reusable components before coding.
2. Implement each user-facing screen file as its own route/surface; keep launcher, landing, app, platform, and OS widget files separate.
3. Extract design tokens into the target stack: colors, type scale, spacing, radius, shadows, and motion.
4. Implement layout with real 2025–2026 responsive breakpoints, fluid type/spacing, and container-query-aware component behavior; test with no horizontal overflow.
5. Preserve interactive controls, hover/focus/pressed states, form behavior, validation, and copy actions where present.
6. Implement domain-specific in-app modules with real states; do not flatten them into generic cards.
7. Keep landing page, product screens, and OS widget/quick-access surfaces separate when present.
8. Confirm the production result visually matches the exported design before refactoring internals.
9. Reject implementation shortcuts that flatten the design into generic cards, generic gradients, placeholder stats, or framework-default typography.
10. If a detail is ambiguous, keep the exported HTML/CSS/JS behavior rather than inventing a new pattern.
