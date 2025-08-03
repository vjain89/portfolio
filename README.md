# Vijay Jain - Portfolio Website

A clean, professional portfolio website showcasing hardware engineering projects and research work.

## Features

- **Clean Design**: Minimalist layout with consistent navigation using modern Inter typography
- **Project Grid**: Homepage displays projects in various tile sizes (1x1, 1x2, 2x1)
- **Markdown Content**: Individual markdown files for each project - easy to write and maintain
- **Template-Based**: Single template file handles all project pages dynamically
- **Responsive Design**: Works on desktop and mobile devices
- **Consistent Navigation**: Name links back to homepage, proper project navigation

## Structure

- `index.html` - Homepage with project grid
- `about.html` - About page with personal information
- `project-template.html` - Single template for all project pages
- `projects.json` - Configuration file for project metadata (visibility, ordering, tile sizes)
- `projects/` - Directory containing individual markdown files for each project

## Architecture

### Content Management
- **Single Source of Truth**: All project content and metadata is stored in markdown files
- **YAML Front Matter**: Metadata (title, description, location, image, size) is stored in YAML at the top of each markdown file
- **Automatic Extraction**: The template automatically extracts all metadata from markdown
- **Configuration**: `projects.json` only contains display settings (visibility, file links)
- **Template**: `project-template.html` loads markdown and converts to HTML

### Benefits
- **No Duplication**: Write content once in markdown, used everywhere
- **Complete Metadata**: All project information (including image and size) in one place
- **Maintainable**: Edit project content in simple markdown files
- **No Boilerplate**: Markdown files contain only content, no HTML
- **Consistent Styling**: All projects use the same template and CSS
- **Easy to Add**: New project = new markdown file + one line in JSON
- **Version Control Friendly**: Markdown is human-readable and diff-friendly

## Customization

### Adding New Projects

1. Add project configuration to `projects.json`:
```json
{
  "link": "new-project.md",
  "visible": true
}
```

2. Create a markdown file `projects/new-project.md`:
```markdown
---
image: images/new-project.jpg
size: [1, 1]
---

# PROJECT-NAME

**Description:** Brief description  
**Location:** Institution | Location

## Project Overview

Your project overview here...

## Technical Details

Technical details here...

## Implementation

Implementation details here...
```

### Modifying Project Information

- **All Content & Metadata**: Edit the `.md` files - everything is extracted automatically
- **Display Settings**: Edit `projects.json` for visibility only
- **Styling**: All styling is centralized in the template files

## Running the Website

Simply open `index.html` in a web browser. No server required - it's a static website.

## Project Tile Sizes

- `[1, 1]` - Square tile
- `[1, 2]` - Tall rectangle (1 wide, 2 tall)
- `[2, 1]` - Wide rectangle (2 wide, 1 tall)

## Navigation

- Click on your name to return to homepage
- Click on "About" to view the about page
- Click on project tiles to view detailed project pages
- On project pages, the current project is underlined in the navigation

## Typography

- **Font**: Inter (modern geometric sans-serif)
- **Weights**: 300, 400, 500, 600, 700
- **Clean Spacing**: Consistent margins and padding
- **Modern Design**: Inspired by contemporary portfolio websites

## Content Writing

Write your project content in markdown format. The template supports:
- **Headers**: `#`, `##`, `###`
- **Bold**: `**text**`
- **Italic**: `*text*`
- **Paragraphs**: Natural line breaks

Example:
```markdown
# PROJECT TITLE

**Description:** Brief description  
**Location:** Institution | Location

## Overview

Your project overview...

## Technical Details

Technical information...

## Results

Project outcomes...
```
