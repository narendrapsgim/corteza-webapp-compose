<template>
  <list-loader
    kind="record"
    :set="set"
    :namespace="namespace"
    :inline="field.options.inline"
    :mode="field.options.mode"
  />
</template>
<script>
import base from './base'
import ListLoader from 'corteza-webapp-compose/src/components/Public/Page/Attachment/ListLoader'

export default {
  components: {
    ListLoader,
  },

  extends: base,

  computed: {
    set () {
      return this.field.isMulti ? this.value : [this.value]
    },
  },
}
</script>
