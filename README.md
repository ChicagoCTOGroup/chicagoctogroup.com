# Chicago CTO Group

## Installation

Read the [Installation Guide](https://jekyllrb.com/docs/installation/#requirements) to ensure that your system has support for `Ruby`, `RubyGems`, and `Bundler`.

```bash
$ git clone git@github.com:ChicagoCTOGroup/chicagoctogroup.com.git
$ cd chicagoctogroup.com
$ gem install bundler
$ bundle install
```

## Running the project

```bash
$ bundle exec jekyll serve
```

While `serve` is the most common use, the `jekyll` package takes a variety of commands. You can read about the options in the [Basic Usage Guide](https://jekyllrb.com/docs/usage/).

Once the server is up and running, you will be able to access the site locally at [http://127.0.0.1:4000/](http://127.0.0.1:4000/).

## Making changes

> This is a good time to read about the [directory structure](https://jekyllrb.com/docs/structure/) and the [configuration](https://jekyllrb.com/docs/configuration/) of jekyll, before you begin making changes.

Once running, the server will watch the file system for local changes then rebuild the project in real-time, allowing you to refresh the site in your browser and see the local changes.

A few notes about this particular project:

- Our SCSS libraries and components are stored in the `_scss` directory, which the files that pull them together are in the `assets/css` directory. Read about how assets are included in the [Assets Guide](https://jekyllrb.com/docs/assets/).
- Images that are referenced within CSS are stored in the `assets/css/images` directory and referenced with a relative url (`url('images/something.png')`) within the stylesheets themsevles. Images that are included and referenced in markup are stored in the `assets/images` directory.
- We don't have any posts yet, but there is still an empty `_posts` directory for a time when we do add posts.
- There is only one main layout (`default`) within the `_layouts` directory. All pages use this layout currently.
- The FAQ page is built using a YML data file from the `_data` directory.
- Don't forget that changes to `_config.yml` will not be processed in a live rebuild while the server is running. The server will need to be stopped and relaunched for config changes to take effect.
- Pushing changes to `master` branch will cause the site to be built and deployed into production. We're hosting on Github Pages so only a [select few whitelisted plugins](https://pages.github.com/versions/) can be used in this project. When the project requires a plugin, either open source or custom to this project, that is not on that list, we will need to pursue hosting elsewhere; this is not a big deal.
