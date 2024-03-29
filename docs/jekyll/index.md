---
title: Tutorial
---

Single github page
---

To create a single jekyll-themed github page in repo, simply add a file named **_config.yml** at the directory where github page is being built. This file is going to read the README file at root directory and design a github page, based on its contents. An example structure of that file is as follows:

```yml
# This file is being read by github pages
description: Jekyll themed documentation # jekyll description bellow title
show_downloads: true                     # show buttons to download github repo in github page
theme: jekyll-theme-cayman               # "cayman" theme used to design page
layout: default                          # layout of the page
```

Enable GitHub Pages for the repository by following these steps:
- Go to the repository on GitHub.
- Click on the "Settings" tab.
- Scroll down to the "GitHub Pages" section.
- In the "Source" dropdown, select the branch you want to use (e.g., "main").
- Choose the `root/docs` folder option or specify the folder path based on your preference.
- Click "Save".

After saving, you will see a message indicating the URL at which your site is published. By default, it will use the repository name as the URL, but you can configure it further.

Multiple github pages
---

To configure a single repository with multiple subfolders to be enabled for GitHub Pages and assign unique URLs to each subfolder as distinct web pages. Here's how you can achieve this:

1. Create a new repository on GitHub named "tutorial".

2. Clone the repository to your local machine using Git:
```bash
git clone https://github.com/TzorAL/tutorial.git
```

3. Create three subfolders within the repository's directory structure:
```
main/docs
├── jekyll/           # jekyll subfolder containing files necessary for jekyll-themed github page
|     └── index.md    # markdwown displayed using jekyll theme
├── redocly/          # redocly subbfolder: see more info in tutorial.html
|     ├── index.html  # set page structure of redocly and set .json file used for api docs
|     ├── dist.json   # json file containing api docs
|     ├── README.md   # Guide to host Swagger API documentation with GitHub Pages using redocly
|     └── favicon.png # png of redocly favicon
├── _config.yml       # contains jekyll setup/theme/description for jekyll-themed github pages
├── index.html        # html file to structure jekyll themed in main/docs github page   
└── README.MD         # documentation to display at main/docs github page
```
- It's important that each github page, has its contents in a seperate subfolder. 
- `_config.yml` must be at the directory where github page is being built (e.g `main/docs`) 


4. Place the necessary files and content for each project within their respective subfolders.

5. Commit and push the changes to GitHub:
``` bash
git add .
git commit -m "Added project folders"
git push origin main
```

6. Enable GitHub Pages for the repository by following these steps:
- Go to the repository on GitHub.
- Click on the "Settings" tab.
- Scroll down to the "GitHub Pages" section.
- In the "Source" dropdown, select the branch you want to use (e.g., "main").
- Choose the `root/docs` folder option or specify the folder path based on your preference.
- Click "Save".

7. After saving, you will see a message indicating the URL at which your site is published. By default, it will use the repository name as the URL, but you can configure it further.

To assign unique URLs to each subfolder as distinct web pages, you can leverage the repository's GitHub Pages URL structure. By default, the URL will be in the format `https://your-username.github.io/my-test-projects/`. You can append the subfolder name to the URL to access each project individually.

For example:
- Project A: [https://tzoral.github.io/documentation-guide/jekyll](https://tzoral.github.io/tutorial/jekyll)
- Project B: [https://tzoral.github.io/documentation-guide/redocly](https://tzoral.github.io/tutorial/redocly)

Each project will have its unique URL and can be accessed as separate web pages under the same GitHub Pages repository.
