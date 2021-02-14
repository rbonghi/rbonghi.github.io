---
title: "docker-dropbox-app"
excerpt: ":whale: Docker syncronization container for Dropbox using a token app "
classes: wide
number: 2018
link: https://github.com/rbonghi/docker-dropbox-app
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/images/docker.jpg
  teaser: /assets/images/docker.jpg
  actions:
    - label: "Github"
      url: "https://github.com/rbonghi/docker-dropbox-app"
---

Docker hub repos: https://hub.docker.com/r/rbonghi/dropbox

When your docker is ready, all files and folders will be sync in realtime. A watchdog check every time if a file or folder is created, deleted or modified, and will be update your dropbox folder.

If you add in your root a file .dropboxignore you can select witch type of file or folder you want exclude, look like your git repository.