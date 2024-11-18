# Personal Website Project using Claude

## Project Overview
This repository contains code and documentation for creating a personal portfolio website using GitHub Pages. The project was developed with assistance from Claude (Anthropic's AI) and includes a homepage, about page, and projects showcase.

## Table of Contents
- [Project Structure](#project-structure)
- [Setup Instructions](#setup-instructions)
- [Working with Claude](#working-with-claude)
- [Page Components](#page-components)
- [Making Updates](#making-updates)
- [Styling Guide](#styling-guide)
- [Troubleshooting](#troubleshooting)

## Project Structure
```
namruth.github.io/
├── index.html           # Homepage
├── about-me/           
│   └── index.html      # About page
└── projects/
    └── index.html      # Projects showcase
```

## Setup Instructions

### 1. Initial Setup with GitHub Pages
1. Create a new repository named `username.github.io`
2. Clone the repository locally
3. Create the basic file structure

```bash
mkdir about-me projects
touch index.html about-me/index.html projects/index.html
```

### 2. File Creation Process
When working with Claude:
1. Request the HTML file content
2. Specify any custom requirements
3. Save the provided code in appropriate files
4. Test locally before pushing to GitHub

## Working with Claude

### 1. Creating New Pages
Example prompt for creating a new page:
```
"Can you help create a [page type] page with the following sections:
- [List of required sections]
- [Specific features needed]
Please maintain consistent styling with existing pages."
```

### 2. Making Updates
Example prompt for updates:
```
"Can you help update the [file name] to:
- Add [new feature]
- Modify [existing section]
- Fix [specific issue]"
```

### 3. Best Practices for Claude Interaction
- Provide existing code when requesting modifications
- Be specific about styling preferences
- Ask for explanations of complex sections
- Request documentation for future reference

## Page Components

### 1. Homepage (index.html)
Key sections:
- Navigation bar
- Hero section
- Featured content cards
- Publications section
- Contact section

Syntax pattern for homepage markdown:
```markdown
:::: nav-container
::: nav-links
[Home](/) [About](/about-me)
[Projects](/projects)
[Publications](#publications) [Contact](#contact)
:::
::::
```

### 2. About Page
Key sections:
- Professional experience
- Education
- Technical skills
- Academic achievements

Important style elements:
```css
:root {
    --primary-color: #2d3748;
    --secondary-color: #4a5568;
    --accent-color: #3182ce;
    --text-color: #2d3748;
    --light-bg: #f7fafc;
    --hover-color: #2c5282;
}
```

### 3. Projects Page
Key sections:
- Security Tools
- Research Projects
- Security Automation

## Making Updates

### 1. Adding New Content

#### Adding a New Project
```html
<article class="project-card">
    <div class="project-content">
        <h3>Project Title</h3>
        <p>Project description</p>
        <div class="project-tags">
            <span class="tag">Tag1</span>
            <span class="tag">Tag2</span>
        </div>
        <div class="project-links">
            <a href="project-url" target="_blank">
                <i class="fab fa-github"></i> View Code
            </a>
        </div>
    </div>
</article>
```

#### Adding a New Publication
```markdown
:::::: publication-card
::::: publication-content
### Publication Title
::: publication-meta
[Conference Name]{.conference} [Year]{.year}
[Paper ID: XXX]{.paper-id}
:::
Abstract text here
::: publication-tags
[Tag1]{.tag} [Tag2]{.tag}
:::
:::::
::::::
```

### 2. Modifying Styles
Key CSS classes and their purposes:
- `.section` - Main content sections
- `.card` - Content cards
- `.tag` - Skill and project tags
- `.button` - Call-to-action buttons

## Styling Guide

### 1. Color Scheme
```css
--primary-color: #2d3748;   /* Main text and headings */
--secondary-color: #4a5568; /* Secondary text */
--accent-color: #3182ce;    /* Links and highlights */
--light-bg: #f7fafc;        /* Background color */
--hover-color: #2c5282;     /* Hover states */
```

### 2. Typography
- Font Family: system-ui, -apple-system, 'Segoe UI', Roboto, sans-serif
- Heading Sizes:
  - h1: 2.5rem
  - h2: 1.5rem
  - h3: 1.25rem

### 3. Spacing
- Section padding: 4rem 2rem
- Card padding: 1.5rem
- Grid gap: 2rem

## Troubleshooting

### Common Issues and Solutions

1. Navigation Links Not Working
- Ensure paths are correct relative to root
- Check for proper markdown link syntax
- Verify file structure matches paths

2. Styling Inconsistencies
- Check root CSS variables
- Verify class names match exactly
- Ensure proper nesting of markdown sections

3. Mobile Responsiveness
- Test with different viewport sizes
- Use responsive units (rem, %, vh/vw)
- Check media queries if needed

### Getting Help from Claude
When encountering issues:
1. Share the specific code section having problems
2. Describe the expected vs actual behavior
3. Include any error messages
4. Ask for step-by-step solutions

## Maintenance Tips

1. Regular Updates
- Keep publications current
- Update project descriptions
- Refresh technical skills
- Check all external links

2. Version Control
- Commit meaningful changes
- Use clear commit messages
- Keep local backup of content

3. Testing
- Test locally before pushing
- Verify all links work
- Check mobile responsiveness
- Validate HTML and CSS

## Resources
- Font Awesome Icons: [https://fontawesome.com/icons](https://fontawesome.com/icons)
- GitHub Pages Documentation: [https://docs.github.com/pages](https://docs.github.com/pages)
- Markdown Guide: [https://www.markdownguide.org](https://www.markdownguide.org)