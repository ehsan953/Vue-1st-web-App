<template>
  <div class="hello">
    <h1>{{ msg }}</h1>

    <div class="form">
      <div>
        <label for="username">Admin: </label>
        <input id="username" type="text" v-model="inputText" />
        <p class="you-typed">
          Your Name is: "<span style="color: red">{{ inputText }}</span
          >"
        </p>
      </div>
      <div>
        <label for="email">Email: </label>
        <input id="email" type="email" v-model="email" />
        <p class="you-typed">
          Your Email is: "<span style="color: red">{{ email }}</span
          >"
        </p>
      </div>
    </div>
  </div>
</template>

<script>
// import {
//   // ref,
//   onBeforeMount,
//   onMounted,
//   onBeforeUpdate,
//   onUpdated,
//   onBeforeUnmount,
//   onUnmounted,
// } from "vue";

import { ref } from "vue";
const fun2 = () => {
  // syncronous Method
  console.log("Fun2 is starting");

  // This is Asyncronous Method (put console.log in a anonymous function)

  // setTimeout(() => {
  //   console.log("Fun2 is starting");
  // }, 3000);
};
const fun1 = () => {
  console.log("Fun1 is starting");
  fun2();
  console.log("Fun1 is ending");
};
fun1();

export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
  data() {
    const inputText = ref("");
    const email = ref("");
    let a = 3;
    let b = 5;
    console.log("a + b = ", a + b);

    return {
      inputText,
      email,
    };
  },

  beforeCreate() {
    console.log("beforecreate child");
  },
  Created() {
    console.log("created child");
  },
  beforeMount() {
    console.log("beforeMount child");
  },
  mounted() {
    console.log("mounted child");
  },
  beforeUpdate() {
    console.log("Before update child");
  },
  updated() {
    console.log("updated child");
  },
  beforeUnmount() {
    console.log("before unmount child");
  },
  unmounted() {
    console.log("unmounted child");
  },

  // setup() {
  //   onBeforeMount(() => {
  //     console.log("onBeforeMount child");
  //   });
  //   onMounted(() => {
  //     console.log("onMounted child");
  //   });
  //   onBeforeUpdate(() => {
  //     console.log("onBeforeUpdate child");
  //   });
  //   onUpdated(() => {
  //     console.log("onUpdated child");
  //   });
  //   onBeforeUnmount(() => {
  //     console.log("onBeforeUnmount child");
  //   });
  //   onUnmounted(() => {
  //     console.log("onUnmounted child");
  //   });
  // },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->

<style scoped>
h3 {
  margin: 40px 0 0;
}

.form {
  width: 50%;
  margin: auto;
  padding: 1rem;
}

label {
  font-weight: bold;
}
</style>
