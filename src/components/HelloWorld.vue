<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <button
      :class="[showChild ? warningClass : succesClass]"
      @click="showChild = !showChild"
    >
      {{ showChild ? "Hide Child" : "Show Child" }}
    </button>
    <hello-child v-if="showChild" msg2="i am the child" />
  </div>
</template>

<script>
import HelloChild from "./HelloChild.vue";
export default {
  name: "HelloWorld",
  components: {
    HelloChild,
  },
  props: {
    msg: String,
  },
  data() {
    return {
      showChild: true,
      warningClass: "btn btn-warning",
      succesClass: "btn btn-success",
    };
  },
  beforeCreate() {
    console.log("Parent before Craete");
  },
  created() {
    console.log("parent is craeted");
  },
  beforeMount() {
    console.log("parent before Mount");
  },
  mounted() {
    console.log("parent Mounted");
  },
  beforeUpdate() {
    console.log("parent before Update");
  },
  Updated() {
    console.log("parent  Updated");
  },
  beforeUnmount() {
    console.log("parent  before Unmount");
  },
  unmounted() {
    console.log("parent unmounted");
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
