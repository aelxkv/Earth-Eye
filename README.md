# 🛰️ Earth Eye

**Image → Feature Detection → Explanation**

An AI/ML demo that analyzes NASA Earth and space images, highlights visible features, and explains the image in simple language.

🔗 **Live demo:** https://aelxkv.github.io/Earth-Eye/

---

## What it does

1. **Image:** upload any NASA or satellite photo
2. **Feature detection:** finds and labels at least 3 visible features
3. **Explanation:** writes a plain-English summary of the image

**Detectable features:** clouds/ice, ocean/water, forest/vegetation, fire/hot spots, land/desert, urban/rocky surfaces, and space/dark areas.

**Example output**

> Detected: Clouds / Ice, Ocean / Water, Land / Desert.
> Explanation: "This image mostly shows open water and bright cloud or ice cover. The biggest feature is open water, covering about 45% of the picture."

---

## Approach

I built a lightweight AI system that analyzes NASA Earth and space images directly in the browser. The image is downscaled, and k-means clustering, an unsupervised machine-learning method, groups pixels into color clusters. Each cluster is converted to HSV and matched to a feature type: clouds/ice, ocean, vegetation, fire, land, rocky/urban surfaces, or space. The app overlays translucent color masks, labels the largest region of each feature, and reports percentage coverage. Finally, a template turns the top detected features into a plain-English explanation. The interface shows Image → Feature Detection → Explanation on a single page.

---

## How to run

- **Online:** open the live demo link above
- **Locally:** download `index.html` and open it in any browser. No installs or server are needed.

Then tap **Choose image** and pick a photo.

---

## Repository contents

| File | Purpose |
|------|---------|
| `index.html` | The full app (HTML, CSS, JavaScript) |
| `samples/` | Sample NASA images used for testing |
| `screenshots/` | Screenshots of feature detection results |

---

## Limitations

- Uses unsupervised clustering plus color rules, not a trained deep-learning model
- Clouds and snow/ice can look similar and may be merged
- Craters are only detected loosely as "rocky surface"

---

## Image & dataset source

Sample images are from publicly available NASA collections:

- NASA Earth Observatory: https://earthobservatory.nasa.gov
- NASA Worldview: https://worldview.earthdata.nasa.gov

Credit: NASA. Images are used for educational purposes.

---

## Built for

NASA Space App challenge · `#evn-sp-ai`
