<template>
  <h1>Color Picker Game</h1>

  <div>{{ message }}</div>

  <button v-for="color in colors" :key="color" @click="matchColor(color)">
    {{ color }}
  </button>
</template>

<script>
import ColorPickerLogic from '../composables/ColorPickerLogic';

export default {
  setup() {
    const { message, colors, matchColor } = ColorPickerLogic();

    return {
      message,
      colors,
      matchColor,
    };
  },
}
</script>

<style></style>
