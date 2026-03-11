# data-model

A standardized data model specification built with [Bikeshed](https://tabatkins.github.io/bikeshed/).

## Overview

This repository contains a W3C-style specification document that defines a comprehensive data model for consistent data representation and exchange.

## Project Structure

- **`index.bs`**: The main Bikeshed source file for the specification. It pulls together all entity tables, vocabularies, and examples.
- **`entities/`**: Contains HTML tables that define the core entities in the data model (for example `person.html`, `address.html`, `date-of-birth.html`).
- **`vocabulary/`**: Contains HTML files that define controlled vocabularies and code lists used by the entities (for example `gender.html`, `status-code.html`).
- **`examples/`**: Contains JSON example files that illustrate how to represent entities and structures defined in the spec (for example `person.json`).

## Viewing the Specification

The specification is automatically deployed to GitHub Pages and can be viewed at:
- **Live Specification**: https://socialcaredata.github.io/data-model/

## Building Locally

To build the specification locally:

1. Install Bikeshed:
   ```bash
   pip install bikeshed
   bikeshed update
   ```

2. Build the specification:
   ```bash
   bikeshed spec index.bs index.html
   ```

3. Open `index.html` in your browser to view the generated specification.

## GitHub Actions Deployment

The specification is automatically built and deployed to GitHub Pages using GitHub Actions. The deployment workflow is triggered:

- On release (when a new release is published)
- Manually via workflow dispatch
- On push to the main branch (when `index.bs` or shema related files - entities, vocabularies, examples - change)

To manually trigger a deployment:
1. Go to the Actions tab in the GitHub repository
2. Select the "Deploy Bikeshed to GitHub Pages" workflow
3. Click "Run workflow"

## Contributing

To contribute to this specification:

1. Edit the `index.bs` file with your changes
2. Test the build locally using bikeshed
3. Commit and push your changes
4. Create a pull request

## License

This specification is maintained by the ODI Development Team.
