# Frontend and UI Standards

## 1. Applicability

Apply to Blade, Livewire, Inertia, Vue, React, or other actual project frontend stacks. Do not introduce a frontend framework solely to match this document.

## 2. UI consistency

Define design tokens, typography, spacing, color, component behavior, forms, navigation, feedback, loading, empty, error, and confirmation states. Reuse components when it improves consistency without creating excessive abstraction.

## 3. Accessibility

Target WCAG 2.2 AA where feasible or required. Consider semantic HTML, keyboard access, visible focus, labels, contrast, error identification, screen-reader names, reduced motion, and responsive zoom. Accessibility must be tested, not assumed from visual appearance.

## 4. Responsive and usability

Define supported viewports/devices and test important workflows at representative sizes. Avoid relying only on hover, color, or icons to communicate state. Provide clear destructive-action confirmation and useful validation messages.

## 5. Frontend security

Treat client input and state as untrusted. Enforce authorization and validation on the server. Avoid unsafe HTML rendering, protect CSRF where applicable, and do not place secrets in browser bundles or local storage without a deliberate threat assessment.

## 6. Performance

Measure bundle size, asset loading, rendering, network requests, and Core Web Vitals where relevant. Optimize images, lazy-load appropriate resources, avoid unnecessary client-side dependencies, and provide loading/error states.

## 7. Testing

Use component/unit tests, browser/E2E tests, accessibility checks, responsive checks, and visual regression where proportionate. Cover keyboard navigation and critical user journeys.
