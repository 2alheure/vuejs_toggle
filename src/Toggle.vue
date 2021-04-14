<style scoped>
.toggler {
  transition: all 0.2s ease-in;
}

.vue-toggle {
  border-radius: 9999px;
  display: inline-block;
  cursor: pointer;
  --tw-shadow: 0 1px 3px 0 rgba(0, 0, 0, 0.1), 0 1px 2px 0 rgba(0, 0, 0, 0.06);
  box-shadow: var(--tw-ring-offset-shadow, 0 0 #0000),
    var(--tw-ring-shadow, 0 0 #0000), var(--tw-shadow);
}

.vue-toggle input {
  display: none;
}

.vue-toggle .toggler {
  width: 50%;
  height: 100%;
  background-color: #fff;
  border-radius: 100%;
  --tw-shadow: 0 1px 3px 0 rgba(0, 0, 0, 0.1), 0 1px 2px 0 rgba(0, 0, 0, 0.06);
  box-shadow: var(--tw-ring-offset-shadow, 0 0 #0000),
    var(--tw-ring-shadow, 0 0 #0000), var(--tw-shadow);
}
</style>

<template>
  <div
    :style="{ backgroundColor: value ? colorOK : colorKO, width: width, height: height }"
    class="vue-toggle"
    @click="$emit('change', !value)"
  >
    <input type="checkbox" name="foo" id="bar" value="baz" :checked="value" />
    <div
      :style="{ transform: `translateX(${value ? 100 : 0}%)` }"
      class="toggler"
    />
  </div>
</template>

<script>
export default {
  model: {
    event: "change",
  },
  props: {
    value: {
      type: Boolean,
      default: false,
    },
    colorOK: {
      type: String,
      default: '#0d9488',
    },
    colorKO: {
      type: String,
      default: '#6b7280',
    },
    width: {
      type: String,
      default: '3rem',
    },
    height: {
      type: String,
      default: '1.5rem',
    },
  },
};
</script>
