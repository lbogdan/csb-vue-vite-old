<template>
  <div>
    <h1>{{ msg }}</h1>
    <h1>{{ reversedMessage }}</h1>
    <button @click="count++">count is: {{ count }}</button>
    <button @click="count--">count is: {{ count }}</button>
  </div>
</template>

<script>
import { computed, defineComponent, reactive } from "vue";

export default defineComponent({
  props: {
    msg: {
      type: String,
      default: "hello"
    }
  },
  setup(props) {
    const reversedMessage = computed(() => {
      return props.msg
        .split("")
        .reverse()
        .join("");
    });

    const state = reactive({
      count: 0
    });

    return {
      ...props,
      count: state.count,
      reversedMessage
    };
  }
});
</script>
