<script setup>
import { AttributeIcon } from '@/components'

defineProps({
  name: {
    type: String,
    required: true
  },
  color: {
    type: String,
    required: true
  },
  rating: {
    type: Number,
    required: true
  },
  iconName: {
    type: String,
    required: true
  }
})
</script>

<template>
  <div :class="`attribute-item ${color}`">
    <div class="l-inline">
      <AttributeIcon :name="iconName" />
      <p class="name">{{ name }}</p>
    </div>
    <p class="rating">
      <span>{{ rating }}</span> / 100
    </p>
  </div>
</template>
