# Sydney Website Design - Landing Page Maintenance Guide

This guide will help you maintain and customize the Sydney Website Design landing page. It's written for beginners and provides detailed instructions for common maintenance tasks.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your brand name and navigation menu. To update:

1. **Brand Name**: Locate this code in the header:
```html
<a href="/" class="text-2xl font-bold text-gray-800">
    Sydney<span class="text-blue-600">Design</span>
</a>
```
- Change "Sydney" and "Design" to your preferred text
- Keep the `<span>` tag to maintain the blue color on the second word

2. **Navigation Menu Items**: Find the navigation div:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```
- Replace text between `<a>` tags with your menu items
- Keep the `href` attributes matching your section IDs

### Hero Section
Located right after the header:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold">
    Best Websites In Sydney
</h1>
<p class="text-xl md:text-2xl text-gray-600">
    Professional web design solutions...
</p>
```
- Update heading and paragraph text as needed
- Maintain the responsive text classes (`text-4xl`, `md:text-5xl`, etc.)

### Understanding Tailwind Classes
Common classes used in this template:
- Text sizes: `text-xl`, `text-2xl`, etc.
- Colors: `text-gray-600`, `bg-blue-600`
- Spacing: `px-6`, `py-4`, `mb-6`
- Responsive prefixes: `md:`, `lg:`

To modify styles:
1. Find the element you want to change
2. Locate its class attribute
3. Reference Tailwind documentation for alternative classes
4. Replace or add classes maintaining the same format

Example:
```html
<!-- Original -->
<div class="bg-blue-600 text-white px-8 py-4">

<!-- Modified for darker blue and larger padding -->
<div class="bg-blue-800 text-white px-10 py-6">
```

## Managing Links

### Current Link Inventory
1. **Navigation Links**:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

2. **Call-to-Action Links**:
```html
<a href="https://twd.com">Get Started Today</a>
<a href="mailto:admin@twd.com">Contact Us Now</a>
```

3. **Social Media Links** (in footer):
```html
<a href="#" class="text-gray-400 hover:text-white">
    <i class="fab fa-facebook text-xl"></i>
</a>
```

### Updating Links
1. Internal Links (same page):
- Keep the `#` prefix
- Ensure the href matches the section ID
```html
<!-- Section ID -->
<section id="features">

<!-- Matching link -->
<a href="#features">
```

2. External Links:
- Replace placeholder URLs
- Include full https:// address
```html
<!-- Original -->
<a href="https://twd.com">

<!-- Updated -->
<a href="https://your-actual-domain.com">
```

3. Email Links:
- Update the email address in mailto: links
```html
<a href="mailto:your-actual-email@domain.com">
```

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links to the Quick Links section:

```html
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Quick Links</h4>
    <ul class="space-y-2">
        <!-- Existing links -->
        <li><a href="#features" class="hover:text-white transition-colors duration-300">Features</a></li>
        
        <!-- Add new links -->
        <li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Creating Policy Pages
1. Create new files:
   - privacy.html
   - terms.html

2. Use consistent styling:
```html
<!-- privacy.html/terms.html template -->
<!DOCTYPE html>
<html lang="en">
<head>
    <!-- Copy head section from index.html -->
</head>
<body class="font-sans antialiased text-gray-900 bg-white">
    <!-- Copy header from index.html -->
    
    <main class="container mx-auto px-6 py-32">
        <h1 class="text-4xl font-bold mb-8">Privacy Policy</h1>
        <!-- Add your policy content here -->
    </main>

    <!-- Copy footer from index.html -->
</body>
</html>
```

## Troubleshooting

Common Issues:
1. **Broken Internal Links**
   - Verify section IDs match href attributes exactly
   - IDs are case-sensitive

2. **Responsive Design Issues**
   - Check mobile view using browser dev tools
   - Ensure responsive classes (md:, lg:) are present

3. **Social Media Icons Not Showing**
   - Verify Font Awesome CDN link in header
   - Check icon class names match Font Awesome 6 syntax

For additional help:
- Consult [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- Use browser developer tools to inspect elements
- Test all links before deploying changes