This is the repository for the website of the CIMM research programme at IMFM (Računsko intenzivne metode v teoretičnem računalništvu, diskretni matematiki, kombinatorični optimizaciji ter numerični analizi in algebri z uporabo v naravoslovju in družboslovju).

## How to edit the web page content

This web site uses [Jekyll](https://jekyllrb.com) for generation of web pages from Markdown source, and [YAMT theme](http://jekyllthemes.org/themes/jekyll-yamt/) as lipstick. The pages are served via [GitHub pages](https://guides.github.com/features/pages/) at [(https://imfm-si.github.io/cimm-site/)](https://imfm-si.github.io/cimm-site/).

The pages are written in the Markdown format and automatically translated to HTML by
GitHub. Simply edit the Markdown files and use Git to push the changes back to the server.
The website always shows the contents of the `main` branch of the GitHub repository.

You can edit the `.md` files in GitHub's online editor, or locally on your machine:

1. `git pull`
2. Make changes to `.md` files (see below)
3. `git status` to see what files you changed
4. `git add XYZ.md` for every file you changed and you wish to commit
5. `git push`
6. Go to the [project web page](https://tydiform.fmf.uni-lj.si), make sure to reload the page.

The `.md` files are Markdown files, here is a [quick Markdown reference](https://guides.github.com/features/mastering-markdown/).

Page source files:

* [`index.md`](./index.md) -- main page
* [`clani.md`](./clani.md) -- members
* [`dejavnosti.md`](./dejavnosti.md) -- a timeline of activities
* [`dosezki.md`](./dosezki.md) -- project group achievements

### How to generate the web page locally

You need not generate the pages before you publish them, but it might be a good idea to do
so and verify that the pages are OK, especially if you make significant changes.

To generate web pages locally for preview, you need [Jekyll](https://jekyllrb.com), which
needs a million subsidiary Ruby packages. Rather than trying to install them with your
bare hands, you should just try

    bundle install

With a bit of luck you've got Ruby installed so this command will do the right thing. The
`bundle` command is part of the Ruby [Bundler](https://bundler.io) package manager. On a
Mac it is available through [Homebrew](https://brew.sh).  On Linux it is available through
your package manager, e.g. on Debian/Ubuntu `sudo apt install ruby-bundler ruby-dev'.

Then to generate and serve the pages locally, run

    bundle exec jekyll serve

The pages will appear at [http://127.0.0.1:4000/](http://127.0.0.1:4000/).
