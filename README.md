# Quiz CLI

Quiz CLI is an interactive command-line quiz game for learning JavaScript.

## Overview

This repository contains a Node.js CLI application that:

- runs in the terminal
- uses ES modules (`type: "module"`)
- loads quiz questions from JSON
- supports interactive category and question selection

## Requirements

- Node.js 18 or newer

## Getting Started

Install dependencies if your environment requires them, then start the app:

```bash
npm start
```

## Testing

Run the test suite with:

```bash
npm test
```

## Project Structure

From the visible application entry point, the app appears to use these internal modules and data files:

- `index.js` — main CLI entry script
- `src/input.js` — terminal input helpers
- `src/quiz.js` — quiz logic
- `src/colors.js` — terminal color helpers
- `data/questions.json` — quiz content

> Note: this README stays intentionally cautious where the repository snapshot is incomplete, and may be updated as additional files are added.

## How It Works

1. The CLI starts and displays a welcome banner.
2. The user selects a quiz category.
3. The user chooses how many questions to answer.
4. The quiz runs question by question in the terminal.
5. Results are shown at the end, with an option to play again.

## License

MIT
