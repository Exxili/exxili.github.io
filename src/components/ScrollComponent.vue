<template>
  <q-scroll-area
  ref="scroller"
  :bar-style="barStyle"
  :thumb-style="thumbStyle"
  style="height: calc(100vh - 50px); max-width: 100vw;"
  >
    <!-- <div class="row no-wrap text-white">
      <div v-for="n in 100" :key="n" style="width: 150px" class="q-pa-sm">
        Lorem ipsum dolor sit amet consectetur adipisicing elit.
        Architecto fuga quae veritatis blanditiis sequi id expedita
        amet esse aspernatur! Iure, doloribus!
      </div>
    </div> -->
    <div class="row no-wrap">
      <HomePage />
      <SkillsPage />
      <HobbiesComponent /> -->
    </div>

  </q-scroll-area>
</template>

<script lang="ts">
import { defineComponent, ref, onMounted } from "vue";
import HomePage from "src/pages/Home.vue";
import SkillsPage from "src/pages/Skills.vue";
// import HobbiesComponent from "src/components/HobbiesComponent.vue";

function ScrollHandler() {
  onMounted(() => {
    // Setup Scrolling to be horizontal
    const scroller = ref(null);

    console.log("Value", ScrollBoi.value);

    // if (scrollArea.value) {
    // // Add event listener for wheel
    //   scrollArea.value.addEventListener("wheel", (event) => {
    //   // Prevent default behaviour
    //     event.preventDefault();

    //     if (scrollArea.value?.scrollLeft) {
    //       scrollArea.value.scrollLeft += event.deltaY;
    //     }
    //   });
    // }
  });

  return {
  };
}

export default defineComponent({
  name: "ScrollComponent",
  components: {
    HomePage,
    SkillsPage,
    // HobbiesComponent,
  },
  setup() {
    return {
      ...ScrollHandler(),
      barStyle: {
        zIndex: "0",
        visible: true,
        right: "2px",
        borderRadius: "9px",
        backgroundColor: "#ffffff",
        width: "8px",
        opacity: 0.1,
      },
      thumbStyle: {
        right: "2px",
        borderRadius: "0px",
        backgroundColor: "#ffffff",
        width: "5px",
        opacity: 0.75,
      },
    };
  },
});
</script>

<style lang="scss">

.rocket {
  position: absolute;
  height: 100px;
  width: 100px;
  left: 0px;
  bottom: 0px;
}

</style>
