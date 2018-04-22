# decentralised-data-workshop

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
    "build": "./node_modules/.bin/biiif collection -u https://[username].github.io/[repo]/collection"
}
```

Add a cat pic to the /collection/_cat folder

    git checkout -b gh-pages
    git add -A
    git commit -m "cat!"
    git push origin gh-pages

Open [username].github.io/[repo]/collection/index.json on universalviewer.io/examples

## metadata

Create /collection/_cat/info.yml containing:

```yml
description: A cute cat
```

    npm run build
    git add -A
    git commit -m "added description"
