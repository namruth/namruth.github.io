# Homepage Documentation - namruth.github.io

## Overview
This documentation explains the structure and components of your personal website's homepage (`index.html`). The site is built using HTML with Pandoc-style Markdown syntax for better readability and maintenance.

## File Structure
```
namruth.github.io/
├── index.html           # Main homepage
├── about-me/           
│   └── index.html      # About page
└── projects/
    └── index.html      # Projects showcase
```

## Homepage Components

### 1. Navigation Section
```markdown
:::: nav-container
::: nav-links
[Home](/) [About](/about-me)
[Projects](/projects)
[Publications](#publications) [Contact](#contact)
:::
::::
```
- Uses nested divs with classes `nav-container` and `nav-links`
- Links to different sections and pages
- The `::::` and `:::` syntax creates nested div elements with respective classes

### 2. Hero Section
```markdown
::::: {.section .hero}
# Namruth Reddy

Security Engineer at NVIDIA | Machine Learning Researcher

::: latest-research
Latest Publication: Temporal Analysis and CWE Code Prediction for
Software Vulnerabilities (IEEE CSITSS 2024)
:::

::: social-links
[](https://www.linkedin.com/in/namruth-reddy/){target="_blank"}
[](https://github.com/namruth){target="_blank"}
[](mailto:namruth@outlook.com)
:::
:::::
```
- Main introductory section with name and title
- Latest research highlight
- Social media links
- The `{.section .hero}` syntax adds multiple classes to the div

### 3. Featured Content Section
```markdown
:::::: {.section .featured-content}
::: card
### Research Focus
...
[View Publications](#publications){.button}
:::

::: card
### Industry Experience
...
[Learn More](/about-me){.button}
:::

::: card
### Projects & Tools
...
[View Projects](/projects){.button}
:::
::::::
```
- Three cards highlighting key areas
- Each card has:
  - Heading
  - Description text
  - Call-to-action button
- Uses `.card` class for styling

### 4. Publications Section
```markdown
::::::::::::::::: {#publications .section .publications-section}
:::::::::::::::: publications-container
## Research Publications

::::::::::::::: publications-grid
:::::: publication-card
...
::::::
:::::::::::::::
::::::::::::::::
:::::::::::::::::
```
- Complex nested structure for publications
- Each publication card contains:
  - Title
  - Conference details
  - Abstract
  - Tags
- Uses multiple levels of nesting for proper organization

### 5. Contact Section
```markdown
::::::::::: {#contact .section .contact-section}
:::::::::: contact-container
## Contact Me

::::::::: contact-info
:::: contact-item
...
::::
:::::::::
::::::::::
:::::::::::
```
- Contact information with multiple methods
- Organized in card-like items
- Each contact item has an icon and details

## Special Syntax Elements

1. **Section Classes**
   - `{.section .classname}` adds multiple classes
   - `{#idname .classname}` adds both ID and class

2. **Links**
   - `[Text](URL)` - Basic link
   - `[Text](URL){target="_blank"}` - Link that opens in new tab
   - `[Text](URL){.button}` - Link styled as button

3. **Nesting Levels**
   - More colons (`:`) indicate deeper nesting
   - Must be balanced (same number at start and end)
   - Used for creating nested div structures

## Making Changes

### Adding a New Section
1. Create a new section using the appropriate nesting level:
```markdown
::::: {.section .new-section}
## New Section Title
Content here
:::::
```

### Modifying Navigation
1. Add new link in the nav-links section:
```markdown
::: nav-links
[Home](/) [NewPage](/new-page)
:::
```

### Adding a New Publication
1. Copy an existing publication-card structure
2. Update the content while maintaining the nesting levels
```markdown
:::::: publication-card
::::: publication-content
### New Publication Title
...
:::::
::::::
```

## Best Practices
1. Maintain consistent nesting levels
2. Use appropriate number of colons for nesting
3. Keep class names consistent with existing ones
4. Test links before committing changes
5. Maintain the hierarchical structure when adding new sections

## Notes
- The Pandoc-style Markdown syntax is used for better organization and readability
- Classes and IDs are important for styling and JavaScript functionality
- Maintaining proper nesting is crucial for the structure to work correctly