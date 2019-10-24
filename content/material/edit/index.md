---
title: 'How to edit'
date: 2019-02-11T19:27:37+10:00
weight: 6
draft: false
summary: a quick explainer how to edit the page
---

The source repo is here: https://github.com/CALDISS-AAU/sdsphd19_source.git
I created a branch as backup and therefore nothing should go bigly wrong

To edit, I'd use github desktop and sublime. You all should have access to the repo. Pull it, edit with Sublime or similar, commit, push.

The `public` folder is initiated as a submodule in git and actually it lives in in another github-pages repo. The page is served here:https://caldiss-aau.github.io/sdsphd19 (I compiled it locally and pushed it manually)

For now I din'd set up Travis CI for automatic compilation (waiting for Kristian to approve my request) but that should run tomorrow. That means: whatever you edit and push into the sourve-repo will be automatically compiled and published within some minutes.

You edit stuff only here: https://github.com/CALDISS-AAU/sdsphd19_source/tree/master/content

The structure is simple as F***

```
content
├── _index.md
├── info
│   ├── _index.md
│   ├── lecturers
│   │   └── index.md
│   ├── logistics
│   │   └── index.md
│   └── stuff
│       └── index.md
└── material
    ├── PyIntro
    │   └── index.md
    ├── _index.md
    ├── example
    │   └── index.md
    ├── install-hugo
    │   └── index.md
    ├── install-theme
    │   └── index.md
    └── specimen
        └── index.md

```


Folders are menus and submenus. Within these you’ll find index.md or _index.md 

Please only make new folders on submenu level and let me know if we need more menus (up right: “home”, “material”, “info”) That requires some rewriting of other configs.

Images go in “static/img” here you can make folders as you like. You refer to them like that `![image](/sdsphd19/img/image.jpg`

```
.
├── archetypes
├── content
│   ├── info
│   └── material
├── data
├── layouts
├── public
│   ├── categories
│   ├── css
│   ├── images
│   ├── img
│   ├── info
│   ├── js
│   ├── material
│   ├── resources
│   └── tags
├── resources
│   └── _gen
├── static
│   └── img
└── themes
    └── whisper

```

In public, `hugo` is compiling the static html page along with the stuff that is needed for the page to show. It's a bit like LaTeX where the folder `public` is our PDF and all the other stuff...well...stuff.

You edit only in `content` and `static`

If you want to see what you're building, I recoomend installing hugo https://gohugo.io and running hugo server while editing. It will then seve a live compiled verion of the page on localhost.

