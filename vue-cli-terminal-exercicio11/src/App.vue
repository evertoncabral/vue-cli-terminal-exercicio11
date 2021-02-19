<template>
  <div id="app">
    <button @click="count1++">{{ count1 }}Click aqui 1</button>
    <button @click="increment">{{ count2 }}Click aqui 2</button>
    <button @click="increment2(2, $event)">{{ count3 }}Click aqui 3</button>

    <input type="text" @keyup.enter.space="increment" /> {{ count2 }}
    <ListItem @incremente="incremente"/>
  </div>
</template>

<script>
import ListenItem from "./ListenItem.vue";

export default {
  name: "App",
  components: {
    ListenItem,
  },
  data() {
    return {
      count1: 0,
      count2: 0,
      count3: 0,
      text: "",
    };
  },
  methods: {
    increment() {
      this.count2++;
    },
    increment2(value) {
      this.count3 += value;
    },
    incremente(){
      this.count2++;
    }
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
