You have to fill some informations on `_config.yml` to customize your site.

```
# Site Settings
title: Thiago Rossener | Front-end Developer
email: youremail@xyz.com
description: Some text about your blog.
baseurl: "" # the subpath of your site, e.g. /blog/ or empty.
url: "https://www.rossener.com" # the base hostname & protocol for your site
google_analytics: "UA-XXXXXXXX-X"

# User settings
username: Thiago Rossener # it will appear on each page title after '|'
user_description: Some text about you.
disqus_username: disqus_username

# Social Media settings
# Remove the item if you don't need it
github_username: github_username
facebook_username: facebook_username
twitter_username: twitter_username
instagram_username: instagram_username
linkedin_username: linkedin_username
medium_username: medium_username
```

## Color customization

All color variables are in [src/styl/_variables.styl](src/styl/_variables.styl).

Default colors:

![#ff0a16](https://placehold.it/15/ff0a16/000000?text=+) `#FF0A16` Theme Color

![#141414](https://placehold.it/15/141414/000000?text=+) `#141414` Primary Dark

![#ffffff](https://placehold.it/15/ffffff/000000?text=+) `#FFFFFF` Accent Dark

![#f2f2f2](https://placehold.it/15/f2f2f2/000000?text=+) `#F2F2F2` Light Gray

![#333333](https://placehold.it/15/333333/000000?text=+) `#333333` Texts

## Creating posts

You can use the `initpost.sh` to create your new posts. Just follow the command:

```
./initpost.sh -c Post Title
```

The new file will be created at `_posts` with this format `date-title.md`.
