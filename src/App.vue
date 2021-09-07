<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->

    <!-- *** interpolation *** -->
    <div id="app-1">
      <h1>{{ headerText }}</h1>
    </div>

    <!-- *** directives *** -->
    <div id="app-2">
      <h1>{{ modelText }}</h1>
      <input v-model="modelText" class="form-control" />
    </div>

    <div id="app-3">
      <button @click="counter += 1">Add 1</button>
      <p>The button above has been clicked {{ counter }} times.</p>
    </div>

    <div id="app-4">
      <h1 v-bind:style="styleObject">{{ headerText }}</h1>
    </div>

    <div id="app-4">
      <p v-html="strongHeaderText"></p>
    </div>

    <!-- *** computed *** -->
    <div id="app-5">
      <p>Original message: "{{ headerText }}"</p>
      <p>Computed reversed message: "{{ reversedMessage }}"</p>
    </div>

    <!-- *** Conditioning *** -->
    <div id="app-6">
      <p v-if="isShow">{{ truthyText }}</p>
      <p v-else>{{ falsyText }}</p>
    </div>

    <!-- *** Looping *** -->
    <div id="app-7">
      <li v-for="(todo, index) in todos" v-bind:key="index">
        {{ todo.text }}
      </li>
    </div>

    <!-- *** component rendering  *** -->
    <div id="app-8">
      <HelloWorld msg="Welcome to Your Vue.js App" />
    </div>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "App",
  data() {
    return {
      headerText: "Vue.js Workshop",
      strongHeaderText: "<strong>Vue.js Workshop</strong>",
      modelText: "Please Update",
      truthyText: "Now you see me",
      falsyText: "Now you can't see me",
      isShow: false,
      counter: 0,
      todos: [
        { text: "Learn JavaScript" },
        { text: "Learn Vue" },
        { text: "Learn React" },
      ],
      styleObject: {
        color: "yellow",
        fontSize: "1rem",
      },
    };
  },
  computed: {
    reversedMessage: function () {
      return this.headerText.split("").reverse().join("");
    },
  },
  components: {
    HelloWorld,
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
</style>
