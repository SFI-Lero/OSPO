# The Lero Open Source Programme Office (OSPO)
Repository for the Lero OSPO website: [https://sfi-lero.github.io/OSPO/](https://sfi-lero.github.io/OSPO/)


![](/img/logos/logo_banner.png)

## Website core configuration
The website can be configured from the [`_config.yml` file](https://github.com/SFI-Lero/OSPO/blob/main/_config.yml). This is where the website contact email, twitter handle, description, title, etc. can be edited, as well as the default ruby gems etc. .

## Adding mentors
Mentors are added inside the `_mentors` directory. 


## Adding/editing pages
Pages can be added by placing `.md` files in the root folder. The markdown content can be freely edited but must have the following type of YML content at the top:

```markdown
---
layout: pagefullwidth
title: "Page title"
description: "Page description"
logo:
header-img: "img/home-bg.jpg"
ordernumber: 5
---
```
Note that HTML files can also be used when they have the YML content at the top. Furthermore HTML can be used within markdown files. 



## Markdown guide
https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet



## Editing the front page
The front page is built using:
https://github.com/SFI-Lero/OSPO/blob/main/index.html

Which includes content from this markdown file:
https://github.com/SFI-Lero/OSPO/blob/main/_includes/Home.md
