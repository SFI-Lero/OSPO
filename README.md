# The Lero Open Source Programme Office (OSPO)
Repository for the Lero OSPO website: [https://sfi-lero.github.io/OSPO/](https://sfi-lero.github.io/OSPO/)


![](/img/logos/logo_banner.png)

## Website core configuration
The website can be configured from the [`_config.yml` file](https://github.com/SFI-Lero/OSPO/blob/main/_config.yml). This is where the website contact email, twitter handle, description, title, etc. can be edited, as well as the default ruby gems etc. .

## Adding people
People are rendered here: https://sfi-lero.github.io/OSPO/People/. You can add yourself by adding YML content in this file (spaces and indenting matters!), you can leave out/delete what doesn't apply:
https://github.com/SFI-Lero/OSPO/blob/main/_data/people.yml

```yml
- name: Dr Kevin M Moerman
  role: Lecturer Biomedical Engineering
  affiliation: National University Ireland Galway
  img: kmm_profile_crop.jpg
  url: https://kevinmoerman.org
  github_username: Kevin-Mattheus-Moerman
  twitter_username: KMMoerman
  orcid_id: 0000-0003-3768-4269
  impactstory_id: u/0000-0003-3768-4269
  linkedin_username: kevin-moerman-98923831
  email_address: kevin.moerman@nuigalway.ie
  interests: Open Source Software, Open Hardware, Open Data, Biomechanics, Bioengineering
  type: lead
```

The people descriptions point at a profile image in this folder:
https://github.com/SFI-Lero/OSPO/tree/main/img/people

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

## Adding/editing blog posts
Blog posts can be added by placing `.md` files in the [`_posts`](https://github.com/SFI-Lero/OSPO/tree/main/_posts) folder. Note that the file names should contain a date to help ordering of the blog posts e.g. `2020-12-08-Lero_OSPO.md`. In addition the rest of the file name should be able to convert to a url, for instance the file name example would translate to: `https://sfi-lero.github.io/OSPO/blog/2020/12/08/Lero_OSPO/`. The markdown content can be freely edited but must have the following type of YML content at the top:

```markdown
---
layout:     post
title:      Introducing the Lero Open Source Programme Office
author:     Patrick Healy
tags: 		  post
subtitle:  	
category:   Blog
thumbnail:  /img/logos/logo_banner.png
---
```

## Markdown guide
https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet



## Editing the front page
The front page is built using:
https://github.com/SFI-Lero/OSPO/blob/main/index.html

Which includes content from this markdown file:
https://github.com/SFI-Lero/OSPO/blob/main/_includes/Home.md
