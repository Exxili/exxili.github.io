<template>
  <div class="column justify-center items-center"
  style="background-color: transparent; width: 100vw; height: calc(100vh - 50px);">

  <div class="row text-white">1</div>
  <div class="row text-white">1</div>
  <div class="row text-white">1</div>
  <div class="col">1</div>

  <!-- Avatar -->
    <q-avatar class="row" size="250px" bordered>
      <q-img class="col" src="~assets/Images/me.jpg"/>
    </q-avatar>

  <!-- Title -->
    <div class="row q-pa-md">
      <div class="col greeting">
        Hey I'm Andy
      </div>
    </div>

  <!-- Continue -->
  <q-btn
    class="continue q-pa-md"
    outline
    rounded
    label="Lets go..."
  />
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'Home',
  setup() {
    return {
    };
  },
});

</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Rock+Salt&display=swap');

.greeting {
  font-family: 'Rock Salt', cursive;
  font-size: 46px;
  color: white;
}

.continue {
  font-size: 18px;
  color: white;
}
</style>
