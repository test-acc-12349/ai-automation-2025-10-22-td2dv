# AI Automation Landing Page - Maintenance & Customization Guide

Welcome! This comprehensive guide will help you maintain and customize your AI Automation landing page. Whether you're updating text, fixing links, or adding new pages, you'll find step-by-step instructions tailored to your specific HTML structure.

---

## Table of Contents

1. [Getting Started](#getting-started)
2. [Updating Text Content](#updating-text-content)
3. [Modifying Tailwind CSS Classes](#modifying-tailwind-css-classes)
4. [Fixing Broken Links](#fixing-broken-links)
5. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
6. [Troubleshooting](#troubleshooting)
7. [Best Practices](#best-practices)

---

## Getting Started

### What You Need to Know

This landing page uses:
- **HTML**: The structure and content of the page
- **Tailwind CSS**: A utility-first framework for styling (colors, spacing, responsive design)
- **Font Awesome**: Icons throughout the page
- **JavaScript**: Interactive features like mobile menu and accordions

### How to Edit the File

1. **Open the file** in a text editor (VS Code, Notepad++, or even Notepad)
2. **Find the section** you want to edit using the section IDs and comments
3. **Make your changes** following the specific instructions below
4. **Save the file** (Ctrl+S or Cmd+S)
5. **Refresh your browser** to see the changes (F5 or Cmd+R)

### File Structure Overview

Your `index.html` contains these main sections:

```
Header/Navigation (sticky at top)
├── Logo & Brand Name
├── Navigation Menu
└── Mobile Hamburger Menu

Hero Section (large welcome area)
├── Headline
├── Subheading
└── Call-to-Action Buttons

Features Section (3-column layout)
├── Feature 1: n8n Integration
├── Feature 2: Low Cost
└── Feature 3: Fast Implementation

Benefits Section (additional value propositions)
├── 3 Main Benefits
└── 4 Additional Benefits

Call-to-Action Section (promotional banner)

FAQ Section (6 expandable questions)

Contact Section (contact form & information)

Footer (links & copyright)
```

---

## Updating Text Content

### 1. Changing the Brand Name

The brand name "AI Automation" appears in two locations:

**Location 1: Header Navigation**
```html
<span class="text-xl font-bold text-gray-900">AI Automation</span>
```

**Location 2: Footer**
```html
<span class="text-xl font-bold text-white">AI Automation</span>
```

**How to change it:**
1. Find the text `AI Automation` in the header (around line 93)
2. Replace it with your company name
3. Find the same text in the footer (around line 633)
4. Replace it there too
5. Save and refresh your browser

**Example:**
```html
<!-- Before -->
<span class="text-xl font-bold text-gray-900">AI Automation</span>

<!-- After -->
<span class="text-xl font-bold text-gray-900">Smart Process Solutions</span>
```

### 2. Updating the Hero Section Headline

The main headline is the first thing visitors see.

**Location:** Search for "AI Automation" inside the `<h1>` tag (around line 111)

```html
<h1 class="text-5xl md:text-6xl lg:text-7xl font-bold text-gray-900 leading-tight tracking-tight">
    <span class="gradient-text">AI Automation</span>
    <span class="block text-gray-900">For Professional Services</span>
</h1>
```

**How to change it:**
- The first `<span class="gradient-text">` contains the colored text
- The second `<span class="block">` contains the regular text below it
- Update both parts to match your messaging

**Example:**
```html
<h1 class="text-5xl md:text-6xl lg:text-7xl font-bold text-gray-900 leading-tight tracking-tight">
    <span class="gradient-text">Intelligent Process</span>
    <span class="block text-gray-900">Automation Solutions</span>
</h1>
```

### 3. Updating the Hero Section Subheading

**Location:** The paragraph below the headline (around line 120)

```html
<p class="text-xl md:text-2xl text-gray-600 max-w-3xl mx-auto leading-relaxed font-light">
    Transform your professional services with intelligent automation. Scale your operations without scaling your costs.
</p>
```

**How to change it:**
Simply replace the text between `<p>` and `</p>` tags with your new message.

**Example:**
```html
<p class="text-xl md:text-2xl text-gray-600 max-w-3xl mx-auto leading-relaxed font-light">
    Streamline your workflows and reduce manual work by up to 70% with our AI-powered automation platform.
</p>
```

### 4. Updating Feature Cards

The three feature cards are in the "Features Section" (around lines 165-200).

**Feature 1: n8n Integration**
```html
<h3 class="text-xl font-bold text-gray-900 mb-3">n8n Integration</h3>
<p class="text-gray-600 leading-relaxed">
    Connect and automate your entire workflow with n8n's powerful no-code automation platform. Seamless integration with hundreds of applications.
</p>
```

**How to change a feature card:**

1. Find the feature card you want to edit
2. Change the `<h3>` text (the title)
3. Change the `<p>` text (the description)
4. Optionally change the badge text at the bottom

**Example - Changing Feature 1:**
```html
<!-- Before -->
<h3 class="text-xl font-bold text-gray-900 mb-3">n8n Integration</h3>
<p class="text-gray-600 leading-relaxed">
    Connect and automate your entire workflow with n8n's powerful no-code automation platform...
</p>

<!-- After -->
<h3 class="text-xl font-bold text-gray-900 mb-3">Workflow Automation</h3>
<p class="text-gray-600 leading-relaxed">
    Connect all your business tools and automate repetitive tasks without writing any code...
</p>
```

### 5. Updating Benefit Cards

The benefits section has 3 main benefit cards (around lines 230-280).

**How to update a benefit card:**

```html
<h3 class="text-lg font-bold text-gray-900 mb-2">Remote Team Enabled</h3>
<p class="text-gray-600 leading-relaxed">
    Empower your distributed team with tools that work anywhere. Collaborate seamlessly across time zones and locations.
</p>
```

Simply replace the `<h3>` title and `<p>` description with your new content.

### 6. Updating FAQ Questions and Answers

Each FAQ item has a question and answer.

**Location:** Search for "FAQ Section" (around line 540)

**Structure of an FAQ item:**
```html
<button class="accordion-toggle w-full px-6 py-4 text-left flex items-center justify-between font-semibold text-gray-900 hover:bg-gray-50 smooth-transition" onclick="toggleAccordion(this)">
    <span>What is n8n and why do we use it?</span>
    <i class="fas fa-chevron-down text-purple-600 transition-transform duration-300"></i>
</button>
<div class="accordion-content">
    <div class="px-6 py-4 text-gray-600 leading-relaxed border-t border-gray-200">
        n8n is a powerful open-source workflow automation platform...
    </div>
</div>
```

**How to change an FAQ item:**

1. Find the question text in the `<span>` tag
2. Replace it with your new question
3. Find the answer text in the `<div class="px-6 py-4">` section
4. Replace it with your new answer

**Example:**
```html
<!-- Before -->
<span>What is n8n and why do we use it?</span>

<!-- After -->
<span>What platforms can you integrate with?</span>
```

### 7. Updating Contact Information

**Location:** Contact section (around line 595)

The contact section displays three contact methods:

```html
<!-- Email -->
<a href="mailto:admin@aia.com" class="text-purple-600 hover:text-purple-700 smooth-transition font-medium">
    admin@aia.com
</a>

<!-- Website -->
<a href="https://aia.com" class="text-blue-600 hover:text-blue-700 smooth-transition font-medium">
    aia.com
</a>
```

**How to change contact information:**

1. **Email:** Replace `admin@aia.com` with your email address in the `href="mailto:"` part
2. **Website:** Replace `https://aia.com` with your website URL

### 8. Updating Footer Text and Copyright

**Location:** Footer section (around line 650)

```html
<p class="text-sm text-gray-400">
    &copy; 2024 AI Automation. All rights reserved. Powered by Claude (Anthropic).
</p>
```

**How to change it:**
- Update the year (2024)
- Update the company name
- Update any additional text as needed

---

## Modifying Tailwind CSS Classes

### Understanding Tailwind CSS

Tailwind CSS uses utility classes to style elements. Instead of writing custom CSS, you add class names to HTML elements. Here's what you need to know:

**Common Tailwind Classes Used in Your Page:**

| Class | What It Does | Example |
|-------|-------------|---------|
| `text-xl` | Font size (extra large) | `<p class="text-xl">` |
| `text-gray-900` | Text color (dark gray) | `<p class="text-gray-900">` |
| `bg-white` | Background color (white) | `<div class="bg-white">` |
| `px-4` | Horizontal padding (left & right) | `<div class="px-4">` |
| `py-4` | Vertical padding (top & bottom) | `<div class="py-4">` |
| `rounded-lg` | Rounded corners | `<div class="rounded-lg">` |
| `mb-4` | Margin bottom (space below) | `<div class="mb-4">` |
| `flex` | Display as flexbox | `<div class="flex">` |
| `grid` | Display as grid | `<div class="grid">` |
| `hover:` | Style on hover | `<a class="hover:text-purple-600">` |
| `md:` | Medium screen and up | `<h1 class="md:text-6xl">` |
| `lg:` | Large screen and up | `<h1 class="lg:text-7xl">` |

### 1. Changing Text Colors

Text colors follow the pattern: `text-[color]-[shade]`

**Common color shades:** 50, 100, 200, 300, 400, 500, 600, 700, 800, 900

**Current colors in your page:**
- `text-gray-900` = Very dark gray
- `text-gray-600` = Medium gray
- `text-purple-600` = Purple
- `text-white` = White

**How to change text color:**

Find a text element and replace the color class:

```html
<!-- Before: Dark gray text -->
<p class="text-gray-900">Your text here</p>

<!-- After: Purple text -->
<p class="text-purple-900">Your text here</p>

<!-- After: Blue text -->
<p class="text-blue-600">Your text here</p>
```

**Available colors:** gray, red, orange, yellow, green, blue, indigo, purple, pink

### 2. Changing Background Colors

Background colors follow the pattern: `bg-[color]-[shade]`

**Current backgrounds in your page:**
- `bg-white` = White background
- `bg-gray-50` = Very light gray
- `bg-gradient-to-r` = Gradient background

**How to change background color:**

```html
<!-- Before: White background -->
<div class="bg-white">Content</div>

<!-- After: Light gray background -->
<div class="bg-gray-50">Content</div>

<!-- After: Purple background -->
<div class="bg-purple-100">Content</div>
```

### 3. Changing Font Sizes

Font sizes follow the pattern: `text-[size]`

**Available sizes in Tailwind:**
- `text-xs` = Extra small
- `text-sm` = Small
- `text-base` = Normal
- `text-lg` = Large
- `text-xl` = Extra large
- `text-2xl` = 2x large
- `text-3xl` = 3x large
- `text-4xl` = 4x large
- `text-5xl` = 5x large
- `text-6xl` = 6x large
- `text-7xl` = 7x large

**Current heading sizes in your page:**
```html
<!-- Hero section heading -->
<h1 class="text-5xl md:text-6xl lg:text-7xl">
```

This means:
- On mobile: `text-5xl` (5x large)
- On medium screens: `text-6xl` (6x large)
- On large screens: `text-7xl` (7x large)

**How to change heading size:**

```html
<!-- Before: Large heading -->
<h1 class="text-5xl md:text-6xl lg:text-7xl">AI Automation</h1>

<!-- After: Smaller heading -->
<h1 class="text-4xl md:text-5xl lg:text-6xl">AI Automation</h1>
```

### 4. Changing Spacing (Padding & Margins)

**Padding** (space inside an element):
- `px-4` = Horizontal padding (left & right)
- `py-4` = Vertical padding (top & bottom)
- `p-4` = Padding on all sides

**Margins** (space outside an element):
- `mx-4` = Horizontal margin (left & right)
- `my-4` = Vertical margin (top & bottom)
- `m-4` = Margin on all sides

**Spacing scale:** 1, 2, 3, 4, 6, 8, 10, 12, 16, 20, 24, 28, 32, etc.

**How to change spacing:**

```html
<!-- Before: Small padding -->
<div class="px-4 py-4">Content</div>

<!-- After: Larger padding -->
<div class="px-8 py-8">Content</div>

<!-- Before: Small margin bottom -->
<h2 class="mb-4">Heading</h2>

<!-- After: Larger margin bottom -->
<h2 class="mb-8">Heading</h2>
```

### 5. Changing Border Radius (Rounded Corners)

Border radius follows the pattern: `rounded-[size]`

**Available sizes:**
- `rounded` = Slightly rounded
- `rounded-lg` = Large rounded corners
- `rounded-xl` = Extra large rounded corners
- `rounded-2xl` = 2x extra large
- `rounded-full` = Completely round

**How to change border radius:**

```html
<!-- Before: Large rounded corners -->
<div class="rounded-xl">Content</div>

<!-- After: Slightly rounded -->
<div class="rounded-lg">Content</div>

<!-- After: Fully rounded -->
<div class="rounded-full">Content</div>
```

### 6. Changing Button Styles

Buttons in your page use gradient backgrounds:

```html
<a class="px-8 py-4 bg-gradient-to-r from-purple-600 to-blue-600 text-white font-semibold rounded-lg hover:shadow-lg smooth-transition hover-lift hover:from-purple-700 hover:to-blue-700">
    Get Started Now
</a>
```

**How to modify button styling:**

**Change button colors:**
```html
<!-- Before: Purple to blue gradient -->
<a class="bg-gradient-to-r from-purple-600 to-blue-600">

<!-- After: Green to teal gradient -->
<a class="bg-gradient-to-r from-green-600 to-teal-600">

<!-- After: Solid color (no gradient) -->
<a class="bg-purple-600">
```

**Change button size:**
```html
<!-- Before: Large padding -->
<a class="px-8 py-4">

<!-- After: Smaller padding -->
<a class="px-6 py-3">
```

### 7. Understanding Responsive Design (Mobile, Tablet, Desktop)

Your page uses breakpoints to look good on all screen sizes:

- **Mobile (default):** No prefix - styles apply to all screens
- **Medium screens (768px+):** `md:` prefix
- **Large screens (1024px+):** `lg:` prefix

**Example from your page:**
```html
<h1 class="text-5xl md:text-6xl lg:text-7xl">
```

This means:
- Mobile phones: `text-5xl`
- Tablets and up: `text-6xl`
- Desktops and up: `text-7xl`

**How to modify responsive behavior:**

```html
<!-- Before: Different sizes on different screens -->
<h1 class="text-5xl md:text-6xl lg:text-7xl">

<!-- After: Same size on all screens -->
<h1 class="text-6xl">

<!-- After: Smaller on mobile, larger on desktop -->
<h1 class="text-4xl md:text-5xl lg:text-6xl">
```

### 8. Changing Grid Layouts

Your features section uses a 3-column grid on desktop:

```html
<div class="grid grid-cols-1 md:grid-cols-3 gap-8 lg:gap-10">
```

This means:
- Mobile: 1 column (`grid-cols-1`)
- Medium screens: 3 columns (`md:grid-cols-3`)
- Large screens: Gap of 10 (`lg:gap-10`)

**How to change grid columns:**

```html
<!-- Before: 3 columns on desktop -->
<div class="grid grid-cols-1 md:grid-cols-3 gap-8">

<!-- After: 2 columns on desktop -->
<div class="grid grid-cols-1 md:grid-cols-2 gap-8">

<!-- After: 4 columns on desktop -->
<div class="grid grid-cols-1 md:grid-cols-4 gap-8">
```

### 9. Changing Gradient Colors

Your page uses gradients in several places:

```html
<!-- Gradient text -->
<span class="gradient-text">AI Automation</span>

<!-- Gradient button -->
<a class="bg-gradient-to-r from-purple-600 to-blue-600">

<!-- Gradient background -->
<div class="bg-gradient-to-br from-blue-50 via-white to-purple-50">
```

**How to change gradients:**

The gradient goes `from-[color]` to `to-[color]`

```html
<!-- Before: Purple to blue -->
<a class="bg-gradient-to-r from-purple-600 to-blue-600">

<!-- After: Green to teal -->
<a class="bg-gradient-to-r from-green-600 to-teal-600">

<!-- After: Orange to red -->
<a class="bg-gradient-to-r from-orange-600 to-red-600">
```

**Gradient directions:**
- `to-r` = Left to right
- `to-b` = Top to bottom
- `to-br` = Top-left to bottom-right
- `to-tr` = Bottom-left to top-right

---

## Fixing Broken Links

### Understanding Links in Your Page

Links appear in these locations:

1. **Navigation menu** (top of page)
2. **Call-to-action buttons** (hero section and CTA section)
3. **Footer links** (bottom of page)
4. **Contact information** (email and website)

### 1. Navigation Menu Links

**Location:** Around line 96-101

```html
<div class="nav-menu flex space-x-8" id="navMenu">
    <a href="#features" class="text-gray-700 hover:text-purple-600 smooth-transition font-medium">Features</a>
    <a href="#benefits" class="text-gray-700 hover:text-purple-600 smooth-transition font-medium">Benefits</a>
    <a href="#faq" class="text-gray-700 hover:text-purple-600 smooth-transition font-medium">FAQ</a>
    <a href="#contact" class="text-gray-700 hover:text-purple-600 smooth-transition font-medium">Contact</a>
</div>
```

**What these links do:**
- `href="#features"` = Scrolls to the Features section
- `href="#benefits"` = Scrolls to the Benefits section
- `href="#faq"` = Scrolls to the FAQ section
- `href="#contact"` = Scrolls to the Contact section

**These links are working correctly** if you have sections with matching IDs. Your page has:
- `<section id="features">` ✓
- `<section id="benefits">` ✓
- `<section id="faq">` ✓
- `<section id="contact">` ✓

### 2. Hero Section Buttons

**Location:** Around line 126-136

```html
<a href="https://aia.com" class="inline-flex items-center justify-center px-8 py-4 bg-gradient-to-r from-purple-600 to-blue-600 text-white font-semibold rounded-lg hover:shadow-lg smooth-transition hover-lift hover:from-purple-700 hover:to-blue-700 transform">
    Get Started Now
    <i class="fas fa-arrow-right ml-2"></i>
</a>
```

**This button links to:** `https://aia.com`

**How to change it:**
1. Replace `https://aia.com` with your actual website URL
2. Make sure to include `https://` at the beginning

**Example:**
```html
<!-- Before -->
<a href="https://aia.com">

<!-- After: If your domain is example.com -->
<a href="https://example.com">

<!-- After: If you want to link to a specific page -->
<a href="https://example.com/get-started">

<!-- After: If you want to open an email -->
<a href="mailto:sales@example.com">
```

### 3. CTA Section Buttons

**Location:** Around line 445-455

```html
<a href="https://aia.com" class="inline-flex items-center justify-center px-8 py-4 bg-white text-purple-600 font-semibold rounded-lg hover:shadow-lg smooth-transition hover-lift hover:bg-gray-50 transform">
    Start Free Trial
    <i class="fas fa-arrow-right ml-2"></i>
</a>
<a href="#contact" class="inline-flex items-center justify-center px-8 py-4 border-2 border-white text-white font-semibold rounded-lg hover:bg-white hover:text-purple-600 smooth-transition hover-lift">
    Schedule Demo
    <i class="fas fa-calendar ml-2"></i>
</a>
```

**These buttons link to:**
- First button: `https://aia.com` (external website)
- Second button: `#contact` (internal contact section)

**How to change them:**
- Update the first button to your actual website or signup page
- Keep the second button as `#contact` if you want it to scroll to the contact form

### 4. Footer Links

**Location:** Around line 650-680

The footer contains several sections with links:

**Product Links:**
```html
<li><a href="#features" class="text-gray-400 hover:text-white smooth-transition">Features</a></li>
<li><a href="#benefits" class="text-gray-400 hover:text-white smooth-transition">Benefits</a></li>
<li><a href="https://aia.com" class="text-gray-400 hover:text-white smooth-transition">Pricing</a></li>
<li><a href="https://aia.com" class="text-gray-400 hover:text-white smooth-transition">Blog</a></li>
```

**Company Links:**
```html
<li><a href="https://aia.com" class="text-gray-400 hover:text-white smooth-transition">About</a></li>
<li><a href="#contact" class="text-gray-400 hover:text-white smooth-transition">Contact</a></li>
<li><a href="https://aia.com" class="text-gray-400 hover:text-white smooth-transition">Careers</a></li>
<li><a href="https://aia.com" class="text-gray-400 hover:text-white smooth-transition">Partners</a></li>
```

**Legal Links:**
```html
<li><a href="https://aia.com" class="text-gray-400 hover:text-white smooth-transition">Privacy Policy</a></li>
<li><a href="https://aia.com" class="text-gray-400 hover:text-white smooth-transition">Terms of Service</a></li>
<li><a href="https://aia.com" class="text-gray-400 hover:text-white smooth-transition">Security</a></li>
<li><a href="https://aia.com" class="text-gray-400 hover:text-white smooth-transition">Compliance</a></li>
```

**How to update footer links:**

1. **Internal section links** (like Features, Benefits):
   - Keep as `#features`, `#benefits`, etc.
   - These scroll to sections on your page

2. **External website links** (like Pricing, Blog):
   - Replace `https://aia.com` with your actual URLs
   - Example: `https://example.com/pricing`

3. **Policy pages** (Privacy, Terms):
   - Replace with links to your policy pages
   - See the next section for detailed instructions

### 5. Contact Information Links

**Location:** Around line 595-610

```html
<!-- Email -->
<a href="mailto:admin@aia.com" class="text-purple-600 hover:text-purple-700 smooth-transition font-medium">
    admin@aia.com
</a>

<!-- Website -->
<a href="https://aia.com" class="text-blue-600 hover:text-blue-700 smooth-transition font-medium">
    aia.com
</a>
```

**How to change contact information:**

**For email:**
```html
<!-- Before -->
<a href="mailto:admin@aia.com">admin@aia.com</a>

<!-- After -->
<a href="mailto:sales@example.com">sales@example.com</a>
```

**For website:**
```html
<!-- Before -->
<a href="https://aia.com">aia.com</a>

<!-- After -->
<a href="https://example.com">example.com</a>
```

### 6. Social Media Links

**Location:** Around line 695-710

```html
<a href="https://twitter.com" aria-label="Twitter" class="text-gray-400 hover:text-white smooth-transition">
    <i class="fab fa-twitter text-lg"></i>
</a>
<a href="https://linkedin.com" aria-label="LinkedIn" class="text-gray-400 hover:text-white smooth-transition">
    <i class="fab fa-linkedin text-lg"></i>
</a>
<a href="https://github.com" aria-label="GitHub" class="text-gray-400 hover:text-white smooth-transition">
    <i class="fab fa-github text-lg"></i>
</a>
<a href="https://facebook.com" aria-label="Facebook" class="text-gray-400 hover:text-white smooth-transition">
    <i class="fab fa-facebook text-lg"></i>
</a>
```

**How to update social media links:**

Replace the generic social media URLs with your actual profiles:

```html
<!-- Before: Generic Twitter link -->
<a href="https://twitter.com">

<!-- After: Your Twitter profile -->
<a href="https://twitter.com/yourhandle">

<!-- Before: Generic LinkedIn link -->
<a href="https://linkedin.com">

<!-- After: Your LinkedIn profile -->
<a href="https://linkedin.com/company/yourcompany">

<!-- Before: Generic GitHub link -->
<a href="https://github.com">

<!-- After: Your GitHub profile -->
<a href="https://github.com/yourprofile">

<!-- Before: Generic Facebook link -->
<a href="https://facebook.com">

<!-- After: Your Facebook page -->
<a href="https://facebook.com/yourpage">
```

### 7. Quick Link Update Checklist

Go through your page and update these links:

- [ ] **Hero "Get Started Now" button** → Your signup/main page
- [ ] **CTA "Start Free Trial" button** → Your trial signup
- [ ] **Footer Pricing link** → Your pricing page
- [ ] **Footer Blog link** → Your blog
- [ ] **Footer About link** → Your about page
- [ ] **Footer Careers link** → Your careers page
- [ ] **Footer Partners link** → Your partners page
- [ ] **Contact email** → Your actual email
- [ ] **Contact website** → Your actual website
- [ ] **All social media links** → Your actual profiles

---

## Linking Privacy and Terms Pages

### Understanding the Structure

To add Privacy and Terms pages to your site, you'll need:

1. **Create new HTML files** for each page
2. **Add links** in your footer and navigation
3. **Ensure consistent styling** with the main page

### Step 1: Create the Privacy Policy Page

**Create a new file named `privacy.html`:**

1. In your file manager, create a new file
2. Name it exactly: `privacy.html`
3. Save it in the **same folder** as your `index.html`

**Copy this template into `privacy.html`:**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Privacy Policy - AI Automation">
    <meta name="author" content="AI Automation">
    <title>Privacy Policy - AI Automation</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap');
        
        * {
            font-family: 'Inter', sans-serif;
        }
    </style>
</head>
<body class="bg-white text-gray-900 antialiased">
    <!-- Header Navigation -->
    <header class="sticky top-0 z-40 bg-white border-b border-gray-100 shadow-sm">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex justify-between items-center">
            <div class="flex items-center space-x-2">
                <div class="w-10 h-10 bg-gradient-to-r from-purple-600 to-blue-600 rounded-lg flex items-center justify-center">
                    <i class="fas fa-brain text-white text-lg"></i>
                </div>
                <span class="text-xl font-bold text-gray-900">AI Automation</span>
            </div>
            
            <a href="index.html" class="text-gray-700 hover:text-purple-600 transition-colors font-medium">
                Back to Home
            </a>
        </nav>
    </header>

    <!-- Main Content -->
    <section class="py-20 md:py-28 bg-white">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-8">Privacy Policy</h1>
            
            <div class="prose prose-lg max-w-none text-gray-600 space-y-6">
                <p>
                    <strong>Last Updated:</strong> [INSERT DATE]
                </p>
                
                <h2 class="text-2xl font-bold text-gray-900 mt-8">1. Introduction</h2>
                <p>
                    AI Automation ("we," "us," "our," or "Company") is committed to protecting your privacy. This Privacy Policy explains how we collect, use, disclose, and safeguard your information when you visit our website and use our services.
                </p>
                
                <h2 class="text-2xl font-bold text-gray-900 mt-8">2. Information We Collect</h2>
                <p>
                    We collect information you voluntarily provide to us, such as when you contact us, fill out forms, or subscribe to our services. This may include:
                </p>
                <ul class="list-disc pl-6 space-y-2">
                    <li>Name and email address</li>
                    <li>Company information</li>
                    <li>Contact details</li>
                    <li>Any other information you choose to provide</li>
                </ul>
                
                <h2 class="text-2xl font-bold text-gray-900 mt-8">3. How We Use Your Information</h2>
                <p>
                    We use the information we collect to:
                </p>
                <ul class="list-disc pl-6 space-y-2">
                    <li>Provide and improve our services</li>
                    <li>Respond to your inquiries</li>
                    <li>Send marketing communications (with your consent)</li>
                    <li>Comply with legal obligations</li>
                </ul>
                
                <h2 class="text-2xl font-bold text-gray-900 mt-8">4. Data Security</h2>
                <p>
                    We implement appropriate technical and organizational measures to protect your personal data against unauthorized access, alteration, disclosure, or destruction. However, no method of transmission over the Internet is 100% secure.
                </p>
                
                <h2 class="text-2xl font-bold text-gray-900 mt-8">5. Contact Us</h2>
                <p>
                    If you have questions about this Privacy Policy, please contact us at:
                </p>
                <p>
                    Email: <a href="mailto:admin@aia.com" class="text-purple-600 hover:text-purple-700">admin@aia.com</a>
                </p>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-300 py-16 md:py-20">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="border-t border-gray-800 pt-8">
                <p class="text-sm text-gray-400">
                    &copy; 2024 AI Automation. All rights reserved.
                </p>
            </div>
        </div>
    </footer>
</body>
</html>
```

### Step 2: Create the Terms of Service Page

**Create a new file named `terms.html`:**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Terms of Service - AI Automation">
    <meta name="author" content="AI Automation">
    <title>Terms of Service - AI Automation</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap');
        
        * {
            font-family: 'Inter', sans-serif;
        }
    </style>
</head>
<body class="bg-white text-gray-900 antialiased">
    <!-- Header Navigation -->
    <header class="sticky top-0 z-40 bg-white border-b border-gray-100 shadow-sm">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex justify-between items-center">
            <div class="flex items-center space-x-2">
                <div class="w-10 h-10 bg-gradient-to-r from-purple-600 to-blue-600 rounded-lg flex items-center justify-center">
                    <i class="fas fa-brain text-white text-lg"></i>
                </div>
                <span class="text-xl font-bold text-gray-900">AI Automation</span>
            </div>
            
            <a href="index.html" class="text-gray-700 hover:text-purple-600 transition-colors font-medium">
                Back to Home
            </a>
        </nav>
    </header>

    <!-- Main Content -->
    <section class="py-20 md:py-28 bg-white">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-8">Terms of Service</h1>
            
            <div class="prose prose-lg max-w-none text-gray-600 space-y-6">
                <p>
                    <strong>Last Updated:</strong> [INSERT DATE]
                </p>
                
                <h2 class="text-2xl font-bold text-gray-900 mt-8">1. Agreement to Terms</h2>
                <p>
                    By accessing and using this website and our services, you accept and agree to be bound by the terms and provision of this agreement. If you do not agree to abide by the above, please do not use this service.
                </p>
                
                <h2 class="text-2xl font-bold text-gray-900 mt-8">2. Use License</h2>
                <p>
                    Permission is granted to temporarily download one copy of the materials (information or software) on AI Automation's website for personal, non-commercial transitory viewing only. This is the grant of a license, not a transfer of title, and under this license you may not:
                </p>
                <ul class="list-disc pl-6 space-y-2">
                    <li>Modify or copy the materials</li>
                    <li>Use the materials for any commercial purpose or for any public display</li>
                    <li>Attempt to decompile or reverse engineer any software contained on the website</li>
                    <li>Remove any copyright or other proprietary notations from the materials</li>
                    <li>Transfer the materials to another person or "mirror" the materials on any other server</li>
                </ul>
                
                <h2 class="text-2xl font-bold text-gray-900 mt-8">3. Disclaimer</h2>
                <p>
                    The materials on AI Automation's website are provided on an 'as is' basis. AI Automation makes no warranties, expressed or implied, and hereby disclaims and negates all other warranties including, without limitation, implied warranties or conditions of merchantability, fitness for a particular purpose, or non-infringement of intellectual property or other violation of rights.
                </p>
                
                <h2 class="text-2xl font-bold text-gray-900 mt-8">4. Limitations</h2>
                <p>
                    In no event shall AI Automation or its suppliers be liable for any damages (including, without limitation, damages for loss of data or profit, or due to business interruption) arising out of the use or inability to use the materials on AI Automation's website.
                </p>
                
                <h2 class="text-2xl font-bold text-gray-900 mt-8">5. Accuracy of Materials</h2>
                <p>
                    The materials appearing on AI Automation's website could include technical, typographical, or photographic errors. AI Automation does not warrant that any of the materials on its website are accurate, complete, or current. AI Automation may make changes to the materials contained on its website at any time without notice.
                </p>
                
                <h2 class="text-2xl font-bold text-gray-900 mt-8">6. Contact Information</h2>
                <p>
                    If you have any questions about these Terms of Service, please contact us at:
                </p>
                <p>
                    Email: <a href="mailto:admin@aia.com" class="text-purple-600 hover:text-purple-700">admin@aia.com</a>
                </p>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-300 py-16 md:py-20">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="border-t border-gray-800 pt-8">
                <p class="text-sm text-gray-400">
                    &copy; 2024 AI Automation. All rights reserved.
                </p>
            </div>
        </div>
    </footer>
</body>
</html>
```

### Step 3: Update Footer Links in index.html

Now you need to update your main `index.html` file to link to these new pages.

**Find the Legal Links section in the footer (around line 680):**

```html
<!-- Legal -->
<div>
    <h4 class="text-white font-semibold mb-4">Legal</h4>
    <ul class="space-y-3">
        <li><a href="https://aia.com" class="text-gray-400 hover:text-white smooth-transition">Privacy Policy</a></li>
        <li><a href="https://aia.com" class="text-gray-400 hover:text-white smooth-transition">Terms of Service</a></li>
        <li><a href="https://aia.com" class="text-gray-400 hover:text-white smooth-transition">Security</a></li>
        <li><a href="https://aia.com" class="text-gray-400 hover:text-white smooth-transition">Compliance</a></li>
    </ul>
</div>
```

**Replace it with:**

```html
<!-- Legal -->
<div>
    <h4 class="text-white font-semibold mb-4">Legal</h4>
    <ul class="space-y-3">
        <li><a href="privacy.html" class="text-gray-400 hover:text-white smooth-transition">Privacy Policy</a></li>
        <li><a href="terms.html" class="text-gray-400 hover:text-white smooth-transition">Terms of Service</a></li>
        <li><a href="https://aia.com" class="text-gray-400 hover:text-white smooth-transition">Security</a></li>
        <li><a href="https://aia.com" class="text-gray-400 hover:text-white smooth-transition">Compliance</a></li>
    </ul>
</div>
```

**What changed:**
- `href="https://aia.com"` → `href="privacy.html"` (for Privacy Policy)
- `href="https://aia.com"` → `href="terms.html"` (for Terms of Service)

### Step 4: Optional - Add Privacy and Terms Links to Navigation

If you want to add these links to your main navigation menu, find the navigation section (around line 96):

```html
<div class="nav-menu flex space-x-8" id="navMenu">
    <a href="#features" class="text-gray-700 hover:text-purple-600 smooth-transition font-medium">Features</a>
    <a href="#benefits" class="text-gray-700 hover:text-purple-600 smooth-transition font-medium">Benefits</a>
    <a href="#faq" class="text-gray-700 hover:text-purple-600 smooth-transition font-medium">FAQ</a>
    <a href="#contact" class="text-gray-700 hover:text-purple-600 smooth-transition font-medium">Contact</a>
</div>
```

**Add these lines at the end (before the closing `</div>`):**

```html
<a href="privacy.html" class="text-gray-700 hover:text-purple-600 smooth-transition font-medium">Privacy</a>
<a href="terms.html" class="text-gray-700 hover:text-purple-600 smooth-transition font-medium">Terms</a>
```

**Complete updated navigation:**

```html
<div class="nav-menu flex space-x-8" id="navMenu">
    <a href="#features" class="text-gray-700 hover:text-purple-600 smooth-transition font-medium">Features</a>
    <a href="#benefits" class="text-gray-700 hover:text-purple-600 smooth-transition font-medium">Benefits</a>
    <a href="#faq" class="text-gray-700 hover:text-purple-600 smooth-transition font-medium">FAQ</a>
    <a href="#contact" class="text-gray-700 hover:text-purple-600 smooth-transition font-medium">Contact</a>
    <a href="privacy.html" class="text-gray-700 hover:text-purple-600 smooth-transition font-medium">Privacy</a>
    <a href="terms.html" class="text-gray-700 hover:text-purple-600 smooth-transition font-medium">Terms</a>
</div>
```

### Step 5: Verify Your File Structure

Your folder should now look like this:

```
your-project-folder/
├── index.html          (your main landing page)
├── privacy.html        (new privacy policy page)
└── terms.html          (new terms of service page)
```

**Important:** All three files must be in the **same folder** for the links to work correctly.

### Step 6: Test Your Links

1. Open your `index.html` in a browser
2. Scroll to the footer
3. Click on "Privacy Policy" - it should open `privacy.html`
4. Click on "Terms of Service" - it should open `terms.html`
5. Click "Back to Home" on either policy page - it should return to `index.html`

### Customizing Your Policy Pages

The template policy pages are generic. You should customize them with your actual information:

**In `privacy.html`, update:**
- The "Last Updated" date
- Section 2: What specific data you collect
- Section 3: How you specifically use the data
- Section 4: Your specific security measures
- Section 5: Your actual contact email

**In `terms.html`, update:**
- The "Last Updated" date
- All sections with your specific terms
- Contact information

### Adding More Policy Pages (Optional)

You can create additional policy pages using the same template:

1. **Create `security.html`** for your Security page
2. **Create `compliance.html`** for your Compliance page
3. Update the footer links to point to these new files

**Example:**
```html
<li><a href="security.html" class="text-gray-400 hover:text-white smooth-transition">Security</a></li>
<li><a href="compliance.html" class="text-gray-400 hover:text-white smooth-transition">Compliance</a></li>
```

---

## Troubleshooting

### Issue: Changes Don't Appear After Saving

**Solution:**
1. Make sure you saved the file (Ctrl+S or Cmd+S)
2. Hard refresh your browser:
   - **Windows:** Press `Ctrl+Shift+R`
   - **Mac:** Press `Cmd+Shift+R`
3. Clear your browser cache and reload

### Issue: Links Don't Work

**Solution:**
1. Check that the URL is correct
   - External links should start with `https://`
   - Internal links should start with `#` (for same page) or the filename
2. Verify the section ID exists for internal links
   - Example: `href="#features"` requires `<section id="features">`
3. For file links, ensure files are in the same folder
   - Example: `href="privacy.html"` works only if `privacy.html` is in the same folder as `index.html`

### Issue: Text Formatting Looks Wrong

**Solution:**
1. Check that you didn't accidentally delete any closing tags (`</p>`, `</div>`, etc.)
2. Verify you're editing text only, not the HTML structure
3. Look for unclosed quotes in class names

**Example of what NOT to do:**
```html
<!-- Wrong: Missing closing tag -->
<p class="text-gray-600">Your text here

<!-- Wrong: Broken class name -->
<p class="text-gray-600"">Your text here</p>

<!-- Correct -->
<p class="text-gray-600">Your text here</p>
```

### Issue: Mobile Menu Not Working

**Solution:**
1. Check that the hamburger menu JavaScript is intact
2. Verify you didn't accidentally delete the `<script>` section at the bottom
3. Clear your browser cache and reload

### Issue: Buttons Look Different Than Expected

**Solution:**
1. Verify you didn't accidentally change the class names
2. Check that gradient colors are spelled correctly
3. Ensure you didn't delete any important classes like `smooth-transition` or `hover-lift`

### Issue: Page Layout Breaks on Mobile

**Solution:**
1. Check that responsive classes are intact (like `md:`, `lg:`)
2. Verify you didn't remove important flex or grid classes
3. Test on different screen sizes to identify the issue

**To test on mobile:**
- Open your browser's Developer Tools (F12)
- Click the mobile device icon (usually top-left)
- Try different screen sizes

### Issue: Colors Don't Match What I Expected

**Solution:**
1. Verify the color name is spelled correctly
   - Available colors: gray, red, orange, yellow, green, blue, indigo, purple, pink
2. Check the shade number (50, 100, 200, 300, 400, 500, 600, 700, 800, 900)
3. Remember that lighter numbers = lighter colors
   - `text-gray-100` = light gray
   - `text-gray-900` = dark gray

### Issue: Form Doesn't Submit

**Solution:**
1. The contact form is set up to show a success message locally
2. To make it actually send emails, you'll need a backend service
3. For now, the form shows a confirmation message when submitted
4. To integrate real email functionality, consider services like:
   - Formspree (formspree.io)
   - Netlify Forms (netlify.com)
   - EmailJS (emailjs.com)

---

## Best Practices

### 1. Always Back Up Your Files

Before making major changes:
1. Make a copy of your `index.html` file
2. Name it something like `index-backup.html`
3. Keep it in the same folder as a safety net

### 2. Make Changes Incrementally

- Change one thing at a time
- Test it in your browser
- If something breaks, you'll know exactly what caused it

### 3. Use Consistent Formatting

- Keep your HTML indentation consistent
- This makes it easier to find and fix errors
- Most text editors have an "Auto Format" option (usually Ctrl+Shift+F)

### 4. Test on Multiple Devices

Always check your page on:
- Desktop (large screen)
- Tablet (medium screen)
- Mobile phone (small screen)

Use your browser's Developer Tools to test different screen sizes.

### 5. Keep Your Links Updated

Regularly check that:
- All external links are working
- Email addresses are current
- Social media profiles are correct
- Policy pages are up to date

### 6. Use Descriptive Link Text

Instead of:
```html
<a href="https://example.com">Click here</a>
```

Use:
```html
<a href="https://example.com">View our pricing plans</a>
```

This is better for accessibility and SEO.

### 7. Don't Modify the JavaScript (Unless You Know What You're Doing)

The JavaScript code at the bottom handles:
- Mobile menu toggle
- Accordion animations
- Form submission
- Smooth scrolling

Leave it alone unless you need to add new functionality.

### 8. Keep Your Color Scheme Consistent

Your page uses:
- **Primary:** Purple (`purple-600`)
- **Secondary:** Blue (`blue-600`)
- **Accent:** Green (`green-600`)

Try to stick with these colors to maintain a cohesive design.

### 9. Update Meta Tags for SEO

In the `<head>` section, update:
```html
<meta name="description" content="YOUR DESCRIPTION HERE">
<meta name="keywords" content="YOUR KEYWORDS HERE">
<meta property="og:title" content="YOUR TITLE HERE">
<meta property="og:description" content="YOUR DESCRIPTION HERE">
<meta property="og:url" content="YOUR WEBSITE URL HERE">
```

These help with search engine optimization and social media sharing.

### 10. Test Your Changes Frequently

After any change:
1. Save the file
2. Refresh your browser
3. Check that everything looks correct
4. Test any interactive elements (buttons, links, forms)

### 11. Keep File Names Simple

Use lowercase, no spaces:
- ✓ `privacy.html`
- ✓ `terms-of-service.html`
- ✗ `Privacy Policy.html`
- ✗ `PRIVACY.HTML`

### 12. Document Your Changes

Keep a simple log of what you've changed:
```
Date: 2024-01-15
Changed: Hero headline text
From: "AI Automation For Professional Services"
To: "Smart Automation Solutions"

Date: 2024-01-15
Updated: Footer email address
From: admin@aia.com
To: sales@example.com
```

This helps if you need to revert changes later.

---

## Common Customization Examples

### Example 1: Change Brand Colors from Purple/Blue to Green/Teal

**Find and replace:**
- `from-purple-600` → `from-green-600`
- `to-blue-600` → `to-teal-600`
- `hover:from-purple-700` → `hover:from-green-700`
- `hover:to-blue-700` → `hover:to-teal-700`
- `text-purple-600` → `text-green-600`
- `bg-purple-100` → `bg-green-100`

### Example 2: Change Feature Card Icons

**Find the feature card icon section:**
```html
<i class="fas fa-link text-white text-2xl"></i>
```

**Replace with different icons:**
- `fa-link` → `fa-cogs` (gears)
- `fa-link` → `fa-plug` (plug)
- `fa-link` → `fa-network-wired` (network)

[Browse Font Awesome icons](https://fontawesome.com/icons)

### Example 3: Add a New Feature Card

**Find the features section (around line 165) and add:**

```html
<!-- Feature 4: Your New Feature -->
<div class="feature-card bg-white border border-gray-200 rounded-xl p-8 hover:shadow-xl smooth-transition hover-lift">
    <div class="feature-card-content">
        <div class="w-14 h-14 bg-gradient-to-br from-pink-400 to-red-500 rounded-lg flex items-center justify-center mb-6">
            <i class="fas fa-star text-white text-2xl"></i>
        </div>
        <h3 class="text-xl font-bold text-gray-900 mb-3">Your Feature Title</h3>
        <p class="text-gray-600 leading-relaxed">
            Your feature description goes here. Explain the benefits and what makes this feature special.
        </p>
        <div class="mt-6 pt-6 border-t border-gray-200">
            <span class="text-sm font-semibold text-pink-600">Your Badge Text</span>
        </div>
    </div>
</div>
```

### Example 4: Change Button Text

**Find a button:**
```html
<a href="https://aia.com" class="inline-flex items-center justify-center px-8 py-4 bg-gradient-to-r from-purple-600 to-blue-600 text-white font-semibold rounded-lg hover:shadow-lg smooth-transition hover-lift hover:from-purple-700 hover:to-blue-700 transform">
    Get Started Now
    <i class="fas fa-arrow-right ml-2"></i>
</a>
```

**Change the text:**
```html
    Get Started Now  →  Start Your Free Trial
```

### Example 5: Add a New FAQ Item

**Find the FAQ section (around line 540) and add before the closing `</div>`:**

```html
<!-- FAQ Item 7 -->
<div class="accordion-item bg-white border border-gray-200 rounded-lg overflow-hidden hover:shadow-md smooth-transition">
    <button class="accordion-toggle w-full px-6 py-4 text-left flex items-center justify-between font-semibold text-gray-900 hover:bg-gray-50 smooth-transition" onclick="toggleAccordion(this)">
        <span>Your Question Here?</span>
        <i class="fas fa-chevron-down text-purple-600 transition-transform duration-300"></i>
    </button>
    <div class="accordion-content">
        <div class="px-6 py-4 text-gray-600 leading-relaxed border-t border-gray-200">
            Your answer goes here. Provide a clear, helpful response to the question.
        </div>
    </div>
</div>
```

---

## Final Checklist Before Publishing

- [ ] All text is updated and accurate
- [ ] All links are working (test each one)
- [ ] Email address is correct
- [ ] Website URL is correct
- [ ] Social media links are correct
- [ ] Page looks good on mobile
- [ ] Page looks good on tablet
- [ ] Page looks good on desktop
- [ ] All buttons are working
- [ ] Contact form is working
- [ ] FAQ accordions are opening/closing
- [ ] Mobile menu is working
- [ ] Privacy and Terms pages are linked
- [ ] Meta tags are updated
- [ ] No broken images or icons
- [ ] Font sizes are readable
- [ ] Colors are consistent
- [ ] Spelling and grammar are correct

---

## Need More Help?

### Resources

- **Tailwind CSS Documentation:** https://tailwindcss.com/docs
- **Font Awesome Icons:** https://fontawesome.com/icons
- **HTML Guide:** https://developer.mozilla.org/en-US/docs/Web/HTML
- **CSS Guide:** https://developer.mozilla.org/en-US/docs/Web/CSS

### Getting Support

If you need help:
1. Check the Troubleshooting section above
2. Review the specific section of this guide
3. Test your changes in a browser's Developer Tools (F12)
4. Compare your code with the examples provided

---

## Summary

You now have the knowledge to:

✓ Update any text on your landing page
✓ Modify colors and styling with Tailwind CSS
✓ Fix broken links and update URLs
✓ Create and link privacy and terms pages
✓ Troubleshoot common issues
✓ Follow best practices for web maintenance

**Remember:** Save frequently, test often, and keep backups of your files!

Good luck with your AI Automation landing page! 🚀