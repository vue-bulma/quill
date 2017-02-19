<template>
  <div class="quill-editor">
  </div>
</template>

<script>
import Quill from 'quill'

export default {

  props: {
    value: {
      type: String
    },
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
      this.$emit('input', this.editor.getText())
    })

  },

  watch: {
    value () {
      if (!this.editor.hasFocus()) {
        console.log('was set')
        this.editor.setText(this.value)
      }
    },
    focused (val) {
      this.editor[val ? 'focus' : 'blur']()
    }
  }

}
</script>

<style lang="styl">
@import '~quill/assets/core'
</style>
