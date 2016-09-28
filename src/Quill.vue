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
    }
  },

  data () {
    return {
      editor: null
    }
  },

  mounted () {
    this.editor = new Quill(this.$el, this.options)
  }

}
</script>

<style lang="styl">
@import '~quill/assets/core'
</style>
