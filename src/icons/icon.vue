<template>
    <component :is="name">
    </component>
</template>

<script>
import * as icons from './variants'
/* eslint-disable vue/multi-word-component-names */
/* eslint-disable */
export default {
  name: 'icon',
  components: {...icons},
  props: {
    name: String,
    required: true
  }
}
</script>
