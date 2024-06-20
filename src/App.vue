<template>
  {{ message }}
  <p v-show="isShow">Show World</p>
  <p v-if="x === 0">x = 0</p>
  <p v-else-if="x === 1">x = 1</p>
  <p v-else-if="x === 2">x = 2</p>
  <p v-else>x != 0</p>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      message: "Hellow World",
      isShow: false,
      x: 2,
    };
  },
};
</script>
