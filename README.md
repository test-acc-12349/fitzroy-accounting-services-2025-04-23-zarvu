# Fitzroy Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Fitzroy Accounting Services landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions.

## 1. Updating Text and Tailwind CSS Classes

### Text Content Updates

#### Hero Section
```html
<!-- Located in the main hero section -->
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight tracking-tight mb-8">
    Proactive accounting for forward-thinking businesses
</h1>
```
To modify:
1. Locate the `<h1>` tag in the hero section
2. Replace the text between the opening and closing tags
3. Maintain the `<br class="hidden md:block"/>` if you want the line break on medium screens

#### Service Cards
Each service card follows this structure:
```html
<div class="bg-gray-900 p-8 rounded-2xl">
    <h3 class="text-xl font-semibold mb-4">Business Valuation</h3>
    <p class="text-gray-400">Comprehensive analysis and valuation...</p>
</div>
```
To update:
1. Find the service cards in the "Services Section"
2. Modify the `<h3>` text for titles
3. Update the `<p>` text for descriptions

### Tailwind CSS Classes Explained

#### Common Class Patterns
- Spacing: `p-8` (padding), `mb-4` (margin-bottom)
- Colors: `bg-gray-900` (background), `text-white` (text color)
- Responsive: `md:text-4xl` (applies at medium screens)
- Hover: `hover:bg-blue-700` (background color on hover)

#### Modifying Responsive Design
```html
<!-- Example of responsive classes -->
<div class="text-xl md:text-2xl lg:text-3xl">
```
Screen breakpoints:
- `sm:` - 640px and up
- `md:` - 768px and up
- `lg:` - 1024px and up

## 2. Fixing Broken Links

### Navigation Menu Links
Current structure:
```html
<div class="hidden md:flex space-x-8">
    <a href="#services">Services</a>
    <a href="#benefits">Benefits</a>
    <a href="#contact">Contact</a>
    <a href="https://theaccountants.com">Get Started</a>
</div>
```

To update:
1. Locate the navigation section in the header
2. Replace `https://theaccountants.com` with your actual URL
3. For internal links (#services, #benefits, #contact), ensure corresponding section IDs exist

### Footer Links
```html
<ul class="space-y-2 text-gray-400">
    <li><a href="#" class="hover:text-white transition-colors duration-300">About Us</a></li>
    <!-- More links -->
</ul>
```

To fix:
1. Replace `href="#"` with actual URLs
2. Example: `href="about.html"` or `href="https://yoursite.com/about"`
3. Test all links after updating

## 3. Linking Privacy and Terms Pages

### Adding Privacy Policy Link
```html
<!-- Locate this section in the footer -->
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2 text-gray-400">
        <li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To implement:
1. Create `privacy.html` and `terms.html` in your root directory
2. Update the href attributes with correct paths
3. Maintain consistent styling using the same classes

## Troubleshooting Tips

### Common Issues and Solutions

1. **Broken Internal Links**
   - Ensure section IDs match exactly (case-sensitive)
   - Example: `href="#Services"` won't link to `id="services"`

2. **Responsive Design Issues**
   - Check mobile view using browser dev tools
   - Verify all `md:` and `lg:` classes are working
   - Test at different screen sizes

3. **Animation Problems**
   - Verify AOS script is loaded
   - Check data-aos attributes in elements
   - Ensure AOS initialization code is present:
```html
<script>
    AOS.init({
        duration: 1000,
        once: true,
    });
</script>
```

## Best Practices

1. Always backup before making changes
2. Test changes in multiple browsers
3. Validate links after updating
4. Maintain consistent spacing and typography
5. Keep brand colors consistent (blue-600, gray-900, etc.)

For additional help or advanced customization, refer to:
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [AOS Documentation](https://michalsnik.github.io/aos/)