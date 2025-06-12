# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This repository contains a comprehensive learning guide for Python in scientific software development, specifically designed for DMI (Danish Meteorological Institute) researchers. The project consists of presentation slides and supporting materials that provide curated learning pathways from beginner to advanced Python development.

### Content Structure

- `slides.md` - Main presentation in Slidev format covering the complete learning roadmap
- `notes.md` - Detailed speaker notes with timing and talking points for each slide
- `objective.md` - Project purpose and goals
- `images/` - Supporting visual assets for the presentation
- `old/` - Archive of previous versions and iterations

## Presentation Technology

The main presentation (`slides.md`) is built for **Slidev** (https://sli.dev), a modern presentation framework that uses:
- Markdown for content structure
- Vue.js components for interactivity
- Tailwind CSS for styling
- Syntax highlighting with Shiki
- Web-based presentation with navigation controls

### Slidev Configuration
- Theme: default
- Transition: slide-left/fade-out
- Line numbers: disabled
- Background: Unsplash collection imagery

## Content Themes

The presentation covers five key learning areas:

1. **Learning Resources** - Curated platforms, books, and online courses
2. **Scientific Python Stack** - NumPy, Pandas, Xarray, Matplotlib, domain-specific libraries
3. **Development Practices** - Clean code, SOLID principles, DRY, testing with pytest
4. **Modern Tools** - IDEs (VS Code, PyCharm, JupyterLab), package managers (uv, conda)
5. **AI-Assisted Development** - Effective use of LLMs for code generation and improvement

## Target Audience

- DMI researchers ranging from complete beginners to intermediate Python users
- Focus on scientific computing applications
- Emphasis on meteorological and climate data processing
- Professional software development practices for research code

## Maintenance Guidelines

When updating content:
- Maintain the Slidev markdown format with proper frontmatter
- Keep the 20-week learning roadmap structure intact
- Ensure speaker notes align with slide content
- Update resource links and verify they remain accessible
- Consider the scientific computing context when adding new tools or libraries

## File Dependencies

- Slides reference external images from Unsplash collections
- Speaker notes contain detailed timing estimates (1-5 minutes per slide)
- Images directory contains local assets for specific tools and books
- Content is designed for a 45-60 minute presentation format