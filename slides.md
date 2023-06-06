# Create your personal Website

![unibe logo](https://www.unibe.ch/media/logo_unibern.png)

DSL Summer Course 2023

06.06.2023

Sebastian Flick;
Data Science Lab (DSL)

---

## Program

Morning: foundations and theory

- What is a website, technically? (Domain, DNS, Host...)
- What are HTML, CSS and Javascript?
- What is Markdown?
- What is _git_ and _GitHub_, and why should I care?

_Lunchbreak_

Afternoon: Getting our hands dirty

- What is Jeckyll? (Static Site generation)
- What are GithubPages (Hosting our page the easy way)
- Choosing a template
- Create Content
- Edit our template
- embedding zotero, videos, etc.

---

## What is a website?

- a Website is a html document
- that is styled with css
- and became functional through javascript

---

### What happens when I type something into my browser?

[![](https://mermaid.ink/img/pako:eNp1kV9rwjAUxb_KXZ4UtHZaN5YHX6bog44xC8LoS9pc24D5syTdEPG7L7XqRFieLuf8ODnceyCF5kgocfhVoypwKlhpmcwUhPe6E6h8fzKZvq0pVN4bRweDWokco6JqmWD1A9GiFB5HcfQyjIbjOHq6C9lg7tB-o4XOLdWlsEQPEsEhgq8QFlqiYSWC3sLlM-jMZ2nfNi2d77bJ_wXe9kkrtAh7XUOpH6Dzgc5o5RB-hK9gka6WkGu-75IekWglEzzs4tDEZyRUkZgRGsacuTD1Wj1ndoGirHzjDZMk_tPnzDRiEo-S8Vn12rwzzoUqG-c5Sa6OExzvrUwdQ5XacOZxxoXXltAt2znsEVZ7vd6rglBva7xA53tdKcPUp9byAuEpY9Xe-HTq4y_1xJt-?type=png)](https://mermaid.live/edit#pako:eNp1kV9rwjAUxb_KXZ4UtHZaN5YHX6bog44xC8LoS9pc24D5syTdEPG7L7XqRFieLuf8ODnceyCF5kgocfhVoypwKlhpmcwUhPe6E6h8fzKZvq0pVN4bRweDWokco6JqmWD1A9GiFB5HcfQyjIbjOHq6C9lg7tB-o4XOLdWlsEQPEsEhgq8QFlqiYSWC3sLlM-jMZ2nfNi2d77bJ_wXe9kkrtAh7XUOpH6Dzgc5o5RB-hK9gka6WkGu-75IekWglEzzs4tDEZyRUkZgRGsacuTD1Wj1ndoGirHzjDZMk_tPnzDRiEo-S8Vn12rwzzoUqG-c5Sa6OExzvrUwdQ5XacOZxxoXXltAt2znsEVZ7vd6rglBva7xA53tdKcPUp9byAuEpY9Xe-HTq4y_1xJt-)

<!-- sequenceDiagram
    Client->>DNS: https://unibe.ch
    DNS--))Client: 130.92.250.6

    Client->>Webserver (130.92.250.6): Let me see the Homepage of unibe.ch (GET-request)
    Webserver (130.92.250.6)--))Client: There you go! (Response with HTML body) -->

---

## What are HTML, CSS and Javascript?

(and whatabout sass)

---

## What is Markdown?

---

## What is _git_ and _GitHub_, and why should I care?

    - Github CodeSpaces

---

## What is Jeckyll? (Static Site generation)

---

## What are GithubPages (Hosting our page the easy way)

---

## Choosing a template

**https://github.com/alshedivat/al-folio**

(There are many more)

- https://github.com/topics/jekyll-theme
- https://pages.github.com/themes/
- https://academicpages.github.io/

### Deploying with GitHub Pages

1. create new repo from template
2. change the action-permission
3. change the config
4. config the ghpages-options

For project pages:

    In _config.yml, set url to https://<your-github-username>.github.io and baseurl to /<your-repository-name>/.
    Set up automatic deployment of your webpage (see instructions below).
    Make changes, commit, and push!
    After deployment, the webpage will become available at <your-github-username>.github.io/<your-repository-name>/.

To enable automatic deployment:

    Click on Actions tab and Enable GitHub Actions; do not worry about creating any workflows as everything has already been set for you.
    Go to Settings -> Actions -> General -> Workflow permissions, and give Read and write permissions to GitHub Actions
    Make any other changes to your webpage, commit, and push. This will automatically trigger the Deploy action.
    Wait for a few minutes and let the action complete. You can see the progress in the Actions tab. If completed successfully, in addition to the master branch, your repository should now have a newly built gh-pages branch.
    Finally, in the Settings of your repository, in the Pages section, set the branch to gh-pages (NOT to master). For more details, see Configuring a publishing source for your GitHub Pages site.

### Setting up the domain

    - buying a domain
    - creating a CNAME DNS Record
    - adding the custom domain to GHPages
    - changing the _config

### Setting up Codespaces

```
rvm install 3.0.5
rvm use 3.0.5
gem install bundler jekyll
bundle update
npm install -g @mermaid-js/mermaid-cli
jekyll serve
```

- https://docs.github.com/de/pages/setting-up-a-github-pages-site-with-jekyll/adding-a-theme-to-your-github-pages-site-using-jekyll

---

<!--### Setting up a local environment

- install docker
- clone your git repo onto your computer
- docker-compose up
-->

## Create Content

features of al-folio: https://github.com/alshedivat/al-folio

---

### adding static pages

just create a new page in the \_pages-folder and add the frontmatter:

```
---
layout: page
permalink: /static/
title: static page
description: Materials and stuff
nav: true
nav_order: 5
---
```

---

### adding publications

upload your bib file into `_bibliography/papers.bib`
edit the _publications_-Page

```
{% bibliography %}
```

if you want the bib-button for every entry: edit `\_layouts\bib.html`

look for _Bib_ and delete the if-statement.

---

#### Special fields

you can add lots of special properties to your items in the bib file:

https://github.com/alshedivat/al-folio#publications

to add them easily in zotero: install [betterbibtex](https://retorque.re/zotero-better-bibtex/installation/)

add the fields in the extra-field:

`tex.field: value`

source: https://retorque.re/zotero-better-bibtex/exporting/extra-fields/

#### Publication preview-images

images to the left of the titles: Reference them in your Bib by filename. Upload the images into `assets/img/publication_preview/`

or just reference an URL of the image.

---

More info: https://github.com/inukshuk/jekyll-scholar

---

### Blogging

to create a new blog post, add a file to _\_posts_.
the filename has to obey the following syntax: _YEAR-MONTH-DAY-TITLE-WITH-SPACES_

Minimal frontmatter: title, layout

more info: https://jekyllrb.com/docs/posts/

---

### Collections

are there to divide subpages into categories - similar to posts.

---

## Styling

Most important variables in _/\_sass/\_themes.scss_

## Bonus add mermaid
