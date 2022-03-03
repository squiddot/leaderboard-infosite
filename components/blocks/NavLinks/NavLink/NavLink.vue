<template>
  <ButtonLink class="nav-link" v-bind="$attrs" v-on="$listeners">
    <slot />
  </ButtonLink>
</template>

<script lang="ts">
import ButtonLink from '@/components/elements/ButtonLink/ButtonLink.vue';

export default {
  name: 'NavLink',
  components: {
    ButtonLink,
  },
};
</script>

<style scoped></style>
