<template>
  <div class="stars"></div>
  <div class="twinkling"></div>
  <div class="clouds"></div>

  <!-- <div id="rocket" class="rocket"></div> -->

  <ScrollComponent style="z-index: 5;" @scroll="onScroll" />
</template>

<script lang="ts">
/* eslint-disable @typescript-eslint/no-unsafe-member-access */
/* eslint-disable @typescript-eslint/no-unsafe-assignment */
import { defineComponent } from 'vue';
import ScrollComponent from 'src/components/ScrollComponent.vue';

function PageIndexHandler() {
  let left = 0;
  let bottom = 0;
  // let flag = false;

  const onScroll = (e: any) => {
    const element = document.getElementById('rocket');

    console.log(e);

    // eslint-disable-next-line @typescript-eslint/no-unsafe-assignment
    if (element !== null) {
      // console.log('here', element.style.left);
      left = e.horizontalPercentage * window.innerWidth;
      bottom = 200 * Math.sin((Math.PI * e.horizontalPercentage));

      // bottom = e.horizontalPercentage * window.innerHeight;

      console.log('left, bottom', left, bottom);

      // console.log('flag', flag);

      // if (bottom === 0) {
      //   flag = false;
      // }

      // if (bottom === 200) {
      //   flag = true;
      // }

      // if (flag === false) {
      //   bottom += 10;
      // } else {
      //   bottom -= 10;
      // }

      element.style.left = `${left}px`;
      element.style.bottom = `${bottom}px`;

      console.log("bottom", element.style.bottom);
    }
  };

  // const onMouseWheel = (e: any) => {
  //   const element = document.getElementById('rocket');

  //   console.log(e);

  //   // eslint-disable-next-line @typescript-eslint/no-unsafe-assignment
  //   if (element !== null) {
  //     // console.log('here', element.style.left);
  //     element.style.left = `${e.scrollPercent * window.innerWidth}px`;
  //   }
  // };

  return {
    onScroll,
    // onMouseWheel,
  };
}

export default defineComponent({
  name: 'PageIndex',
  components: { ScrollComponent },
  setup() {
    return {
      ...PageIndexHandler(),
    };
  },
});
</script>

<style lang="scss">

.rocket {
  z-index: 11;
  position: absolute;
  height: 100px;
  width: 100px;
  left: 0px;
  bottom: 0px;
  background-color: red;
}

.stars, .twinkling, .clouds {
  position:absolute;
  display:block;
  top:0; bottom:0;
  left:0; right:0;
  width:100%; height:100%;
}

.stars {
  z-index: 0;
  background: #000 url('https://image.ibb.co/mjnygo/stars.png') repeat top center;
}

.twinkling{
  z-index: 1;
  background:transparent url('https://image.ibb.co/ir1DE8/twinkling.png') repeat top center;
  animation: move-twink-back 200s linear infinite;
}

.clouds{
  z-index: 2;
  background:transparent url('https://image.ibb.co/bT4N7T/clouds.png') repeat top center;
  animation: move-clouds-back 200s linear infinite;
}

@keyframes move-twink-back {
  from {background-position:0 0;}
  to {background-position:-10000px 5000px;}
}

@keyframes move-clouds-back {
  from {background-position:0 0;}
  to {background-position:10000px 0;}
}

</style>
