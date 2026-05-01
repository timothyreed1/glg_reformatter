# GLG Response Formatter

A lightweight local browser tool for reformatting raw GLG expert network profile exports into clean, readable markdown.

## Setup

1. Clone or download the repo
2. Rename the file `config.js-template` to `config.js` in the same folder as `glg_reformatter_openai.html` and edit to replate `yourKeyHere` to your actual OpenAI API key.

```javascript
const OPENAI_API_KEY = 'sk-yourKeyHere';
```

3. Open `glg_reformatter_openai.html` in a browswer.

> If your browser blocks local HTML or `file://` URLs, switch browsers of run a local server (`python3 -m http.server 8000`) and open `localhost:8000/glg_reformatter_openai.html`.

## Usage

- Open your profile questions at `https://members.glgresearch.com/profile-questions/`
- Select the page content and copy
- Paste raw content into the left box
- Click **Format**
- Copy the output from the right box

## Features

- Formats each question as a numbered list item
- Converts vendor experience grids into sorted markdown tables
- Converts comments into bullet lists
- Strips dates and redundant labels

## Requirements

- OpenAI API key (uses `gpt-4o-mini`)
- No dependencies or build

## Distribution

Do not include `config.js` when sharing -- recipients add their own key.
