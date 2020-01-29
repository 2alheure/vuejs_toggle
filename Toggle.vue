<style>
.toggler {
  transition: all 0.2s ease-in;
}
</style>

<template>
  <div
    :class="value ? 'bg-teal-600' : 'bg-gray-500'"
    class="w-12 h-6 rounded-full shadow inline-block cursor-pointer"
    @click="$emit('change', !value)"
  >
    <input type="checkbox" name="foo" id="bar" value="baz" :checked="value" class="hidden" />
    <div
      :style="{ transform: `translateX(${value ? 100 : 0}%)` }"
      class="w-1/2 h-full bg-white rounded-full shadow toggler"
    />
  </div>
</template>

<script>
export default {
  model: {
    event: "change"
  },
  props: {
    value: {
      type: Boolean,
      default: false
    }
  }
};
</script>
