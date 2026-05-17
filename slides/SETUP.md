# Setting Up the JPMC Slide Framework in VS Code

## Step 1: Install the Marp Extension
1. Open VS Code Extensions (Ctrl+Shift+X)
2. Search "Marp for VS Code"
3. Install it (publisher: marp-team) — no admin required

## Step 2: Configure VS Code to find the theme
Add this to your VS Code settings (open with Ctrl+Shift+P → "Open User Settings JSON"):

```json
"markdown.marp.themes": [
  "${workspaceFolder}/slides/jpmc-theme.css"
]
```

## Step 3: Open any .md slide file
- Open `slides/template.md`
- Click the preview icon (top right) or press Ctrl+Shift+V
- You should see the slides render with JPMC styling

## Step 4: Export to PowerPoint or PDF
- Open Command Palette: Ctrl+Shift+P
- Type "Marp: Export Slide Deck"
- Choose .pptx or .pdf
- No additional software needed

## Creating a New Deck
1. Copy `slides/template.md` and rename it
2. Ask Copilot: "Create a slide deck about [your topic] using the JPMC slide framework"
3. Copilot will read `.github/copilot-instructions.md` and generate proper slides

## Fonts Note
The theme uses Garamond/Georgia (serif) and Calibri/Segoe UI (sans) — both standard
on Windows work laptops. These are close substitutes for JPMC Tiangong and JPMC Sans.
No installation needed.
