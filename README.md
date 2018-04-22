# decentralised-data-workshop

Create a github repo.

Clone it.

    npm init -y
    npm i biiif --save
    npm i biiif-cli --save
    mkdir collection
    mkdir collection/_cats
    echo node_modules >> .gitignore
    touch .nojekyll

Add this to your package.json:

```
"scripts": {
    "build": "./node_modules/.bin/biiif collection -u https://[username].github.io/[repo]/collection"
}
```

Add some images of cats to the /collection/_cats folder

    git checkout -b gh-pages
    git add -A
    git commit -m "cats!"
    git push origin gh-pages

Open [username].github.io/[repo]/collection/index.json on universalviewer.io/examples
