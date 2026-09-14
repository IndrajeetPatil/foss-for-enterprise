# FOSS for Enterprise

This presentation provides a comprehensive overview of Free and Open Source Software (FOSS) for enterprise use, focusing on inbound FOSS consumption.

## Topics Covered

- **FOSS Movement**: Free Software Foundation vs. Open Source Initiative
- **Software Licenses**: Understanding reciprocal (copyleft) vs. permissive licenses
- **Legal Aspects**: When licenses matter and what triggers obligations
- **Enterprise Risks**: License compliance, security vulnerabilities, and sustainability concerns
- **Case Studies**: Real-world examples including Equifax, Log4Shell, Heartbleed, license violations, and sustainability failures
- **Automated Tools**: Using Trivy and Black Duck for FOSS management
- **Worth it?**: Why FOSS is essential for modern software development

The slides can be seen here:<br>
<https://www.indrapatil.com/foss-for-enterprise/>

<a href="https://www.indrapatil.com/foss-for-enterprise/" target="_blank" rel="noopener noreferrer">
<img src="media/dependency.webp" alt="FOSS for Enterprise - Dependency" width="500"/>
</a>

## Scope

This presentation focuses on **inbound FOSS** (using open source software in your products).

**Outbound FOSS** (releasing your software as open source) is out of scope.

## Development

This project uses Python 3.14 (see `.python-version`) with [uv](https://docs.astral.sh/uv/) for dependency management, [Quarto](https://quarto.org/) for rendering slides, and [just](https://github.com/casey/just) as a command runner.

### Prerequisites

```bash
# Install just (macOS)
brew install just
```

### Setup

```bash
just install
```

### Just Commands

```bash
just help     # Show all available commands
just install  # Install Python dependencies and the a11y extension
just update   # Update Python dependencies
just render   # Render slides to HTML
just preview  # Start a live preview with auto-reload
just open     # Alias for preview (live-reload dev server over localhost)
just clean    # Remove generated files and caches
just check    # Check the Quarto and Python setup
just axe      # Preview with an accessibility report slide
just          # Install dependencies and start live-reload preview
```

Quarto commands run through `uv run`, which syncs the locked environment and makes
the project Python interpreter available automatically.

`just axe` opts into the `_quarto-a11y.yml` profile for local accessibility audits.
Normal renders and deployments do not include the axe checker or report slide.
Preview options can be forwarded, for example `just axe --no-browser --port 4200`.

### Accessibility

`just install` and the shared CI workflow install the latest
[`quarto-revealjs-a11y`](https://github.com/mcanouil/quarto-revealjs-a11y) directly
from upstream with `quarto add mcanouil/quarto-revealjs-a11y --no-prompt`.
The extension handles browser zoom, slide isolation, focus indicators, link
underlines, reduced motion, and screen-reader announcements.

Run `just install` again after `just clean`, which removes installed extensions.

The `accessibility.html` helper still handles scrollable code, slide-menu focus,
and vertical-slide semantics. Unused tabset handling has been removed.
The extension's slide-menu patch and accessibility settings panel are disabled
as in the reference deck: version 0.2.3 introduces ARIA and contrast failures in
those components.

Use `just axe` to inspect slides, fragments, and menu panels in presentation and
scroll views. Normal builds omit the axe checker.

## Feedback

Feedback and suggestions are welcome in [the issue tracker](https://github.com/IndrajeetPatil/foss-for-enterprise/issues).

## Acknowledgments

The dependency illustration in the title slide is from [xkcd #2347: Dependency](https://xkcd.com/2347/) by Randall Munroe, licensed under [Creative Commons Attribution-NonCommercial 2.5 License](https://creativecommons.org/licenses/by-nc/2.5/).
