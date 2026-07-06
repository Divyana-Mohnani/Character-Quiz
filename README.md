# Character-Quiz
Client-side quiz app built with vanilla HTML, CSS, and JavaScript. Dynamically renders questions from a JS data array and calculates results via positional score-mapping

Tech Stack
- HTML5 — semantic structure, three toggleable "screens" (intro, quiz, result)
- CSS3 — flexbox layout, gradient background, class-based show/hide (`.hidden`)
- Vanilla JavaScript (ES6)** — DOM manipulation via `createElement`/`addEventListener`, no libraries or build tools

How it works
- Question and character data are stored as JS arrays/objects (`questions`, `characters`)
- Each question's answer options map positionally to a fixed character list (e.g., option index 0 always corresponds to the first character)
- User selections increment a running `scores` object; after the final question, the character with the highest score is displayed
- All logic runs client-side — no server calls, no data persistence between sessions

Architecture notes
- Single-file implementation (`index.html`) — HTML, CSS, and JS are co-located for simplicity
- No package manager, dependencies, or build step required — open directly in a browser or serve via GitHub Pages
- State (current question index, scores) is held in-memory via JS variables, reset via `restartQuiz()`

Running locally
