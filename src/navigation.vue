<template>
  <!-- <view class="container">
    <text class="text-color-primary">{{ title }}</text>
    <Hello />
  </view>-->
  <!-- <HomeScreen
      v-if="activeScreen === 'homeScreen'"
      :testingData="testingData"
      :navigate="navigate"
    />
  <Screen1 v-if="activeScreen === 'screen1'" :navigate="navigate" />-->
  <!-- <HomeScreen /> -->
  <root>
    <AppNavigation />
  </root>
</template>

<script>
// import Hello from "./src/components/Hello";
import HomeScreen from "@/screens/HomeScreen";
import Screen1 from "@/screens/Screen1";
import Screen2 from "@/screens/Screen2";
import Screen3 from "@/screens/Screen3";
import { Root } from "native-base";
import { createAppContainer } from "react-navigation";
import { createStackNavigator } from "react-navigation-stack";
import { createBottomTabNavigator } from "react-navigation-tabs";
import { createDrawerNavigator } from "react-navigation-drawer";

const HomeStack = createStackNavigator(
  {
    Home: HomeScreen,
    Screen1: Screen1
    // Screen2: Screen2
  },
  {
    initialRouteName: "Home"
  }
);
const SomeOtherStack = createStackNavigator({
  Screen2
});
const SomeOtherOtherStack = createStackNavigator({
  Screen3
});
const DrawerNavigation = createDrawerNavigator({
  DrawerStack1: SomeOtherStack,
  DrawerStack2: SomeOtherOtherStack
  // Screen2,
  // Screen3
});
const TabNavigation = createBottomTabNavigator({
  Meetups: HomeStack,
  Other: DrawerNavigation
});
const AppNavigation = createAppContainer(TabNavigation);
// import Screen1 from "@/screens/Screen1";
export default {
  components: {
    // Hello
    AppNavigation,
    Root
    // Screen1
  }
  // data() {
  //   return {
  //     title: "MY NEW APP ::MYAPP"
  //   };
  // }
  // data() {
  //   return {
  //     activeScreen: "homeScreen",
  //     testingData: "value from App Component"
  //   };
  // },
  // methods: {
  //   navigate(screen) {
  //     this.activeScreen = screen;
  //   }
  // }
};
</script>
