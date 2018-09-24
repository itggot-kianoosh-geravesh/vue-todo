<template lang="pug">
  //- .home
  //-   img(alt="Vue logo" src="../assets/logo.png")
  //-   HelloWorld(msg="Welcome to Your Vue.js + TypeScript App")
  .home
    TodoApp
</template>

<script lang="ts">
import Vue from 'vue';
// import HelloWorld from '@/components/HelloWorld.vue'; // @ is an alias to /src
import TodoApp from '@/components/TodoApp.vue';

export default Vue.extend({
  name: 'home',
  components: {
    // HelloWorld,
    TodoApp
  },
});
</script>
