# Sample WebApp for IPFS

Goal of this sample app is to better understand what is necessary to tweak in mondern javascript frameworks so that they will work with the ipfs gateway.

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).

## deploy to ipfs cluster

pre checkout [this project](https://github.com/idev4u/ipfs-cluster-playground)

```
$ ipfs-cluster-ctl add -r dist/
```

Current knowledge
Tweaks:
* switch to relative path so that the merkle hash as path prefix is not a issue when files get loaded.
  example `/js/some.js` to `js/some.js` this handles the ipfs resource path `http://127.0.0.1:8080/ipfs/QmRm8PZQT8EL9sTTghBhbUVjQJxxxxxxxxxMbaLyfSXBDy5/js/some.js`

