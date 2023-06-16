<script setup>
import { defineAsyncComponent } from 'vue'

const props = defineProps({
  name: {
    type: String,
    required: true
  }
})

const icon = defineAsyncComponent(() => import(`@/components/icons/${props.name}.vue`))
</script>

<template>
  <component :is="icon" />
</template>
