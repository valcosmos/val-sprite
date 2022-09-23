<script setup lang="ts">
import { PropType } from 'vue'
const props = defineProps({
  name: {
    type: String as PropType<'vue' | 'add'>,
    required: true
  },
  onClick: {
    type: Function as PropType<(e: MouseEvent | TouchEvent) => void>
  }
})
</script>

<template>
  <svg class="icon" @click="props.onClick">
    <use :xlinkHref="'#' + props.name"></use>
  </svg>
</template>

<style scoped>
.icon {
  width: 1.2em;
  height: 1.2em;
}
</style>
