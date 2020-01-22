<template>
  <view class="container">
    <!-- <view class="container">
    <text class="text-color-primary">{{ title }}</text>
    <Hello />
    </view>-->
    <HomeScreen
      v-if="activeScreen === 'homeScreen'"
      :testingData="testingData"
      :navigate="navigate"
    />
    <Screen1 v-if="activeScreen === 'screen1'" :navigate="navigate" />
  </view>
</template>

<script>
// import Hello from "./src/components/Hello";
import HomeScreen from "@/screens/HomeScreen";
import Screen1 from "@/screens/Screen1";
export default {
  components: {
    // Hello
    HomeScreen,
    Screen1
  },
  // data() {
  //   return {
  //     title: "MY NEW APP ::MYAPP"
  //   };
  // }
  data() {
    return {
      activeScreen: "homeScreen",
      testingData: "value from App Component"
    };
  },
  methods: {
    navigate(screen) {
      this.activeScreen = screen;
    }
  }
};
</script>

<style>
.container {
  background-color: white;
  align-items: center;
  justify-content: center;
  flex: 1;
}
.text-color-primary {
  color: blue;
}
</style>
