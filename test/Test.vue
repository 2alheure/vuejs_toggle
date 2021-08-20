<template>
  <Toggle v-model="isToggled" />
</template>

<script>
  import Toggle from "../src/Toggle.vue";

  export default {
    components: {
      Toggle
    },
    data() {
      return {
        isToggled: false
      }
    }
  };
</script>