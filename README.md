# Template App Migration Dojo Cookbook Site

This is a [Hugo](https://github.com/spf13/hugo) site. It is driven by markdown files that can be generated using the commands provided in this document.

## Getting Started

### Initial Setup

- Install `hugo`
  - With homebrew (Mac): `brew update && brew install hugo`
  - Manual download: https://github.com/spf13/hugo/releases
- Clone this repo with the `--recursive` flag to include the theme, which is a submodule:
```
git clone https://github.com/pivotalservices/modernization-cookbook-template.git --recursive
```
Clone this branch:
```
git clone -b canonical-cookbook-template https://github.com/pivotalservices/modernization-cookbook-template.git --recursive
```
  - Alternatively, fetch the theme manually: `git submodule update --init --recursive`

### Run locally (default: `localhost:1313`)
```
./localserver
```

### Publish Instructions
```
./publish
cf push
```

### Add New Inception document
```
hugo new inception/(title).md
```

### Add New Application
```
hugo new applications/(title).md
```
### Add New Blocker
```
hugo new blockers/(title).md
```

Add `resolved=true` to metadata header to mark a blocker resolved.

### Add New Recipe
```
hugo new recipes/(title).md
```
### Add New Document
```
hugo new documents/(title).md
```

### Add New Lightweight Architecture Decision Record
```
hugo new decisions/(title).md
```

## Updating the theme

This site uses the `hugo-theme-docdock` theme, which is stored as a git submodule
under the `themes` directory.

To pull the latest version of the theme, simply update your submodules: `git submodule update --init --recursive`.
