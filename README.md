# Podium Fetch

## This repo has 3 parts:

1. `index.html`, `games.json` and `assets/` are for the frontend website, **do not upload any other files to the frontend!**
1. `scrape.mjs` generates the `games.json` file, and saturates the `assets/` directory. `package.json` comes with `scrape.mjs`
1. `saturate.js` is only for PoCs to get emails of participants along with their names in the `saturated.json` file

## To run:

Run `scrape.mjs` and follow the TUI instructions

```bash
npm install
```

```bash
node scrape.mjs
```

## To saturate:

First make sure `games.json` exists already, then read the comments inside `saturate.py`

Get an export of `Legal First Name,Legal Last Name,Email` from Attend. Paste it as `participants.csv` in this folder. Then run:

```bash
node saturate.js
```

It may prompt you in case of conflicts.

## To deploy:

Copy the `index.html`, `games.json` and `assets/` into a new folder or repo so that they're the only files inside. It is optional but recommended to delete the `id` and `votes` field from `games.json` before publishing.
