---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "{roistats}: an R package for fast and easy multiple testing analysis"
summary: "The goal of this package is to apply same basic statistical tests with multiple comparison correction across multiple sub-groups, with the output being a nice arranged data.frame instead of detailed listed information."
authors: []
tags: 

categories: []
date: 2021-03-06T13:53:48-07:00

# Optional external URL for project (replaces project detail page).
external_link: ""

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: true

# Custom links (optional).
#   Uncomment and edit lines below to show custom links.
links:
- name: Website
  url: https://irisfee.github.io/roistats/
  icon_pack: fa
  icon: link
- name: Code
  url: https://github.com/Irisfee/roistats/
  icon_pack: fab
  icon: github

# url_code: "https://github.com/Irisfee/roistats/"
url_pdf: ""
url_slides: ""
url_video: ""

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: ""
---
While working on my first grad school project, I found in our research field, the analysis of multiple testing is involved in almost every project, since we need to compute same analysis over multiple brain regions. Thus, we need to apply same basic descriptive statistics, different variants of t-tests, and multiple comparison correction to multiple groups.

Quickly I got tedious about writing similar long pipelines of doing the multiple testing analysis, so I decided to wrap up my pipeline into functions, and combine functions into a package, and {roistats} came out! All the functions from the package can be used in combination with dplyr.

For the detail of what functions are included and how to use them, check out the website for this package: https://irisfee.github.io/roistats/index.html

![](fig1.png)





