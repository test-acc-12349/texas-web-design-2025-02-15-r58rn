# Texas Web Design Landing Page - Maintenance Guide

This guide will help you maintain and customize the Texas Web Design landing page. It's written for beginners with no prior coding experience.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains your logo and navigation menu. To update:

1. Change the logo text:
```html
<!-- Find this line in the header -->
<a href="/" class="text-2xl font-bold text-blue-600">TWD</a>
```
Simply replace "TWD" with your desired text.

### Hero Section
The main headline and subheading can be modified here:
```html
<h1 class="text-4xl md:text-6xl font-bold text-gray-900 mb-6">Texas Web Design</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">Best Websites In Texas</p>
```

Common Tailwind CSS classes used:
- `text-4xl`: Large text size
- `md:text-6xl`: Larger text on medium screens
- `mb-6`: Margin bottom spacing
- `text-gray-900`: Dark gray text color

### Features Section
To update feature cards:
```html
<div class="bg-white p-8 rounded-2xl shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="text-blue-600 mb-4">
        <i class="fas fa-server text-4xl"></i>
    </div>
    <h3 class="text-xl font-bold mb-4">Free Hosting</h3>
    <p class="text-gray-600">Premium hosting included with every website package at no additional cost.</p>
</div>
```

To modify:
1. Change the icon by updating the `fa-server` class
2. Update the heading text inside `<h3>`
3. Modify the description text inside `<p>`

## Fixing Broken Links

### Navigation Menu Links
Current navigation links are:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Features</a>
    <a href="#video" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Video</a>
    <a href="#faq" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Contact</a>
</div>
```

To update:
1. Locate the `href` attribute
2. Replace the value with your new link
   - For internal sections, use `#section-name`
   - For external links, use the full URL: `https://example.com`

### Call-to-Action Links
Update the "Get Started" button links:
```html
<a href="https://twd.com" class="inline-block bg-blue-600 text-white px-8 py-4 rounded-full">Start Your Project</a>
```
Replace `https://twd.com` with your actual URL.

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links to the Quick Links section:
```html
<div>
    <h4 class="text-white text-lg font-bold mb-4">Quick Links</h4>
    <ul class="space-y-2">
        <!-- Add these new lines -->
        <li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Creating Policy Pages
1. Create two new files: `privacy.html` and `terms.html`
2. Copy the header and footer from `index.html`
3. Add your policy content between them
4. Maintain consistent styling using the same Tailwind classes

## Troubleshooting

Common issues and solutions:

1. **Broken Internal Links**
   - Ensure section IDs match href values
   - Check for typos in IDs
   - IDs are case-sensitive

2. **Responsive Design Issues**
   - Check `md:` prefixed classes for medium screen styles
   - Verify the mobile menu is working
   - Test on different screen sizes

3. **Icon Not Showing**
   - Confirm Font Awesome is properly loaded
   - Check icon class names against Font Awesome documentation
   - Ensure internet connectivity for CDN access

4. **Styling Problems**
   - Tailwind classes must be spelled exactly right
   - Multiple classes should be space-separated
   - Check for conflicting classes

For additional help, consult the [Tailwind CSS documentation](https://tailwindcss.com/docs) or reach out to your development team.