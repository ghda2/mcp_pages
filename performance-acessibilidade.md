# ⚡ PERFORMANCE E OTIMIZAÇÃO AVANÇADA

## 🚀 CHECKLIST DE PERFORMANCE COMPLETO

### 📊 Core Web Vitals Optimization

```html
<!-- Performance Monitoring Script -->
<script>
class PerformanceMonitor {
    constructor() {
        this.metrics = {};
        this.init();
    }
    
    init() {
        this.measureLCP();
        this.measureFID();
        this.measureCLS();
        this.measureTTFB();
        this.measureFCP();
    }
    
    // Largest Contentful Paint
    measureLCP() {
        new PerformanceObserver((entryList) => {
            const entries = entryList.getEntries();
            const lastEntry = entries[entries.length - 1];
            this.metrics.lcp = lastEntry.startTime;
            this.reportMetric('LCP', lastEntry.startTime);
        }).observe({ entryTypes: ['largest-contentful-paint'] });
    }
    
    // First Input Delay
    measureFID() {
        new PerformanceObserver((entryList) => {
            for (const entry of entryList.getEntries()) {
                this.metrics.fid = entry.processingStart - entry.startTime;
                this.reportMetric('FID', this.metrics.fid);
            }
        }).observe({ entryTypes: ['first-input'] });
    }
    
    // Cumulative Layout Shift
    measureCLS() {
        let clsValue = 0;
        new PerformanceObserver((entryList) => {
            for (const entry of entryList.getEntries()) {
                if (!entry.hadRecentInput) {
                    clsValue += entry.value;
                }
            }
            this.metrics.cls = clsValue;
            this.reportMetric('CLS', clsValue);
        }).observe({ entryTypes: ['layout-shift'] });
    }
    
    // Time to First Byte
    measureTTFB() {
        const navigation = performance.getEntriesByType('navigation')[0];
        this.metrics.ttfb = navigation.responseStart - navigation.requestStart;
        this.reportMetric('TTFB', this.metrics.ttfb);
    }
    
    // First Contentful Paint
    measureFCP() {
        new PerformanceObserver((entryList) => {
            for (const entry of entryList.getEntries()) {
                if (entry.name === 'first-contentful-paint') {
                    this.metrics.fcp = entry.startTime;
                    this.reportMetric('FCP', entry.startTime);
                }
            }
        }).observe({ entryTypes: ['paint'] });
    }
    
    reportMetric(name, value) {
        // Send to analytics or display in development
        if (this.isDevelopment()) {
            console.log(`${name}: ${value.toFixed(2)}ms`);
            this.updateDevPanel(name, value);
        }
        
        // Send to analytics service
        if (typeof gtag !== 'undefined') {
            gtag('event', 'web_vitals', {
                event_category: 'Performance',
                event_label: name,
                value: Math.round(value),
                non_interaction: true
            });
        }
    }
    
    isDevelopment() {
        return window.location.hostname === 'localhost' || 
               window.location.hostname === '127.0.0.1';
    }
    
    updateDevPanel(metric, value) {
        if (!document.getElementById('perf-panel')) {
            this.createDevPanel();
        }
        
        const panel = document.getElementById('perf-panel');
        const metricElement = panel.querySelector(`[data-metric="${metric}"]`);
        
        if (metricElement) {
            metricElement.textContent = `${metric}: ${value.toFixed(2)}ms`;
            
            // Color code based on thresholds
            const thresholds = {
                LCP: { good: 2500, poor: 4000 },
                FID: { good: 100, poor: 300 },
                CLS: { good: 0.1, poor: 0.25 },
                TTFB: { good: 200, poor: 500 },
                FCP: { good: 1800, poor: 3000 }
            };
            
            const threshold = thresholds[metric];
            if (threshold) {
                if (value <= threshold.good) {
                    metricElement.className = 'text-green-600 font-semibold';
                } else if (value <= threshold.poor) {
                    metricElement.className = 'text-yellow-600 font-semibold';
                } else {
                    metricElement.className = 'text-red-600 font-semibold';
                }
            }
        }
    }
    
    createDevPanel() {
        const panel = document.createElement('div');
        panel.id = 'perf-panel';
        panel.className = 'fixed bottom-4 right-4 bg-black/80 text-white p-4 rounded-lg text-sm z-50';
        panel.innerHTML = `
            <h4 class="font-bold mb-2">Performance Metrics</h4>
            <div data-metric="LCP">LCP: Loading...</div>
            <div data-metric="FID">FID: Loading...</div>
            <div data-metric="CLS">CLS: Loading...</div>
            <div data-metric="TTFB">TTFB: Loading...</div>
            <div data-metric="FCP">FCP: Loading...</div>
            <button onclick="this.parentElement.remove()" class="mt-2 text-xs text-gray-400 hover:text-white">× Close</button>
        `;
        document.body.appendChild(panel);
    }
    
    generateReport() {
        return {
            timestamp: new Date().toISOString(),
            url: window.location.href,
            metrics: this.metrics,
            userAgent: navigator.userAgent,
            connection: navigator.connection?.effectiveType || 'unknown'
        };
    }
}

// Initialize performance monitoring
new PerformanceMonitor();
</script>
```

### 🖼️ Image Optimization System

```html
<!-- Advanced Image Optimization -->
<script>
class ImageOptimizer {
    constructor() {
        this.webpSupported = this.checkWebPSupport();
        this.avifSupported = this.checkAVIFSupport();
        this.init();
    }
    
    init() {
        this.optimizeImages();
        this.setupLazyLoading();
        this.setupResponsiveImages();
    }
    
    checkWebPSupport() {
        const canvas = document.createElement('canvas');
        canvas.width = 1;
        canvas.height = 1;
        return canvas.toDataURL('image/webp').indexOf('data:image/webp') === 0;
    }
    
    checkAVIFSupport() {
        return new Promise((resolve) => {
            const avif = new Image();
            avif.onload = avif.onerror = () => resolve(avif.height === 2);
            avif.src = 'data:image/avif;base64,AAAAIGZ0eXBhdmlmAAAAAGF2aWZtaWYxbWlhZk1BMUIAAADybWV0YQAAAAAAAAAoaGRscgAAAAAAAAAAcGljdAAAAAAAAAAAAAAAAGxpYmF2aWYAAAAADnBpdG0AAAAAAAEAAAAeaWxvYwAAAABEAAABAAEAAAABAAABGgAAAB0AAAAoaWluZgAAAAAAAQAAABppbmZlAgAAAAABAABhdjAxQ29sb3IAAAAAamlwcnAAAABLaXBjbwAAABRpc3BlAAAAAAAAAAIAAAACAAAAEHBpeGkAAAAAAwgICAAAAAxhdjFDgQ0MAAAAABNjb2xybmNseAACAAIAAYAAAAAXaXBtYQAAAAAAAAABAAEEAQKDBAAAACVtZGF0EgAKCBgABogQEAwgMg8f8D///8WfhwB8+ErK42A=';
        });
    }
    
    optimizeImages() {
        const images = document.querySelectorAll('img[data-src]');
        
        images.forEach(img => {
            this.loadOptimalFormat(img);
        });
    }
    
    loadOptimalFormat(img) {
        const baseSrc = img.dataset.src.replace(/\.[^/.]+$/, '');
        const extension = img.dataset.src.split('.').pop();
        
        // Try to load best format available
        if (this.avifSupported) {
            this.tryLoadImage(img, `${baseSrc}.avif`, baseSrc, extension);
        } else if (this.webpSupported) {
            this.tryLoadImage(img, `${baseSrc}.webp`, baseSrc, extension);
        } else {
            this.tryLoadImage(img, img.dataset.src, baseSrc, extension);
        }
    }
    
    tryLoadImage(img, src, baseSrc, originalExt) {
        const testImg = new Image();
        
        testImg.onload = () => {
            img.src = src;
            img.classList.add('loaded');
        };
        
        testImg.onerror = () => {
            // Fallback to WebP if AVIF fails
            if (src.includes('.avif') && this.webpSupported) {
                this.tryLoadImage(img, `${baseSrc}.webp`, baseSrc, originalExt);
            } 
            // Fallback to original format
            else if (src.includes('.webp') || src.includes('.avif')) {
                this.tryLoadImage(img, `${baseSrc}.${originalExt}`, baseSrc, originalExt);
            }
        };
        
        testImg.src = src;
    }
    
    setupLazyLoading() {
        const imageObserver = new IntersectionObserver((entries, observer) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    const img = entry.target;
                    this.loadOptimalFormat(img);
                    observer.unobserve(img);
                }
            });
        }, {
            rootMargin: '50px 0px'
        });
        
        document.querySelectorAll('img[data-src]').forEach(img => {
            imageObserver.observe(img);
        });
    }
    
    setupResponsiveImages() {
        const images = document.querySelectorAll('img[data-srcset]');
        
        images.forEach(img => {
            const srcset = img.dataset.srcset;
            const sizes = img.dataset.sizes || '100vw';
            
            img.srcset = srcset;
            img.sizes = sizes;
        });
    }
    
    // Progressive image loading
    createProgressiveImage(container, src, placeholder) {
        const img = new Image();
        const placeholderImg = new Image();
        
        // Load tiny placeholder first
        placeholderImg.onload = () => {
            container.style.backgroundImage = `url(${placeholder})`;
            container.style.filter = 'blur(10px)';
            container.style.transform = 'scale(1.1)';
        };
        
        // Load full image
        img.onload = () => {
            container.style.backgroundImage = `url(${src})`;
            container.style.filter = 'blur(0)';
            container.style.transform = 'scale(1)';
            container.style.transition = 'all 0.3s ease';
        };
        
        placeholderImg.src = placeholder;
        img.src = src;
    }
}

// Initialize image optimization
new ImageOptimizer();
</script>

<!-- Progressive Image Component -->
<div class="progressive-image-container">
    <img data-src="/images/hero-image.jpg" 
         data-srcset="/images/hero-image-400.jpg 400w,
                     /images/hero-image-800.jpg 800w,
                     /images/hero-image-1200.jpg 1200w"
         data-sizes="(max-width: 768px) 100vw, 50vw"
         alt="Hero Image"
         class="w-full h-auto opacity-0 transition-opacity duration-500"
         loading="lazy">
</div>
```

### 🎯 Critical CSS Inlining

```html
<!-- Critical CSS Strategy -->
<style>
/* Critical CSS - Above the fold content only */
.hero-section {
    min-height: 100vh;
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    display: flex;
    align-items: center;
    justify-content: center;
}

.hero-title {
    font-size: clamp(2rem, 5vw, 4rem);
    font-weight: 700;
    color: white;
    text-align: center;
    line-height: 1.2;
    margin-bottom: 1rem;
}

.hero-subtitle {
    font-size: clamp(1rem, 2.5vw, 1.5rem);
    color: rgba(255, 255, 255, 0.9);
    text-align: center;
    margin-bottom: 2rem;
}

.cta-button {
    display: inline-block;
    padding: 1rem 2rem;
    background: #ff6b6b;
    color: white;
    text-decoration: none;
    border-radius: 0.5rem;
    font-weight: 600;
    transition: transform 0.2s ease;
}

.cta-button:hover {
    transform: translateY(-2px);
}

/* Loading state */
.loading {
    opacity: 0;
    animation: fadeIn 0.5s ease forwards;
}

@keyframes fadeIn {
    to { opacity: 1; }
}
</style>

<!-- Preload critical resources -->
<link rel="preload" href="/fonts/inter-var.woff2" as="font" type="font/woff2" crossorigin>
<link rel="preload" href="/images/hero-bg.webp" as="image">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://www.google-analytics.com">
<link rel="dns-prefetch" href="https://cdn.jsdelivr.net">

<!-- Load non-critical CSS asynchronously -->
<link rel="preload" href="/css/non-critical.css" as="style" onload="this.onload=null;this.rel='stylesheet'">
<noscript><link rel="stylesheet" href="/css/non-critical.css"></noscript>

<script>
// Critical CSS loading strategy
class CSSLoader {
    constructor() {
        this.loadedStyles = new Set();
        this.init();
    }
    
    init() {
        this.loadConditionalCSS();
        this.setupIntersectionObserver();
    }
    
    loadConditionalCSS() {
        // Load CSS based on device capabilities
        if (window.matchMedia('(prefers-reduced-motion: no-preference)').matches) {
            this.loadCSS('/css/animations.css');
        }
        
        if (window.innerWidth > 1024) {
            this.loadCSS('/css/desktop-enhancements.css');
        }
        
        if ('IntersectionObserver' in window) {
            this.loadCSS('/css/scroll-animations.css');
        }
    }
    
    setupIntersectionObserver() {
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    const section = entry.target;
                    const cssFile = section.dataset.css;
                    
                    if (cssFile && !this.loadedStyles.has(cssFile)) {
                        this.loadCSS(cssFile);
                        this.loadedStyles.add(cssFile);
                    }
                }
            });
        }, { rootMargin: '100px 0px' });
        
        // Observe sections that need specific CSS
        document.querySelectorAll('[data-css]').forEach(section => {
            observer.observe(section);
        });
    }
    
    loadCSS(href) {
        const link = document.createElement('link');
        link.rel = 'stylesheet';
        link.href = href;
        link.onload = () => console.log(`Loaded: ${href}`);
        document.head.appendChild(link);
    }
}

new CSSLoader();
</script>
```

---

## 🎨 ACCESSIBILITY (A11Y) AVANÇADA

### ♿ ARIA Implementation Complete

```html
<!-- Accessible Navigation Component -->
<nav class="main-navigation" role="navigation" aria-label="Main navigation">
    <div class="nav-container">
        <!-- Skip to content link -->
        <a href="#main-content" class="skip-link">Skip to main content</a>
        
        <!-- Logo with proper alt text -->
        <div class="logo">
            <img src="/logo.svg" alt="Company Name - Homepage" width="120" height="40">
        </div>
        
        <!-- Mobile menu button -->
        <button class="mobile-menu-toggle" 
                aria-expanded="false" 
                aria-controls="mobile-menu"
                aria-label="Toggle navigation menu">
            <span class="hamburger-line" aria-hidden="true"></span>
            <span class="hamburger-line" aria-hidden="true"></span>
            <span class="hamburger-line" aria-hidden="true"></span>
        </button>
        
        <!-- Navigation menu -->
        <ul class="nav-menu" id="mobile-menu" aria-hidden="false">
            <li class="nav-item">
                <a href="/" class="nav-link" aria-current="page">Home</a>
            </li>
            <li class="nav-item has-dropdown">
                <button class="nav-link dropdown-toggle" 
                        aria-expanded="false" 
                        aria-haspopup="true"
                        aria-controls="services-menu">
                    Services
                    <svg class="dropdown-icon" aria-hidden="true">
                        <path d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z"/>
                    </svg>
                </button>
                
                <ul class="dropdown-menu" id="services-menu" aria-hidden="true">
                    <li><a href="/web-design" class="dropdown-link">Web Design</a></li>
                    <li><a href="/development" class="dropdown-link">Development</a></li>
                    <li><a href="/seo" class="dropdown-link">SEO</a></li>
                </ul>
            </li>
            <li class="nav-item">
                <a href="/about" class="nav-link">About</a>
            </li>
            <li class="nav-item">
                <a href="/contact" class="nav-link">Contact</a>
            </li>
        </ul>
    </div>
</nav>

<script>
class AccessibleNavigation {
    constructor() {
        this.nav = document.querySelector('.main-navigation');
        this.mobileToggle = this.nav.querySelector('.mobile-menu-toggle');
        this.mobileMenu = this.nav.querySelector('#mobile-menu');
        this.dropdownToggles = this.nav.querySelectorAll('.dropdown-toggle');
        
        this.init();
    }
    
    init() {
        this.bindEvents();
        this.setupKeyboardNavigation();
    }
    
    bindEvents() {
        // Mobile menu toggle
        this.mobileToggle.addEventListener('click', () => {
            this.toggleMobileMenu();
        });
        
        // Dropdown toggles
        this.dropdownToggles.forEach(toggle => {
            toggle.addEventListener('click', (e) => {
                this.toggleDropdown(e.target);
            });
        });
        
        // Close menus on outside click
        document.addEventListener('click', (e) => {
            if (!this.nav.contains(e.target)) {
                this.closeAllMenus();
            }
        });
        
        // Handle escape key
        document.addEventListener('keydown', (e) => {
            if (e.key === 'Escape') {
                this.closeAllMenus();
            }
        });
    }
    
    toggleMobileMenu() {
        const isExpanded = this.mobileToggle.getAttribute('aria-expanded') === 'true';
        
        this.mobileToggle.setAttribute('aria-expanded', !isExpanded);
        this.mobileMenu.setAttribute('aria-hidden', isExpanded);
        
        if (!isExpanded) {
            // Focus first menu item when opening
            const firstLink = this.mobileMenu.querySelector('a, button');
            if (firstLink) firstLink.focus();
        }
    }
    
    toggleDropdown(toggle) {
        const isExpanded = toggle.getAttribute('aria-expanded') === 'true';
        const dropdownId = toggle.getAttribute('aria-controls');
        const dropdown = document.getElementById(dropdownId);
        
        // Close other dropdowns
        this.dropdownToggles.forEach(otherToggle => {
            if (otherToggle !== toggle) {
                otherToggle.setAttribute('aria-expanded', 'false');
                const otherId = otherToggle.getAttribute('aria-controls');
                const otherDropdown = document.getElementById(otherId);
                if (otherDropdown) {
                    otherDropdown.setAttribute('aria-hidden', 'true');
                }
            }
        });
        
        // Toggle current dropdown
        toggle.setAttribute('aria-expanded', !isExpanded);
        dropdown.setAttribute('aria-hidden', isExpanded);
        
        if (!isExpanded) {
            // Focus first dropdown item
            const firstLink = dropdown.querySelector('a');
            if (firstLink) firstLink.focus();
        }
    }
    
    setupKeyboardNavigation() {
        // Handle arrow keys in navigation
        this.nav.addEventListener('keydown', (e) => {
            const focusedElement = document.activeElement;
            const menuItems = Array.from(this.nav.querySelectorAll('a, button'));
            const currentIndex = menuItems.indexOf(focusedElement);
            
            switch (e.key) {
                case 'ArrowDown':
                    e.preventDefault();
                    this.focusNextItem(menuItems, currentIndex);
                    break;
                case 'ArrowUp':
                    e.preventDefault();
                    this.focusPreviousItem(menuItems, currentIndex);
                    break;
                case 'ArrowRight':
                    if (focusedElement.classList.contains('dropdown-toggle')) {
                        e.preventDefault();
                        this.toggleDropdown(focusedElement);
                    }
                    break;
                case 'ArrowLeft':
                    if (focusedElement.closest('.dropdown-menu')) {
                        e.preventDefault();
                        const parentToggle = focusedElement.closest('.has-dropdown').querySelector('.dropdown-toggle');
                        parentToggle.focus();
                        this.toggleDropdown(parentToggle);
                    }
                    break;
            }
        });
    }
    
    focusNextItem(items, currentIndex) {
        const nextIndex = (currentIndex + 1) % items.length;
        items[nextIndex].focus();
    }
    
    focusPreviousItem(items, currentIndex) {
        const prevIndex = currentIndex === 0 ? items.length - 1 : currentIndex - 1;
        items[prevIndex].focus();
    }
    
    closeAllMenus() {
        // Close mobile menu
        this.mobileToggle.setAttribute('aria-expanded', 'false');
        this.mobileMenu.setAttribute('aria-hidden', 'true');
        
        // Close all dropdowns
        this.dropdownToggles.forEach(toggle => {
            toggle.setAttribute('aria-expanded', 'false');
            const dropdownId = toggle.getAttribute('aria-controls');
            const dropdown = document.getElementById(dropdownId);
            if (dropdown) {
                dropdown.setAttribute('aria-hidden', 'true');
            }
        });
    }
}

new AccessibleNavigation();
</script>
```

---

## 🔍 SEO E STRUCTURED DATA

### 📊 Schema.org Implementation

```html
<!-- Advanced Schema.org Markup -->
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Organization",
  "name": "Your Company Name",
  "url": "https://yourwebsite.com",
  "logo": "https://yourwebsite.com/logo.png",
  "description": "Complete description of your business",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "123 Business St",
    "addressLocality": "City",
    "addressRegion": "State",
    "postalCode": "12345",
    "addressCountry": "US"
  },
  "contactPoint": {
    "@type": "ContactPoint",
    "telephone": "+1-555-123-4567",
    "contactType": "customer service",
    "availableLanguage": ["English", "Portuguese"]
  },
  "sameAs": [
    "https://facebook.com/yourcompany",
    "https://twitter.com/yourcompany",
    "https://linkedin.com/company/yourcompany"
  ]
}
</script>

<!-- Service Schema -->
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Service",
  "name": "Web Design Services",
  "description": "Professional web design and development services",
  "provider": {
    "@type": "Organization",
    "name": "Your Company Name"
  },
  "areaServed": {
    "@type": "Country",
    "name": "United States"
  },
  "hasOfferCatalog": {
    "@type": "OfferCatalog",
    "name": "Web Design Services",
    "itemListElement": [
      {
        "@type": "Offer",
        "itemOffered": {
          "@type": "Service",
          "name": "Custom Web Design"
        }
      },
      {
        "@type": "Offer",
        "itemOffered": {
          "@type": "Service",
          "name": "E-commerce Development"
        }
      }
    ]
  }
}
</script>

<!-- FAQ Schema -->
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "How long does it take to build a website?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Typically, a custom website takes 4-8 weeks depending on complexity and features required."
      }
    },
    {
      "@type": "Question",
      "name": "Do you provide ongoing support?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Yes, we offer comprehensive maintenance and support packages to keep your website running smoothly."
      }
    }
  ]
}
</script>
```

### 🎯 Advanced Meta Tags

```html
<!-- Comprehensive Meta Tags -->
<head>
    <!-- Basic Meta -->
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    
    <!-- SEO Meta -->
    <title>Professional Web Design Services | Your Company Name</title>
    <meta name="description" content="Transform your business with custom web design and development. Get stunning, mobile-responsive websites that convert visitors into customers.">
    <meta name="keywords" content="web design, web development, responsive design, custom websites">
    <meta name="author" content="Your Company Name">
    <meta name="robots" content="index, follow, max-image-preview:large">
    <link rel="canonical" href="https://yourwebsite.com/">
    
    <!-- Open Graph Meta -->
    <meta property="og:site_name" content="Your Company Name">
    <meta property="og:type" content="website">
    <meta property="og:title" content="Professional Web Design Services | Your Company Name">
    <meta property="og:description" content="Transform your business with custom web design and development. Get stunning, mobile-responsive websites that convert visitors into customers.">
    <meta property="og:url" content="https://yourwebsite.com/">
    <meta property="og:image" content="https://yourwebsite.com/og-image.jpg">
    <meta property="og:image:width" content="1200">
    <meta property="og:image:height" content="630">
    <meta property="og:image:alt" content="Professional web design showcase">
    <meta property="og:locale" content="en_US">
    
    <!-- Twitter Meta -->
    <meta name="twitter:card" content="summary_large_image">
    <meta name="twitter:site" content="@yourcompany">
    <meta name="twitter:creator" content="@yourcompany">
    <meta name="twitter:title" content="Professional Web Design Services | Your Company Name">
    <meta name="twitter:description" content="Transform your business with custom web design and development. Get stunning, mobile-responsive websites that convert visitors into customers.">
    <meta name="twitter:image" content="https://yourwebsite.com/twitter-image.jpg">
    <meta name="twitter:image:alt" content="Professional web design showcase">
    
    <!-- Additional Meta -->
    <meta name="theme-color" content="#667eea">
    <meta name="msapplication-TileColor" content="#667eea">
    <meta name="application-name" content="Your Company Name">
    <meta name="apple-mobile-web-app-title" content="Your Company Name">
    <meta name="apple-mobile-web-app-capable" content="yes">
    <meta name="apple-mobile-web-app-status-bar-style" content="default">
    
    <!-- Structured Data for Breadcrumbs -->
    <script type="application/ld+json">
    {
      "@context": "https://schema.org",
      "@type": "BreadcrumbList",
      "itemListElement": [
        {
          "@type": "ListItem",
          "position": 1,
          "name": "Home",
          "item": "https://yourwebsite.com/"
        },
        {
          "@type": "ListItem",
          "position": 2,
          "name": "Services",
          "item": "https://yourwebsite.com/services/"
        }
      ]
    }
    </script>
</head>
```