# AI Coding Logs — Bridge of Time

This folder documents the key AI prompts used during development of the Bridge of Time prototype, as required by the CPT208 AI usage policy.

**Tool**: Claude (Anthropic), claude-opus model  
**Period**: March 2026 – May 2026  
**Usage**: Vibe coding (AI-assisted development)

---

## Core Component Generation

### 1. Screen Scaffolding (All 7 Screens)

**Prompt pattern:**
> "Create a React component for [ScreenName] with the following requirements: [design spec from Figma]. It should accept an `onBack` callback and a `largeFont` boolean prop. Use inline styles for conditional sizing. The visual style should match: warm colours (#e67e22 orange, #2c3e50 dark navy, #27ae60 green), rounded cards, Noto Serif SC for headings."

**Applied to:** SplashScreen, RoleSelectScreen, HomeScreen, StoryScreen, CookScreen, QuizScreen, AlbumScreen

**Validation:** Each component was tested manually in the browser at 375px width to match our mobile-first design requirement. Layout, typography, and interaction states were verified against Figma wireframes.

---

### 2. Accessibility — Large Font Mode (FontContext)

**Prompt:**
> "Create a React Context that provides `largeFont` (boolean) and `setLargeFont` to all screen components. Move the toggle from outside the app frame into the RoleSelectScreen, specifically on the Grandparent card's top-right corner as a gear icon. When toggled, all font sizes should increase by 30-50% and touch targets should enlarge to 52px+."

**Validation:** Tested with 3 peer reviewers acting as grandparent users. Verified that all text and buttons scale correctly, that no content overflows, and that the toggle is discoverable.

---

### 3. Quiz Celebration Animation

**Prompt:**
> "Add a confetti celebration animation when the user completes all quiz questions. Use CSS keyframes (no external libraries). Show colourful dots/particles falling, an animated score counter, and encouraging text. The animation should feel joyful and reinforce positive feedback."

**Validation:** Animation runs smoothly on mobile devices (tested on iPhone 12 and Pixel 6 emulators). No performance issues detected. Peer feedback confirmed it "makes you want to play again."

---

### 4. Navigation System

**Prompt:**
> "Implement a history-based navigation in App.tsx. Use a stack of screen IDs. `navigate(screen)` pushes to stack, `goBack()` pops. Also add a `jumpTo(screen)` for the prototype demo that sets a meaningful history so back buttons always work correctly."

**Validation:** Tested all navigation paths: forward, back, and jump. No dead-ends or broken back buttons found.

---

### 5. Deployment Configuration

**Prompt:**
> "Configure Vite to build for GitHub Pages deployment at the path /prototype/. Set the base path and ensure asset paths resolve correctly."

**Validation:** Built and deployed successfully. All assets load from the correct paths on cpt208-b4-3.github.io/prototype/.

---

## Ethical Verification Checklist

| Concern | How we verified |
|---------|----------------|
| Accessibility | All components tested at large font mode; touch targets measured ≥52px |
| Cultural bias | Reviewed quiz questions and story content for stereotyping |
| Elder dignity | Ensured grandparent role is positioned as "expert", not "learner" |
| Data privacy | Prototype stores zero user data (fully stateless) |
| Code correctness | Manual testing of all user flows; `npm run build` with zero errors |

---

## Summary

AI was used as a **productivity tool** to accelerate implementation of our team's original design decisions. All design rationale, user research, requirements, and evaluation methodology are original team work. The AI did not make design decisions — it translated our specifications into code.
