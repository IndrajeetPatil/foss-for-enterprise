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
<https://indrajeetpatil.github.io/foss-for-enterprise/>

<a href="https://indrajeetpatil.github.io/foss-for-enterprise/" target="_blank">
<img src="media/dependency.png" alt="FOSS for Enterprise - Dependency" width="500"/>
</a>

## Scope

This presentation focuses on **inbound FOSS** (using open source software in your products).

**Outbound FOSS** (releasing your software as open source) is out of scope.

# Development

This project uses Python 3.13+ with [uv](https://docs.astral.sh/uv/) for dependency management, [Quarto](https://quarto.org/) for rendering slides, and [just](https://github.com/casey/just) as a command runner.

## Prerequisites

```bash
# Install just (macOS)
brew install just
```

## Setup

```bash
# Install dependencies
just install

# Or update to latest versions
just update
```

## Common Commands

```bash
just help      # Show all available commands
just render    # Render slides to HTML
just preview   # Live preview with auto-reload
just open      # Open rendered slides in browser
just clean     # Remove generated files
just check     # Check Quarto and Python setup
just           # Install, render, and open slides (default)
```

## Acknowledgments

The dependency illustration in the title slide is from [xkcd #2347: Dependency](https://xkcd.com/2347/) by Randall Munroe, licensed under [Creative Commons Attribution-NonCommercial 2.5 License](https://creativecommons.org/licenses/by-nc/2.5/).

# Feedback

I'd love to hear thoughts and comments [here](https://github.com/IndrajeetPatil/foss-for-enterprise/issues).

# Code of Conduct

Please note that the foss-for-enterprise project is released with a [Contributor Code of Conduct](https://www.contributor-covenant.org/version/3/0/code_of_conduct/). By contributing to this project, you agree to abide by its terms.
