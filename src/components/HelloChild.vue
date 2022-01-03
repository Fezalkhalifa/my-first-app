<template>
  <div class="child">
    <h2>{{ msg2 }}</h2>
    <button
      :class="[secondChildShow ? warningClass : succesClass]"
      @click="secondChildShow = !secondChildShow"
    >
      {{ secondChildShow ? "Hide Second Child" : "Show Second Child" }}
    </button>
    <hello-second-child
      v-if="secondChildShow"
      msgChild="Hello this is child from child"
    />
  </div>
</template>
<script>
import HelloSecondChild from "./HelloSecondChild.vue";
export default {
  components: { HelloSecondChild },
  name: "HelloChild",
  props: {
    msg2: String,
  },
  data() {
    return {
      secondChildShow: true,
      warningClass: "btn btn-primary",
      succesClass: "btn btn-default",
    };
  },
  beforeCreate() {
    console.log("Child before Craete");
  },
  created() {
    console.log("child is craeted");
  },
  beforeMount() {
    console.log("child before Mount");
  },
  mounted() {
    console.log("child Mounted");
  },
  beforeUpdate() {
    console.log("child before Update");
  },
  Updated() {
    console.log("child  Updated");
  },
  beforeUnmount() {
    console.log("child  before Unmount");
  },
  unmounted() {
    console.log("child unmounted");
  },
};
</script>