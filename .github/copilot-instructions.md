## Copilot Instructions for `website-links`

This project is a static HTML link page designed for sharing personal links and social media profiles. It leverages Bootstrap 5 for responsive design and styling.

### 1. Architecture Overview

The project consists of a single `index.html` file, which is a standalone page. There are no backend services, complex data flows, or JavaScript frameworks involved. All content is directly embedded in the HTML.

### 2. Styling Guidelines

Styling is managed through a combination of Bootstrap CSS, a custom `css/styles.css` file, and `scss/styles.scss` for Sass-based overrides.

- **`index.html`**: Links directly to `css/styles.css` for custom styles.
- **`css/styles.css`**: Contains custom CSS rules that define the color scheme, fonts, and specific element styles.
- **`scss/styles.scss`**: This file is intended for overriding Bootstrap's default Sass variables (e.g., `$primary`, `$body-bg`). **Note:** For changes in `scss/styles.scss` to take effect, they must be compiled into CSS. There is no automated build process configured in `package.json` for this compilation. If changes are made here, a manual or external Sass compilation step is required.

**Recommendation for AI Agents:**

- When modifying or adding styles, prioritize using Bootstrap utility classes where possible.
- For custom styles beyond Bootstrap, add them to `css/styles.css`.

### 3. Key Dependencies

- **Bootstrap 5**: Used for the overall layout, components, and responsive behavior.
- **Bootstrap Icons**: Provides a set of vector icons used throughout the page.
- **Google Fonts (Lato, Lora)**: Imported via `<link>` tags in `index.html` for typography.

### 4. Development Workflow

There is no explicit build, test, or debugging workflow defined within the `package.json` scripts. Development primarily involves direct editing of `index.html`, `css/styles.css`, and `scss/styles.scss` (with manual Sass compilation if `scss/styles.scss` is modified).

### 5. Project-Specific Conventions

- **Link Cards**: Interactive link elements (`.link-card`) have custom hover effects defined in `css/styles.css` and `scss/styles.scss` (if compiled). These effects provide a subtle scaling and shadow animation.
- **Color Scheme**: A specific, calming color scheme (muted teal, rosy red, cream, dark grey) is established in `css/styles.css`.

### Key Files and Directories

- `index.html`: The main and only HTML file.
- `css/styles.css`: Custom CSS rules.
- `scss/styles.scss`: Sass variables and custom styles (requires compilation).
- `package.json`: Basic project metadata.
