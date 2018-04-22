# decentralised-data-workshop

You'll need git and npm installed.

Create a github repo.

Clone it.

    npm init -y
    npm i biiif --save
    npm i biiif-cli --save
    mkdir collection
    mkdir collection/_cat
    echo node_modules >> .gitignore
    touch .nojekyll

Add this to your package.json:

```
"scripts": {
    "build": "./node_modules/.bin/biiif collection -u https://edsilv.github.io/decentralised-data-workshop/collection"
}
```

Add a cat pic to the /collection/_cat folder

    git checkout -b gh-pages
    git add -A
    git commit -m "cat!"
    git push origin gh-pages

Open on [http://universalviewer.io/examples](http://universalviewer.io/examples/#?c=&m=&s=&cv=&manifest=https%3A%2F%2Fedsilv.github.io%2Fdecentralised-data-workshop%2Fcollection%2Findex.json)

## metadata

Create /collection/_cat/info.yml containing:

```yml
label: Cat
description: A cute cat
```

    npm run build
    git add -A
    git commit -m "added description"
    git push origin gh-pages

Open on [http://universalviewer.io/examples](http://universalviewer.io/examples/#?c=&m=&s=&cv=&manifest=https%3A%2F%2Fedsilv.github.io%2Fdecentralised-data-workshop%2Fcollection%2Findex.json)