# rnext.it - [![CC BY-NC-ND 4.0][cc-by-nc-nd-image]][cc-by-nc-nd]

My personal website

To open the website go to [https://rnext.it/](https://rnext.it/)

# Run locally

If you have **docker** and **docker-compose** you can use only this command

```
docker compose up
```

**Note:** If you are updating `config.yml` or `_config.dev.yml` please **restart** container.

# Install ruby and run on your host

If you want install all environment on your desktop you need to install **ruby**:

https://gorails.com/setup/ubuntu/20.04#ruby-rbenv
* Using rbenv
* version 2.7.3

When is done, please run:

```
bundle
```

to run on your local machine, please execute:

```
rake serve
```

eq of: `bundle exec jekyll serve --config _config.yml,_config.dev.yml --incremental --livereload`

# Theme reference

Allowed plugins https://pages.github.com/versions/

* https://mmistakes.github.io/minimal-mistakes/
* https://github.com/mmistakes/mm-github-pages-starter
* https://ptc-it.de/enabling-cookie-consent-with-jekyll-minimal-mistakes/
* https://ptc-it.de/add-favicon-to-mm-jekyll-site/
* https://www.aleksandrhovhannisyan.com/blog/how-to-add-a-copy-to-clipboard-button-to-your-jekyll-blog/
* Make a table from csv file https://jekyllrb.com/tutorials/csv-to-table/
* https://github.com/jekyll/jekyll-redirect-from
* https://github.com/ayastreb/jekyll-maps
  * https://www.maps.ie/coordinates.html
  * https://www.barattalo.it/convert-address-lat-long

# Other
* https://emojipedia.org/
* https://realfavicongenerator.net/
* https://docs.github.com/en/free-pro-team@latest/github/managing-files-in-a-repository/3d-file-viewer

# Website license

This website is under license [Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International][cc-by-nc-nd].

[cc-by-nc-nd]: https://creativecommons.org/licenses/by-nc-nd/4.0/
[cc-by-nc-nd-image]: https://i.creativecommons.org/l/by-nc-nd/4.0/80x15.png
