<template>
  <div class="quill-editor">
    <slot></slot>
  </div>
</template>

<script>
import Quill from 'quill'

export default {

  props: {
    value: String,
    options: {
      type: Object,
      default: () => ({})
    },
    autofocus: Boolean
  },

  data () {
    return {
      focused: this.autofocus,
      editor: null
    }
  },

  mounted () {
    let rootEl = this.$el
    this.editor = new Quill(rootEl, this.options)
    this.editor.on('text-change', () => {
      this.$emit('input', rootEl.querySelector('.ql-editor').innerHTML)
    })
  },

  watch: {
    focused (val) {
      this.editor[val ? 'focus' : 'blur']()
    }
  }

}
</script>

<style lang="styl">
@import '~quill/assets/core'
</style>
