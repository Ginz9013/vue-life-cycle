<script>
export default {
  beforeCreate() {
    console.log("內層1: beforeCreate");
  },
  created() {
    console.log("內層1: created");
  },
  beforeMount() {
    console.log("內層1: beforeMount");
  },
  mounted() {
    console.log("內層1: mounted");
  },
  beforeUpdate() {
    console.log("內層1: beforeUpdate");
  },
  updated() {
    console.log("內層1: updated");
  },
};
</script>
<template>
  <h2>內層1</h2>
</template>
