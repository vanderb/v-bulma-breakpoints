# v-bulma-breakpoints

Vue directive for conditional rendering (like v-if) element based on bulma-breakpoints

Based on package [vue-not-visible](https://github.com/PxyUp/vue-not-visible)

## Install

```bash
$ npm install --save vue-not-visible
```

```bash
$ yarn add vue-not-visible
```


## Use default

```js
import Vue from 'vue'
import VBulmaBreakpoints from 'v-bulma-breakpoints'

Vue.use(VBulmaBreakpoints)
```

```html
<template>
  <div id="test">
        {{ message }} {{ count }}
        <div v-is-breakpoint="'desktop'"> 
            <div v-on:click="count = count + 1">Not visible on touch(screen < 1024)</div>
        </div>
        <div v-is-breakpoint="'touch'">
            <div v-on:click="count = count + 1">Not visible on desktop(screen > 1024)</div>
        </div>
    </div>
</template>
```

## Breakpoints

Breakpoints are set to [https://bulma.io/documentation/overview/responsiveness/](bulma breakpoints).

**mobile (until 768px)**

```v-is-breakpoint="'mobile'"```

**tablet (from 769px)**

```v-is-breakpoint="'tablet'"```

**tablet-only (from 769px and until 1023px)**

```v-is-breakpoint="'tablet-only'"```

**touch (until 1023px)**

```v-is-breakpoint="'touch'"```

**desktop (from 1024px)**

```v-is-breakpoint="'desktop'"```

**desktop-only (from 1024px and until 1215px)**

```v-is-breakpoint="'desktop-only'"```

**widescreen (from 1216px)**

```v-is-breakpoint="'widescreen'"```

**widescreen-only (from 1216px and until 1407px)**

```v-is-breakpoint="'widescreen-only'"```

**fullhd (from 1408px)**

```v-is-breakpoint="'fullhd'"```

## License
[MIT License](https://github.com/PxyUp/vue-not-visible/blob/master/LICENSE)
