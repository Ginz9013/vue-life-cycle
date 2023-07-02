<script>
export default {
  data() {
    return {
      storage: null,
    };
  },
  beforeCreate() {
    console.log("%c內層2: beforeCreate", "color: pink");
  },
  created() {
    console.log("%c內層2: created", "color: pink");
  },
  beforeMount() {
    console.log("%c內層2: beforeMount", "color: pink");
  },
  mounted() {
    console.log("%c內層2: mounted", "color: pink");
    this.storage = localStorage.getItem("key");
  },
  beforeUpdate() {
    console.log("%c內層2: beforeUpdate", "color: pink");
  },
  updated() {
    console.log("%c內層2: updated", "color: pink");
  },
};
</script>
<template>
  <h2>內層2</h2>
  <p>Storage: {{ storage }}</p>
</template>
