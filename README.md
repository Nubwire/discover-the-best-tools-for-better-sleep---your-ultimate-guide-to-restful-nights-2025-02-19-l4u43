# SleepGuide Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the SleepGuide landing page. Whether you're new to web development or need a quick reference, you'll find step-by-step guidance for common updates.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the logo and navigation menu:
```html
<div class="text-2xl font-bold text-blue-600">SleepGuide</div>
```
To update the logo text:
1. Locate this div in the header section
2. Replace "SleepGuide" with your desired text
3. Adjust size using Tailwind classes:
   - `text-xl` (smaller)
   - `text-2xl` (current size)
   - `text-3xl` (larger)

### Hero Section
The main headline and subheading are in the hero section:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6 leading-tight">
    Discover the Best Tools for Better Sleep
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-10">
    Your Guide to Better Sleep Tools & Tips
</p>
```
To modify:
1. Replace the text between the tags
2. Maintain the responsive sizing classes:
   - `text-4xl md:text-5xl lg:text-6xl` makes text responsive across devices
   - `md:` prefix applies styles to medium screens and up
   - `lg:` prefix applies styles to large screens and up

### Features Section
Each feature card follows this structure:
```html
<div class="bg-white rounded-xl shadow-lg p-8 hover:shadow-xl transition duration-300">
    <i class="fas fa-star text-blue-600 text-3xl mb-6"></i>
    <h3 class="text-xl font-semibold mb-4">Expert-Reviewed Products</h3>
    <p class="text-gray-600">Carefully curated sleep products vetted by sleep specialists.</p>
</div>
```
To update:
1. Change the icon by replacing `fa-star` with any [Font Awesome icon](https://fontawesome.com/icons)
2. Modify the heading text within the `<h3>` tags
3. Update the description within the `<p>` tags

## Managing Links

### Navigation Menu Links
Current navigation links are in the header:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-blue-600 transition duration-300">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-blue-600 transition duration-300">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-blue-600 transition duration-300">Contact</a>
</div>
```
To update:
1. Locate the `<a>` tag you want to modify
2. Change the `href` attribute:
   - Use `#section-id` for same-page links
   - Use full URLs for external links
   - Use relative paths for other pages (e.g., `/about.html`)

### Call-to-Action Links
The main CTA buttons use this format:
```html
<a href="https://www.sleepguide.com.au" class="inline-block bg-blue-600 text-white px-8 py-4 rounded-lg font-semibold hover:bg-blue-700 transform hover:scale-105 transition duration-300">
    Start Your Journey to Better Sleep
</a>
```
To update:
1. Replace the `href` URL with your destination link
2. Modify the button text between the tags
3. Keep the styling classes to maintain the button appearance

## Adding Privacy and Terms Pages

### Footer Legal Links
Current placeholder links in the footer:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition duration-300">Terms of Service</a></li>
    </ul>
</div>
```
To link to policy pages:
1. Create your privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Ensure section IDs match the href attributes
   - Section IDs should not contain spaces
   - Example: `<section id="features">` matches `href="#features"`

2. **Responsive Design Issues**
   - Check that you're maintaining the responsive classes:
     - `md:` for medium screens
     - `lg:` for large screens
   - Don't remove the `container` and `mx-auto` classes from section wrappers

3. **Icon Not Displaying**
   - Verify the Font Awesome CDN link is present in the head section
   - Check that icon class names are correct
   - Example: `fas fa-star` must use exact Font Awesome class names

4. **Styling Inconsistencies**
   - Keep the existing color classes (e.g., `text-blue-600`, `bg-gray-50`)
   - Maintain spacing classes (e.g., `mb-6`, `py-24`)
   - Use the same transition classes for interactive elements

Remember to always test your changes across different screen sizes using browser developer tools before deploying updates.