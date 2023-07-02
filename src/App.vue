<script>
import Outer from "./components/Outer.vue";
export default {
  components: {
    Outer,
  },
  beforeCreate() {
    console.log("%c根元素: beforeCreate", "color: orange");
  },
  created() {
    console.log("%c根元素: created", "color: orange");
  },
  beforeMount() {
    console.log("%c根元素: beforeMount", "color: orange");
  },
  mounted() {
    console.log("%c根元素: mounted", "color: orange");
  },
  beforeUpdate() {
    console.log("%c根元素: beforeUpdate", "color: orange");
  },
  updated() {
    console.log("%c根元素: updated", "color: orange");
  },
};
</script>

<template>
  <h1>Root</h1>
  <Outer />
</template>
