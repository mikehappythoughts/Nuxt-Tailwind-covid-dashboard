<template>
  <button
    v-bind="$attrs"
    v-on="{
      ...$listeners,
    }"
    @click.prevent="handleClick"
  >
    <slot></slot>
  </button>
</template>

<script>
export default {
  name: 'BaseButton',
  methods: {
    handleClick() {
      this.$emit('clicked')
    },
  },
}
</script>
<style></style>
