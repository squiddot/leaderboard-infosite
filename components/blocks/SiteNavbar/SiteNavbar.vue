<template>
  <div>
    <div>
      <div>
        <NuxtLink to="/">
          <h1 v-show="lg">Leaderboards.gg</h1>
        </NuxtLink>
      </div>
      <div>
        <NavLinks />
      </div>
      <div>
        <select v-model="$colorMode.preference">
          <option value="system">System</option>
          <option value="dark">Dark</option>
          <option value="light">Light</option>
        </select>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import NavLinks from '@/components/blocks/NavLinks/NavLinks.vue';
import { defineComponent, ref } from '@nuxtjs/composition-api';
import { useBreakpoints } from '@vueuse/core';
import { theme } from '~/tailwind.config';
const breakpoints = useBreakpoints(theme.screens);

export default defineComponent({
  name: 'SiteNavbar',
  components: {
    NavLinks,
  },
  setup() {
    const lg = breakpoints.greater('lg');
    const mobileNavIsActive = ref(false);

    return {
      lg,
      mobileNavIsActive,
    };
  },
});
</script>
