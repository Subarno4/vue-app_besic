<template>
  <view>
    <text class="text-color-primary">{{ title }}</text>
    <!-- <text>{{ testingData }}</text> -->
    <!-- <button title="Go to screen1" :on-press="goToScreen1" /> -->
    <!-- <nb-button light title="Go to screen1" :on-press="goToScreen1"> -->
    <Hello />
    <nb-button info light title="Go to screen1" :on-press="goToScreen1">
      <nb-text>Go to screen1</nb-text>
    </nb-button>
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
