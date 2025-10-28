# West Coast Neuroecon 2025 Website

This is the official website for the West Coast Neuroeconomics Mini-Symposium 2025, hosted at UCLA and organized by Ian Krajbich and Kianté Fernandez.

## About

The West Coast Neuroecon symposium is an annual gathering of researchers, scholars, and practitioners in neuroeconomics from across the West Coast and beyond. The symposium features invited talks, contributed presentations, and poster sessions covering all aspects of neuroeconomics research.

## Website Structure

The website is built using [Quarto](https://quarto.org/), a scientific publishing system that makes it easy to create professional academic websites.

### Pages

- **Home** (`index.qmd`) - Landing page with conference overview
- **About** (`about.qmd`) - Information about the symposium and neuroeconomics
- **Program** (`program.qmd`) - Schedule and session details
- **Speakers** (`speakers.qmd`) - Invited speakers and presenters
- **Registration** (`registration.qmd`) - Registration information and fees
- **Venue** (`venue.qmd`) - Location details, travel, and accommodations
- **Organizers** (`organizers.qmd`) - Symposium organizers and contacts
- **Sponsors** (`sponsors.qmd`) - Sponsorship information and acknowledgments

## Building the Website

### Prerequisites

- [Quarto](https://quarto.org/docs/get-started/) must be installed on your system

### Build Commands

To render the website locally:

```bash
quarto render
```

To preview the website with live reload:

```bash
quarto preview
```

The rendered website will be in the `docs/` directory.

## Customization

### Styling

The website uses a custom color scheme based on UCLA colors:
- Primary: UCLA Blue (#003B5C)
- Secondary: UCLA Gold (#FFD100)

Styles are defined in:
- `styles/custom.scss` - SCSS variables and component styles
- `styles/styles.css` - Additional CSS styling

### Configuration

Main website configuration is in `_quarto.yml`, including:
- Navigation menu structure
- Theme settings
- Footer content
- Output directory

### Images

Place images in the `images/` directory. You may want to add:
- Favicon (`images/favicon.png`)
- UCLA or conference logos
- Photos of speakers and organizers
- Venue photos

## Deployment

### GitHub Pages

To deploy to GitHub Pages:

1. Ensure the `output-dir: docs` setting is in `_quarto.yml` (already configured)
2. Commit and push all changes to your GitHub repository
3. Go to repository Settings > Pages
4. Set source to "Deploy from a branch"
5. Select the `main` branch and `/docs` folder
6. Save and wait for deployment

The `.nojekyll` file in the docs directory ensures GitHub Pages renders the site correctly.

### Custom Domain

To use a custom domain:
1. Add a `CNAME` file to the docs directory with your domain name
2. Configure DNS settings with your domain provider
3. Enable custom domain in GitHub Pages settings

## Updating Content

### Adding Content

All content pages are written in Quarto Markdown (`.qmd` files). Edit these files to update content.

After making changes:
1. Run `quarto render` to rebuild the site
2. Check the output in `docs/`
3. Commit and push changes

### Common Updates

**Update dates and deadlines:**
- Edit the relevant `.qmd` files (especially `index.qmd`, `program.qmd`, `registration.qmd`)
- Replace "TBD" with actual dates

**Add speakers:**
- Edit `speakers.qmd`
- Add speaker information, photos, and bios
- Consider creating a data file for easier management

**Update program schedule:**
- Edit `program.qmd`
- Update the schedule table with session details

**Add sponsors:**
- Edit `sponsors.qmd`
- Add sponsor logos to `images/sponsors/`
- Update sponsor tier listings

## Maintenance Tips

1. **Keep content updated**: Regularly update TBD items as information becomes available
2. **Test locally**: Always run `quarto preview` before deploying
3. **Check links**: Verify all internal and external links work correctly
4. **Optimize images**: Compress images before adding to reduce page load time
5. **Mobile testing**: Check the site on mobile devices for responsive design

## Contact

For questions about the website or the symposium:
- Email: wcneuroecon@gmail.com

## License

See [LICENSE](LICENSE) file for details
