# Animated Radio Button Styles

[![Live Demo](https://img.shields.io/badge/Live%20Demo-GitHub%20Pages-blue?style=for-the-badge&logo=github)](https://mrchandrayee.github.io/animated-radio-button-styles/)
[![HTML](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org) [![CSS](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://developer.mozilla.org) [![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org)
[![License: MIT](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](./LICENSE)

Complete runnable recreation of the uploaded 17.2-second screen recording.

## Screen content, in order

The video title is **Animated Radio button styles**. It presents five animated radio-button designs, each with a live preview and HTML/CSS code panel:

1. **Pulse Glow** — cyan outline, filled cyan selected state, glow and pulse.
2. **Sliding Dot** — pink outline with a small pink dot sliding into place.
3. **Glass Effect** — translucent glass-style circle with a teal selected glow.
4. **Neon Ring** — cyan outline with a cyan neon glow and rotation animation.
5. **Game Pop** — yellow filled selected state with a short pop animation.

The page uses a near-black background, blue glowing heading, thin orange section borders, dark green code-card backgrounds, cyan HTML/CSS labels and green monospace code.

## Visible source code transcribed

### Pulse Glow

```html
<label class="radio pulse">
  <input type="radio">
  <span></span> Select
</label>
```

```css
.pulse span {
  border: 2px solid #00f7ff;
}

.pulse input:checked + span {
  background: #00f7ff;
  box-shadow: 0 0 15px #00f7ff;
  animation: pulse 0.6s;
}

@keyframes pulse {
  50% { transform: scale(1.4); }
}
```

### Sliding Dot

```html
<label class="radio slide">
  <input type="radio">
  <span></span>
</label>
```

```css
.slide span { border: 2px solid #ff4081; }

.slide span::after {
  content: "";
  width: 10px;
  height: 10px;
  background: #ff4081;
  border-radius: 50%;
  position: absolute;
  left: -15px;
  top: 4px;
  transition: 0.4s;
}

.slide input:checked + span::after {
  left: 5px;
}
```

### Glass Effect

```html
<label class="radio glass">
  <input type="radio">
  <span></span>
</label>
```

```css
.glass span {
  backdrop-filter: blur(10px);
  background: rgba(255,255,255,0.1);
  border: 1px solid rgba(255,255,255,0.3);
}

.glass input:checked + span {
  background: rgba(0,255,200,0.4);
  box-shadow: 0 0 15px rgba(0,255,200,0.7);
}
```

### Neon Ring

```html
<label class="radio neon">
  <input type="radio">
  <span></span>
</label>
```

```css
.neon span { border: 2px solid #0ff; }

.neon input:checked + span {
  box-shadow: 0 0 10px #0ff, 0 0 30px #0ff;
  animation: rotate 0.8s linear;
}

@keyframes rotate {
  to { transform: rotate(360deg); }
}
```

### Game Pop

```html
<label class="radio game">
  <input type="radio">
  <span></span>
</label>
```

```css
.game span { border: 2px solid #ffd700; }

.game input:checked + span {
  background: #ffd700;
  animation: pop 0.3s;
}

@keyframes pop {
  50% { transform: scale(1.3); }
}
```

## Run

1. Extract the ZIP.
2. Open `index.html` in a modern browser.
3. Click each radio control to see its selected animation.

No dependencies, npm install, server, or external assets required.

## Project files

- `index.html` — all five examples, previews and visible code panels
- `style.css` — styling and working radio animations
- `README.md` — transcription and run guide

## Fidelity note

The snippets above are transcribed from the visible code panels. The shared layout/base styling and minor adjustments required to make each control display and work in a standalone page are reconstructed. This is not represented as the creator's complete hidden original source.

## 👨‍💻 Author

**mrchandrayee** · [GitHub](https://github.com/mrchandrayee)

## 📄 License

[MIT License](./LICENSE)
