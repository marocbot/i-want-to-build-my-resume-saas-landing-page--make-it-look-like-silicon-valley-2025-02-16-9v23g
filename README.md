# Landing Page Maintenance Guide

This guide will help you maintain and customize the ResumePro landing page. It's written for beginners with no prior coding experience.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your logo and navigation menu. To update:

```html
<!-- Find this section at the top of the page -->
<a href="#" class="text-2xl font-bold text-gray-800">ResumePro</a>
```

To change the logo text:
1. Locate this line in the header section
2. Replace "ResumePro" with your desired text
3. Adjust size using `text-2xl` (options: `text-sm`, `text-lg`, `text-3xl`)

### Hero Section
The main banner section contains your primary headline:

```html
<h1 class="text-4xl md:text-6xl font-bold mb-6 leading-tight">
    Build Your Resume Like a Silicon Valley Pro
</h1>
```

To modify:
1. Find this section (usually after the header)
2. Change the text between the `<h1>` tags
3. Maintain the existing classes for responsive design
   - `text-4xl`: Size on mobile
   - `md:text-6xl`: Size on desktop
   - `mb-6`: Bottom margin spacing

### Features Section
Each feature card follows this structure:

```html
<div class="bg-white rounded-xl shadow-lg p-8">
    <div class="w-16 h-16 bg-blue-100 rounded-full">
        <i class="fas fa-magic text-2xl text-blue-600"></i>
    </div>
    <h3 class="text-xl font-semibold mb-4">Background Cleaner</h3>
    <p class="text-gray-600">Remove backgrounds instantly...</p>
</div>
```

To update features:
1. Locate the features section (search for `id="features"`)
2. Change icon: Replace `fa-magic` with any [Font Awesome icon](https://fontawesome.com/icons)
3. Update heading: Modify text in `<h3>` tags
4. Update description: Change text in `<p>` tags

## Managing Links

### Navigation Menu Links
Current navigation links are:

```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-gray-900">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-gray-900">FAQ</a>
    <a href="https://buy.stripe.com/6oE17Y2hFard6Pu5kk" class="bg-blue-600 text-white">Buy Now</a>
</div>
```

To update:
1. Find the navigation section in the header
2. Internal links (starting with #) point to page sections
3. External links (starting with http) go to other websites
4. Replace `href` values with your desired URLs

### Call-to-Action (CTA) Links
The "Buy Now" buttons appear throughout the page:

```html
<a href="https://buy.stripe.com/6oE17Y2hFard6Pu5kk" 
   class="inline-block bg-blue-600 text-white px-8 py-4 rounded-full">
    Get Started Now
</a>
```

To update all CTAs:
1. Use your text editor's find feature (usually Ctrl+F)
2. Search for "stripe.com"
3. Replace all instances with your payment or signup URL
4. Update button text between `<a>` tags as needed

## Adding Privacy and Terms Pages

### Footer Link Setup
Locate the footer's legal section:

```html
<div>
    <h3 class="text-white text-lg font-semibold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white">Terms of Service</a></li>
    </ul>
</div>
```

To add policy pages:
1. Create new files:
   - `privacy.html`
   - `terms.html`
2. Update the links in footer:
```html
<li><a href="privacy.html" class="hover:text-white">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white">Terms of Service</a></li>
```

## Troubleshooting

Common issues and solutions:

1. **Broken Layout**
   - Check for missing closing tags (`</div>`, `</section>`)
   - Verify Tailwind CSS classes are spelled correctly
   - Ensure responsive classes (md:, lg:) remain intact

2. **Missing Icons**
   - Verify Font Awesome link in `<head>` section exists
   - Check icon class names against Font Awesome website
   - Ensure `fas`, `fab`, or `far` prefix is correct

3. **Links Not Working**
   - Internal links (#features) must match section IDs exactly
   - External links need complete URLs (https://...)
   - Check for typos in href attributes

Remember:
- Always backup before making changes
- Test on multiple devices and browsers
- Maintain the responsive design classes
- Keep the original structure intact

Need more help? Contact: technik.adisam@gmail.com