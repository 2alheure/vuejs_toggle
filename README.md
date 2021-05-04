# Vue.js Toggle button
A simple Vue.js toggle button.

- [Vue.js Toggle button](#vuejs-toggle-button)
	- [Simple usage](#simple-usage)
	- [Props](#props)

It has been inspired by [this article by ALEXANDRU STRATULAT](https://sandulat.com/blog/custom-switch-with-tailwind-and-vue), so check it out if you wish to understand how it works. 

## Simple usage
First run `npm install @2alheure/vue-toggle`.  
Then its usage is simple :  
```js
<template><Toggle v-model="isToggled" /></template>

<script>
import Toggle from "@2alheure/vue-toggle";

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
```

Please note the `v-model` directive, as it is usable as an input (and is one, intrinsically).

## Props
| Name    |  Type  |   Default value    | Description                                     |
| :------ | :----: | :----------------: | ----------------------------------------------- |
| name    | String | Some random string | The name of the inner input.                    |
| colorOK | String |     `#0d9488`      | The color of the toggle when it is toggled ON.  |
| colorKO | String |     `#6b7280`      | The color of the toggle when it is toggled OFF. |
| width   | String |       `3rem`       | The width of the toggle.                        |
| height  | String |      `1.5rem`      | The height of the toggle.                       |
