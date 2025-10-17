# Modern Dental Website Style Guide

This guide details the design specifications for a modern website rebuild, adhering to the original legacy site's color scheme while utilizing the **Tailwind CSS color palette** for utility-first implementation.

## 1. Tailwind Color Palette

The color scheme maintains the original **Teal/Cyan** for branding and **Orange/Red** for emergency focus.

| Element              | Tailwind Utility Class | Hex Code  | Role                                               |
| :------------------- | :--------------------- | :-------- | :------------------------------------------------- |
| **Primary Accent**   | `cyan-500`             | `#06B6D4` | Branding, key headings, secondary CTAs.            |
| **Secondary Accent** | `orange-600`           | `#EA580C` | **Primary CTA**, emergency focus, critical alerts. |
| **Dark Neutral**     | `gray-900`             | `#111827` | Body text, primary headings, footer background.    |
| **Light Neutral**    | `gray-100`             | `#F3F4F6` | Section backgrounds, card backgrounds, borders.    |
| **White**            | `white`                | `#FFFFFF` | Main page background, high-contrast text.          |

---

## 2. Typography

The design requires a modern, highly legible **Sans-Serif** stack. The default Tailwind `font-sans` stack should be used, preferably mapping to **Montserrat** (for headings) and **Open Sans** (for body) if custom fonts are permitted.

| Element                | Tailwind Classes (Example)              | Use Case                       |
| :--------------------- | :-------------------------------------- | :----------------------------- |
| **H1 (Hero Title)**    | `text-5xl font-extrabold text-gray-900` | Main headline.                 |
| **H2 (Section Title)** | `text-3xl font-bold text-cyan-500`      | Major content section headers. |
| **H3 (Sub-Header)**    | `text-xl font-semibold text-gray-900`   | Card titles, sidebar headings. |
| **Body Text**          | `text-base text-gray-900`               | All paragraph and list text.   |

---

## 3. Layout & Structure

### A. Header & Navigation

- **Top Bar (Urgency):** Must be a full-width, sticky element with `bg-orange-600` and `text-white`.
  - **Content:** "24 HR EMERGENCY DENTAL: (619) 282-7060" with a prominent `tel:` link.
- **Main Navigation:** Should be a `bg-white` sticky component with standard links styled in `text-gray-900`. Hover state should use `text-cyan-500`.
- **Links:** HOME, SERVICES, ABOUT US, FAQ, NEWS.

### B. Call-to-Action (CTA) Priority

**Crucial Requirement:** The site **must not** contain any contact forms. All interaction points (CTAs) must be direct **Click-to-Call** or **Click-to-Text** links.

| CTA Type                 | Tailwind Classes                                                                        | Functionality/Protocol                                    |
| :----------------------- | :-------------------------------------------------------------------------------------- | :-------------------------------------------------------- |
| **Primary CTA** (Call)   | `bg-orange-600 hover:bg-orange-700 text-white font-bold py-4 px-8 rounded-lg shadow-xl` | `<a href="tel:6192827060">Call Now (619) 282-7060</a>`    |
| **Secondary CTA** (Text) | `bg-cyan-500 hover:bg-cyan-600 text-white font-bold py-4 px-8 rounded-lg shadow-xl`     | `<a href="sms:6192827060">Text Us for an Appointment</a>` |

### C. Body Content and Modularity

- **Design:** Use generous padding and margins (`p-10`, `m-4`) to create ample white space (`bg-white`).
- **Services:** Content (Extraction, Root Canal, etc.) should be presented in modular, responsive cards or a modern accordion view.
- **FAQs/Address:** These are implemented as separate **Information Cards** (`bg-gray-100` or `bg-white` with a shadow) in a grid layout.
- **Alert Banner (Payment/Disclaimer):** Replaces the legacy red box for a professional caution look.
  - **Classes:** `bg-red-50 border-l-4 border-red-600 p-4`

### D. Footer

- **Design:** Professional, full-width section.
  - **Classes:** `bg-gray-900 text-gray-100`.
- **Content:** Organized into responsive columns for Navigation, Location, and Contact Information (repeating the Primary CTA). Includes copyright and sitemap link.
