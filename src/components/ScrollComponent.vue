<template>
  <q-scroll-area :bar-style="barStyle" :thumb-style="thumbStyle"
  style="height: 100vh; max-width: 100vw;">
    <div class="row no-wrap text-white">
      <div v-for="n in 100" :key="n" style="width: 150px" class="q-pa-sm">
        Lorem ipsum dolor sit amet consectetur adipisicing elit.
        Architecto fuga quae veritatis blanditiis sequi id expedita
        amet esse aspernatur! Iure, doloribus!
      </div>
    </div>
  </q-scroll-area>
</template>

<script>
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'ScrollComponent',
  setup() {
    return {
      barStyle: {
        zIndex: '0',
        visible: true,
        right: '2px',
        borderRadius: '9px',
        backgroundColor: '#ffffff',
        width: '8px',
        opacity: 0.1,
      },
      thumbStyle: {
        right: '2px',
        borderRadius: '0px',
        backgroundColor: '#ffffff',
        width: '5px',
        opacity: 0.75,
      },
    };
  },
});
</script>
