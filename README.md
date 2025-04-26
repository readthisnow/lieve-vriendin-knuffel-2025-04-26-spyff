# Landing Page Maintenance Guide
## For Lieve Vriendin Knuffel Website

This guide will help you maintain and customize the Lieve Vriendin Knuffel landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Main Sections Location Guide
The page is divided into these key sections:
```html
<header> <!-- Navigation bar at top -->
<main>
    <section class="pt-32"> <!-- Hero section -->
    <section id="features"> <!-- Features section -->
    <section id="benefits"> <!-- Benefits section -->
    <section id="faq"> <!-- FAQ section -->
    <section class="py-24 bg-pink-600"> <!-- Call to action -->
<footer> <!-- Footer section -->
```

### Updating Text Content

#### Hero Section
To update the main headline, locate:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6 leading-tight">
    Lieve Vriendin Knuffel
</h1>
```
Simply replace "Lieve Vriendin Knuffel" with your desired text.

#### Features Section
Each feature card follows this structure:
```html
<div class="bg-white rounded-xl shadow-lg p-8">
    <h3 class="text-xl font-semibold mb-4">Beperkte Voorraad</h3>
    <p class="text-gray-600">Nog maar enkele exemplaren beschikbaar.</p>
</div>
```
To add new features, copy this entire `<div>` block and modify the text within the `<h3>` and `<p>` tags.

### Tailwind CSS Classes Explained

#### Common Class Patterns
- `text-[size]`: Controls text size (xl, 2xl, 3xl, etc.)
- `mb-[number]`: Adds margin bottom (4, 6, 8, etc.)
- `py-[number]`: Adds padding top and bottom
- `bg-[color]-[shade]`: Sets background color

#### Responsive Design Classes
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl">
```
This means:
- Mobile (default): text-4xl
- Medium screens (md:): text-5xl
- Large screens (lg:): text-6xl

## Managing Links

### Navigation Menu Links
Current navigation links are in the header:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Kenmerken</a>
    <a href="#benefits">Voordelen</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update a link:
1. Locate the `<a>` tag
2. Modify the `href` attribute
3. Update the text between the tags

Example:
```html
<a href="#new-section" class="text-gray-600 hover:text-pink-600">New Section</a>
```

### Call-to-Action Links
The main CTA button uses this structure:
```html
<a href="https://amzn.to/3RDsgJc" class="inline-flex items-center px-8 py-4 bg-pink-600">
    Bestel Nu Met Korting
</a>
```
Replace `https://amzn.to/3RDsgJc` with your desired URL.

## Adding Privacy and Terms Pages

### Footer Link Structure
Current privacy and terms links:
```html
<ul class="space-y-2">
    <li><a href="#" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white">Terms of Service</a></li>
</ul>
```

### Steps to Add Policy Pages
1. Create new files:
   - `privacy.html`
   - `terms.html`

2. Update the footer links:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Links**
   - Check that all `href` attributes start with either:
     - `#` for internal page sections
     - `http://` or `https://` for external links
     - Relative paths (`privacy.html`) for local pages

2. **Responsive Design Issues**
   - Ensure you maintain the responsive classes:
     - `md:` for medium screens
     - `lg:` for large screens
   - Don't remove these prefixes when updating classes

3. **Style Consistency**
   - Copy existing class combinations when adding new elements
   - For buttons, use:
   ```html
   class="inline-flex items-center px-8 py-4 bg-pink-600 text-white font-semibold rounded-lg"
   ```

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Validate your HTML at [W3C Validator](https://validator.w3.org/)
- Test responsive design using browser developer tools (F12)

Remember to always test your changes across different screen sizes and browsers before publishing updates.