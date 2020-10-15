# Thorntail.io

This is the content for the Thorntail web site.


## Build the Site

    $ make

## Develop the Site

Write content in asciidoc or markdown, your choice. Open an issue if you want
to write content in some other format.

Put blog posts in `src/posts`. Name the files, whatever you want. You can add
front matter to the file to set the title, publish date, etc. Permalinks are
created for the content based on the title of the document. Typically posts
should use the `post.jade` layout.

Here is an example post.

    ---
    Title: Thorntail Buzz
    PublishDate: 2015-11-07
    ModifyDate: 2015-11-09
    Author: Joseph Stinger
    Layout: post.jade
    Gist: lance/0cfd8539d5c395b43f16
    ---

    One of the easiest ways to include source code in your Thorntail
    blog posts is by using the `metalsmith-gist` plugin. You
    don't need to know anything about the plugin to use it though,
    so don't worry.

    To use the plugin, just add a `gist` property to the front matter
    of your file. Then you can insert the gist anywhere you like in
    the body of the file. Like so:

    gist: lance/0cfd8539d5c395b43f16

    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent
    in aliquet eros, vel posuere mi. Suspendisse a orci eu sapien
    accumsan ullamcorper. Nunc scelerisque, purus vitae aliquam
    aliquam, nibh elit ornare leo, eu aliquam sapien tortor iaculis
    arcu. In eu mattis augue. Donec porttitor leo eu venenatis
    posuere. Nulla facilisi. Nullam fringilla bibendum blandit.

If you want to include source code in your posts, one of the easiest ways to
do this is by using gist.

For styling, the site uses [Bootstrap CSS](http://getbootstrap.com) for styling
and layouts. Add additional styling and overrides to `src/css/site.css`. For
templates, we use [Jade](http://jade-lang.com/).

To build the site and run a simple web server, watching for changes to files.
Note: changes to layouts require a restart.

    $ make serve

## Publish the Site

The site is published when changes are pushed to the `master` branch.
This will trigger a CI build at {ADD LINK TO CI}.
If the build completes successfully, the generated site content will be pushed to
the `gh-pages` branch on github.com, and GitHub Pages will serve the new content at
https://thorntail.io.
