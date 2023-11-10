# Unikernel Alliance

Unikernel Alliance gathers all unikernel and library OS projects under one umbrella.
The aim is to promote unikernel technologies in commercially viable products, in research and in education.

This repository stores information for the [Unikernel Alliance site](https://unikernelalliance.org).

## Build locally

### Clone the repo:

```console
git clone https://github.com/unikernelalliance/unikernelalliance.org
```

### Fetch dependencies:

```console
cd unikernelalliance.org
npm install
```

### (a) Run locally:

```console
npm run dev
```

The website is accessible through http://localhost:1313 (or any other port provided by Hugo, check the output of the above command):

```console
$ npm run dev

> unikernelalliance.org@0.0.0 dev
> exec-bin node_modules/.bin/hugo/hugo server --bind=0.0.0.0 --disableFastRender --baseURL=http://localhost --noHTTPCache

Watching for changes in /develop/unikernelalliance.org/{assets,content,layouts,node_modules,package.json,static}
Watching for config changes in /develop/unikernelalliance.org/config/_default, /develop/unikernelalliance.org/config/_default/menus
Start building sites …
hugo v0.119.0-b84644c008e0dc2c4b67bd69cccf87a41a03937e+extended linux/amd64 BuildDate=2023-09-24T15:20:17Z VendorInfo=gohugoio


                   | EN
-------------------+-----
  Pages            | 37
  Paginator pages  |  0
  Non-page files   |  0
  Static files     | 72
  Processed images | 14
  Aliases          |  5
  Sitemaps         |  2
  Cleaned          |  0

Built in 405 ms
Environment: "development"
Serving pages from memory
Web Server is available at http://localhost:1313/ (bind address 0.0.0.0)
Press Ctrl+C to stop
```

### (b) Build static site:

```console
npm run build
```

The static website should be in the `public` directory:

```text
public/
|-- 404.html
|-- apple-touch-icon.png
|-- blog/
|   |-- example-post/
|   |   `-- index.html
|   |-- index.html
|   |-- index.xml
|   |-- page/
|   |   `-- 1/
|   |       `-- index.html
|   `-- sitemap.xml
|-- categories/
|   |-- index.html
|   |-- index.xml
|   `-- page/
|       `-- 1/
|           `-- index.html
|-- contributors/
|   |-- index.html
|   |-- index.xml
|   `-- page/
|       `-- 1/
|           `-- index.html
|-- cover.png
|-- docs/
|   |-- guides/
|   |   |-- example-guide-111/
|   |   |   `-- index.html
|   |   |-- index.html
|   |   |-- index.xml
|   |   `-- sitemap.xml
|   |-- index.html
|   |-- index.xml
|   |-- reference/
|   |   |-- example-reference/
|   |   |   `-- index.html
|   |   |-- index.html
|   |   |-- index.xml
|   |   `-- sitemap.xml
|   `-- sitemap.xml
|-- en/
|   |-- index.html
|   `-- sitemap.xml
|-- favicon-150x150.png
|-- favicon-16x16.png
|-- favicon-192x192.png
|-- favicon-32x32.png
|-- favicon-512x512.png
|-- favicon.ico
|-- favicon.svg
|-- fonts/
[...]
|-- index.html
|-- index.xml
|-- js/
|   |-- app.1e84dcdaa5ccef6fe83f6d88ac1e444a1f237111cfa2a7a97427f758e9c27ef4.js
|   |-- color-mode.86a91f050a481d0a3f0c72ac26543cb6228c770875981c58dcbc008fd3f875c8.js
|   |-- flexsearch.78e4b7a9456a2770bd6faffb1f6488b30db12ca157c3df4e89e3ae2e258888ae.js
|   `-- search-modal.c4c023efcdee308e4b5f1110afe1db6b1656f217e67aa7efe54e2f4bf2feccf8.js
|-- main.77ec3b13291e19da56fd3d976a516a363623a782a2d5533bb4421e553b5207ee09816f4a448adac85cff292ac1ab9f46d86e64bd0f325c95beb792912a0a2bd1.css
|-- mask-icon.svg
|-- privacy/
|   `-- index.html
|-- projects/
|   |-- bima/
|   |   `-- index.html
|   |-- flexos/
|   |   `-- index.html
|   |-- genezio/
|   |   `-- index.html
|   |-- hermit/
|   |   `-- index.html
|   |-- hermitux/
|   |   `-- index.html
|   |-- index.html
|   |-- index.xml
|   |-- loupe/
|   |   `-- index.html
|   |-- mirage/
|   |   `-- index.html
|   |-- osv/
|   |   `-- index.html
|   |-- sitemap.xml
|   |-- toro/
|   |   `-- index.html
|   |-- unikraft/
|   |   `-- index.html
|   `-- urunc/
|       `-- index.html
|-- robots.txt
|-- search-index.json
|-- sitemap.xml
`-- tags/
    |-- index.html
    |-- index.xml
    `-- page/
        `-- 1/
            `-- index.html

36 directories, 135 files
```

and the output something like the following:

```console
$ npm run build

> unikernelalliance.org@0.0.0 build
> exec-bin node_modules/.bin/hugo/hugo --cleanDestinationDir --minify

Start building sites …
hugo v0.119.0-b84644c008e0dc2c4b67bd69cccf87a41a03937e+extended linux/amd64 BuildDate=2023-09-24T15:20:17Z VendorInfo=gohugoio


                   | EN
-------------------+-----
  Pages            | 37
  Paginator pages  |  0
  Non-page files   |  0
  Static files     | 72
  Processed images | 16
  Aliases          |  5
  Sitemaps         |  2
  Cleaned          |  0

Total in 1150 ms
```

## Auto-deploy on GitHub pages:

There's a deploy action through GitHub Actions in `.github/workflows/deploy-github.yml`.
Essentially, this action builds the static website and adds the `public/` directory to a separate branch `gh-pages`.
Enabling the `Pages` functionality of GitHub, allows the website to be deployed to `unikernelalliance.github.io` or to a custom domain we set from the `Settings`->`Pages`->`custom domain` option of the repository.

**Note**: The above was derived from: https://github.com/h-enk/doks-gh-pages, https://getdoks.org/docs/start-here/getting-started/.
