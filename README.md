# Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the WebLDN landing page. Follow these steps to make common updates while preserving the design integrity.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the logo and navigation menu. To update:

1. **Logo Text**
```html
<!-- Find this line in the header section -->
<a href="/" class="text-2xl font-bold text-gray-800">WebLDN</a>
```
- Replace "WebLDN" with your company name
- Adjust text size using `text-2xl` (options: `text-xl`, `text-3xl`, etc.)

### Hero Section
Located at the top of the page with the main headline:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">
    Best Websites In London
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Custom Websites For Your Business
</p>
```
- Update headline and subheadline text
- Responsive text sizes are defined with:
  - Mobile: `text-4xl`
  - Tablet: `md:text-5xl`
  - Desktop: `lg:text-6xl`

### Features Section
Each feature card follows this structure:
```html
<div class="bg-white p-8 rounded-2xl shadow-lg hover:shadow-xl transition-shadow duration-300">
    <h3 class="text-xl font-semibold text-gray-900 mb-4">Easy to Use</h3>
    <p class="text-gray-600 leading-relaxed">Your feature description here</p>
</div>
```
- Replace feature titles and descriptions
- Maintain consistent spacing with `mb-4` (margin-bottom)
- Keep text colors consistent using `text-gray-900` for headings and `text-gray-600` for body text

## Fixing Broken Links

### Navigation Menu Links
Current internal links in the navigation:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```
To update:
1. Internal links (same page):
   - Use `#section-id` format
   - Ensure section IDs match exactly
2. External links:
   - Replace `href="#"` with full URL
   - Example: `href="https://your-domain.com/page"`

### Call-to-Action Links
Current CTA buttons point to:
```html
<a href="https://sigmaseo.io" class="inline-block px-8 py-4 bg-blue-600...">
```
To update:
1. Replace `https://sigmaseo.io` with your desired URL
2. Test links after updating
3. Maintain button styling classes

## Linking Privacy and Terms Pages

### Footer Legal Links
Current placeholder links:
```html
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add privacy and terms pages:
1. Create new files:
   - `privacy.html`
   - `terms.html`
2. Update links in footer:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Layout**
- Check for missing closing tags
- Verify Tailwind CSS classes are spelled correctly
- Ensure responsive classes (`md:`, `lg:`) are properly ordered

2. **Non-Working Links**
- Verify file names match exactly (case-sensitive)
- Check for proper URL formatting
- Test all links after updates

3. **Inconsistent Styling**
- Copy existing class strings for new elements
- Maintain color scheme using provided gray/blue values
- Keep consistent spacing using provided margin/padding classes

### Need Help?
- Reference [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Check HTML validity using [W3C Validator](https://validator.w3.org/)
- Test responsive design using browser developer tools

Remember to:
- Back up files before making changes
- Test on multiple devices and browsers
- Maintain consistent spacing and formatting
- Keep brand colors and styling consistent throughout