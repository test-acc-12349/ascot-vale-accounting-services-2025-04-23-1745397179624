# AV Accounting Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the AV Accounting landing page. Whether you're new to web development or need a quick reference, follow these steps to make common updates.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the company logo and navigation menu:

```html
<header class="fixed w-full bg-white/95 backdrop-blur-sm shadow-sm z-50">
    <nav class="container mx-auto px-6 py-4">
        <div class="flex items-center justify-between">
            <a href="/" class="text-2xl font-bold text-blue-600">AV Accounting</a>
            <!-- Navigation items -->
        </div>
    </nav>
</header>
```

To update:
1. Change company name: Modify the text "AV Accounting"
2. Adjust logo size: Change `text-2xl` to `text-3xl` for larger text
3. Modify color: Replace `text-blue-600` with other Tailwind colors (e.g., `text-red-600`)

### Hero Section
The main headline and call-to-action:

```html
<section class="pt-32 pb-24 bg-gradient-to-br from-blue-50 to-white">
    <div class="container mx-auto px-6">
        <div class="max-w-4xl mx-auto text-center">
            <h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">
                Ascot Vale accounting services
            </h1>
            <!-- Subheading and button -->
        </div>
    </div>
</section>
```

To update:
1. Change headline: Replace the h1 text
2. Adjust spacing: Modify `pt-32` (top padding) or `pb-24` (bottom padding)
3. Change background: Update gradient colors in `bg-gradient-to-br`

### Common Tailwind Classes Explained
- `container mx-auto`: Centers content with maximum width
- `px-6`: Adds horizontal padding (left and right)
- `py-4`: Adds vertical padding (top and bottom)
- `text-xl/2xl/3xl`: Controls text size
- `md:`: Applies styles at medium screen sizes
- `hover:`: Applies styles on mouse hover

## Fixing Broken Links

### Navigation Menu Links
Current navigation links in the header:

```html
<div class="hidden md:flex space-x-8">
    <a href="#services" class="text-gray-600 hover:text-blue-600">Services</a>
    <a href="#benefits" class="text-gray-600 hover:text-blue-600">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-blue-600">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-blue-600">Contact</a>
</div>
```

To update:
1. Internal links: Keep `#` prefix for same-page sections
2. External links: Replace `href="#"` with full URL (e.g., `href="https://example.com"`)
3. Verify all `id` attributes match their corresponding links

### Call-to-Action Buttons
Current placeholder links:

```html
<a href="https://theaccountants.com" class="inline-block bg-blue-600 text-white px-8 py-4">
    Get Started Today
</a>
```

To update:
1. Replace `https://theaccountants.com` with your actual URL
2. Ensure consistent styling across all CTA buttons

## Linking Privacy and Terms Pages

### Footer Legal Links
Current placeholder links in footer:

```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white">Terms of Service</a></li>
    </ul>
</div>
```

To add privacy and terms pages:
1. Create new files:
   ```
   privacy.html
   terms.html
   ```

2. Update footer links:
   ```html
   <li><a href="privacy.html" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
   <li><a href="terms.html" class="text-gray-400 hover:text-white">Terms of Service</a></li>
   ```

3. Maintain consistent styling:
   - Copy the header and footer from index.html
   - Use same Tailwind classes for consistency

## Troubleshooting

Common issues and solutions:

1. **Broken Internal Links**
   - Verify section IDs match exactly (case-sensitive)
   - Example: `href="#FAQ"` won't link to `id="faq"`

2. **Responsive Design Issues**
   - Check mobile preview in browser dev tools
   - Ensure `md:` classes are used for responsive layouts

3. **Inconsistent Styling**
   - Copy exact Tailwind classes from existing elements
   - Use browser inspector to compare styles

4. **Layout Problems**
   - Verify all `container` classes have `mx-auto`
   - Check for missing closing div tags

Remember to test all changes across different screen sizes and browsers before deploying to production.