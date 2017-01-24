# Jsdoc to markdown

Instruction how to use [jsdoc-to-markdown](https://www.npmjs.com/package/jsdoc-to-markdown) package
to generate api documentation in README.md files.

## Instructions
First install [jsdoc-to-markdown](https://www.npmjs.com/package/jsdoc-to-markdown) globally
```
npm install -g jsdoc-to-markdown
```

Run `cp README.md README.hbs` (hbs is ending for handlebars)

Add the following code to your README.hbs in a approperiate place 
```md
## API
{{>main}}
```

Update package.json with 

```json
 "scripts": {
    "jsdoc-to-markdown":"jsdoc2md --template README.hbs --files {source files with jsdoc space separated} > README.md"
  },
``` 
