# Typing Speed Test

Measure your WPM (words per minute) and accuracy in real time with 4 difficulty modes.

🔗 **[Live Demo](https://mahtxx.github.io/typing-speed-test/)**

## Features

- ⌨️ 4 difficulty modes: Easy, Medium, Hard, Code
- 📊 Live WPM, accuracy %, and error count
- ⏱ 60-second countdown with animated SVG ring timer
- 🎨 Per-character highlighting: correct (green), wrong (red), cursor (purple)
- 🔁 Instant restart button
- 📱 Mobile-friendly hidden input focus trick

## How WPM Is Calculated

`WPM = (characters typed / 5) / (elapsed minutes)`

The standard 5-characters-per-word measure is used for consistency with industry benchmarks.

## How to Customize

### Change timer duration
Find this line in the `start()` function:
```js
timeLeft = totalTime = 60; // change to 30 for 30 seconds, 120 for 2 minutes
```

### Add custom word lists
Add a new key to the `WORDS` object:
```js
const WORDS = {
  easy: [...],
  medium: [...],
  // Add yours:
  tech: ['kubernetes','terraform','microservices','latency','throughput'],
  medical: ['diagnosis','pathology','cardiology','neurology']
};
```
Then add a button in the HTML:
```html
<button class="diff-btn" data-diff="tech">Tech</button>
```

### Change word count
```js
for(let i = 0; i < 80; i++) // was 60 — more words = longer test
```

## Tech Stack
- Vanilla HTML/CSS/JS
- SVG animation for timer ring
- No dependencies
