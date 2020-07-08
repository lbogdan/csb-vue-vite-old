<template>
  <div>
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Hello Vue 3.0 + Vite + CodeSandbox"/>
    <!-- <Message message="hello world"/> -->
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
// import Message from "./components/Message.vue";

export default {
  name: "App",
  components: {
    HelloWorld
    // Message
  }
};
</script>
