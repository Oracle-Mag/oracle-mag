# PLIS Oracle Magazine

Source code for the [website](https://wowthemesnet.github.io/mundana-theme-jekyll/) of the official magazine of Park Lane International school, built with Jekyll and the Mundana theme.

### Contributing

[General documentation](https://bootstrapstarter.com/mundana-theme-jekyll/) for how to create pages and run locally.

### Site-specific Documentation

#### Adding a new post

Create a new file in the `_posts` directory with the following naming convention:

`YYYY-MM-DD-title-of-post.md`

At the top of the file, add the configuration information for the post:

```yaml
---
layout: post
title:  "Title of Post"
author: authorname # as shown in _config.yml
categories: [ category1, category2 ] # one of advice, current affairs, and entertainment
image: assets/images/cover-image.extension
tags: featured  # if you want it to show up on the sidebar, or 'sticky' to be the main post on the page
---
```

Then add in the post contents using the Markdown language syntax. Images, formatting, etc. is all supported.

#### Adding a new page

Create a new HTML file in the `_pages` directory. It should have the `.html` extension, and the following configuration information at the top:

```yaml
---
layout: page
title: "Title of Page"
permalink: /permalink/ # the URL of the page
---
```

Then fill out the page with whatever HTML you want.

#### Adding a new author

If there are any new posts being added that are by authors who are not already on the website, a couple of things have to be done. Firstly, a page has to be made for that author in the `_pages` directory, using the format: `author-firstname-lastname.html`. Any Czech diacritics etc. *should* be included. Afterwards, take a random, already finished author page, and copy over its contents. All you need to do in the copied-over, new author page is to change the configuration information (title and permalink) and then the author being linked to (replace e.g. `juliastogel` in the HTML following the config information with `firstnamelastname` of the new author). There should be four of these HTML references that require replacing.

Next, you need to add the author to the site configuration file, `_config.yml`. Under the `authors` category, add in the following new entry:

```yaml
authorname: # as shown in the post
  name: "Author Name"
  avatar: assets/images/students/avatar.extension  # add some .png or .jpg file to the assets/images/students directory
  bio: "Author bio"
  is_writer: true
  role: Writer # this gets shown on the /teams description page; some people are writers but called 'Founder' for example
```

#### Adding a new team member

Repeat the second step shown above, but instead do not give the `is_writer` role to the new team member. Instead, use some descriptive, short phrase that describes what they do. Additionally, don't place this entry under the `authors` category — it should be under `other_team_members` instead.

#### Linking to a new edition

Go to `_pages/full-issues.html` and paste in the Canva embed for the new magazine edition, as explained on Canva's site [here](https://www.canva.com/embeds/).

### Extension Ideas
- [x] Find and use a favicon that better matches the dark green
- [ ] Create image of magazine to use for landing page
- [ ] Implement dark and light mode (harder)
- [ ] Add a countdown timer for the /future page, counting down to the next release date
- [ ] Make the search bar a bit wider
- [ ] Make search bar results theme line up with rest of site
- [x] Minify CSS
- [ ] Minify images to increase page load speed

### Technical Difficulties?

Feel free to contact Simon Ilincev (Destaq). You can find his email address on his GitHub profile [here](https://github.com/Destaq).
