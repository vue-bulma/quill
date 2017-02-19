# Quill

Your powerful, rich text editor http://quilljs.com


## Installation

```
$ npm install vue-bulma-quill --save
```


## Examples

```vue
<template>
  <div class="box">
    <h3 class="title">
      Your powerful, rich text editor.
      <a href="http://quilljs.com">http://quilljs.com</a>
    </h3>
    <quill :options="{ theme: 'snow' }" v-model="htmlContent">
      <h2>One Ring to Rule Them All</h2>
      <p><a href="http://en.wikipedia.org/wiki/One_Ring">http://en.wikipedia.org/wiki/One_Ring</a></p>
      <p><br/></p>
      <p>Three Rings for the <em>Elven-kings</em> under the sky,</p>
      <p>Seven for the <u>Dwarf-lords</u><span> in halls of stone,</p>
      <p>Nine for <u>Mortal Men</u>, doomed to die,</p>
      <p>One for the <u>Dark Lord</u> on his dark throne.</p>
      <p><br/></p>
      <p>In the Land of Mordor where the Shadows lie.</span></p>
      <p>One Ring to <strong>rule</strong> them all, One Ring to <strong>find</strong> them,</p>
      <p>One Ring to <strong>bring</strong> them all and in the darkness <strong>bind</strong> them.</p>
      <p>In the Land of Mordor where the Shadows lie.</p>
    </quill>
  </div>
</template>

<script>
import Quill from 'vue-bulma-quill'

export default {
  components: {
    Quill
  },
  data: () {
    return {
      htmlContent: ''
    }
  }
}
</script>

<style lang="styl">
@import "~quill/assets/snow"
</style>
```


## Badges

![](https://img.shields.io/badge/license-MIT-blue.svg)
![](https://img.shields.io/badge/status-stable-green.svg)

---

> [fundon.me](https://fundon.me) &nbsp;&middot;&nbsp;
> GitHub [@fundon](https://github.com/fundon) &nbsp;&middot;&nbsp;
> Twitter [@_fundon](https://twitter.com/_fundon)
