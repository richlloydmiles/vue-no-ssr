# vue-no-ssr

[![NPM version](https://img.shields.io/npm/v/vue-no-ssr.svg?style=flat)](https://npmjs.com/package/vue-no-ssr) [![NPM downloads](https://img.shields.io/npm/dm/vue-no-ssr.svg?style=flat)](https://npmjs.com/package/vue-no-ssr) [![CircleCI](https://circleci.com/gh/egoist/vue-no-ssr/tree/master.svg?style=shield)](https://circleci.com/gh/egoist/vue-no-ssr/tree/master)  [![donate](https://img.shields.io/badge/$-donate-ff69b4.svg?maxAge=2592000&style=flat)](https://github.com/egoist/donate)

## Install

```bash
yarn add vue-no-ssr
```

## Usage

```vue
<template>
  <div id="app">
    <h1>My Website</h1>
    <no-ssr>
      <!-- this component will only be rendered on client-side -->
      <comments />
    </no-ssr>
  </div>
</template>

<script>
  import NoSSR from 'vue-no-ssr'

  export default {
    components: {
      'no-ssr': NoSSR
    }
  }
</script>
```

Note that `<no-ssr />` can only contain at most **ONE** child component/element.

### Placeholder

Use a component or text as placeholder until `<no-ssr />` is mounted on client-side.

eg, show a loading indicator.

```vue
<template>
  <div id="app">
    <h1>My Website</h1>
    <no-ssr :placeholder="Loading">
      <!-- this component will only be rendered on client-side -->
      <comments />
    </no-ssr>
  </div>
</template>

<script>
  import NoSSR from 'vue-no-ssr'

  export default {
    data() {
      return {
        Loading: require('./Loading.vue')
      }
    },
    components: {
      'no-ssr': NoSSR
    }
  }
</script>
```

## Development

```bash
yarn install

# Run example
yarn example
```

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D


## Author

**vue-no-ssr** © [egoist](https://github.com/egoist), Released under the [MIT](./LICENSE) License.<br>
Authored and maintained by egoist with help from contributors ([list](https://github.com/egoist/vue-no-ssr/contributors)).

> [egoistian.com](https://egoistian.com) · GitHub [@egoist](https://github.com/egoist) · Twitter [@rem_rin_rin](https://twitter.com/rem_rin_rin)
