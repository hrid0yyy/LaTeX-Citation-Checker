# LaTeX Citation Checker

A browser-based tool to compare citations between your source LaTeX document and its summary/condensed version.

## What It Does

Extracts all `\cite{}` keys from two text inputs and shows you which citations are missing in your summary.

## Use Case

**Perfect for:**
- Creating paper summaries while ensuring all references are preserved
- Condensing drafts without losing citation coverage
- Verifying that shortened versions maintain proper attribution
- Quality-checking literature reviews and reference sections

## How to Use

1. **Paste your full source text** (left panel) — the complete LaTeX document with all citations
2. **Paste your summary text** (right panel) — the condensed/shortened version
3. **Click "Analyze Citations"** (or press Ctrl/Cmd+Enter)

## Results

The tool shows:
- **Missing Citations** — keys in source but not in summary (⚠️ these need attention)
- **Shared Citations** — keys present in both texts
- **Extra Citations** — keys only in summary (might be new additions)
- **Source/Summary Keys** — complete lists from each text

All citation lists can be copied with one click.

## Technical Details

- Uses regex pattern: `\\cite\{([^}]*)\}`
- Handles multi-key citations: `\cite{Smith2020,Jones2019}`
- Automatically deduplicates and sorts keys
- Works entirely in-browser (no server needed)

## Example

```latex
Source:    \cite{Smith2020,Jones2019} and \cite{Lee2021}
Summary:   \cite{Smith2020}

Missing:   Jones2019, Lee2021
```

---

**No installation required** — just open the HTML file in any modern browser.
