<template>
  <div class="secondchild">
    <h2>{{ msgChild }}</h2>
  </div>
</template>

<script>
export default {
  name: "HelloSecondChild",
  props: {
    msgChild: String,
  },
  beforeCreate() {
    console.log("SecondChild before Craete");
  },
  created() {
    console.log("SecondChild is craeted");
  },
  beforeMount() {
    console.log("SecondChild before Mount");
  },
  mounted() {
    console.log("SecondChild Mounted");
  },
  beforeUpdate() {
    console.log("SecondChild before Update");
  },
  Updated() {
    console.log("SecondChild  Updated");
  },
  beforeUnmount() {
    console.log("SecondChild  before Unmount");
  },
  unmounted() {
    console.log("SecondChild unmounted");
  },
};
</script>
