<template>
  <NuxtLink class="button-link" :to="url" v-bind="$attrs" v-on="$listeners">
    <slot>Placeholder Link Text</slot>
  </NuxtLink>
</template>

<script lang="ts">
export default {
  name: 'ButtonLink',
  props: {
    alt: {
      type: String,
      default: '',
    },
    target: {
      type: String,
      default: '',
    },
    url: {
      type: String,
      default: '',
    },
  },
};
</script>

<style lang="postcss" scoped></style>
