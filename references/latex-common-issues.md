# LaTeX Common Issues Reference

Common LaTeX problems to check for, organized by category.

## References and Cross-References

### Undefined References
- \ref{label} or \eqref{label} pointing to a label that doesn't exist
- Usually shows as "??" in compiled PDF
- Check: every \ref{} has a corresponding \label{} somewhere

### Orphaned Labels
- \label{} defined but never referenced with \ref{}
- Not an error, but indicates unused structure

### Citation Issues
- \cite{key} with no matching entry in .bib file or \bibitem
- Bibliography entries that are never \cited (orphaned references)
- Missing bibliography file (\bibliography{} pointing to non-existent .bib)
- Wrong bibliography style for the required citation format

### Non-Breaking Spaces
- Always use ~ before \cite: "as shown by Smith~\cite{smith2023}"
- Always use ~ before \ref: "see Figure~\ref{fig:results}"
- Prevents line breaks between the word and the reference number

## Environments

### Mismatched Environments
- Every \begin{X} needs a matching \end{X}
- Nested environments must be properly closed in order
- Common: forgetting \end{itemize}, \end{enumerate}, \end{figure}

### Float Placement
- Figures and tables are floats; LaTeX places them where it sees fit
- Use placement specifiers: [htbp] or [H] (requires float package)
- [H] forces exact placement but can cause bad page breaks
- [htbp] gives LaTeX flexibility (usually best)

### Missing Captions
- Every figure and table should have \caption{}
- \caption should go BELOW figures, ABOVE tables (convention)
- \label{} must come AFTER \caption{} (otherwise \ref will be wrong)

## Text Formatting

### Quotation Marks
- WRONG: "quoted text" (straight quotes)
- RIGHT: ``quoted text'' (LaTeX proper quotes)
- Or use the csquotes package: \enquote{quoted text}

### Ellipsis
- WRONG: ... (three periods)
- RIGHT: \ldots or \dots

### Hyphens, En Dashes, Em Dashes
- Hyphen (-): compound words (well-known)
- En dash (--): ranges (pages 1--5) — BUT this skill forbids en dashes
- Em dash (---): parenthetical — BUT this skill forbids em dashes
- For this skill: use hyphens for compounds only, "to" for ranges,
  and restructure sentences to avoid em/en dash usage

### Paragraph Breaks
- WRONG: using \\ or \\[space] for paragraph breaks
- RIGHT: leave a blank line between paragraphs
- \\ is for line breaks within an environment (tabular, align, etc.)

## Math Mode

### Variables Outside Math Mode
- Single-letter variables should be in math mode: $x$, $n$, $k$
- Multi-letter identifiers should use \text{} or \mathrm{}: $\text{score}$
- Numbers in running text don't need math mode

### Equation Numbering
- Use equation environment for important equations that are referenced
- Use equation* or \[ \] for equations that don't need numbers
- Don't number equations you never reference

### Common Math Issues
- Using * for multiplication instead of \times or \cdot
- Missing \left and \right for auto-sizing brackets
- Using | | instead of \| \| or \lVert \rVert for norms

## Bibliography

### Style Consistency
- All entries should follow the same format
- Author names should be consistent (don't mix "John Smith" and "Smith, J.")
- Journal names should be consistent (don't mix abbreviated and full)
- Check year, volume, pages are present for journal articles
- Check publisher, address for books

### Common BibTeX Issues
- Special characters in titles need braces: {DNA} not DNA (prevents lowercasing)
- Accented characters need proper LaTeX encoding
- URLs should use \url{} command (requires url or hyperref package)
- DOIs should be included when available

## Document Structure

### Preamble Issues
- Missing required packages
- Package conflicts (e.g., loading two packages that redefine the same command)
- Package loaded but never used (minor, but clean code is good)
- Options passed to documentclass that conflict

### Section Numbering
- Consistent depth (don't jump from \section to \subsubsection)
- Not too deep (avoid \paragraph and \subparagraph unless the style requires it)

### Table of Contents
- If required, is \tableofcontents present?
- Are List of Figures / List of Tables required and present?
- Do section titles in TOC match the actual section titles?

### Page Layout
- Are margins set as required? (geometry package)
- Is line spacing set as required? (setspace package: \singlespacing,
  \onehalfspacing, \doublespacing)
- Is the font correct? (check documentclass options or font packages)
- Are page numbers present and correctly positioned?

## Compilation Warnings

These won't break the document but indicate problems:
- "Overfull \hbox": text extends past the margin (fix: rephrase or add hyphenation)
- "Underfull \hbox": text is too spread out (fix: rephrase)
- "Label(s) may have changed": recompile to fix references
- "There were undefined references": something \ref'd doesn't have a \label
- "Empty bibliography": .bib file has no entries or isn't being read
