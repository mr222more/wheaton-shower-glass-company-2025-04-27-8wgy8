# Wheaton Shower Glass Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Wheaton Shower Glass landing page. Whether you're new to web development or need a quick reference, you'll find step-by-step guidance for common updates.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

```html
<!-- Company Name (Line 19) -->
<a href="/" class="text-xl font-bold tracking-tight hover:text-blue-400 transition-colors duration-300">
    Wheaton Shower Glass  <!-- Edit this text -->
</a>

<!-- Navigation Menu Items (Lines 22-24) -->
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>  <!-- Edit menu item text here -->
    <a href="#benefits">Benefits</a>
    <a href="#contact">Contact</a>
</div>
```

### Hero Section
The main banner section contains your primary heading and call-to-action:

```html
<!-- Main Heading (Lines 39-41) -->
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-6">
    Quick shower glass repairs today  <!-- Edit this headline -->
</h1>

<!-- Subheading (Lines 42-44) -->
<p class="text-xl md:text-2xl text-gray-400 mb-12 max-w-3xl mx-auto">
    Professional shower glass solutions...  <!-- Edit this description -->
</p>
```

#### Understanding Tailwind Classes
Common classes used throughout:
- Text sizes: `text-xl`, `text-2xl`, etc. (larger number = bigger text)
- Colors: `text-gray-400`, `bg-gray-900` (higher number = lighter shade)
- Spacing: `px-6`, `py-4` (p=padding, x=horizontal, y=vertical)
- Responsive: `md:text-5xl` (applies at medium screens and larger)

## Managing Links

### Navigation Links
The page uses both internal anchor links and external URLs:

```html
<!-- Internal Links (Lines 22-24) -->
<a href="#features">Features</a>  <!-- Links to section with id="features" -->
<a href="#benefits">Benefits</a>  <!-- Links to section with id="benefits" -->
<a href="#contact">Contact</a>    <!-- Links to section with id="contact" -->

<!-- External Links (Line 45) -->
<a href="http://www.customeuroglass.com">  <!-- Update with your website URL -->
```

To update external links:
1. Locate the `href` attribute
2. Replace the URL between the quotes
3. Test the link to ensure it works

### Email Links
Email links are found in the contact section and footer:

```html
<!-- Update email addresses in these locations -->
<a href="mailto:lt@customeuroglass.com">lt@customeuroglass.com</a>
```

## Adding Privacy and Terms Pages

### Footer Link Setup
The footer contains placeholder links for Privacy Policy and Terms of Service:

```html
<!-- Footer Legal Links (Lines 115-118) -->
<div class="space-y-2">
    <a href="#" class="block text-gray-400 hover:text-blue-400 transition-colors duration-300">Privacy Policy</a>
    <a href="#" class="block text-gray-400 hover:text-blue-400 transition-colors duration-300">Terms of Service</a>
</div>
```

To link to new pages:
1. Create `privacy.html` and `terms.html` in your website directory
2. Update the href attributes:
```html
<a href="privacy.html" class="block text-gray-400 hover:text-blue-400 transition-colors duration-300">Privacy Policy</a>
<a href="terms.html" class="block text-gray-400 hover:text-blue-400 transition-colors duration-300">Terms of Service</a>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Ensure section IDs match exactly (case-sensitive)
   - Check for extra spaces in IDs
   - Verify hash (#) prefix in href attributes

2. **Responsive Design Issues**
   - Check mobile view using browser dev tools
   - Verify `md:` and `lg:` classes are properly set
   - Test at different screen sizes

3. **Style Changes Not Appearing**
   - Confirm Tailwind CSS link is working
   - Check for typos in class names
   - Verify class order (later classes override earlier ones)

### Need Help?
- Tailwind CSS Documentation: [tailwindcss.com/docs](https://tailwindcss.com/docs)
- HTML Reference: [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/HTML)
- Test your page using [W3C Validator](https://validator.w3.org/)

Remember to always test your changes across different devices and browsers before publishing updates to your live site.