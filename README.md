# Reproducibility on the HPC presentation 

Located at: [https://www.twin.uk.com/hpc-reproducibility/](https://www.twin.uk.com/hpc-reproducibility/)

This presentation is written in markdown and converted to reveal.js.

## Building with NodeJS

In NodeJS, the presentation is built using [`reveal-md`](https://github.com/webpro/reveal-md). 

You'll need to install nodejs to build. The easiest way to get the latest version:

* Install using [node version manager](https://github.com/nvm-sh/nvm)
* Install using conda (conda-forge channel) `conda install -c conda-forge nodejs`


### Install dependencies
```
npm install
```

### Run the slides with watcher

```
npm start
```

### Build to  `_site` folder

```
npm run build
```

### Automatic deployment

When pushing/merging to a master branch, a github action builds the site and publishes it to github pages.


