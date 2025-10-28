# Quick Start Guide

This guide will help you quickly get started with updating and maintaining the West Coast Neuroecon website.

## First Steps

### 1. Preview the Site Locally

```bash
quarto preview
```

This opens a live preview in your browser that automatically updates when you save changes to any `.qmd` file.

### 2. Make Your First Edit

Try editing `index.qmd` to update the conference date or location. Save the file and watch the preview update automatically!

## Common Tasks

### Update Conference Dates

1. Open `index.qmd` and replace "TBD 2025" with actual dates
2. Update `program.qmd` with the schedule
3. Update `registration.qmd` with registration deadlines

### Add Speakers

1. Open `speakers.qmd`
2. Replace the placeholder content with speaker information:

```markdown
## Keynote Speaker

### Dr. Jane Smith
**University of Example**

Dr. Smith is a leading researcher in neuroeconomics...

[Website](https://example.com) | [Google Scholar](#)
```

3. Optional: Add speaker photos to `images/speakers/` directory

### Update the Program

1. Open `program.qmd`
2. Update the schedule table with actual times and sessions
3. Add session descriptions and topics

### Add Sponsor Logos

1. Add logo images to `images/sponsors/` directory
2. Open `sponsors.qmd`
3. Add sponsor information:

```markdown
### Platinum Sponsors

![Sponsor Name](images/sponsors/logo.png)

**Sponsor Name** - Brief description
```

## Publishing to GitHub Pages

### Initial Setup

1. Make sure all changes are committed:
```bash
git add .
git commit -m "Update conference website"
git push
```

2. Go to your GitHub repository Settings > Pages
3. Set source to "Deploy from a branch"
4. Select `main` branch and `/docs` folder
5. Save

### Updating the Site

Every time you make changes:

```bash
quarto render              # Build the site
git add .                  # Stage changes
git commit -m "Your message"  # Commit changes
git push                   # Push to GitHub
```

GitHub will automatically deploy your changes in a few minutes.

## File Organization

```
WCNE/
├── _quarto.yml           # Main configuration
├── *.qmd                 # Content pages
├── styles/               # CSS and SCSS files
│   ├── custom.scss       # Theme customization
│   └── styles.css        # Additional styles
├── images/               # Images and logos
│   ├── speakers/         # Speaker photos
│   └── sponsors/         # Sponsor logos
└── docs/                 # Generated website (don't edit directly)
```

## Tips

1. **Always preview before deploying**: Use `quarto preview` to check your changes
2. **Keep it simple**: Quarto uses Markdown - it's easy to learn!
3. **Use headers**: Structure your content with `#`, `##`, `###` for headings
4. **Add images**: Use `![Alt text](path/to/image.png)` to add images
5. **Create links**: Use `[Link text](url)` for links

## Markdown Basics

```markdown
# Large Heading
## Medium Heading
### Small Heading

**Bold text**
*Italic text*

- Bullet point
- Another point

1. Numbered list
2. Second item

[Link](https://example.com)
![Image](path/to/image.png)
```

## Styling Boxes

Use these special boxes in your content:

```markdown
::: {.info-box}
This is an information box
:::

::: {.important-box}
This is an important notice box
:::
```

## Need Help?

- [Quarto Documentation](https://quarto.org/docs/guide/)
- [Markdown Guide](https://www.markdownguide.org/)
- Email: wcneuroecon@gmail.com

## Troubleshooting

**Site won't build?**
- Check for syntax errors in `.qmd` files
- Make sure YAML front matter is correct (between `---`)

**Changes not showing on GitHub Pages?**
- Wait a few minutes for deployment
- Check that you ran `quarto render` before pushing
- Verify Settings > Pages is configured correctly

**Preview not working?**
- Make sure you're in the project directory
- Check that Quarto is installed: `quarto --version`
