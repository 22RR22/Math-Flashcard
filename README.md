# Math Flashcards Master

An interactive, high-contrast, and beautiful flashcard website to help students memorize and understand math formulas and facts from Grades 6–12. The site is a single, self-contained HTML file with smooth animations, keyboard navigation, search, grade filters, and 700+ cards with practical examples.


## ✨ Highlights
- Grades covered: 6, 7, 8, 9, 10, 11, 12
- 700+ formulas, identities, theorems, and facts (each with a concrete example)
- High-contrast, student-friendly UI with animations and a modern heading
- Real-time search and grade/category filtering
- Shuffle, next/previous, grid view toggle, and keyboard shortcuts
- Fully responsive (mobile/desktop) and works offline locally (no server required)
- Tech stack: HTML + CSS + JavaScript (no build tools, no libraries)


## 🚀 Getting Started
You can use this app directly by opening the HTML file—no installs required.

### Option A: Open directly
1. Locate `index.html`
2. Double-click to open in your browser

### Option B: Serve locally (optional, recommended)
This avoids some browsers’ file URL restrictions.

```bash
# macOS / Linux / Windows (with Python 3)
python3 -m http.server 8000
# Then open http://localhost:8000 in your browser
```


## 🧭 How to Use
- Choose a grade using the filter buttons at the top
- Use the search box to find formulas (e.g., “Pythagorean”, “quadratic”, “area”)
- Click a card to flip between question and answer
- Use controls to shuffle cards or switch between single-card and grid view

### Keyboard Shortcuts
- Left/Right Arrow: Previous/Next card
- Space: Flip current card
- G: Toggle grid view
- S: Shuffle
- Esc: Clear search


## 📦 Project Structure
```
mathflashcard/
├── index.html   # The entire app (UI, styles, data, logic)
└── README.md    # You are here
```


## 🧱 Data Model (Flashcard)
Cards are defined in a JavaScript array inside `index.html` like this:

```js
{
  grade: 10,                  // Number (6–12)
  category: "Trigonometry",   // Short topic name
  front: "Pythagorean Triples", // Front (question / prompt)
  back:  "a² + b² = c²\nExample: 3² + 4² = 5²" // Back (answer)
}
```

Tips:
- Use `<br>` for line breaks in `front`/`back` when needed
- Keep examples concise: `Formula<br>Example: …`
- Group related formulas under consistent `category` labels


## 🎨 Customization
You can easily tweak the look and feel in the `<style>` section of `index.html`:
- Brand colors: background gradient `#667eea → #764ba2`, accents `#ffd700`
- Heading: animated shimmering gold title and glassmorphism header card
- Card sizing, spacing, shadows, and flip animations

Suggested quick tweaks:
- Change the gradient or accent color
- Reduce animation if needed (search for `animation:` in CSS)
- Adjust card grid breakpoints for smaller screens


## ➕ Adding or Editing Cards
1. Open `index.html`
2. Search for the `flashcards` array
3. Add a new object with `grade`, `category`, `front`, and `back`
4. Keep examples clear and correct; use `<br>` for readability

Example addition:
```js
{ grade: 9, category: "Algebra", front: "Quadratic Formula",
  back: "x = [-b ± √(b²-4ac)]/(2a)<br>Example: a=1,b=-3,c=2 → x=1,2" },
```


## 🔎 Features (at a glance)
- Grade filter: All, 6, 7, 8, 9, 10, 11, 12
- Search-as-you-type across prompts and answers
- Shuffle deck
- Single-card and grid view toggle
- Flip animation with 3D transform
- Mobile responsive layout
- Keyboard navigation


## 🌐 Deployment
You can host this as a static site anywhere. Two easy options:

### GitHub Pages
1. Create a new repo and push this folder
2. In GitHub: Settings → Pages → Deploy from branch → Select `main`/`master`
3. Place `index.html` at repo root

### Any static host
Upload `index.html` to services like Netlify, Vercel (static), Firebase Hosting, or your school server.


## 🧪 Quality and Accuracy
- All formulas have been verified for correctness
- Each theoretical card includes at least one concrete example
- Content spans arithmetic, algebra, geometry, trigonometry, functions, sequences/series, probability, statistics, matrices, logarithms/exponents, calculus (derivatives/integrals), and more


## 🛠️ Troubleshooting
- “Nothing shows up”: Make sure you opened `index.html` in a modern browser (Chrome, Edge, Safari, Firefox)
- Search not filtering: Clear the search field (Esc) and try again
- Mobile layout issues: Reduce zoom or rotate device; the grid adapts at common breakpoints
- Emoji not rendering: Ensure your OS/browser emoji font is available


## 🗺️ Roadmap Ideas (Optional Enhancements)
- Dark/Light theme toggle
- Spaced repetition (SRS) and progress tracking
- Quiz modes and timed challenges
- LaTeX/Katex math rendering
- User-created custom decks and sharing
- Cloud sync and teacher dashboards


## 🤝 Contributing
- Fork the project, create a feature branch, and open a pull request
- Please keep formulas accurate and provide brief examples for each addition
- Keep styling consistent with the current aesthetic (high-contrast and readable)


## 📜 License
MIT License


## 🙌 Acknowledgements
- Built with vanilla HTML/CSS/JavaScript
- Designed for students in Grades 6–12 to build confidence through repetition and examples
