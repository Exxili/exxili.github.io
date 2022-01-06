<template>
<div class="column justify-center items-center"
  style="background-color: transparent; width: 100vw; height: calc(100vh - 50px);">

    <!-- Title -->
    <div class="row q-pa-md">
      <div class="col skillsTitle">
        Technologies I'm great with
      </div>
    </div>

    <!-- Technology Logos Row 1-->
    <div class="row q-pa-md">
      <!-- Javascript -->
      <q-img class="grayscale"
      src="~assets/Images/jsLogo.png" style="height: 50px; width: 50px; margin: 2px;"/>
      <!-- Typescript -->
      <q-img class="grayscale"
      src="~assets/Images/tsLogo.png" style="height: 50px; width: 50px; margin: 2px;"/>
      <!-- Quasar Framework -->
      <q-img class="grayscale"
      src="~assets/Images/quasarLogo.png" style="height: 50px; width: 50px; margin: 2px"/>
      <!-- Electron -->
      <q-img class="grayscale"
      src="~assets/Images/electronLogo.svg" style="height: 50px; width: 50px; margin: 2px"/>
      <!-- CSharp Logo -->
      <q-img class="grayscale"
      src="~assets/Images/csharpLogo.png" style="height: 50px; width: 50px; margin: 2px"/>
      <!-- WPF Logo -->
      <q-img class="grayscale"
      src="~assets/Images/wpfLogo.png" style="height: 50px; width: 50px; margin: 2px"/>
      <!-- VsCode Logo -->
      <q-img class="grayscale"
      src="~assets/Images/vsCodeLogo.png" style="height: 50px; width: 50px; margin: 2px"/>
      <!-- Visual Studio Logo -->
      <q-img class="grayscale"
      src="~assets/Images/visualStudioLogo.png" style="height: 50px; width: 50px; margin: 2px"/>
       <!-- Capacitor Logo -->
      <q-img class="grayscale"
      src="~assets/Images/capacitorLogo.png" style="height: 50px; width: 50px; margin: 2px"/>
       <!-- Cordova Logo -->
      <q-img class="grayscale"
      src="~assets/Images/cordovaLogo.png" style="height: 50px; width: 50px; margin: 2px"/>
    </div>

    <!-- Technology Logos Row 2-->
    <div class="row q-pa-md">
      <!-- Gitlab -->
      <q-img class="grayscale"
      src="~assets/Images/gitlabLogo.png" style="height: 50px; width: 50px; margin: 2px;"/>
      <!-- Github -->
      <q-img class="grayscale"
      src="~assets/Images/githubLogo.png"
      style="height: 50px; width: 50px; margin: 2px;"/>
      <!-- Vue-->
      <q-img class="grayscale"
      src="~assets/Images/vueLogo.svg" style="height: 50px; width: 50px; margin: 2px;"/>
      <!-- AWS -->
      <q-img class="grayscale"
      src="~assets/Images/awsLogo.png"
      style="height: 50px; width: 80px; margin: 2px;"/>
      <!-- DigitalOcean -->
      <q-img class="grayscale"
      src="~assets/Images/doLogo.png" style="height: 50px; width: 50px; margin: 2px;"/>
      <!-- Ubuntu -->
      <q-img class="grayscale"
      src="~assets/Images/ubuntuLogo.svg" style="height: 50px; width: 50px; margin: 2px;"/>
      <!-- NestJS -->
      <q-img class="grayscale"
      src="~assets/Images/nestjsLogo.svg" style="height: 50px; width: 50px; margin: 2px;"/>
      <!-- Serverless Framework -->
      <q-img class="grayscale"
      src="~assets/Images/serverlessLogo.svg" style="height: 50px; width: 50px; margin: 2px;"/>
      <!-- MySql -->
      <q-img class="grayscale"
      src="~assets/Images/mysqlLogo.png" style="height: 50px; width: 70px; margin: 2px;"/>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "Skills",
  setup() {
    return {

    };
  },
});

</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Rock+Salt&display=swap');

.skillsTitle {
  font-family: 'Rock Salt', cursive;
  font-size: 30px;
  color: white;
}

.grayscale {
  filter: url("data:image/svg+xml;utf8,<svg xmlns=\'http://www.w3.org/2000/svg\'><filter id=\'grayscale\'><feColorMatrix type=\'matrix\' values=\'0.3333 0.3333 0.3333 0 0 0.3333 0.3333 0.3333 0 0 0.3333 0.3333 0.3333 0 0 0 0 0 1 0\'/></filter></svg>#grayscale"); /* Firefox 3.5+ */
  filter: gray; /* IE6-9 */
  -webkit-filter: grayscale(100%); /* Chrome 19+ & Safari 6+ */
}

.grayscale:hover {
  filter: none;
  -webkit-filter: grayscale(0%);
}
</style>
