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
    <quill :options="{ theme: 'snow' }"></quill>
  </div>
</template>

<script>
import Quill from 'vue-bulma-quill'

export default {
  components: {
    Quill
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
