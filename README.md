# Contact Us Page

A responsive contact page built as part of the [GreatFrontEnd Projects](https://www.greatfrontend.com/projects/challenges/contact-us-page) challenge series.

## Live Site

[Contact Us Page](https://contact-us-page-gamma.vercel.app/)

## Challenge

This project is a GreatFrontEnd challenge that focuses on combining components I had already built in previous challenges.
The goal is to combine a Navbar, Contact Section, FAQ Section, and Footer into a cohesive page while respecting layout rules, responsive behavior, and inter-section interactions.
The key interaction requirement: clicking "Get in touch" or "customer support" in the FAQ section smooth-scrolls to the contact form and focuses the Name input.

## Stack

- **React 19** + **TypeScript**
- **Tailwind CSS v4**
- **Radix UI** — Accordion primitive
- **Vite** - No SSR or complex routing needed here — Vite is the straightforward choice.
- **CVA** — To manage component variants in a structured way.
- **clsx** + **tailwind-merge** - To prevent CSS precedence issues.

## Features

- Contact form with validation, submitted to the GreatFrontEnd API endpoint
- Success and error states with accessible feedback
- Smooth scroll + focus management from FAQ to contact form
- Sticky navbar with scroll-aware background
- Responsive mobile menu with focus trap and keyboard navigation
- Care for A11y — semantic HTML, ARIA attributes, WAI-ARIA patterns

## Code Conventions

- **Named exports** via `export { }` at the bottom of each file.
- **`type`** over `interface` for all type definitions.
- **kebab-case** for everything non-React.
- **camelCase** for hooks.
- **PascalCase** for component files.

## Project Structure

```
src/
├── blocks/
│   ├── contact-section/     # Contact form, success state, form logic
│   ├── faq-section/         # FAQ accordion with scroll-to-contact interaction
│   ├── footer/              # Footer with social icons
│   └── navigation/          # Navbar and mobile menu
├── components/
│   └── ui/                  # Button, Link, Textarea, Toast, Accordion, Badge, Portal
├── hooks/                   # useMediaQuery, useFocusTrap
└── utils/                   # cn(), validateEmail()
```

## Getting Started

```bash
pnpm install
pnpm dev
pnpm build
pnpm lint
pnpm format
```
