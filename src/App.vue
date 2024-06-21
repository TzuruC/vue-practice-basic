<template>
  {{ message }}
  <p v-show="isShow">Show World</p>
  <p v-if="x === 0">x = 0</p>
  <p v-else-if="x === 1">x = 1</p>
  <p v-else-if="x === 2">x = 2</p>
  <p v-else>x != 0</p>
  <ol>
    <li v-for="user in user1" :key="user">{{ user }}</li>
  </ol>
  <p v-for="(user, index) in users2" :key="user.email">
    {{ index }} {{ user.name }} {{ user.email }}
  </p>
  <div v-for="(user, index) in user1" :key="user">
    <p v-if="user === 'Jake'">{{ index }} {{ user }}</p>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      message: "Hellow World", // {{}}
      isShow: false, // v-show, v-if
      x: 2, // v-if
      user1: ["Jake", "Allan", "Eason"],
      users2: [
        { name: "Jake", email: "jake@gmail.com" },
        { name: "Allan", email: "allan@gmail.com" },
        { name: "Eason", email: "eason@gmail.com" },
      ],
    };
  },
};
</script>
