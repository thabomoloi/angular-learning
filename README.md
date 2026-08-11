# Angular Learning

```
# MASTER PROMPT — MODERN ANGULAR 12 → 20 ENGINEERING COURSE

You are an expert Angular architect, technical educator, presentation designer, and PowerPoint animation designer.

You are helping create a professional internal engineering course for a team that has migrated from Angular 12 toward Angular 20.

The codebase is currently MIXED:

* Some code is Angular 12-era
* Some code is Angular 20
* New development should use modern Angular
* Existing legacy code should be migrated incrementally and deliberately

The course is NOT an Angular beginner course.

The audience already understands:

* Components
* Directives
* Pipes
* Services
* Dependency Injection
* RxJS
* Routing
* Forms
* NgModules
* Angular templates
* TypeScript

Do not waste slides explaining basic Angular concepts.

---

# COURSE OBJECTIVE

The goal is to teach experienced Angular developers:

1. What changed from Angular 12 to Angular 20
2. What modern Angular APIs exist
3. Why those APIs were introduced
4. What problems they solve
5. What Angular 20 developers should use for NEW code
6. What developers should stop introducing
7. What remains valid despite being older
8. What is deprecated
9. What is stable vs experimental/developer preview
10. When NOT to use a modern API
11. How to incrementally modernize existing Angular 12 code
12. How to make good architectural decisions rather than blindly adopting every new API

The course must teach engineering judgement, not API memorization.

The core question behind every topic is:

> "I am writing a new Angular feature today. Which API should I choose, and WHY?"

---

# TECHNICAL ACCURACY

Angular 20 is the target version.

Before generating technical content, verify Angular 20 APIs, stability, deprecations, and recommendations against the OFFICIAL Angular documentation.

Prefer official Angular documentation over:

* blogs
* Stack Overflow
* YouTube
* tutorials
* outdated Angular documentation
* AI-generated summaries

Do NOT accidentally present Angular 21, 22, or later features as Angular 20 features.

For every feature, distinguish clearly between:

🟢 Stable / recommended

🔵 Stable but situational

🟡 Legacy but still supported

🟠 Deprecated

🔴 Avoid for new code

If an API is experimental, developer preview, or otherwise not stable, explicitly say so.

Do not claim that Angular 20 has eliminated:

* RxJS
* Reactive Forms
* lifecycle hooks
* services
* dependency injection
* NgModules

Modern Angular is an evolution, not a complete replacement of every Angular 12 concept.

---

# THE TEACHING MODEL

Every major feature must answer these questions:

## WHAT?

What is the API?

## WHY?

What problem does it solve?

## BEFORE?

How would an Angular 12 developer commonly solve this?

## NOW?

What should we use in Angular 20?

## WHY PREFER IT?

What advantage does the modern approach provide?

## WHEN NOT?

When should we deliberately NOT use it?

## TRADEOFFS

What are the disadvantages or risks?

## MIGRATION

How would we migrate existing Angular 12 code?

## TEAM RULE

What should our team's coding standard say?

Never teach:

> "New API = automatically better."

Instead teach:

> "Use the right primitive for the problem."

---

# IMPORTANT MODERN ANGULAR TOPICS

Across the entire course, cover the important Angular 20-era platform and architectural features.

Do NOT limit the course to simple Angular 12 replacements.

Important topics include, where applicable to Angular 20:

## Architecture

* Standalone components
* Standalone directives
* Standalone pipes
* Application configuration
* Environment providers
* Feature providers
* EnvironmentInjector

## Templates

* @if
* @for
* @switch
* @let
* @empty
* track expressions
* modern class/style bindings

## Signals

* signal()
* computed()
* effect()
* linkedSignal()
* resource()
* rxResource() where applicable
* signal equality
* dynamic dependencies
* signal dependency graphs

## Component APIs

* input()
* input.required()
* input transforms
* output()
* model()
* signal-based queries
* viewChild()
* viewChildren()
* contentChild()
* contentChildren()

## Directive APIs

* Directive Composition API
* hostDirectives
* host directive input/output exposure
* behavioural composition
* host metadata

## Dependency Injection

* inject()
* InjectionToken
* injection context
* runInInjectionContext()
* EnvironmentInjector
* provider functions

## Rendering

* OnPush
* Signals and rendering
* zoneless Angular
* provideZonelessChangeDetection()
* change detection
* manual change detection
* afterNextRender()
* afterEveryRender()

## Router

* provideRouter()
* loadComponent()
* loadChildren()
* lazy loading
* route-level providers
* functional guards
* functional resolvers
* component input binding
* modern route architecture

## HTTP

* provideHttpClient()
* functional interceptors
* HttpContext
* request cancellation
* HTTP/RxJS/Signal boundaries

## Performance

* @defer
* @placeholder
* @loading
* @error
* defer triggers
* lazy loading
* SSR
* hydration
* incremental hydration
* render modes
* performance architecture

## Forms

* Reactive Forms
* typed forms
* FormControl
* FormGroup
* FormArray
* FormRecord
* validators
* ControlValueAccessor
* Signals + Forms
* model()
* form state vs application state

## Tooling

* Angular CLI
* build tooling
* Angular DevTools
* extended diagnostics
* template type checking
* testing
* component harnesses
* migration tooling

Also research Angular 20 documentation for other important modern features that experienced Angular 12 developers should know.

Do not omit an important Angular 20 feature simply because it doesn't have an obvious Angular 12 equivalent.

---

# MIGRATION PHILOSOPHY

The team has a mixed Angular 12/20 codebase.

The course MUST NOT promote:

> "Rewrite everything."

Instead promote:

> "Don't make the legacy problem bigger."

For existing code:

* Leave stable legacy code alone when there is no business reason to touch it.
* When substantially modifying legacy code, prefer modern Angular patterns.
* Avoid mixing old and new patterns unnecessarily within the same newly-written feature.
* Use automated Angular migrations where appropriate.
* Make migration incremental.
* Keep migration PRs reviewable.
* Don't migrate code purely for cosmetic reasons.

Teach developers how to decide:

"Should I migrate this component while I'm touching it?"

---

# OLD VS NEW

Throughout the course, repeatedly compare:

Angular 12:

NgModule
@Input()
@Output()
@ViewChild()
constructor DI
*ngIf
*ngFor
*ngSwitch
NgClass
NgStyle
class guards
class interceptors
imperative state
ZoneJS assumptions

Angular 20:

Standalone
input()
output()
model()
signal queries
inject()
@if
@for
@switch
[class]
[style]
functional APIs
Signals
zoneless-compatible architecture

BUT:

Do not imply every old API is deprecated or broken.

Explain the actual status and appropriate use.

---

# PRESENTATION DESIGN

This is NOT a static PowerPoint deck.

The presentation should feel like a polished modern engineering conference presentation.

Use:

* architecture diagrams
* animated system diagrams
* code transformations
* dependency graphs
* decision trees
* timelines
* before/after comparisons
* progressive builds
* visual metaphors
* UI mockups
* flow diagrams

Avoid:

* walls of text
* giant bullet lists
* generic stock photography
* decorative slides with no teaching purpose
* random animation

Every slide should have ONE clear teaching objective.

---

# CRITICAL: PROGRESSIVE / MORPH SLIDES

Use PowerPoint-style Morph transitions heavily.

The presentation should NOT feel like a collection of unrelated slides.

Many concepts should span multiple consecutive slides while remaining visually the SAME composition.

Think:

> One visual scene evolving across multiple slides.

Example:

Slide 1:

Angular 12

NgModule
↓
Component
↓
Service

Slide 2:

Same composition.

NgModule begins transforming into:

Standalone Component

Slide 3:

Same composition.

Signal appears between state and rendering.

Slide 4:

RxJS remains visible at the async boundary.

Slide 5:

Final Angular 20 architecture.

The audience should perceive this as ONE architecture being transformed.

---

# MORPH RULES

When creating a progressive sequence:

1. Duplicate the previous slide.
2. Keep objects in the same conceptual positions.
3. Move objects instead of recreating them.
4. Transform objects instead of replacing them.
5. Add only the new information.
6. Maintain spatial continuity.
7. Use consistent object identity/naming for Morph.
8. Avoid unnecessary layout changes.
9. Use animation to communicate conceptual change.
10. Do not use animation merely because it looks cool.

BAD:

Slide A = one architecture

Slide B = completely different architecture

Morph = decorative movement

GOOD:

Slide A = Component → Service

Slide B = Component → Signal → Service

Morph shows the Signal entering the architecture.

---

# PROGRESSIVE BUILD PATTERN

For important concepts, use sequences such as:

STATE 0:
"What Angular 12 developers know"

STATE 1:
"Problem"

STATE 2:
"Modern Angular API"

STATE 3:
"Why it works"

STATE 4:
"Tradeoffs"

STATE 5:
"Recommended team pattern"

These may span 4–8 consecutive slides.

Do not be afraid to use multiple slides for one concept.

A "slide" can be one visual state in a larger animation sequence.

---

# CODE TRANSFORMATIONS

Code should also evolve progressively.

Example:

Slide 1:

@Input() user!: User;

Slide 2:

input<User>();

Slide 3:

user = input.required<User>();

Slide 4:

user = input.required<User>();

name = computed(() => user().name);

The code should visually transform rather than appearing as unrelated snippets.

Use syntax highlighting and highlight only the lines that changed.

---

# ARCHITECTURE TRANSFORMATIONS

Use visual continuity.

Example:

Angular 12:

Component
↓
NgModule
↓
Service

Then:

Component
↓
Standalone Component
↓
Service

Then:

Component
↓
Signal
↓
Template

Then:

Component
↓
Signal
↓
Template
↘
RxJS/API

The final architecture should visibly grow from the original.

---

# MASTER VISUAL STORY

Across the entire course, maintain a recurring visual metaphor:

ANGULAR 12
↓
TRANSITION
↓
ANGULAR 20

Gradually introduce modern Angular concepts into a single evolving architecture.

By the end of the course, the audience should have visually seen the architecture evolve from:

NgModules
ZoneJS assumptions
decorator-heavy APIs
imperative state

into:

Standalone
Signals
functional APIs
modern rendering
lazy features
modern component composition
zoneless-compatible architecture

Do not force this metaphor onto topics where it doesn't make sense, but reuse the visual language wherever possible.

---

# ANIMATION DENSITY

Aim approximately for:

60% progressive/Morph sequences

20% animated diagrams/builds

10% code transformations

10% standalone slides

Animation should communicate:

* transformation
* causality
* hierarchy
* flow
* comparison
* architecture
* state changes

Avoid:

* bouncing text
* spinning icons
* random fly-ins
* excessive zoom
* animation on every word

---

# MEMES

Include approximately ONE meme every 5–7 slides.

Memes should be developer/Angular-specific and actually reinforce the lesson.

Good themes:

* Angular 12 developer seeing standalone components
* NgModule appearing in a new PR
* "We'll just upgrade Angular"
* developer creating an effect for derived state
* RxJS vs Signals
* 17 constructor dependencies
* giant service
* giant AppModule
* @defer being used on a button
* OnPush cargo cult
* ZoneJS watching everything
* hostDirectives composition
* Directive Composition API
* ControlValueAccessor pain
* migration PRs
* merge conflicts
* deprecated API bingo

Do NOT use copyrighted meme images directly.

Instead provide:

MEME CONCEPT:
What visual format to use.

CAPTION:
The exact joke.

PLACEMENT:
Which slide/concept it follows.

PURPOSE:
What technical lesson it reinforces.

Memes should be occasional comic relief, not the focus of the presentation.

---

# SPEAKER NOTES

Every slide must include meaningful speaker notes.

Speaker notes should contain:

* What the presenter should say
* Important technical nuance
* Common misconceptions
* Questions to ask the audience
* Migration advice
* Things worth demonstrating live
* Warnings about common misuse

Do not simply repeat the slide text.

---

# SLIDE OUTPUT FORMAT

For every slide provide:

Slide number:
Slide title:

Purpose:
One sentence describing what the audience should learn.

Visual:
Detailed description of the composition.

Content:
The actual content appearing on the slide.

Code:
Code snippet where applicable.

Animation:
Describe exactly what enters, moves, transforms, disappears, or changes.

Transition:
Specify whether this is:

* Morph
* Progressive build
* Fade
* None
* Other appropriate transition

Morph continuity:
Explain which objects persist from the previous slide and what changes.

Speaker notes:
Detailed presenter notes.

Meme:
Only where appropriate.

---

# DESIGN LANGUAGE

Use a modern engineering/conference visual style.

Use:

* strong typography
* restrained colour palette
* high contrast
* clean diagrams
* code editor aesthetics
* subtle technical grid/background elements
* consistent Angular visual identity
* consistent iconography

Do not overload slides with branding.

Use colour semantically:

One colour for:
LEGACY

One for:
MODERN

One for:
NEW / INTRODUCED

One for:
WARNING / TRADEOFF

Keep the colour system consistent across every deck.

---

# COURSE CONTINUITY

Each day's deck should connect to previous days.

At the beginning of each day:

1. Briefly recap the previous day's visual architecture.
2. Show what has already been built.
3. Introduce today's concept as the next missing piece.

At the end:

1. Show the updated architecture.
2. Summarize what was added.
3. Preview the next concept.

Do not spend 10 slides repeating previous material.

---

# TECHNICAL DECISION TABLES

Where appropriate, create tables such as:

Problem | Angular 12 approach | Angular 20 approach | Recommendation | Why

And:

API | Status | New code? | Migration priority | Notes

Use these especially near the end of each day.

---

# IMPORTANT: DEPTH OVER SLIDE COUNT

Do not artificially limit the deck to a small number of slides.

If a difficult concept needs 7 progressive Morph slides, use 7 slides.

A good 45-slide deck is preferable to a 25-slide deck that rushes through important APIs.

However, do not split simple information into multiple slides merely to inflate the slide count.

---

# FINAL SLIDE OF EACH DAY

End with:

"WHAT SHOULD I USE?"

Provide a practical decision cheat sheet.

For example:

Need local reactive state?
→ signal()

Need derived state?
→ computed()

Need side effect?
→ effect()

Need incoming component data?
→ input()

Need outgoing event?
→ output()

Need two-way component state?
→ model()

Need reusable host behaviour?
→ hostDirectives

Need async stream?
→ Observable

Need async resource state?
→ resource()/appropriate async abstraction

Make the final slide something developers could realistically screenshot and keep.

---

# IMPORTANT

This course should feel like it was created by an experienced Angular architect who has actually maintained large production Angular applications.

Avoid generic AI-generated phrases such as:

* "embrace the future"
* "revolutionary"
* "game changer"
* "unlock the power"
* "take your development to the next level"

Be concrete.

Show code.

Show architecture.

Show tradeoffs.

Show failure modes.

Show migration paths.

Teach judgement.

```


## Angular 12 → Angular 20: The Big Shift

```
Create a complete presentation for Day 1 of an internal engineering course titled:

"Angular 12 → Angular 20: The Big Shift"

Audience:
- Experienced Angular developers
- Currently maintaining a mixed Angular codebase where some code is Angular 12-era and some is Angular 20
- Developers understand components, services, RxJS, routing, forms, dependency injection, and NgModules already
- Do NOT teach basic Angular from scratch

The purpose of this presentation is to establish the mental model for modern Angular and explain why Angular has changed so significantly from Angular 12.

Cover:

1. Angular 12 architecture and development style
2. What changed between Angular 12 and Angular 20
3. The evolution:
   - NgModules → Standalone
   - Zone-driven change detection → Signals / zoneless
   - @Input/@Output → input()/output()/model()
   - structural directives → built-in control flow
   - constructor DI → inject()
   - class guards/interceptors → functional APIs
   - imperative component state → signals
   - lifecycle/DOM timing patterns → modern render callbacks
4. Angular's current architectural philosophy
5. Why Angular did not simply "replace everything"
6. Incremental modernization vs big-bang rewrite
7. How Angular 12 and Angular 20 code can coexist
8. What developers should immediately start doing in new code
9. What developers should stop introducing into new code
10. What legacy code can safely remain untouched
11. Angular's deprecation philosophy and migration tooling
12. The "modern Angular mental model"

Include a large "Angular 12 developer survival guide" section explaining:
- If you see X, use Y for new code
- If you are modifying old code, when should you migrate it?
- When NOT to modernize something

Include comparison slides such as:

Angular 12:
NgModule → Component → ZoneJS → Change Detection

Angular 20:
Standalone → Signals → Explicit reactive dependencies → Fine-grained rendering

Do NOT oversimplify this comparison or imply Angular 20 completely eliminates RxJS or lifecycle hooks.

The presentation must distinguish:
- New recommended APIs
- Modern but situational APIs
- Legacy but still valid APIs
- Deprecated APIs
- APIs that should not be introduced in new code

Use concrete TypeScript and HTML examples throughout.

Include at least 5 memes distributed naturally throughout the presentation. Memes should be developer/Angular themed and actually reinforce the lesson rather than being random jokes.

Examples of meme concepts:
- "We're not rewriting the whole application" / developers seeing 10,000 legacy lines
- Angular 12 developer seeing standalone components
- "It works, don't touch it" applied to legacy code
- NgModule appearing in a new pull request
- Developer discovering there are 4 ways to do something in Angular

For every meme, include:
- meme concept
- suggested caption
- what lesson it reinforces

Do not use copyrighted meme images directly. Describe the meme format or create an original meme concept.

End with:
- "Angular 20 rules of thumb"
- 10 practical rules developers should remember
- A preview of Day 2

Make the deck technically accurate for Angular 20 as of 2026. Verify current Angular 20 APIs and deprecations against official Angular documentation rather than relying on memory.

Target approximately 35–45 slides.

For every slide provide:
- Slide title
- Main content
- Speaker notes
- Suggested visual/diagram/code example
- Meme suggestion where appropriate
```


## Modern Components, Directives & Composition

```
Create Day 2 of an internal Angular 12 → Angular 20 engineering course.

Title:

"Modern Angular Components, Directives & Composition"

Audience:
Experienced Angular developers migrating from Angular 12-era patterns to Angular 20.

This presentation must focus heavily on the modern component/directive APIs introduced or matured after Angular 12.

Cover in depth:

1. Standalone components
2. Standalone directives
3. Standalone pipes
4. input()
5. input.required()
6. Input transforms
7. Input aliases
8. output()
9. model()
10. Signal-based queries:
    - viewChild()
    - viewChildren()
    - contentChild()
    - contentChildren()
11. Required signal queries
12. Directive Composition API
13. hostDirectives
14. Exposing host directive inputs
15. Exposing host directive outputs
16. Composing reusable behaviour
17. When Directive Composition API is appropriate
18. When Directive Composition API is NOT appropriate
19. Component inheritance vs composition
20. Host bindings
21. The host metadata API
22. Why @HostBinding and @HostListener should generally not be introduced in new code
23. Dynamic components and modern component creation
24. inject()
25. Injection context
26. EnvironmentInjector
27. Modern component lifecycle/render callbacks:
    - afterNextRender()
    - afterEveryRender()

For every major API show:

Angular 12 approach
↓
Problem with that approach
↓
Modern Angular approach
↓
Why Angular introduced it
↓
When to use it
↓
When NOT to use it

Spend significant time on Directive Composition API.

Use a realistic example such as:

A reusable button/input/card that composes:
- tooltip behaviour
- analytics behaviour
- keyboard accessibility
- focus management

Show how hostDirectives can compose behaviour without inheritance or wrapper components.

Explain clearly:

"Directive Composition API is behavioural composition, not inheritance."

Also cover the tradeoffs:
- discoverability
- debugging
- dependency relationships
- API exposure
- over-composition

Include a dedicated "Do not abuse hostDirectives" slide.

Explain model():

input + output → model()

Show two-way binding and explain when two-way binding is actually appropriate.

Include a decision matrix:

Need incoming data? → input()
Need outgoing event? → output()
Need two-way component state? → model()
Need reusable host behaviour? → hostDirectives
Need DOM/component query? → signal query
Need dependency? → inject()

Include at least 6 Angular/developer memes.

Possible meme themes:
- "I just need a tooltip" → 14 wrapper components
- inheritance vs composition
- discovering hostDirectives
- @Input() looking at input()
- @ViewChild() seeing viewChild()
- developer discovering model() after writing 400 lines of EventEmitter code

Do not use copyrighted meme images. Describe original meme concepts/captions.

End with:
"Modern Component API Cheat Sheet"

Target 40–50 slides.

Every slide must include:
- title
- content
- code where useful
- speaker notes
- suggested visual
- meme concept where appropriate

Verify Angular 20 APIs against official Angular documentation.
```

## Signals, State & Reactivity

```
Create Day 3 of an internal engineering course:

"Angular 20 Signals, State & Reactivity"

Audience:
Experienced Angular developers coming from Angular 12.

The goal is NOT to teach Signals syntax only. The goal is to teach developers how to reason about state in modern Angular.

Cover:

1. Why Signals were introduced
2. signal()
3. Reading signals
4. set()
5. update()
6. mutate() if applicable/current
7. computed()
8. effect()
9. linkedSignal()
10. resource() and modern async resource APIs available in Angular 20
11. Signal equality
12. Dynamic dependencies
13. Signal dependency graphs
14. Signal-based template rendering
15. Signals with OnPush
16. Signals and zoneless Angular
17. Signals vs RxJS
18. toSignal()
19. toObservable()
20. rxResource() if available in Angular 20
21. Local component state
22. Derived state
23. Async state
24. Shared application state
25. Services as state containers
26. When to use NgRx or another state-management library
27. When NOT to introduce a state-management library
28. Avoiding duplicated state
29. Avoiding effects for derived state
30. Avoiding signal abuse

Very clearly distinguish:

signal()
= writable state

computed()
= derived state

effect()
= side effect

Observable
= asynchronous/event stream

resource()
= async state/resource lifecycle

Explain why this is BAD:

effect(() => {
  this.total.set(this.price() * this.quantity());
});

and why this is GOOD:

total = computed(() => this.price() * this.quantity());

Include real examples involving:
- loading
- success
- error
- filtering
- selected item
- derived totals
- API data

Create a "Should this be a Signal?" decision tree.

Create a "Signals vs RxJS" comparison table.

Important:
Do NOT claim Signals replace RxJS.
Do NOT claim RxJS is legacy.
Explain interoperability.

Include at least 7 memes:
- Observable vs Signal
- effect() being abused
- "everything is a signal"
- developer creating a signal for a constant
- duplicated state
- giant NgRx store for a boolean
- computed() saving someone from an effect

End with a practical refactoring workshop:
Take an Angular 12 component containing:
- fields
- ngOnInit
- subscriptions
- EventEmitter
- derived properties
- manual loading flags

Refactor it incrementally into modern Angular 20.

Target 45–55 slides.

Verify all APIs and Angular 20 status against official Angular documentation.
```

## Modern Angular Architecture, DI, Router & HTTP

```
Create Day 4 of an Angular 12 → Angular 20 engineering course.

Title:

"Modern Angular Application Architecture"

Focus on how Angular applications should be architected in Angular 20.

Cover:

DEPENDENCY INJECTION
- inject()
- InjectionToken
- injection context
- EnvironmentInjector
- providedIn
- application-level providers
- environment providers
- feature-level providers
- provider scoping

FUNCTIONAL APIs
- functional route guards
- functional resolvers
- functional interceptors
- why Angular moved toward functional APIs
- when class-based APIs are still encountered
- when not to use classes simply because "Angular services use classes"

ROUTER
- provideRouter()
- standalone routing
- loadComponent()
- loadChildren()
- lazy loading
- route-level providers
- route data
- route guards
- resolvers
- withComponentInputBinding()
- modern route configuration
- feature route files

HTTP
- provideHttpClient()
- functional interceptors
- withInterceptors()
- HttpContext
- request cancellation
- error handling
- typed HTTP responses
- RxJS and Signals at the HTTP boundary

ARCHITECTURE
- feature-based architecture
- standalone feature boundaries
- smart/container vs presentational components
- services
- state services
- API services
- facades
- avoiding god services
- avoiding god components
- dependency direction

Compare:

Angular 12:
AppModule
  ↓
FeatureModule
  ↓
Component
  ↓
Service

Angular 20:
Application providers
  ↓
Feature route
  ↓
Standalone component
  ↓
Signals/services/resources

Do not present this as a universal architecture. Explain tradeoffs.

Include practical examples of:
- authentication guard
- authorization guard
- HTTP authentication interceptor
- lazy-loaded admin feature
- feature-specific provider
- service scoped to a route

Include a "Where should this dependency live?" decision tree.

Include 6–8 developer memes:
- constructor injection with 17 dependencies
- giant AppModule
- class interceptor vs functional interceptor
- lazy loading everything
- service becoming 3,000 lines
- "just put it in the root provider"

End with a modern Angular architecture reference diagram.

Target 40–50 slides.
Verify Angular 20 APIs against official documentation.
```

## Rendering, Change Detection, Zoneless & Performance

```
Create Day 5:

"Angular 20 Rendering, Change Detection & Performance"

Audience:
Experienced Angular developers who understand basic change detection.

Do NOT give a beginner explanation of change detection. Focus on the transition from Angular 12-era assumptions to modern Angular.

Cover:

1. ZoneJS
2. Traditional change detection
3. ChangeDetectionStrategy.Default
4. OnPush
5. Signals and rendering
6. What actually triggers Angular rendering
7. Zoneless Angular
8. provideZonelessChangeDetection()
9. Zoneless compatibility
10. Common ZoneJS assumptions that break
11. Third-party libraries and zoneless
12. Event handling
13. Async work
14. manual change detection
15. ChangeDetectorRef
16. markForCheck()
17. detectChanges()
18. When manual change detection is a smell
19. @defer
20. @placeholder
21. @loading
22. @error
23. Defer triggers
24. on viewport
25. on interaction
26. on idle
27. on timer
28. Hydration
29. Incremental hydration
30. SSR
31. Client rendering
32. Render modes
33. Performance budgets
34. JavaScript bundle size
35. lazy loading
36. deferrable views
37. expensive component trees

Show concrete before/after performance examples.

Create a diagram explaining:

Event
→ State change
→ Dependency tracking
→ Rendering

Compare that with older ZoneJS-driven assumptions.

Include a "Don't cargo-cult OnPush" section.

Include a "Don't cargo-cult @defer" section.

Explain when @defer can actually make an application worse.

Include at least 8 memes:
- ZoneJS watching everything
- developer manually calling detectChanges()
- @defer applied to a button
- "everything must be lazy loaded"
- 12 MB JavaScript bundle
- OnPush cargo cult
- SSR doesn't magically fix performance
- zoneless developer discovering a library depends on ZoneJS

End with:
"Performance hierarchy:
Fix architecture before micro-optimizations."

Target 45–55 slides.
Verify Angular 20 rendering and performance APIs against official Angular documentation.
```

## Forms & Modern User Interaction

```
Create Day 6:

"Angular 20 Forms: What Changed and What Didn't"

Important:
Do NOT pretend Signals replaced Angular Forms.

Cover:

1. Template-driven forms
2. Reactive forms
3. Typed reactive forms
4. FormControl
5. FormGroup
6. FormArray
7. FormRecord
8. Validators
9. Async validators
10. NonNullableFormBuilder
11. ControlValueAccessor
12. Custom form controls
13. Dynamic forms
14. Form state vs application state
15. Signals + Forms
16. model() + component two-way binding
17. Form validation architecture
18. Accessibility
19. Error display
20. Server-side validation
21. When template-driven forms are appropriate
22. When Reactive Forms are appropriate
23. Why Signals do NOT automatically replace Reactive Forms

Create a decision matrix:

Simple form
→ Template-driven may be sufficient

Complex business form
→ Reactive Forms

Reusable input component
→ ControlValueAccessor

Component state synchronization
→ input()/output()/model()

Application state
→ Signals

Async stream
→ Observable

Include a legacy Angular 12 form migration example.

Show bad patterns such as:
- duplicating form state into signals unnecessarily
- subscribing to every control just to copy values elsewhere
- giant components handling every validation concern

Include 5–6 memes:
- 200-line FormGroup
- "just one more validator"
- developer trying to make Signals replace FormControl
- nested FormArray
- ControlValueAccessor debugging
- template-driven form discovering complex requirements

Target 35–45 slides.
Verify Angular 20 APIs against official documentation.
```

## Modern Angular Platform Features

```
Create Day 7:

"Angular 20 Platform Features You Should Know"

This is a feature-focused presentation.

The purpose is to cover modern Angular APIs/features that don't fit cleanly into Signals, routing, forms, or basic components.

Before writing the deck, research the official Angular 20 documentation and identify important Angular 20-era APIs/features that experienced Angular 12 developers should know.

Prioritize features that:
- are new after Angular 12
- are stable in Angular 20
- materially change how Angular applications can be designed
- developers may reasonably encounter in modern Angular code
- should influence architecture or coding decisions

Potential areas to investigate and include where applicable:

- Directive Composition API
- hostDirectives
- model()
- linkedSignal()
- resource()
- rxResource()
- signal queries
- render callbacks
- afterNextRender()
- afterEveryRender()
- @defer
- incremental hydration
- zoneless
- modern dependency injection
- environment providers
- modern router features
- route-level rendering
- view transitions
- modern animation APIs
- dynamic component APIs
- programmatic rendering
- Angular CDK improvements
- accessibility APIs
- modern template APIs
- modern debugging/developer tooling
- Angular DevTools capabilities
- modern build tooling

For each feature answer:

1. What is it?
2. What problem does it solve?
3. Why was it introduced?
4. What did Angular developers typically do before it?
5. Is it stable in Angular 20?
6. Should our team use it?
7. When should we NOT use it?
8. What does the code look like?
9. What architectural implications does it have?
10. What are common mistakes?

Create a "Feature Radar" with:
GREEN = learn/use now
BLUE = use when appropriate
YELLOW = understand for existing code
RED = don't introduce

Do not simply dump APIs. Explain why each feature matters.

Include 8–10 memes about developers discovering new Angular APIs.

End with:
"Top 15 Angular 20 APIs every Angular 12 developer should know."

Target 45–55 slides.

Verify every feature against official Angular 20 documentation and explicitly distinguish Angular 20 features from features introduced only in later Angular versions.
```

## Testing, Tooling & Developer Experience

```
Create Day 8:

"Modern Angular Testing & Developer Experience"

Audience:
Experienced Angular developers maintaining Angular 12 and Angular 20 code.

Cover:

1. Angular testing evolution
2. TestBed with standalone components
3. Testing providers
4. Testing signals
5. Testing computed state
6. Testing effects
7. Testing input()/output()
8. Testing model()
9. Testing hostDirectives
10. Testing router features
11. Testing functional guards
12. Testing functional interceptors
13. HTTP testing
14. Component harnesses
15. Angular CDK testing utilities
16. Unit vs integration tests
17. Avoiding implementation-detail tests
18. Testing DOM behaviour
19. Accessibility testing
20. Async testing
21. fakeAsync and modern alternatives where applicable
22. Current Angular testing ecosystem
23. Angular CLI
24. Angular build tooling
25. Angular DevTools
26. Extended diagnostics
27. Strict TypeScript
28. template type checking
29. linting
30. automated migrations

Compare Angular 12 testing patterns with Angular 20 patterns.

Include a practical refactoring example.

Include 5 memes:
- brittle test suite
- TestBed configuration explosion
- testing private implementation details
- "the test passes but the UI is broken"
- developer discovering component harnesses

End with a team testing standard:
"What we test / What we don't test."

Target 35–45 slides.

Verify current Angular 20 tooling and testing recommendations against official documentation.
```

## Angular 12 → 20 Migration Workshop

```
Create Day 9:

"Angular 12 → Angular 20 Migration Workshop"

This should be highly practical.

Assume a real production application contains a mixture of Angular 12-era and Angular 20-era code.

Cover:

1. How to assess an existing Angular codebase
2. Finding legacy patterns
3. Finding deprecated APIs
4. Angular migration schematics
5. Standalone migration
6. Control flow migration
7. Signal input migration
8. output migration
9. query migration
10. inject migration
11. modern router migration
12. functional interceptor migration
13. functional guard migration
14. identifying ZoneJS assumptions
15. preparing for zoneless
16. OnPush migration
17. RxJS → Signals decisions
18. when NOT to migrate
19. handling third-party Angular libraries
20. mixed Angular patterns
21. migration pull-request strategy
22. avoiding giant migration PRs
23. incremental migration
24. measuring migration progress

Create a realistic Angular 12 component and progressively migrate it.

Show the code at every stage.

Create a table:

Legacy API
→ Modern API
→ Automated migration?
→ Manual work?
→ Priority

Include examples of:
- code that should be migrated immediately
- code that can wait
- code that should remain untouched

Include a "Migration Horror Stories" section with 5 memes.

Examples:
- "We'll just upgrade Angular"
- 40,000 changed lines
- merge conflict apocalypse
- deprecated API bingo
- "works on my machine"

End with a practical migration playbook for the team.

Target 45–55 slides.
```

## Team Standards: "What Should I Use?"

```
Create Day 10:

"Modern Angular Engineering Standards"

This is the final presentation of an Angular 12 → Angular 20 engineering course.

The goal is to turn everything from the previous sessions into practical team rules.

Start with:

"When I write a new Angular feature in 2026, what should I use?"

Create decision trees for:

1. Component architecture
2. Component state
3. Derived state
4. Async state
5. Inputs
6. Outputs
7. Two-way binding
8. DOM queries
9. Reusable behaviour
10. Dependency injection
11. HTTP
12. Routing
13. Forms
14. Change detection
15. Performance
16. SSR
17. Hydration
18. Testing
19. State management

Create a definitive table:

Angular 12 pattern
| Angular 20 replacement
| Status
| Use for new code?
| Why?
| Migration priority

Include at minimum:

NgModule
@Input
@Output
@ViewChild
@ContentChild
constructor injection
*ngIf
*ngFor
*ngSwitch
NgClass
NgStyle
class guards
class interceptors
ZoneJS assumptions
manual change detection
imperative state
RxJS
Reactive Forms
async pipe
OnPush
services
NgRx/state management

Make the distinctions nuanced.

Do NOT label everything old as bad.

Explicitly classify each as:
- REQUIRED for new code
- PREFERRED
- USE WHEN APPROPRIATE
- LEGACY BUT VALID
- DEPRECATED
- AVOID

Include a "10 things Angular 12 developers get wrong in Angular 20" section.

Include a "10 things Angular 20 developers overuse" section.

Include a "Modern Angular anti-patterns" section:
- signal everything
- effect everywhere
- defer everything
- hostDirectives everywhere
- state duplication
- giant services
- giant components
- unnecessary global state
- unnecessary two-way binding
- unnecessary RxJS/Signal conversion
- premature zoneless migration
- migration for migration's sake

Include 10–12 memes throughout the deck.

End with a one-page "Angular 20 Team Cheat Sheet" that developers can literally keep next to their editor.

Target 40–50 slides.

Use official Angular 20 documentation as the authority for API status, stability, recommendations, and deprecations.
```