<template>
  <view>
    <text class="text-color-primary">{{ title }}</text>
    <text>{{ testingData }}</text>
    <button title="Go to screen1" :on-press="()=>navigate('screen1')" />
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
    testingData: {
      type: String,
      required: false
    },
    navigate: {
      type: Function,
      required: true
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
