<template>
  <nb-container>
    <nb-header>
      <nb-left>
        <nb-button :on-press="toggleDrawer" transparent>
          <nb-icon name="menu" />
        </nb-button>
      </nb-left>
      <nb-body></nb-body>
      <nb-right></nb-right>
    </nb-header>
    <view>
      <!-- <text class="text-color-primary">{{ title }}</text> -->
      <!-- <button title="Go to Home" :on-press="()=>navigate('homeScreen')" /> -->
    </view>
  </nb-container>
</template>

<script>
import { DrawerActions } from "react-navigation-drawer";
export default {
  props: {
    navigation: {
      type: Object
    }
  },
  data() {
    return {
      title: "I am Screen2"
    };
  },
  methods: {
    toggleDrawer() {
      this.navigation.dispatch(DrawerActions.toggleDrawer());
    }
  }
};
</script>
