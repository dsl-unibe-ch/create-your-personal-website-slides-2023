# Create your personal Website

![unibe logo](https://www.unibe.ch/media/logo_unibern.png)

DSL Summer Course 2023

06.06.2023

Sebastian Flick;
Data Science Lab (DSL)

---

## Program

**foundations and theory**

- What is a website, technically? (Domain, DNS, Host...)
- What are HTML, CSS (and Javascript)?
- What is Markdown?
- What is _git_ and _GitHub_, and why should I care?
- What is Jekyll
- What are GithubPages (Hosting our page the easy way)

---

**Getting our hands dirty**

- Choosing a template
- deploying
- buying and setting up a domain
- setting up GitHub Codespaces
- Create Content
- Style our template
- embedding zotero, etc.

---

## What is a website?

- a Website is a html document
- that is styled with css
- and became functional through javascript

We will get to know html and css (and their derivatives)

---

### What happens when I type something into my browser?

[![](https://mermaid.ink/img/pako:eNp1kV9rwjAUxb_KXZ4UtHZaN5YHX6bog44xC8LoS9pc24D5syTdEPG7L7XqRFieLuf8ODnceyCF5kgocfhVoypwKlhpmcwUhPe6E6h8fzKZvq0pVN4bRweDWokco6JqmWD1A9GiFB5HcfQyjIbjOHq6C9lg7tB-o4XOLdWlsEQPEsEhgq8QFlqiYSWC3sLlM-jMZ2nfNi2d77bJ_wXe9kkrtAh7XUOpH6Dzgc5o5RB-hK9gka6WkGu-75IekWglEzzs4tDEZyRUkZgRGsacuTD1Wj1ndoGirHzjDZMk_tPnzDRiEo-S8Vn12rwzzoUqG-c5Sa6OExzvrUwdQ5XacOZxxoXXltAt2znsEVZ7vd6rglBva7xA53tdKcPUp9byAuEpY9Xe-HTq4y_1xJt-?type=png)](https://mermaid.live/edit#pako:eNp1kV9rwjAUxb_KXZ4UtHZaN5YHX6bog44xC8LoS9pc24D5syTdEPG7L7XqRFieLuf8ODnceyCF5kgocfhVoypwKlhpmcwUhPe6E6h8fzKZvq0pVN4bRweDWokco6JqmWD1A9GiFB5HcfQyjIbjOHq6C9lg7tB-o4XOLdWlsEQPEsEhgq8QFlqiYSWC3sLlM-jMZ2nfNi2d77bJ_wXe9kkrtAh7XUOpH6Dzgc5o5RB-hK9gka6WkGu-75IekWglEzzs4tDEZyRUkZgRGsacuTD1Wj1ndoGirHzjDZMk_tPnzDRiEo-S8Vn12rwzzoUqG-c5Sa6OExzvrUwdQ5XacOZxxoXXltAt2znsEVZ7vd6rglBva7xA53tdKcPUp9byAuEpY9Xe-HTq4y_1xJt-)

We will configure a DNS entry

<!-- sequenceDiagram
    Client->>DNS: https://unibe.ch
    DNS--))Client: 130.92.250.6

    Client->>Webserver (130.92.250.6): Let me see the Homepage of unibe.ch (GET-request)
    Webserver (130.92.250.6)--))Client: There you go! (Response with HTML body) -->

---

## What is HTML

- It's a **Markup language** (like XML)
- There is content inside a hierarchical structure made up of tags

`<p class="red-paragraph">This is the content</p>`

---

## What is CSS

- Cascading **Style Sheets**
- describes how the elements in the HTML-Markup should be displayed

```css
.red-paragraph {
  color: red;
  border: 1px solid;
}
```

<style>
.red-paragraph {
   color: red;
   border: 1px solid;
}

</style>
<p class="red-paragraph">This is the content</p>

---

## What is Markdown?

- Markdown is a simple and easy to use markup language than can be compiled (translated) to html.

`It's what **all of us** should write _all_ the time!`
-->
It's what **all of us** should write _all_ the time!

[Markdown Guide](https://www.markdownguide.org/basic-syntax/)

---

### Bonus: What is Mermaid? 🧜‍♀️

Mermaid is Markdown for diagrams and visualizations.

```
pie title Pets adopted by volunteers
    "Dogs" : 386
    "Cats" : 85
    "Rats" : 15
```

[![](https://mermaid.ink/img/pako:eNpd0MFqwzAMBuBXMTrn0K3OVnxdx3YZlO42fFEqLTUktrGVQil99znN3MF8kr9fWEYXOARiMBAdK3EysNqxZIUUojCp7qxOYZi8MKdsvSrHwjb02YIyar15qvaCstimrbSv9NBCAyOnER2VUZe5wYIceWQLppQd5lI1i3eY3tn1R5mzR61Xf_6GcUa9Wuv2VyXEHRI538_Js9b3JDvi_5H11_KVKRIKv5KTkMB845C5AZwkfJ79AYykiWvT1mGfcKwY0X-FcL_y7YmPZYO3RV5_AKNyaTM?type=png)](https://mermaid.live/edit#pako:eNpd0MFqwzAMBuBXMTrn0K3OVnxdx3YZlO42fFEqLTUktrGVQil99znN3MF8kr9fWEYXOARiMBAdK3EysNqxZIUUojCp7qxOYZi8MKdsvSrHwjb02YIyar15qvaCstimrbSv9NBCAyOnER2VUZe5wYIceWQLppQd5lI1i3eY3tn1R5mzR61Xf_6GcUa9Wuv2VyXEHRI538_Js9b3JDvi_5H11_KVKRIKv5KTkMB845C5AZwkfJ79AYykiWvT1mGfcKwY0X-FcL_y7YmPZYO3RV5_AKNyaTM)

[documentation](https://mermaid.js.org/intro/n00b-gettingStarted.html) //
Live Editor:
https://mermaid.live

---

## What is _git_ and _GitHub_, and why should I care?

- git is the foundation of software development.
- it keeps track of everthing that was.
- it enables people to work at the same file at the same time and then take care of the merging later

---

- Github is a service owned by Microsoft.
- It provides many additional services on top of typical git-functions (like git remote servers). We will be using:
  - Github Template Repositories
  - Github Actions
  - Github Codespaces

---

## What is Jekyll?

- Static site generator
- digests Markdown (and many other file formats) and creates a functioning website out of it
- based on ruby
- easy set up with themes

---

## What are GithubPages (Hosting our page the easy way)

- Free Hosting-Service of Github

---

Time for a break?

---

## Choosing a template

**https://github.com/alshedivat/al-folio**

(There are many more)

- https://github.com/topics/jekyll-theme
- https://pages.github.com/themes/
- https://academicpages.github.io/

---

## Deploying with GitHub Pages

1. create new repo from [template](https://github.com/alshedivat/al-folio)

<details><summary>2. change the action-permission</summary>
<p>Click on Actions tab and Enable GitHub Actions</p>
<p>Go to Settings -> Actions -> General -> Workflow permissions, and give Read and write permissions to GitHub Actions.</p>
</details>
<details><summary>3. change the config</summary>
<p>In _config.yml, set url to https://&#060;your-github-username>.github.io and baseurl to /&#060;your-repository-name>/.</p></details>
<details><summary>4. config the ghpages-options</summary>
<p>In the Settings of your repository, in the Pages section, set the branch to gh-pages (NOT to master).</p>
</details>

---

### Setting up the domain

1. [buying a domain](http://www.domains.ch)
2. creating a CNAME DNS Record (username.github.io) or [A Name](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site#configuring-an-apex-domain)
3. adding the custom domain to GHPages
4. changing the \_config

---

## 🥳 Celebrate! 🥳

---

## Setting up Codespaces

```
rvm install 3.0.5
rvm use 3.0.5
gem install bundler jekyll
bundle update
npm install -g @mermaid-js/mermaid-cli
jekyll serve
```

([source](https://docs.github.com/de/pages/setting-up-a-github-pages-site-with-jekyll/adding-a-theme-to-your-github-pages-site-using-jekyll))

---

<!--### Setting up a local environment

- install docker
- clone your git repo onto your computer
- docker-compose up
-->

## Create Content

[features of al-folio](https://github.com/alshedivat/al-folio#features)

---

### adding static pages

just create a new page in the _\_pages_-folder and add the frontmatter:

```YAML
layout: page
permalink: /static/
title: static page
description: Materials and stuff
nav: true
nav_order: 5
```

---

### adding publications

- upload your bib file into `_bibliography/papers.bib`
- edit the _publications_-Page

```
{% bibliography %}
```

- if you want the bib-button for every entry: edit `\_layouts\bib.html`
  --> look for _Bib_ and delete the if-statement.

---

#### Special fields

you can add lots of special properties to your items in the bib file:
https://github.com/alshedivat/al-folio#publications

- to add them easily in zotero: install [betterbibtex](https://retorque.re/zotero-better-bibtex/installation/)
- add the fields in the extra-field:
  `tex.field: value`

[source](https://retorque.re/zotero-better-bibtex/exporting/extra-fields/)
---
#### Publication preview-images

(pictures to the left of the titles)

- Reference them in your Bib by filename.
- Upload the images into `assets/img/publication_preview/`

or just reference a URL of the image.

---

More info: https://github.com/inukshuk/jekyll-scholar

---

### Blogging

- to create a new blog post, add a file to _\_posts_.
- the filename has to obey the following syntax: _YEAR-MONTH-DAY-TITLE-WITH-SPACES_

Minimal frontmatter: title, layout

more info: https://jekyllrb.com/docs/posts/

---

### Collections

are there to divide subpages into categories - similar to posts.

---

## Styling

Most important variables in _/\_sass/\_themes.scss_

---

That's it for now! Happy coding!

---

These slides are here: https://dsl-unibe-ch.github.io/create-your-personal-website-slides-2023/

The repo we created is here: http://dsl.flick.solutions
