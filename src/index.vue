<template>
  <view class="container">
    <navigation />
  </view>
</template>

<script>
import navigation from "./navigation";
import Vue from "vue-native-core";
import { VueNativeBase } from "native-base";

Vue.use(VueNativeBase);
export default {
  components: {
    navigation
  }
};
</script>
<style>
.container {
  flex: 1;
}
.text-color-primary {
  color: blue;
}
</style>
// align-items: center; // justify-content: center;
