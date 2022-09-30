<template>
  <div>
    <GreetS />
    <CardC></CardC>
    <InputS v-model="name" />
    <CardC>Card Content</CardC>
    <CardC><h2>Card Content</h2></CardC>
    <CardC><img src="https://picsum.photos/200" /></CardC>
    <CardC>
      <template v-slot:header>
        <h3>Header</h3>
      </template>
      <template v-slot:default>
        <h3>Default Content</h3>
        <img src="https://picsum.photos/200" />
      </template>
      <template v-slot:footer>
        <h3>footer</h3>
        <button>View Details</button>
      </template>
    </CardC>
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  </div>
</template>

<script>
import CardC from "./components/CardC.vue";
import InputS from "./components/InputS.vue";
// import HelloWorld from './components/HelloWorld.vue'
import GreetS from "./components/GreetS.vue";
export default {
  name: "App",
  components: {
    GreetS,
    InputS,
    CardC,
  },
  data() {
    return {
      name: "",
    };
  },
  methods: {},
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
