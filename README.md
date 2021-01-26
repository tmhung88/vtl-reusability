## Description

This example uses [a cli](https://github.com/fnobi/ejs-cli) built on top of [EJS](https://github.com/mde/ejs). It's capable to insert one VTL script to another.
- Input:
```
# File: src/vtl/Query.query1.vtl
<%- include('level1/level1-scriptA.vtl'); %>
// perform query1.vtl
<%- include('level1/level1-scriptB.vtl'); %>
```

- Output:

```
# File: dist/vtl/Query.query1.vtl
// perform level2-script.vtl
// perform level1-scriptA.vtl

// perform query1.vtl
// perform level2-script.vtl
// perform level1-scriptB.vtl
```


## How to
- Execute `npm run build` to process vtl scripts
