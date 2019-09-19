# btvmesh.net

Website for [Burlington Mesh](https://www.btvmesh.net/) ([https://www.btvmesh.net/](https://www.btvmesh.net/)), built with [Jekyll](https://jekyllrb.com/), [Font Awesome](http://fontawesome.io/) icons, and [Skeleton](http://getskeleton.com/) CSS.

Copyright (C) 2019 Burlington Mesh contributors.

[Creative Commons boilerplate pointing to repo]

## Getting Involved

## Content

Our website content is primarily written in [markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) and the key pages are:

~~~
Home Page (index.html)
├── About (about.md)
├── Get Involved (get-involved.md)
├── Timeline (timeline.md)
│   └── <each timeline item can be found under _timeline />
├── Events (events.md)
│   └── <each event has its own page under _posts />
├── Contact (contact.md)
└── Code of Conduct (code-of-conduct.md)
~~~

Much of the content does not change, we primarily add new events.

### Events
New events are added as new `.md` files in the `_posts/` directory using `_posts/_event-template.md`. We request you copy the template if you are submitting a new event.

### Announcements
Announcements are displayed at the top of each page up until a defined date and should be kept to a short line length. Announcements are added as new `.md` files in the `_announcements/` directory.

### Timeline Posts
Timeline posts are displayed in reverse chronological order on the timeline page. Timeline posts are added as new `.md` files in the `_timeline/` directory.

## Development

### 1. Install Dependencies

Install the Jekyll and Bundler gems:

```bash
$ gem install jekyll bundler
```
**Windows users:** [Run Jekyll on Windows](http://jekyll-windows.juthilo.com/)

Install required gems:

```bash
$ bundle install
```

### 2. Running Locally

```bash
$ bundle exec jekyll serve
```

A development server will run at `http://localhost:4000/`

## Deployment

Commits and merges into `master` will be deployed automatically to the production web server through webhook posts from GitHub.

[jekyll-hook](https://github.com/developmentseed/jekyll-hook) listens for incoming webhook posts from GitHub and runs `jekyll build`.

### Daily Builds

A cron task runs `jekyll build` daily at midnight, Eastern Standard Time. The build task can be found in the [scripts directory](scripts/btvmesh-build.sh). The cron task can be edited with `sudo crontab -e`
