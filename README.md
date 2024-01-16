---
layout: default
title: Documentation Guide - Home
---

## Documentation on github pages

This repo describes a guide to properly display documentation using redocly and jekyll themes (or their combination)

1. The github repo's file system is as follows in order to host two different github pages:
```
main/docs
├── jekyll/           # jekyll subfolder containing files necessary for jekyll-themed github page
|     └── index.md    # markdwown displayed using jekyll theme
├── redocly/          # redocly subbfolder: see more info in tutorial.html
├──   ├── index.html  # set page structure of redocly and set .json file used for api docs
├──   ├── dist.json   # json file containing api docs
├──   ├── README.md   # Guide to host Swagger API documentation with GitHub Pages using redocly
├──   └── favicon.png # png of redocly favicon
├── _config.yml       # contains jekyll setup/theme/description for jekyll-themed github pages
├── index.html        # html file to structure jekyll themed in main/docs github page   
└── README.MD         # documentation to display at main/docs github page
```
- It's important that each github page, has its contents in a seperate subfolder. 
- `_config.yml` **must** be at the github page build directory (e.g `main/docs`) 

2. See detailed guide on how to set up each different page (redocly/jekyll) on the respective subfolder.

3. For multiple github pages in the same repo, please check the guide at "jekyll" subfolder.

4. To see the end result github pages, append "jekyll" or "redocly" at the end of github page [link](tzoral.github.io/documentation-guide/) 
    - Jekyll:  [https://tzoral.github.io/documentation-guide/jekyll](https://tzoral.github.io/documentation-guide/jekyll)
    - Redocly: [https://tzoral.github.io/documentation-guide/redocly](https://tzoral.github.io/documentation-guide/redocly)
