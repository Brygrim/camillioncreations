# Adding Images to Camille's Portfolio

## 📁 Folder Structure

```
portfolio-v3/
├── images/
│   ├── portrait/         ← Photo of Camille
│   ├── watercolor/       ← Watercolor paintings
│   ├── chalk/            ← Chalk art photos
│   └── ceramics/         ← Ceramic pieces
```

## 🖼️ Image Sizes (Recommended)

| Type | Size | Example |
|------|------|---------|
| **Portrait** | 800×1000px | Camille's photo |
| **Wide** | 1200×900px | Landscape artworks |
| **Tall** | 900×1200px | Portrait artworks |
| **Square** | 1000×1000px | Any format |

## 📝 Step-by-Step: Adding Images

### Step 1: Download Your Images

From your Adobe Express page or wherever your art is stored:
1. Navigate to the image
2. **Right-click** → "Save Image As..."
3. Save to your **Downloads** folder first

### Step 2: Rename Files (Important!)

Use simple, descriptive names with **NO spaces**:

✅ **Good:** `watercolor-sunset.jpg`, `chalk-festival-2024.jpg`, `camille-portrait.jpg`
❌ **Bad:** `My Painting.jpg`, `IMG_1234.jpeg`, `art (2).png`

### Step 3: Move to Correct Folder

| Image Type | Destination Folder |
|------------|-------------------|
| Photo of Camille | `images/portrait/` |
| Watercolors | `images/watercolor/` |
| Chalk Art | `images/chalk/` |
| Ceramics | `images/ceramics/` |

### Step 4: Update HTML

Open `index.html` in a text editor (TextEdit, VS Code, etc.)

#### For Portrait (Camille's Photo)

Find this line (around line 162):
```html
<div class="image-placeholder portrait-large">
    <span>Camille Grimshaw</span>
</div>
```

Replace with:
```html
<img src="images/portrait/camille-portrait.jpg" alt="Camille Grimshaw">
```

#### For Gallery Images

Find a `.gallery-item` block, like this:
```html
<div class="gallery-item">
    <div class="image-placeholder wide">
        <span>Watercolor 1</span>
    </div>
</div>
```

Replace with:
```html
<div class="gallery-item">
    <img src="images/watercolor/sunset-flowers.jpg" alt="Watercolor painting of sunset flowers" class="gallery-img">
</div>
```

**Class options for sizing:**
- `class="gallery-img wide"` — landscape (4:3)
- `class="gallery-img tall"` — portrait (3:4)
- `class="gallery-img square"` — square (1:1)

### Step 5: Add CSS for Images

You need to add this to `style.css` so images display correctly:

```css
.artist-portrait img,
.gallery-img {
    display: block;
    width: 100%;
    height: 100%;
    object-fit: cover;
}

.gallery-img.wide {
    width: 400px;
    height: 300px;
}

.gallery-img.tall {
    width: 300px;
    height: 400px;
}

.gallery-img.square {
    width: 320px;
    height: 320px;
}
```

## ✅ Quick Checklist

- [ ] Download images from Adobe Express
- [ ] Rename files (no spaces, lowercase)
- [ ] Move to correct folder
- [ ] Update HTML `src` paths
- [ ] Add `alt` text for accessibility
- [ ] Add CSS for image sizing
- [ ] Open `index.html` in browser to test

## 🎯 Example: Complete Gallery Item

```html
<div class="gallery-item">
    <img src="images/watercolor/mountain-sunset.jpg" 
         alt="Watercolor painting of mountain sunset with purple and orange sky" 
         class="gallery-img wide">
</div>
```

## 🔧 Troubleshooting

**Image not showing?**
- Check the filename matches exactly (capitals matter!)
- Make sure it's in the right folder
- Try opening the image directly in browser to confirm path

**Image looks squished?**
- Add the correct class: `wide`, `tall`, or `square`
- Use `object-fit: cover` in CSS

**Need to add MORE images?**
- Just copy/paste another `.gallery-item` block
- Add as many as you want — the gallery scrolls horizontally!

---

## 🚀 Pro Tip

After adding all images, test by:
1. Opening `index.html` in Chrome/Safari
2. Scrolling through each gallery
3. Checking the portrait loads in "Meet the Artist"

Need help? The HTML sections are labeled with comments like `<!-- Watercolor -->`
