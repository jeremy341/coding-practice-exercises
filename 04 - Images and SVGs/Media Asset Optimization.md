# Media Asset Optimization

Web pages with unoptimized images and videos load slowly, resulting in a poor user experience and lower search engine rankings (SEO). Optimizing your media assets is one of the most effective ways to speed up your website.

Here are the key strategies for optimizing media assets:

---

## 1. Choose the Right Format
Different images require different formats depending on their complexity:

* **SVGs (Scalable Vector Graphics)**: Ideal for logos, icons, and illustrations. Because they are code-based vector graphics, they scale infinitely without losing quality and have extremely small file sizes.
* **WebP / AVIF**: Modern image formats that offer superior compression compared to JPEG and PNG. They support transparency and animation, and typically reduce file sizes by 30% to 50% without visible loss in quality.
* **PNG**: Best for graphics that require transparency and sharp text/lines, but file sizes can be large.
* **JPEG**: Good fallback for photographs, but should be compressed before use.

---

## 2. Compress Your Images
Before uploading images to your website, compress them to remove unnecessary metadata and optimize pixel encoding.
* **Lossless Compression**: Reduces file size without affecting the quality of the image.
* **Lossy Compression**: Reduces file size by removing details that are barely noticeable to the human eye.
* **Tools**: Use tools like TinyPNG, ImageOptim, or Squoosh to compress files.

---

## 3. Implement Responsive Images
Do not serve a huge $4000 \times 3000\text{px}$ image to a mobile phone. Use HTML features to deliver the right size image based on the user's screen:

### The `srcset` and `sizes` attributes
Provide a list of images at different widths, and let the browser select the most appropriate one:
```html
<img 
  src="image-large.jpg" 
  srcset="image-small.jpg 480w, image-medium.jpg 800w, image-large.jpg 1200w" 
  sizes="(max-width: 600px) 480px, (max-width: 900px) 800px, 1200px" 
  alt="A scenic view"
/>
```

### The `<picture>` element
Serve different formats (e.g., AVIF or WebP with JPEGs as fallbacks) or change the crop of the image for mobile screens (art direction):
```html
<picture>
  <source srcset="image.avif" type="image/avif" />
  <source srcset="image.webp" type="image/webp" />
  <img src="image.jpg" alt="A scenic view" />
</picture>
```

---

## 4. Use Lazy Loading
Lazy loading defers the loading of off-screen images until the user scrolls near them, saving bandwidth and speed up initial page load:
```html
<img src="image.jpg" loading="lazy" alt="Descriptive text" />
```
* **`loading="lazy"`**: Built-in browser support for lazy loading. Should be applied to most below-the-fold images.
