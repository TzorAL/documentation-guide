---
title: Tutorial
---

To configure a single repository with multiple subfolders to be enabled for GitHub Pages and assign unique URLs to each subfolder as distinct web pages. Here's how you can achieve this:

1. Create a new repository on GitHub named "tutorial".

2. Clone the repository to your local machine using Git:
```bash
git clone https://github.com/TzorAL/tutorial.git
```

3. Create three subfolders within the repository's directory structure:
```
root/docs
├── jekyll/         # jekyll subfolder containing files necessary for jekyll-themed github page
|     ├── index.md  # markdwown displayed using jekyll theme
├── redocly/        # redocly subbfolder: see more info in tutorial.html
└── _config.yml     # contains jekyll setup/theme/description
```

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

To assign unique URLs to each subfolder as distinct web pages, you can leverage the repository's GitHub Pages URL structure. By default, the URL will be in the format `https://tzoral.github.io/tutorial/`. You can append the subfolder name to the URL to access each project individually.

For example:

- Project A: `https://your-username.github.io/TzorAL/tutorial/jekyll`
- Project B: `https://your-username.github.io/TzorAL/tutorial/redocly`

Each project will have its unique URL and can be accessed as separate web pages under the same GitHub Pages repository.
