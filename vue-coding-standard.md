
# Coding Standard For Vue.js Projects

### JavaScript Standard Rules

We follow https://github.com/standard/standard#the-rules to write JS.

The linter is configured to follow these rules too.

### JSDoc
We follow https://en.wikipedia.org/wiki/JSDoc to write doc blocks

### Vue.js Official Style Guide
https://vuejs.org/v2/style-guide/

### The best parts of Idiomatic JavaScript
We follow main principals from the [Idiomatic Style Manifesto](https://github.com/rwaldron/idiomatic.js) but if some of them conflict with the JavaScript Standard Rules - the Standard wins.

Most useful parts of it are: [Type checking](https://github.com/rwaldron/idiomatic.js/#type) and [Conditional Evaluation](https://github.com/rwaldron/idiomatic.js/#cond)

### Styles
- We use SCSS preprocessor http://sass-lang.com/
- Avoid putting style inside Vue components

### Variables and functions naming

1. **variable name** - should be noun. The variable name should clearly and briefly explain what a variable exactly stores.
**Don't use the "Hungarian notation" identifiers names.**

2. **function name** - should be a verb or should start with verb. Function names should be written in English using **camelCase**. The function name should clearly and shortly explain what the function exactly does.

3. **Cases**:
```js
functionNamesLikeThis
variableNamesLikeThis
ConstructorNamesLikeThis
ClassNameLikeThis
EnumNamesLikeThis
methodNamesLikeThis
SYMBOLIC_CONSTANTS_LIKE_THIS
```

4. **Other naming related recommendations**
```
// string
const dog = '...'

// array
const dogs = []
```

### Inline comments

1. Single-line comments one line above the code
2. Multi-line comments are also welcome
3. Avoid comments at the end of the line


### Vue Component/instance options order

**Component/instance options should be ordered consistently.**

This is the default order we use for component options. They're split into categories, so you'll know where to add new properties.

1. **Side Effects** (triggers effects outside the component)
  - `el`

2. **Global Awareness** (requires knowledge beyond the component)
  - `name`
  - `parent`

3. **Component Type** (changes the type of the component)
  - `functional`

4. **Template Modifiers** (changes the way templates are compiled)
  - `delimiters`
  - `comments`

5. **Template Dependencies** (assets used in the template)
  - `components`
  - `directives`
  - `filters`

6. **Composition** (merges properties into the options)
  - `extends`
  - `mixins`

7. **Interface** (the interface to the component)
  - `inheritAttrs`
  - `model`
  - `props`/`propsData`

8. **Local State** (local reactive properties)
  - `data`
  - `computed`

9. **Events** (callbacks triggered by reactive events)
  - `watch`
  - Lifecycle Events (in the order they are called)

10. **Non-Reactive Properties** (instance properties independent of the reactivity system)
  - `methods`

11. **Rendering** (the declarative description of the component output)
  - `template`/`render`
  - `renderError`


### Vuex usage convention

- Use actions only if you need wrap some mutation with some async logic. Don't just duplicate a mutation with an action.
- Use getter only if it returns some computed value and don't use it if in case it just returns state value

### Git conventions
- We follow GitFlow process https://danielkummer.github.io/git-flow-cheatsheet/
- We do code review via Pull Request in GitHub/Gitlab/Bitbucket

### ES6 first
Prefer ES6 syntax over older ES versions

### Functional Programming
[Recommendation] Prefer functional approach when possible
