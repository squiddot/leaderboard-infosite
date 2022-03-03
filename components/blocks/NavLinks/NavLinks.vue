<template>
  <nav class="nav-link-container">
    <NavLink v-for="navLink in navLinks" v-bind="navLink" :key="navLink.name">
      {{ navLink.name }}
    </NavLink>
  </nav>
</template>

<script lang="ts">
import { defineComponent } from '@nuxtjs/composition-api';
import NavLink from './NavLink/NavLink.vue';

export default defineComponent({
  name: 'NavLinks',
  components: {
    NavLink,
  },
  props: {
    navLinks: {
      default: () => [
        {
          name: 'Blog',
          to: '/blog',
        },
        {
          name: 'About',
          to: '/',
        },
      ],
      type: Array,
    },
  },
});
</script>

<style scoped></style>
