<template>
  <q-layout view="lHh Lpr lFf">
    <q-header flat class="transparent">

      <!-- HeaderSVG -->
      <!-- <q-img src="~assets/Images/HeaderBar.svg"
      style="position: absolute; min-height: 50%; max-height: 100vh; overflow: visible;" /> -->

      <!-- Logo -->
      <!-- <q-img :src="LogoTransparent"
      style="position: absolute; min-height: 50%; max-height: 100vh; overflow: visible;" /> -->

      <q-toolbar>
        <!-- <q-btn
          flat
          dense
          round
          icon="menu"
          aria-label="Menu"
          @click="toggleLeftDrawer"
        />

        <q-toolbar-title>
          Quasar App
        </q-toolbar-title>

        <div>Quasar v{{ $q.version }}</div> -->
      </q-toolbar>
    </q-header>

    <!-- <q-drawer
      v-model="leftDrawerOpen"
      show-if-above
      overlay
      mobile
      style="background-color: #151515;"
    >
      <q-list>
      </q-list>
    </q-drawer> -->

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';

export default defineComponent({
  name: 'MainLayout',

  components: {
  },

  setup() {
    const leftDrawerOpen = ref(false);

    return {
      leftDrawerOpen,
      toggleLeftDrawer() {
        leftDrawerOpen.value = !leftDrawerOpen.value;
      },
    };
  },
});
</script>
