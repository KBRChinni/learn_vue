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
    <NameList>
      <template v-slot:default="slotProps">
        {{ slotProps.firstName }} {{ slotProps.lastName }}
      </template>
    </NameList>
    <NameList>
      <template v-slot:default="slotProps">
        {{ slotProps.lastName }} , {{ slotProps.firstName }}
      </template>
    </NameList>
    <NameList>
      <template v-slot:default="slotProps">
        {{ slotProps.firstName }}
      </template>
    </NameList>
    <h4>App Component Text</h4>
    <!-- <ChildStyles /> -->
    <ChildStyles>
      <h4>Child Styles Components Text</h4>
    </ChildStyles>
    <button @click="activeTab = 'TabA'">Tab A</button>
    <button @click="activeTab = 'TabB'">Tab B</button>
    <button @click="activeTab = 'TabC'">Tab C</button>
    <TabA v-if="activeTab === 'TabA'" />
    <TabB v-if="activeTab === 'TabB'" />
    <TabC v-if="activeTab === 'TabC'" />
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  </div>
</template>

<script>
import TabA from "./components/TabA.vue";
import TabB from "./components/TabB.vue";
import TabC from "./components/TabC.vue";
import ChildStyles from "./components/ChildStyles.vue";
import NameList from "./components/NameList.vue";
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
    NameList,
    ChildStyles,
    TabA,
    TabB,
    TabC,
  },
  data() {
    return {
      activeTab: "TabA",
    };
  },
  methods: {},
};
</script>

<style scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
h4 {
  color: orange;
}
</style>
