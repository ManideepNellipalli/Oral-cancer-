# GitHub Pages Deployment Guide

## Step-by-step instructions to deploy the live demo

---

### Step 1 — Push the repository to GitHub

```bash
git init
git add .
git commit -m "Initial commit: oral cancer detection project"
git remote add origin https://github.com/YOUR-USERNAME/oral-cancer-detection.git
git branch -M main
git push -u origin main
```

---

### Step 2 — Enable GitHub Pages

1. Go to your repository on GitHub
2. Click **Settings** (top menu)
3. Scroll to **Pages** in the left sidebar
4. Under **Source**, select:
   - Branch: `main`
   - Folder: `/docs`
5. Click **Save**

GitHub will display:
> ✅ Your site is live at `https://your-username.github.io/oral-cancer-detection/`

It may take 1–2 minutes for the first deployment.

---

### Step 3 — Update your README links

Replace `your-username` in `README.md` with your actual GitHub username:

```markdown
🔗 **[View Project Demo on GitHub Pages](https://your-username.github.io/oral-cancer-detection/)**
```

Also update in `docs/index.html`:
```html
<a href="https://github.com/your-username/oral-cancer-detection">📂 View on GitHub</a>
```

---

### Step 4 — Add screenshots (optional but recommended)

Place your actual output images in `screenshots/`:

| File | What to capture |
|---|---|
| `training_history.png` | Loss & accuracy plot from notebook |
| `confusion_matrix.png` | Seaborn confusion matrix |
| `patch_visualization.png` | ViT patch grid visualization |

Then commit and push:
```bash
git add screenshots/
git commit -m "Add project screenshots"
git push
```

---

### Step 5 — Add GitHub repository metadata

On your GitHub repo page, click the ⚙️ gear icon next to **About** and add:

**Description:**
```
Binary oral cancer image classification using a custom CNN and Vision Transformer (ViT) built from scratch. TensorFlow/Keras | Medical Imaging | Deep Learning
```

**Website:**
```
https://your-username.github.io/oral-cancer-detection/
```

**Topics (tags):**
```
deep-learning  computer-vision  medical-imaging  oral-cancer  cnn
vision-transformer  vit  tensorflow  keras  binary-classification
image-classification  python  kaggle  healthcare-ai
```

---

### Verification checklist

- [ ] `docs/index.html` exists in the repo
- [ ] GitHub Pages is enabled with source set to `/docs`
- [ ] Live URL loads correctly
- [ ] README links updated with your actual username
- [ ] Repository description and topics added
