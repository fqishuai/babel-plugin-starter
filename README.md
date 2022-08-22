## babel-plugin-starter
> using this starter to create your own babel plugin

### Babel Plugin Development
> [babel-handbook](https://github.com/jamiebuilds/babel-handbook/blob/master/translations/en/plugin-handbook.md)

```js
export default function() {
  return {
    visitor: {
      Identifier(path) {
        const name = path.node.name;
        // reverse the name: JavaScript -> tpircSavaJ
        path.node.name = name
          .split("")
          .reverse()
          .join("");
      },
    },
  };
}
```

### Use this starter
```js
npx degit fqishuai/babel-plugin-starter#main your-project-name
```