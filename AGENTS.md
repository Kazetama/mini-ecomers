# Pratama — AI Engineering & UI/UX Development Rules

## 1. PROJECT OVERVIEW

This project is Pratama, a premium digital services e-commerce website.

The platform provides:
- Academic document similarity checking services.
- Document editing and formatting services.
- Academic consultation services.
- Customer order management.
- Secure document uploads and downloads.
- Payment processing.
- Customer dashboard.
- Admin dashboard.

The application must be developed as a production-oriented web application with maintainable architecture, consistent UI/UX, strong security, and reliable business logic.

Do not treat this project as a simple landing page or disposable prototype.

---

## 2. MANDATORY NEXT.JS DOCUMENTATION

IMPORTANT: This project may use a Next.js version with breaking changes.

Before implementing or modifying Next.js functionality:

1. Read the relevant documentation inside the installed Next.js package.
2. Locate the documentation relative to the directory containing the relevant AGENTS.md file.
3. Use the installed documentation as the primary source of truth.
4. Verify the current APIs, conventions, routing behavior, rendering strategies, and configuration.
5. Check for deprecated APIs and migration notices.
6. Never assume that APIs from previous Next.js versions remain valid.
7. Do not invent framework APIs, configuration options, or file conventions.
8. Follow the installed version's App Router and Server Component conventions.
9. Verify compatibility before introducing new dependencies.
10. When documentation is unavailable or incomplete, explicitly identify the uncertainty before proceeding.

Documentation location:

node_modules/next/dist/docs/

In a monorepo, resolve the documentation from the directory containing the applicable Next.js package.

---

## 3. ENGINEERING PRINCIPLES

Act as a senior software engineer, software architect, and UI/UX designer.

Before implementing a feature:

1. Understand the existing project structure.
2. Identify the relevant feature modules.
3. Inspect existing components and utilities.
4. Read the relevant documentation.
5. Identify dependencies and integration points.
6. Plan the implementation.
7. Implement the smallest maintainable solution.
8. Verify the implementation.
9. Update documentation when architectural changes occur.

Do not:
- Rewrite working code without a clear reason.
- Introduce unnecessary abstractions.
- Duplicate existing functionality.
- Create unnecessary dependencies.
- Ignore existing project conventions.
- Modify unrelated files.
- Claim that code works without verification.

Prefer maintainability, correctness, accessibility, and consistency over unnecessary complexity.

---

## 4. UI/UX DESIGN PHILOSOPHY

The application must have a distinctive, professional, premium visual identity.

Design direction:

- Style: Clean Premium.
- Primary color: Electric Blue.
- Secondary color: Navy.
- Background: White and neutral surfaces.
- Typography: Modern, readable, and professional.
- Visual character: Trustworthy digital service business.
- Layout: Structured, spacious, responsive, and intentional.

The design must not resemble a generic AI-generated dashboard or template.

### 4.1 Design Quality Requirements

Every page must have:

- A clear visual hierarchy.
- Purposeful typography.
- Consistent spacing.
- Consistent alignment.
- Appropriate contrast.
- Clear primary and secondary actions.
- Meaningful information grouping.
- Responsive behavior.
- Appropriate loading, empty, success, and error states.

Design decisions must be based on the purpose of the page and the needs of its users.

### 4.2 Avoid Generic AI Design

Do not automatically generate:

- Excessive gradient backgrounds.
- Unnecessary glassmorphism.
- Excessive rounded cards.
- Identical card-based layouts on every page.
- Random decorative elements.
- Excessive floating elements.
- Unnecessary glowing effects.
- Unnecessary animated backgrounds.
- Repetitive hero sections.
- Excessive dashboard statistics.
- Arbitrary color combinations.
- Emoji-based professional navigation icons.
- Unnecessary marketing copy.
- Artificially large headings without hierarchy.

Do not use a visual effect merely because it is fashionable.

Every visual element must serve a clear purpose.

### 4.3 Page-Specific Design

Do not force every page into the same layout.

Landing pages, service catalogs, checkout pages, customer dashboards, authentication pages, and admin dashboards must have layouts appropriate to their respective functions.

Examples:

Landing page:
- Clear value proposition.
- Focused service discovery.
- Strong primary call to action.
- Relevant trust indicators.
- Simple navigation.

Service catalog:
- Clear service descriptions.
- Pricing information.
- Service categories.
- Relevant filtering.
- Easy service selection.

Checkout:
- Clear order summary.
- Document upload.
- Service configuration.
- Price transparency.
- Payment selection.
- Validation and error feedback.

Customer dashboard:
- Order overview.
- Order status.
- Relevant actions.
- Document delivery.
- Payment information.

Admin dashboard:
- Operational overview.
- Order management.
- Customer management.
- Service management.
- Payment verification.
- Document processing.

### 4.4 Responsive Design

Every feature must support:

- Mobile devices.
- Tablets.
- Desktop screens.

Requirements:

1. Use responsive layouts.
2. Avoid horizontal overflow.
3. Ensure forms remain usable on mobile.
4. Ensure navigation works on smaller screens.
5. Use appropriate responsive typography.
6. Maintain accessible touch targets.
7. Test important layouts at different viewport sizes.

Do not treat mobile responsiveness as an optional finishing step.

---

## 5. UI COMPONENT LIBRARIES

Use the following libraries when appropriate.

### Primary UI Foundation

- Tailwind CSS.
- shadcn/ui.
- Radix UI.
- Lucide React.

### Optional Visual Enhancement

- Motion.
- React Bits.
- Magic UI.
- Aceternity UI.

### Library Rules

1. Prefer shadcn/ui for standard application components.
2. Use Radix UI primitives when accessible interaction behavior is required.
3. Use Lucide React for consistent interface icons.
4. Use Motion for purposeful transitions and interactions.
5. Use React Bits, Magic UI, or Aceternity UI selectively.
6. Read the official documentation before implementing unfamiliar APIs.
7. Verify compatibility with the installed React and Next.js versions.
8. Do not install multiple libraries for the same purpose without justification.
9. Do not introduce a dependency for a trivial component that can be implemented cleanly with existing tools.
10. Preserve the application's visual consistency when using third-party components.

Do not copy an entire component library's visual identity.

Adapt components to the Pratama design system.

---

## 6. DESIGN SYSTEM

Maintain a consistent design system.

Centralize design tokens for:

- Colors.
- Typography.
- Spacing.
- Border radius.
- Shadows.
- Layout widths.
- Breakpoints.
- Component states.

Use CSS variables and Tailwind conventions appropriate to the installed versions.

Do not scatter arbitrary styling values across unrelated components.

### Color Rules

Use:
- Electric Blue for primary actions and important interactions.
- Navy for selected branding and emphasis.
- Neutral colors for backgrounds, surfaces, borders, and secondary text.

Avoid:
- Excessive saturated colors.
- Multiple competing accent colors.
- Inconsistent color usage between pages.
- Color-only status indicators.

### Typography Rules

1. Establish a consistent typography scale.
2. Use readable body text.
3. Maintain appropriate line height.
4. Avoid unnecessary font weight variations.
5. Use typography to establish hierarchy.
6. Do not use oversized headings without a clear design reason.

### Component Rules

Reusable components must have:

- Clear responsibilities.
- Consistent styling.
- Appropriate TypeScript types.
- Accessible interaction behavior.
- Explicit variants when needed.

Avoid creating multiple components with identical functionality.

---

## 7. ARCHITECTURE AND SEPARATION OF CONCERNS

Use a feature-oriented architecture with clear separation of responsibilities.

The application must separate:

- Routing.
- UI components.
- Business logic.
- Data access.
- Validation.
- Authentication.
- Payment integration.
- File storage.
- Shared utilities.
- Configuration.
- Documentation.

Do not place the entire application inside the app directory.

### 7.1 Recommended Structure

src/
  app/
    (marketing)/
    (auth)/
    (customer)/
    admin/
    api/

  components/
    ui/
    layout/
    shared/
    providers/

  features/
    auth/
    services/
    orders/
    payments/
    documents/
    users/

  lib/
    db/
    auth/
    payments/
    storage/
    validations/
    utils/

  hooks/
  config/
  types/
  constants/

docs/

prisma/

public/

This structure is a starting point, not an absolute requirement.

Adapt it to the actual project size and installed Next.js conventions.

### 7.2 App Directory

The app directory is responsible for:

- Routing.
- Layout composition.
- Page composition.
- Route-level loading states.
- Route-level error handling.
- Framework-specific rendering behavior.

Keep business logic out of page components whenever it can be placed in a dedicated feature module.

### 7.3 Feature Modules

Each feature must own its related functionality.

A feature may contain:

- components/
- hooks/
- services/
- schemas/
- types/
- actions/
- index.ts

Only create folders that are actually needed.

Do not create empty folders simply to satisfy a template.

### 7.4 UI Components

Separate components into:

- Primitive UI components.
- Shared application components.
- Feature-specific components.
- Layout components.

Do not place database queries, payment processing, or business rules inside presentational components.

### 7.5 Business Logic

Business logic must be implemented in appropriate feature services or server-side modules.

Examples:

- Order creation.
- Order status transitions.
- Payment verification.
- Service pricing.
- Document processing.
- Customer authorization.

Business logic must not depend on presentation components.

### 7.6 Data Access

Database access must be centralized in appropriate server-side data access modules.

Requirements:

1. Use the project's established ORM.
2. Keep database operations out of presentational components.
3. Validate input before database mutations.
4. Enforce authorization before accessing protected records.
5. Use transactions for operations that require atomicity.
6. Avoid duplicated queries.
7. Avoid exposing internal database models directly to client components.

Do not create a repository abstraction for every database operation unless it provides meaningful value.

### 7.7 Server and Client Components

Follow the installed Next.js documentation.

Prefer Server Components for server-rendered content and data access.

Use Client Components only when browser interactivity, client-side state, or client-only APIs are required.

Do not add "use client" unnecessarily.

Never expose secrets or privileged server-side operations to client components.

---

## 8. TYPESCRIPT AND CODE QUALITY

Use TypeScript throughout the application.

Requirements:

1. Avoid unnecessary any types.
2. Define explicit interfaces or types for important data structures.
3. Use discriminated unions for complex application states when appropriate.
4. Avoid duplicated type definitions.
5. Keep function responsibilities focused.
6. Use meaningful variable and function names.
7. Avoid excessively large components.
8. Avoid deeply nested conditional logic.
9. Handle errors explicitly.
10. Remove unused imports and variables.

Do not use TypeScript merely to suppress errors.

Fix the underlying type problem.

---

## 9. VALIDATION AND BUSINESS RULES

Use a consistent validation strategy.

Validation must occur on the server for all sensitive operations.

Use Zod or the project's established validation library when appropriate.

Validate:

- Authentication inputs.
- Service selections.
- Order creation.
- Payment callbacks.
- Document uploads.
- Administrative operations.
- User-generated content.

Client-side validation improves usability but does not replace server-side validation.

Never trust client-provided prices, roles, payment statuses, or ownership information.

---

## 10. SECURITY REQUIREMENTS

Security is mandatory.

### Authentication

- Use secure authentication practices.
- Protect authenticated routes.
- Verify authorization on the server.
- Enforce role-based access control.
- Never trust client-provided roles.

### Documents

- Store customer documents privately.
- Validate file types.
- Validate file sizes.
- Use randomized storage identifiers.
- Prevent unauthorized document access.
- Use signed download URLs when appropriate.
- Avoid exposing private storage paths.
- Restrict document access to authorized users and administrators.
- Define document retention and deletion policies.

### Payments

- Never trust payment success based only on the browser.
- Verify payment notifications using the provider's official mechanism.
- Validate transaction authenticity.
- Prevent duplicate payment processing.
- Use idempotency where supported.
- Keep payment credentials server-side.
- Do not store sensitive card information directly.

### Database

- Use parameterized queries through the ORM.
- Enforce ownership checks.
- Avoid exposing sensitive fields.
- Protect administrative operations.
- Handle transactions appropriately.

---

## 11. DOCUMENTATION REQUIREMENTS

Maintain documentation in the docs directory.

### Required Documentation

docs/
  architecture.md
  design-system.md
  database.md
  api.md
  authentication.md
  payment.md
  development-guide.md

### Documentation Responsibilities

architecture.md:
- Architecture overview.
- Module responsibilities.
- Data flow.
- Important architectural decisions.

design-system.md:
- Color tokens.
- Typography.
- Spacing.
- Component conventions.
- UI design principles.

database.md:
- Database schema.
- Relationships.
- Important constraints.
- Migration conventions.

api.md:
- Available endpoints.
- Request validation.
- Response structure.
- Authorization requirements.

authentication.md:
- Authentication flow.
- Session handling.
- Role permissions.

payment.md:
- Payment lifecycle.
- Verification process.
- Failure handling.

development-guide.md:
- Development setup.
- Commands.
- Coding conventions.
- Testing instructions.

### Documentation Rules

1. Update documentation when architecture changes.
2. Document important decisions.
3. Avoid documenting implementation details that change frequently without value.
4. Keep examples consistent with actual code.
5. Never invent implemented functionality in documentation.
6. Clearly distinguish planned features from implemented features.

---

## 12. TESTING REQUIREMENTS

Every significant feature must be verified.

Use the testing tools already established in the project.

Testing should cover:

- Business logic.
- Validation.
- Authentication.
- Authorization.
- Order creation.
- Payment verification.
- Document access.
- Important UI interactions.

When appropriate, use:

- Unit tests.
- Integration tests.
- End-to-end tests.

Do not claim tests passed unless they were actually executed.

Before completing a task:

1. Run relevant tests.
2. Run linting.
3. Run type checking.
4. Verify the build when practical.
5. Inspect the resulting changes.
6. Report any remaining issues.

---

## 13. PERFORMANCE AND ACCESSIBILITY

Prioritize:

- Efficient server-side rendering.
- Appropriate data fetching.
- Avoiding unnecessary client-side JavaScript.
- Optimized images.
- Avoiding unnecessary dependencies.
- Avoiding repeated database queries.
- Accessible semantic HTML.
- Keyboard navigation.
- Visible focus states.
- Accessible form labels.
- Appropriate contrast.
- Meaningful error messages.

Do not sacrifice accessibility for visual effects.

Do not optimize prematurely without evidence.

---

## 14. DEVELOPMENT WORKFLOW

For every new feature:

### Step 1: Understand

Inspect the relevant files and existing implementation.

### Step 2: Research

Read the official documentation for the installed framework and relevant libraries.

### Step 3: Plan

Identify:
- UI components.
- Data requirements.
- Business logic.
- Validation.
- Authorization.
- API integration.
- Testing requirements.

### Step 4: Implement

Use the existing architecture.

Keep responsibilities separated.

### Step 5: Verify

Run appropriate checks.

Inspect the UI and behavior.

### Step 6: Document

Update relevant documentation.

### Step 7: Report

Summarize:
- What was implemented.
- Files changed.
- Important design decisions.
- Tests performed.
- Known limitations.

---

## 15. CHANGE MANAGEMENT

Before modifying existing functionality:

1. Inspect the current implementation.
2. Identify dependencies.
3. Preserve working behavior.
4. Avoid unrelated changes.
5. Avoid replacing established patterns without justification.
6. Verify the impact of database changes.
7. Update migrations and documentation when necessary.

Never delete important functionality simply to simplify implementation.

Do not modify generated files unnecessarily.

Respect existing Next.js-generated instructions.

---

## 16. FINAL QUALITY STANDARD

A feature is not complete merely because it renders.

A feature is considered complete when:

- It satisfies its requirements.
- Its UI follows the design system.
- Its business logic is separated appropriately.
- Its data access is secure.
- Its inputs are validated.
- Its authorization is enforced.
- Its error states are handled.
- Its responsive behavior is considered.
- Relevant tests have been executed.
- Necessary documentation has been updated.

The final implementation must be understandable, maintainable, secure, and consistent with the existing project.

Do not prioritize generating more code over generating correct and maintainable code.

---

## 17. AI DEVELOPMENT BEHAVIOR

When requirements are unclear:

- Inspect the existing implementation first.
- Identify the specific uncertainty.
- Ask a focused clarification when the uncertainty materially affects architecture or behavior.
- Do not invent business requirements.

When requirements are sufficiently clear:

- Proceed without unnecessary questions.
- Make reasonable implementation decisions.
- Explain important trade-offs.
- Keep the implementation aligned with the project architecture.

Do not claim that a feature, integration, or test is complete without verification.

Always prioritize correctness, maintainability, security, and user experience.