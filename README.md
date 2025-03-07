This is Template repo for creating a workspace for a research map on https://airesearchmaps.com

## Developing

### Getting Started

1. Ensure you have [Git installed](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) on your system.

2. After copying this repository as a termplate, clone it.

3. For the best editing experience, we recommend using either:
   - [Obsidian](https://obsidian.md)
   - [VS Code](https://code.visualstudio.com)

### Obsidian

After installing Obsidian, (if already installed, click on your vault > Manage vaults) once opened press "Open folder as vault" and select this repository.

### VS Code

After opening the repository, you will be prompted to install the mervin.markdown-formatter extension. Please accept. This is to ensure consistent Markdown formatting.

## Standards

Failing to follow these standards may result in unexpected behaviour when deployed to the site.

- Node directories CANNOT have spaces: use underscores instead (they will be converted back to spaces on the site)
- Each node's content should be in a markdown file named identically to its directory (with a .md extension)
- See `/Root_Node_Example` and its contents for more details on formatting and structuring nodes

## `meta.json`

This file contains metadata about the map: functionality, formatting, content for the preview card of the map (map card), etc.. The following is a complete example with comments explaining all possible fields. Unless otherwise specified, assume fields to be required. If a field is not required, the value shown is its default value.

```json5
{
  "rootDir": "Root_Node_Example",  // Relative path to root node directory
  "title": "Title",  // Title on map card
  "note": "",  // Optional note added in italics to map card and root node description (use for giving credit)
  "coverRootDescription": "",  // Description on map card
  "disableExpandAll": true,  // The expand all feature opens all nodes in the default mode
  "customSettings": {  // Optional, these settings specify formatting & functionality for the map. All fields within it are also optional
    "defaultMode": {
      "nodeWidth": 2600,
      "nodeHeight": 1400,
      "verticalSpacing": 250,
      "siblingNodeSpacing": 500,
      "nodeGroupSpacing": 600,
      "padding": 1000
    },
    "titlesMode": {
      "widthAddition": 80,
      "horizontalSpacing": 600,
      "siblingNodeSpacing": 40,
      "nodeGroupSpacing": 70,
      "avgTextCharSizes": [
         {
           "textSize": 70,
           "charW": 34
         },
         {
           "textSize": 50,
           "charW": 26
         },
         {
           "textSize": 30,
           "charW": 14.7
         },
         {
           "textSize": 22,
           "charW": 10.7
         },
         {
           "textSize": 18,
           "charW": 8.8
         }
      ],
      "defaultTitleCharSize": {
        "textSize": 15,
        "charW": 7.287
      },
      "horizontalSpacingAdditions": [350, 70, 70],
      "baseColors": [
        "rgb(102, 153, 204)", // Muted blue
        "rgb(179, 153, 204)", // Muted purple
        "rgb(204, 153, 153)", // Muted red
        "rgb(153, 204, 153)", // Muted green
        "rgb(204, 179, 153)", // Muted gold
        "rgb(153, 204, 204)" // Muted teal
      ],
      "padding": 400
    }
  }
}
```

## Coming Soon!

- Custom linter to enforce formatting
- local dev version to see a live preview of the map
