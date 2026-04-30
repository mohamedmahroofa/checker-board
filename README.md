# Bootstrap Checkerboard

A classic 8×8 checkerboard built with **Bootstrap 4** and custom CSS. This project demonstrates how Bootstrap's grid system can be combined with custom class names to produce structured, repeating layouts — without a single line of JavaScript logic.

---

## Preview

An 8×8 grid of alternating **light green** and **black** squares, rendered inside a bordered container on a warm beige background.

---

## Technologies Used

| Technology | Version | Purpose                                      |
| ---------- | ------- | -------------------------------------------- |
| HTML5      | —       | Page structure                               |
| Bootstrap  | 4.1.3   | Grid layout via `.container`, `.row`, `.col` |
| Custom CSS | —       | Square colors, sizing, and page styling      |
| jQuery     | 3.3.1   | Bootstrap JS dependency                      |
| Popper.js  | 1.14.3  | Bootstrap JS dependency                      |

---

## Project Structure

```
bootstrap-checkerboard/
├── index.html       # Main HTML file with the 8x8 grid markup
├── style.css        # Custom styles for colors, sizing, and borders
└── README.md        # Project documentation
```

---

## How It Works

### Grid Structure

Bootstrap's grid system provides the foundation. Each row is built using `.row`, and each cell uses `.col` — Bootstrap's equal-width column class — so all 8 columns share the row width evenly.

```html
<div class="container">
  <div class="row">
    <div class="col green"></div>
    <div class="col black"></div>
    <!-- ...8 columns per row -->
  </div>
  <!-- ...8 rows total -->
</div>
```

### Checkerboard Pattern

The alternating pattern is achieved by manually offsetting each row. Odd rows start with `.green`, even rows start with `.black` — producing the classic checkerboard effect without any JavaScript or loops.

### Custom CSS Classes

Two custom classes handle the square colors:

```css
.black {
  background-color: black;
}

.green {
  background-color: lightgreen;
}
```

Square dimensions and the container styling are also handled in `style.css`:

```css
.col {
  height: 150px;
  width: 150px;
  border: none;
}

.container {
  background-color: rgb(109, 240, 194);
  border: 15px solid black;
}
```

---

## Getting Started

### Prerequisites

No installations required. The project loads Bootstrap via CDN and runs entirely in the browser.

### Running Locally

1. Clone or download this repository
2. Open `index.html` in any modern web browser
3. The checkerboard renders immediately — no build step needed

```bash
# Optional: open directly from terminal
open index.html        # macOS
start index.html       # Windows
xdg-open index.html    # Linux
```

---

## Key Concepts Demonstrated

- **Bootstrap `.col` equal-width columns** — all 8 cells in each row share the available width automatically
- **Combining Bootstrap and custom classes** — `.col` handles layout, `.green` / `.black` handle appearance
- **Manual alternating pattern** — each row is hand-coded with an offset to produce the checkerboard effect
- **Container border styling** — a thick black border frames the entire board using plain CSS

---

## Possible Extensions

- Add draggable checker pieces using JavaScript
- Use a JavaScript loop to generate the grid dynamically instead of hard-coded HTML
- Make the board responsive so it scales on mobile screens
- Add a color theme toggle using Bootstrap utility classes

---

## Author

Built as part of a Bootstrap learning exercise focusing on grid layout and class composition.

---

## License

This project is open source and available under the [MIT License](LICENSE).
