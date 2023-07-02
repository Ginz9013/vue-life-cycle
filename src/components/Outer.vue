<script>
import Inner1 from "./Inner1.vue";
import Inner2 from "./Inner2.vue";
export default {
  components: {
    Inner1,
    Inner2,
  },
  data() {
    return {
      isSwitch: true,
      inputText: "",
    };
  },
  methods: {
    switchView() {
      console.log("--------SWITCH--------");
      localStorage.setItem("key", this.inputText);
      console.log("Set Storage");
      this.isSwitch = !this.isSwitch;
    },
  },
  beforeCreate() {
    console.log("%c外層: beforeCreate", "color: yellow");
  },
  created() {
    console.log("%c外層: created", "color: yellow");
  },
  beforeMount() {
    console.log("%c外層: beforeMount", "color: yellow");
  },
  mounted() {
    console.log("%c外層: mounted", "color: yellow");
  },
  beforeUpdate() {
    console.log("%c外層: beforeUpdate", "color: yellow");
  },
  updated() {
    console.log("%c外層: updated", "color: yellow");
  },
};
</script>
<template>
  <h2>外層</h2>
  <button type="button" @click="switchView">Switch</button>
  <input type="text" v-model="inputText" />
  <Inner1 v-if="isSwitch" />
  <Inner2 v-else />
</template>
