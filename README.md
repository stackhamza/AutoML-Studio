# AutoML Studio

**No-code AutoML tool that runs entirely in the browser.**  
Upload a CSV, clean data, train models, and deploy a shareable prediction demo — without installing Python.

© Developed by [XpertsWP](https://xpertswp.com/)

---

## Features

| Step | What you can do |
|------|------------------|
| **Upload & Preview** | Load a CSV dataset and inspect rows/columns |
| **Analyze Dataset** | Column types, missing values, basic profiling |
| **Clean Data** | Handle missing values, encode categoricals, scale numerics |
| **Statistics & Visualization** | Summary stats, correlation, charts |
| **Model Training** | Choose target column, select features, train models |
| **Backend & Deploy** | Deploy a live prediction demo to Netlify |
| **Export Clean Data** | Download cleaned CSV |
| **Code Panel** | View generated Python-style training code |

### Models included (all free)

- Linear Regression, Logistic Regression  
- K-Nearest Neighbors  
- Ridge, Lasso, Decision Tree, Naive Bayes  
- Random Forest, Extra Trees, Gradient Boosting  
- SVM, K-Means, DBSCAN  
- Baselines (mean / most frequent)  
- **Quick Train** — auto-tests several algorithms and keeps the best  

### Privacy

- Runs **100% in your browser**  
- Your dataset is **not uploaded** to any server during training  
- Only the generated **demo HTML** is sent when you deploy to Netlify  

---

## Quick start

1. Open `ai-ml-studio-free-pro.html` in a modern browser (Chrome, Edge, Firefox).  
2. Upload a CSV file.  
3. (Optional) Clean and explore data.  
4. Go to **Model Training**:
   - Select the **target column** (what you want to predict)  
   - Adjust features if needed  
   - Click **Quick Train** or train a model manually  
5. Go to **Backend & Deploy** to publish a public demo URL.

No build step, no Node install, no Python required for the in-browser flow.

---

## Choose your own target column

On **Model Training**:

1. Use **🎯 Choose the column you want to predict (target)**  
2. Pick any column from the dropdown  
3. Features update automatically  
4. Run **Quick Train (on selected target)** or train manually  

The model is trained to predict **your selected target** from the other columns.

---

## Deploy a shareable demo (Netlify)

Anyone can open the demo URL and try predictions in the browser.

### Get a free Netlify token

1. Sign up: [app.netlify.com/signup](https://app.netlify.com/signup)  
2. Open [Personal access tokens](https://app.netlify.com/user/applications#personal-access-tokens)  
3. Click **New access token** → generate → copy (`nfp_…`)  

### Deploy from the app

1. Open **Backend & Deploy**  
2. Paste the token  
3. Click **Deploy to Netlify & get demo URL**  
4. Open / copy the `*.netlify.app` link and share it  

### Manual alternative

1. Click **Download index.html**  
2. Open [app.netlify.com/drop](https://app.netlify.com/drop) while logged in  
3. Drag `index.html` onto the page  

---

## Model accuracy notes

- Training uses **your real data** (with a row sample if the file is very large, for browser speed).  
- Metrics such as **R²** (regression) and **accuracy** (classification) are shown on a held-out test split.  
- Algorithms are **lightweight JavaScript implementations** inspired by scikit-learn — good for demos and learning, not a full production sklearn pipeline.  
- For production-grade training, use the exported project / Python workflow from **Backend & Deploy** when available.  

**Tip:** Clean missing values and encode categoricals before training for better results.

---

## Project structure

```text
ai-ml-studio-free-pro.html   # Full app (HTML + CSS + JS, single file)
README.md                    # This file
```

Single-file design: open the HTML file and everything runs offline except Netlify deploy.

---

## Browser support

- Chrome / Edge / Firefox / Safari (recent versions)  
- Recommended: desktop browser with a stable connection for deploy  

---

## Credits

**Developed by [XpertsWP](https://xpertswp.com/)**

All features are free in the current build.

---

## License

For commercial use, redistribution, or white-labeling, contact [XpertsWP](https://xpertswp.com/).
