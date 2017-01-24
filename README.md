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
{{>all-docs~}}
```

One can also user `{{>main-index~}}` to get html and `{{>main}`

Update package.json with 

```json
 "scripts": {
    "jsdoc-to-markdown":"jsdoc2md --template README.hbs --files {src files} > README.md"
  },
``` 

## Design
For parameters use list
- a parameter
  - a subparamter
- another parameter

@returns {promise} list with data from each file
