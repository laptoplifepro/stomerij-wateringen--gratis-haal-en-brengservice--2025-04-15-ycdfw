# Landing Page Maintenance Guide

This guide will help you maintain and customize the Stomerij Wateringen landing page. Follow these detailed instructions to make common updates while preserving the page's functionality and design.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the company name and navigation menu:

```html
<header class="fixed w-full bg-white/95 backdrop-blur-sm z-50 border-b border-gray-100">
    <nav class="container mx-auto px-6 py-4">
        <div class="flex items-center justify-between">
            <a href="/" class="text-2xl font-bold text-blue-600">Stomerij Wateringen</a>
            <!-- Navigation items -->
        </div>
    </nav>
</header>
```

To update:
1. Company name: Locate `Stomerij Wateringen` and replace with your business name
2. Header styling: Modify these Tailwind classes:
   - `bg-white/95`: Controls background transparency
   - `text-blue-600`: Changes text color
   - `text-2xl`: Adjusts font size

### Hero Section
The main banner section contains:

```html
<section class="pt-32 pb-20 bg-gradient-to-br from-blue-50 to-white">
    <div class="max-w-4xl mx-auto text-center">
        <h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8">
            Professionele Stomerij met Gratis Haal- en Brengservice
        </h1>
        <p class="text-xl text-gray-600 mb-12">
            Uw kleding verdient de beste zorg...
        </p>
    </div>
</section>
```

To modify:
1. Main heading: Replace text inside `<h1>` tags
2. Subheading: Update text in the `<p>` tag
3. Responsive text sizes:
   - `text-4xl`: Mobile size
   - `md:text-5xl`: Tablet size
   - `lg:text-6xl`: Desktop size

## Fixing Broken Links

### Navigation Menu Links
Current navigation links are:

```html
<div class="hidden md:flex space-x-8">
    <a href="#diensten" class="text-gray-600 hover:text-blue-600">Diensten</a>
    <a href="#voordelen" class="text-gray-600 hover:text-blue-600">Voordelen</a>
    <a href="#faq" class="text-gray-600 hover:text-blue-600">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-blue-600">Contact</a>
</div>
```

To update:
1. Internal links (starting with #): Ensure section IDs match
   - Example: `href="#diensten"` should match `id="diensten"` in the corresponding section
2. External links: Replace with full URLs
   - Example: `href="https://your-website.com/page"`

### Call-to-Action Links
Located in multiple sections:

```html
<a href="https://wasserettewestland.nl" class="px-8 py-4 bg-blue-600 text-white rounded-full">
    Maak een Afspraak
</a>
```

To modify:
1. Update `href` attribute with your booking system URL
2. Maintain the styling classes for consistent design

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links to the footer:

```html
<!-- Add this to the footer links section -->
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

Steps to implement:
1. Create `privacy.html` and `terms.html` files
2. Add the links to the footer section
3. Match existing styling using provided classes

## Troubleshooting

Common issues and solutions:

1. **Broken Internal Links**
   - Check that section IDs match exactly with href attributes
   - IDs are case-sensitive
   - Example: `href="#FAQ"` won't link to `id="faq"`

2. **Responsive Design Issues**
   - Verify breakpoint classes are correct:
     - `md:` for tablet (768px)
     - `lg:` for desktop (1024px)
   - Test at different screen sizes

3. **Styling Inconsistencies**
   - Copy existing Tailwind classes for similar elements
   - Maintain color scheme using existing color classes:
     - Primary: `blue-600`
     - Text: `gray-600`
     - Background: `white`, `gray-50`

Remember to:
- Test all changes in multiple browsers
- Verify mobile responsiveness
- Keep backup copies of working code
- Maintain consistent spacing and indentation

For additional help, refer to:
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [HTML MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/HTML)