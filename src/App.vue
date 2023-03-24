<template>
  <div class="name">
    {{ name }}
  </div>
  <button class="btn btn-primary" v-on:click="updateName"> Click </button>
</template>

<script>
import { ref } from 'vue';
export default {
  setup() {
    const name = ref('Sangjin Coder!'); //ref로 감싸서 변경 가능

    // const greeting = (name) => {
    //   return 'Hello!' + name;
    // };

    // const greet = greeting(name);

    const updateName = () => {
      name.value = 'Cossie Coder1'; //ref로 감싼것은 .value를 써서 호출
      console.log(name)
    };

    return {
      name,
      updateName,
    };
  }
}
</script>

<style>
  .name {
    color: red;
  }
</style>
