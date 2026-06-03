# CSS Specificity - JavaScript Language Card

A mini project to practice and understand **CSS Specificity** concepts using a JavaScript language showcase card.

## What is CSS Specificity?

CSS Specificity determines which style rule wins when multiple rules target the same element. The browser follows a points system:

| Selector Type | Points |
|---|---|
| Inline style | 1,0,0,0 |
| ID selector | 0,1,0,0 |
| Class selector | 0,0,1,0 |
| Tag selector | 0,0,0,1 |

Higher points = higher priority = that style wins!

## What this project demonstrates

### 1. Class beats Tag
```css
h1 { color: orange; }       /* tag selector — loses */
.blue-text { color: blue; } /* class selector — WINS */
```
The `h1` heading appears **blue** because `.blue-text` has higher specificity than the `h1` tag selector.

### 2. ID beats Class
```css
.language-description { font-size: 16px; } /* class — loses */
#description { font-size: 20px; }           /* ID — WINS */
```
The paragraph shows **20px** font size because `#description` (ID) beats `.language-description` (class).

### 3. Inline Style beats everything
```html
<button style="background-color: orange">Learn</button>
```
The button stays **orange** because inline styles have the highest specificity — no external CSS can override them (without `!important`).

## Files

| File | Description |
|---|---|
| `index.html` | HTML structure of the JavaScript card |
| `style.css` | CSS styles demonstrating specificity rules |

## How to Run

1. Download or clone this repository
2. Open `index.html` in any web browser
3. Inspect the elements using browser DevTools to see which CSS rules win!

## Concepts Covered

- CSS Specificity hierarchy
- Inline styles vs external CSS
- ID selectors vs Class selectors
- Class selectors vs Tag selectors
- Google Fonts import

## Author

**Hacshitha** — Learning web development one project at a time!

---
*Built as part of CSS fundamentals practice*
