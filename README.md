# Quiz CLI

A simple Node.js command-line quiz game for learning JavaScript.

## Overview

**Quiz CLI** is an interactive terminal app that:

- lets you choose a quiz category
- lets you choose how many questions to answer
- runs the quiz one question at a time in the terminal
- shows your results at the end
- offers the option to play again

The app is built with **Node.js** and uses **ES Modules** with built-in Node APIs.

## Features

- Interactive command-line experience
- Category-based quiz selection
- Custom question count selection
- Terminal color output
- Result summary after each quiz
- Replay flow after finishing a round
- Async file loading for quiz data
- Error handling around quiz startup and gameplay

## Prerequisites

- **Node.js 18 or newer**
- npm

## Installation

Clone the repository and install dependencies:

```bash
git clone <repository-url>
cd test-app
npm install
```

> This project does not declare any external npm dependencies in `package.json`, but running `npm install` is still a good first step to make sure the project is ready.

## Usage

Start the quiz app:

```bash
npm start
```

This runs:

```bash
node index.js
```

## How it works

When you start the app, it:

1. clears the terminal
2. prints a banner
3. loads quiz questions from `data/questions.json`
4. asks you to pick a category
5. asks how many questions you want
6. runs the quiz interactively
7. displays your score and results
8. asks whether you want to play again

## Scripts

From `package.json`:

```json
{
  "start": "node index.js",
  "test": "node --test"
}
```

### Available scripts

- `npm start` — launch the quiz app
- `npm test` — run the Node.js test runner

## Project structure

Based on the visible repository analysis, the project appears to use this structure:

```text
test-app/
├── index.js
├── package.json
├── data/
│   └── questions.json
├── src/
│   ├── input.js
│   ├── quiz.js
│   └── colors.js
├── test-app.zip
└── .DS_Store
```

### Important note

Only `index.js` and `package.json` are visible in the repository tree provided here.  
`index.js` references these paths:

- `data/questions.json`
- `src/input.js`
- `src/quiz.js`
- `src/colors.js`

If those files are not present in the visible repository, they may be included in the archive (`test-app.zip`) or may be missing from the current tree.

## Implementation notes

From `index.js`, the app appears to use:

- **ES Modules** via `import`
- built-in Node modules such as:
  - `fs/promises`
  - `url`
  - `path`
- a `Quiz` class for the main gameplay loop
- local helper modules for input handling and terminal colors

## Notes and limitations

- The quiz data file is expected at `data/questions.json`.
- The app depends on the local modules under `src/`.
- If any of those files are missing, the app may not run until they are restored.
- No external npm packages are required based on the current `package.json`.

## Troubleshooting

If the app fails to start:

- confirm you are using **Node.js 18+**
- check that `data/questions.json` exists
- check that the `src/` modules referenced by `index.js` exist
- run `npm install` again in case the environment is not fully set up
