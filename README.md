## Documentation on github pages

This repo describes a guide to properly display documentation using redocly and jekyll themes (or their combination)

1. The github repo's file system is as follows in order to host two different github pages:
```
main/docs
├── jekyll/         # jekyll subfolder containing files necessary for jekyll-themed github page
|     ├── index.md  # markdwown displayed using jekyll theme
├── redocly/        # redocly subbfolder: see more info in tutorial.html
├── _config.yml     # contains jekyll setup/theme/description for jekyll-themed github pages
├── index.html      # html file to structure jekyll themed in main/docs github page   
└── README.MD       # documentation to display at main/docs github page
```
- It's important that each github page, has its contents in a seperate subfolder. 
- `_config.yml` must be at the directory where github page is being built (in our case it's `main/docs`) 

2. You can see detailed instrucitons on how to set up each different page (either redocly or jekyll) on the respective subfolder.

3. For multiple github pages in the same repo, please check the guide at "jekyll" subfolder.

4. To see the end result github pages, append "jekyll" or "redocly" at the end of github page [link](tzoral.github.io/documentation-guide/) 
    - Jekyll themed:  https://tzoral.github.io/documentation-guide/jekyll
    - Redocly themed: https://tzoral.github.io/documentation-guide/redocly
