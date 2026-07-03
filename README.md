# Contact Us Page

A responsive contact page built as part of the [GreatFrontEnd Projects](https://www.greatfrontend.com/projects/challenges/contact-us-page) challenge series.

## Live Site

[Contact Us Page](https://contact-us-page-gamma.vercel.app/)

## Challenge

This project is a GreatFrontEnd challenge that focuses on assembling previously built components into a complete contact page. The goal is to combine a Navbar, Contact Section, FAQ Section, and Footer into a cohesive page while respecting layout rules, responsive behavior, and cross-section interactions. The main technical requirement is wiring the FAQ section's "Get in touch" and "customer support" links to smooth-scroll to the contact form and focus the Name input.

## Features

- **Contact form** — Contact form with validation, submits to the GreatFrontEnd API endpoint, and swaps in a success state or error toast depending on the response.
- **FAQ-to-contact scroll interaction** — clicking "Get in touch" or "customer support" in the FAQ section scrolls the Name field into view and focuses it.
- **Independent FAQ accordions** — each `FaqItem` wraps its own Radix `Accordion.Root`, so expanding one item doesn't affect the others.
- **Mobile menu with focus trap** — slide-in drawer rendered via `Portal`, closes on Escape or overlay click, traps keyboard focus with `useFocusTrap`.
- **Scroll-aware sticky navbar** - Background switches to blurred white as the page scrolls.
- **Care for A11y** — semantic HTML, ARIA attributes, WAI-ARIA patterns.

## Stack

- **React 19** + **TypeScript**
- **Tailwind CSS v4**
- **Radix UI** — Accordion primitive
- **Vite** - No SSR or complex routing needed here — Vite is the straightforward choice.
- **CVA** — To manage component variants in a structured way.
- **clsx** + **tailwind-merge** - To prevent CSS precedence issues.

## Project Structure

```
src/
├── blocks/
│   ├── contact-section/   # ContactSection, FormSuccess, useContactForm reducer
│   ├── faq-section/       # FaqSection, FaqItem, faq data, open/close icons
│   ├── footer/             # Footer, footer link/icon data, social icons
│   └── navigation/         # Navbar, MobileMenu, nav link data, icons
├── components/
│   └── ui/                 # Button, Link, Textarea, Toast, Badge, Portal, Accordion, button-variants
├── hooks/                  # useMediaQuery, useFocusTrap
├── utils/                  # cn(), validateEmail()
├── App.tsx                 # Page composition: Navbar, ContactSection, FaqSection, Footer
```

## Getting Started

```bash
pnpm install
pnpm dev
pnpm build
pnpm lint
pnpm format
```

## Code Conventions

- **Named exports** via `export { }` at the bottom of each file.
- **`type`** over `interface` for all type definitions.
- **kebab-case** for everything non-React.
- **camelCase** for hooks.
- **PascalCase** for component files.
