# Biohome Landing Page Maintenance Guide

This guide will help you maintain and customize the Biohome landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions to make common updates.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the logo and navigation menu. To update:

1. **Logo Text**
```html
<!-- Find this line in the header -->
<a href="#" class="text-2xl font-bold bg-gradient-to-r from-purple-600 to-blue-500 bg-clip-text text-transparent">Biohome</a>
```
- Replace "Biohome" with your desired text
- Keep the classes to maintain the gradient effect

2. **Navigation Menu Items**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors">Features</a>
    <!-- Additional menu items -->
</div>
```
- Update text between `>` and `</a>`
- Maintain the class structure for consistent styling

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold mb-6 bg-gradient-to-r from-purple-600 to-blue-500 bg-clip-text text-transparent">Koop Biohome Ultimate Met Korting</h1>
```
- Update the heading text between the `<h1>` tags
- The classes control:
  - `text-4xl/5xl/6xl`: Text size at different screen sizes
  - `bg-gradient-to-r`: Right-flowing gradient
  - `font-bold`: Text weight

### Tailwind CSS Tips for Beginners
- Numbers in classes (like `text-xl`) control size
- `md:` and `lg:` prefixes apply styles at specific screen sizes
- Color classes follow pattern: `text-{color}-{shade}`
- Common shades range from 50 to 900

## Managing Links

### Navigation Menu Links
Current internal links:
```html
<a href="#features">Features</a>
<a href="#benefits">Voordelen</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```
To update:
1. Change the `href` value to match your section IDs
2. Ensure corresponding sections have matching ID attributes
3. For external links, use complete URLs:
```html
<a href="https://your-external-link.com">Link Text</a>
```

### Call-to-Action Buttons
Current product link:
```html
<a href="https://amzn.to/3Guq4Bu" class="inline-block bg-gradient-to-r from-purple-600 to-blue-500 text-white font-semibold px-8 py-4 rounded-full">
    Profiteer Nu van de Korting
</a>
```
To update:
1. Replace `https://amzn.to/3Guq4Bu` with your product link
2. Update button text between `<a>` tags
3. Maintain classes for consistent styling

## Adding Privacy and Terms Pages

### Footer Links Setup
Current placeholder links:
```html
<ul class="space-y-2">
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors">Privacy Policy</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors">Terms of Service</a></li>
</ul>
```

To add proper links:
1. Create new files:
   - `privacy.html`
   - `terms.html`
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors">Terms of Service</a></li>
```

### Creating Policy Pages
Basic structure for policy pages:
```html
<!DOCTYPE html>
<html lang="nl" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Privacy Policy - Biohome Ultimate</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
</head>
<body class="font-['Inter'] antialiased bg-white text-gray-900">
    <!-- Copy header from index.html -->
    
    <main class="container mx-auto px-4 pt-32 pb-24">
        <h1 class="text-3xl font-bold mb-8">Privacy Policy</h1>
        <!-- Add your privacy policy content here -->
    </main>

    <!-- Copy footer from index.html -->
</body>
</html>
```

## Troubleshooting

Common Issues and Solutions:

1. **Broken Internal Links**
   - Check that section IDs match href values exactly
   - IDs are case-sensitive
   - Remove any spaces in IDs

2. **Styling Issues**
   - Verify Tailwind CSS is loading (check script tag)
   - Classes must be exact matches (no spaces in class names)
   - Check for missing closing tags

3. **Responsive Design Problems**
   - Test at different screen sizes
   - Ensure `md:` and `lg:` prefixes are used correctly
   - Verify the viewport meta tag is present

Need help? Contact technical support or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).