<template>
  <q-scroll-area
  ref="scrollAreaRef"
  @wheel="onWheel"
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
    <div ref="abc" class="row no-wrap">
      <HomePage />
      <SkillsPage />
      <HobbiesPage />
    </div>

  </q-scroll-area>
</template>

<script lang="ts">
import { defineComponent, ref } from "vue";
import HomePage from "src/pages/Home.vue";
import SkillsPage from "src/pages/Skills.vue";
import HobbiesPage from "src/pages/Hobbies.vue";
import { QScrollArea } from "quasar";
// import HobbiesComponent from "src/components/HobbiesComponent.vue";

function ScrollHandler() {
  // onMounted(() => {

  //   // if (scrollArea.value) {
  //   // // Add event listener for wheel
  //   //   scrollArea.value.addEventListener("wheel", (event) => {
  //   //   // Prevent default behaviour
  //   //     event.preventDefault();

  //   //     if (scrollArea.value?.scrollLeft) {
  //   //       scrollArea.value.scrollLeft += event.deltaY;
  //   //     }
  //   //   });
  //   // }
  // });

  return {
  };
}

export default defineComponent({
  name: "ScrollComponent",
  components: {
    HomePage,
    SkillsPage,
    HobbiesPage,
  },
  setup() {
    const scrollAreaRef = ref<QScrollArea>();
    let position = 0;

    const onWheel = (event: any) => {
      // eslint-disable-next-line @typescript-eslint/no-unsafe-member-access
      // console.log(event.deltaY);
      // eslint-disable-next-line @typescript-eslint/no-unsafe-member-access
      // const amount = event.deltaY <= 0 ? -30 : 30;
      // const left = scrollAreaRef.value?.getScrollPosition().left;
      // console.log(left);
      // eslint-disable-next-line @typescript-eslint/no-unsafe-assignment
      // if (left) {
      // const position = left + amount;
      // console.log("innerWidth", window.innerWidth);

      // eslint-disable-next-line @typescript-eslint/no-unsafe-member-access
      if (event.deltaY > 0) {
        // eslint-disable-next-line @typescript-eslint/no-unsafe-member-access
        // console.log("deltaY", event.deltaY);
        position += 10;
        scrollAreaRef.value?.setScrollPosition("horizontal", position, 10);
        console.log(scrollAreaRef.value);
        // console.log("Position", position);
      // eslint-disable-next-line @typescript-eslint/no-unsafe-member-access
      } else if (event.deltaY < 0) {
        // eslint-disable-next-line @typescript-eslint/no-unsafe-member-access
        // console.log("deltaY", event.deltaY);
        position -= 10;
        scrollAreaRef.value?.setScrollPosition("horizontal", position, 10);
        // console.log("Position", position);
      }
      // console.log(scrollAreaRef.value);
      // }
    };
    // Setup Scrolling to be horizontal
    // const scroller = ref<HTMLElement>();
    // const abc = ref();

    // onMounted(() => {
    //   // console.log("scroller", scroller.value);
    //   // console.log("abc", abc.value);

    //   if (scroller.value) {
    //     // Add event listener for wheel
    //     scroller.value.addEventListener("wheel", (event) => {
    //       // Prevent default behaviour
    //       event.preventDefault();

    //       if (scroller.value?.scrollLeft) {
    //         scroller.value.scrollLeft += event.deltaY;
    //       }
    //     });
    //   }
    // });

    return {
      scrollAreaRef,
      onWheel,
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
