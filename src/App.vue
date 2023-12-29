<template>
<img class="logo-img" alt="Vue logo" src="./assets/ehsan8.jpeg">
<HelloWorld msg="Welcome to Ehsan App" />
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  },
  data() {
    let a = 2;
    let b = 5;
    console.log("a + b = ", a + b);
    return {};
  },
  beforeCreate() {
    console.log("beforecreate parent");
  },
  Created() {
    console.log("created parent");
  },
  beforeMount() {
    console.log("beforeMount parent");
  },
  mounted() {
    console.log("mounted parent");
  },
  beforeUpdate() {
    console.log("Before update parent");
  },
  updated() {
    console.log("updated parent");
  },
  beforeUnmount() {
    console.log("before unmount parent");
  },
  unmounted() {
    console.log("unmounted parent");
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.logo-img {
  width: 200px;
  height: 200px;
  border-radius: 50%;
}
</style>
