<template>
  <a :class="[classes, 'text-center']" :href="link">{{ label }}</a>
</template>

<script>
export default {
  name: 'BaseButton',
  props: {
    label: {
      type: String,
      default: 'Button',
    },
    link: {
      type: String,
      default: '#',
    },
    classes: {
      type: String,
      default: 'btn',
    },
  },
}
</script>
