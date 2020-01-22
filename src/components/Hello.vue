<template>
  <view>
    <text class="text-color-primary">{{ maassag }}</text>
    <button :title="btnMessage" :on-press="handleClick" />
    <text class="text-color-primary">{{ clickCount }}</text>
    <text class="text-color-primary">{{ clickMotivation }}</text>
  </view>
</template>

<script>
export default {
  data() {
    return {
      maassag: "MY NEW APP ::MYAPP in Vue",
      btnMessage: "Click ME",
      clickCount: 0
    };
  },
  computed: {
    clickMotivation() {
      if (this.clickCount < 5) {
        return "Please keep clicking";
      } else {
        return "Good, keep Clicking";
      }
    }
  },
  methods: {
    handleClick() {
      this.clickCount++;
      // alert(`I am clicked!Click Count:${this.clickCount}`);
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
