# Quiz CLI

An interactive command-line quiz game for learning JavaScript.

## Description

**Quiz CLI** is a Node.js terminal application that loads questions from a JSON file, lets the user choose a category and quiz length, and then runs an interactive multiple-choice quiz in the console.

The repository metadata and entry script indicate that the app uses ES modules and targets Node.js 18 or newer.

## Features

- Interactive command-line quiz flow
- Category selection
- Choice of question count
- Results summary at the end of each quiz
- Replay support
- Colorized terminal output
- Built with modern Node.js ES modules

## Requirements

- Node.js 18.0.0 or newer

## Setup

Clone the repository and install dependencies:

```bash
git clone <repository-url>
cd test-app
npm install
```

> Note: The visible `package.json` does not list external dependencies, so `npm install` may complete quickly.

## Run

Start the app with:

```bash
npm start
```

This runs:

```bash
node index.js
```

You can also run the entry file directly:

```bash
node index.js
```

## Testing

Run the test script with:

```bash
npm test
```

This uses Node's built-in test runner:

```bash
node --test
```

No test files were visible in the repository snapshot, so this command may do nothing until tests are added.

## Project structure

From the visible files, the repository includes:

- `index.js` — main CLI entry point
- `package.json` — project metadata and scripts
- `README.md` — project documentation
- `test-app.zip` — archive of the project contents

The entry file also imports these project modules and data files, which are expected to exist in the full app:

- `src/input.js`
- `src/quiz.js`
- `src/colors.js`
- `data/questions.json`

## How it works

At runtime the app:

1. clears the terminal and shows a banner
2. loads quiz questions from `data/questions.json`
3. asks the user to choose a category
4. asks how many questions to answer
5. runs the quiz question by question
6. displays the final score
7. asks whether the user wants to play again

## Troubleshooting

- **Missing file errors**: If `src/` or `data/questions.json` are not present, the app will not start correctly.
- **Node version issues**: Make sure Node.js 18+ is installed.
- **Invalid JSON**: Check that `data/questions.json` is valid JSON if loading fails.

## License

MIT
