# biiif-workshop

Learn how to use [biiif](https://github.com/edsilv/biiif) to generate [IIIF](http://iiif.io) data from static files and host it on github pages.

Browse: https://edsilv.github.io/biiif-workshop/

---

## Setup

Ensure you have [git](https://git-scm.com/) and [nodejs](https://nodejs.org/en/) installed.

Create a github repo named 'biiif-workshop'.

From here onwards, `[username]` should be replaced with your github username.

Clone your repo and `cd` into it. Now run:

    git checkout -b gh-pages
    npm init -y
    npm i biiif-cli -g
    biiif collection -u https://[username].github.io/biiif-workshop/collection -s

Add this to your `package.json`:

```
"scripts": {
    "build": "biiif collection -u https://[username].github.io/biiif-workshop/collection"
}
```

    mkdir collection/_cat

Add a cat pic to the `/collection/_cat` folder

    npm run build
    git add -A
    git commit -m "cat pic"
    git push origin gh-pages

Open `https://[username].github.io/biiif-workshop/collection/index.json` on [http://universalviewer.io/examples](http://universalviewer.io/examples/#?c=&m=&s=&cv=&manifest=https%3A%2F%2Fedsilv.github.io%2Fbiiif-workshop%2Fcollection%2Findex.json)

## Metadata

Create `/collection/_cat/info.yml` containing:

```yml
label: Cat
description: A picture of a cat
```

    npm run build
    git add -A
    git commit -m "added description"
    git push origin gh-pages

Open `https://[username].github.io/biiif-workshop/collection/index.json` on [http://universalviewer.io/examples](http://universalviewer.io/examples/#?c=&m=&s=&cv=&manifest=https%3A%2F%2Fedsilv.github.io%2Fbiiif-workshop%2Fcollection%2Findex.json)

Open the 'more information' panel on the right hand side to see the descriptive metadata.

## Advanced

See the contents of this repository for a more complete example (a book about cats!)