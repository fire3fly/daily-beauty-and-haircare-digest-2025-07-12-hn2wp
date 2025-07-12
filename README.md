# Daily Beauty and Haircare Digest - Landing Page Maintenance Guide

This guide will help you maintain and customize the Daily Beauty and Haircare Digest landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common maintenance tasks.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the site title and navigation menu. To update:

1. **Site Title**
```html
<!-- Located in the header section -->
<h1 class="text-2xl font-bold text-gray-800">Beauty Digest</h1>
```
Simply replace "Beauty Digest" with your desired title.

2. **Navigation Menu Items**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Features</a>
    <!-- Additional menu items -->
</div>
```
Update both the desktop and mobile menu text by changing the text between `<a>` tags.

### Hero Section
The main banner section contains:
```html
<h2 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">Daily Beauty and Haircare Digest</h2>
<p class="text-xl md:text-2xl text-gray-600 mb-12">Your Daily Dose of Beauty – Where Science Meets Self-Care</p>
```
- To modify heading size: adjust the `text-4xl`, `text-5xl`, and `text-6xl` classes
- To change colors: replace `text-gray-900` with other Tailwind color classes (e.g., `text-blue-900`)

### Tailwind CSS Tips
- Font sizes use the pattern: `text-[size]` (xs, sm, base, lg, xl, 2xl, etc.)
- Colors use: `[property]-[color]-[shade]` (e.g., `bg-pink-600`)
- Spacing uses: `m-[number]` for margin, `p-[number]` for padding
- Responsive classes start with screen sizes: `sm:`, `md:`, `lg:`

## Managing Links

### Navigation Links
Current internal links are:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

To update:
1. Identify the section ID you want to link to
2. Add a matching ID to the target section:
```html
<section id="your-section-name">
```
3. Update the href attribute:
```html
<a href="#your-section-name">Your Link Text</a>
```

### External Links
The main call-to-action button links to:
```html
<a href="https://essenceofaj.com/" class="inline-block bg-pink-600...">
```
To update:
1. Replace the URL in `href=""`
2. Test the link after updating
3. Consider adding `target="_blank"` for external links

## Adding Privacy and Terms Pages

### Current Footer Links
```html
<div>
    <h4 class="text-xl font-bold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To link privacy and terms pages:

1. Create new HTML files:
   - `privacy.html`
   - `terms.html`

2. Update the footer links:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

3. Maintain consistent styling by copying these classes to new page links:
```html
class="text-gray-400 hover:text-white transition-colors duration-300"
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Check that section IDs match href attributes exactly
   - IDs are case-sensitive
   - Remove any spaces in IDs

2. **Responsive Design Issues**
   - Verify screen-specific classes (sm:, md:, lg:) are in correct order
   - Test on different devices or using browser dev tools
   - Check for missing responsive classes in parent containers

3. **Styling Problems**
   - Confirm Tailwind CSS CDN link is working
   - Check for typos in class names
   - Verify class order (Tailwind applies last applicable class)

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Verify HTML syntax using an [HTML validator](https://validator.w3.org/)
- Test responsiveness using browser developer tools (F12 in most browsers)

Remember to always test changes across different devices and browsers before deploying to production.