# AI Website Builder Landing Page - Maintenance Guide

This guide will help you maintain and customize the AI Website Builder landing page. Whether you're new to web development or just getting started, follow these instructions to make updates while preserving the design integrity.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the logo and navigation menu. To modify:

1. Update the logo text:
```html
<!-- Find this section near the top -->
<div class="text-2xl font-bold bg-gradient-to-r from-purple-600 to-blue-500 bg-clip-text text-transparent">
    AI Builder  <!-- Change this text -->
</div>
```

2. Modify navigation menu items:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Features</a>
    <!-- Add or modify menu items here -->
</div>
```

### Hero Section
Located at the top of the page:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-6 bg-gradient-to-r from-purple-600 to-blue-600 bg-clip-text text-transparent">
    Build Your Website in Minutes, Not Days  <!-- Update main headline here -->
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-10">
    Best AI Website Builder, No Code Required  <!-- Update subheadline here -->
</p>
```

### Tailwind CSS Classes Explained
Common classes used throughout:
- `text-[size]`: Controls text size (e.g., `text-xl`, `text-2xl`)
- `font-[weight]`: Controls text weight (e.g., `font-bold`, `font-semibold`)
- `mb-[size]`: Adds margin bottom (e.g., `mb-6`, `mb-10`)
- `py-[size]`: Adds padding top and bottom (e.g., `py-24`)
- `bg-[color]`: Sets background color (e.g., `bg-white`, `bg-gray-50`)

## Managing Links

### Navigation Menu Links
The page uses anchor links to scroll to sections:

1. Find the navigation menu:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
</div>
```

2. To update links:
- Internal sections: Use `#section-id`
- External pages: Use full URL (e.g., `https://example.com`)

### Call-to-Action Buttons
Update the "Get Started" buttons:

```html
<!-- Replace yourwebsitesite.com with your actual URL -->
<a href="https://yourwebsitesite.com" class="inline-flex items-center justify-center px-8 py-4...">
    Start Building Free
</a>
```

## Adding Privacy and Terms Pages

### Step 1: Locate Footer Links
Find the legal section in the footer:

```html
<div>
    <h4 class="text-white text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Step 2: Update Link Paths
Replace the `#` with proper file paths:

```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

### Step 3: Create Policy Pages
1. Create new files:
   - `privacy.html`
   - `terms.html`
2. Use the same header and footer as `index.html`
3. Maintain consistent styling using Tailwind classes

## Troubleshooting

### Common Issues and Solutions

1. **Broken Links**
   - Check for typos in `href` attributes
   - Ensure file names match exactly
   - Verify file locations in your directory

2. **Styling Problems**
   - Make sure Tailwind CDN is loading properly
   - Check for missing closing tags
   - Verify class names are spelled correctly

3. **Responsive Design Issues**
   - Test on different screen sizes
   - Look for `md:` and `lg:` prefixes in classes
   - Don't remove responsive classes unless you're sure

### Need Help?
- Check the Tailwind CSS documentation
- Verify all HTML tags are properly closed
- Use browser developer tools to inspect elements
- Maintain the existing class structure when making changes

Remember to always test your changes across different devices and browsers before publishing updates to your live site.