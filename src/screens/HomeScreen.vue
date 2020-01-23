<template>
  <view>
    <text class="text-color-primary">{{ title }}</text>
    <!-- <text>{{ testingData }}</text> -->
    <button title="Go to screen1" :on-press="goToScreen1" />
    <Hello />
  </view>
</template>

<script>
import Hello from "../components/Hello";
export default {
  components: {
    Hello
  },
  props: {
    navigation: {
      type: Object
    }
  },
  // props: {
  //   testingData: {
  //     type: String,
  //     required: false
  //   },
  //   navigate: {
  //     type: Function,
  //     required: true
  //   }
  // },
  methods: {
    goToScreen1() {
      this.navigation.navigate("Screen1");
    }
  },
  data() {
    return {
      title: "Home Screen"
    };
  }
};
</script>
>
