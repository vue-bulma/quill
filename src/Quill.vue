<template>
  <div class="quill-editor">
    <slot></slot>
  </div>
</template>

<script>
import Quill from 'quill'

export default {

  props: {
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
    this.editor = new Quill(this.$el, this.options)
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
