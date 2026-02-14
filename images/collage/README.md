# Collage / Slideshow Images Folder

This folder contains images for the landing page **CSS slideshow** background.

## Current System: Auto-Crossfading Slideshow

The landing page now features an **automatic CSS slideshow** that crossfades between 4 images every 5 seconds.

---

## Required Files

Put 4 images in this folder with these exact names:

| Filename | Timing | Description |
|----------|--------|-------------|
| `collage-1.jpg` | 0-5 seconds | First image shown |
| `collage-2.jpg` | 5-10 seconds | Second image |
| `collage-3.jpg` | 10-15 seconds | Third image |
| `collage-4.jpg` | 15-20 seconds | Fourth image |

**Full paths:**
- `/portfolio-v3/images/collage/collage-1.jpg`
- `/portfolio-v3/images/collage/collage-2.jpg`
- `/portfolio-v3/images/collage/collage-3.jpg`
- `/portfolio-v3/images/collage/collage-4.jpg`

---

## How to Add Images

1. **Choose 4 images** you want to feature on the landing page
   - Can be any of: watercolor, chalk art, ceramics, portraits
   - Pick your best/most representative work

2. **Copy them into this folder**:
   ```
   portfolio-v3/images/collage/
   ```

3. **Rename them exactly**:
   - `collage-1.jpg` (shown first when page loads)
   - `collage-2.jpg`
   - `collage-3.jpg`
   - `collage-4.jpg`

4. **Refresh the page** to see the slideshow in action!

---

## Image Tips

| Recommendation | Why |
|----------------|-----|
| Use **JPG format** | Smaller file size, faster loading |
| **1200-1600px wide** | Good quality, not too heavy |
| **Landscape orientation** | Fills screen better |
| **Keep under 500KB each** | Faster page load |

---

## How It Looks

- Images **auto-crossfade** every 5 seconds
- Each transition takes **1.5 seconds**
- Full cycle = **20 seconds** (then repeats)
- **Slow zoom effect** while image is visible
- **Subtle grayscale** filter (adds elegant mood)

---

## To Use a Different Number of Images

**Want 3 images instead of 4?** Edit the CSS in `style.css`:

Change the animation delay values:
```css
.landing-slideshow .slideshow-img:nth-child(1) { animation-delay: 0s; }
.landing-slideshow .slideshow-img:nth-child(2) { animation-delay: 5s; }
.landing-slideshow .slideshow-img:nth-child(3) { animation-delay: 10s; }
/* Remove the 4th one or set to 15s */
```

And update the animation duration (15s for 3 images, 20s for 4, etc.)

---

## To Roll Back to 4-Image Grid

If you want the original 2×2 grid instead of slideshow:

1. Undo the HTML changes in `index.html` (search for `landing-slideshow`)
2. Undo the CSS changes in `style.css` (search for `landing-collage`)
3. Images stay in same folder with same names

*Ask me and I can undo it instantly!*

---

## Current Status

- [ ] `collage-1.jpg` - needs image
- [ ] `collage-2.jpg` - needs image  
- [ ] `collage-3.jpg` - needs image
- [ ] `collage-4.jpg` - needs image

*Check these off as you add each image*
