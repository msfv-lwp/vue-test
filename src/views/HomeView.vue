<template>
  <div class="home">
    <HelloWorld :name="'seyed '+person.name" />
    <HelloWorld2 />
  </div>
  <h3>{{ person.name }} {{ person.last_name }}</h3>
  <button v-on:mouseover="test()">click here</button>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";
import HelloWorld2 from "@/components/HelloWorld2.vue";
//click ,mouseover ,mouseout ,keyup ,keydown
export default {
  name: "HomeView",
  components: {
    HelloWorld,
    HelloWorld2,
  },
  data() {
    return {
      person: {
        name: "ali",
        last_name: "alavi",
      },
    };
  },
  beforeCreate() {},
  created() {},
  beforeMount() {},
  mounted() {},
  methods: {
    test() {
      console.log("test method run" + this.person.name);
    },
  },
};
</script>
