<script setup>
import { ref } from 'vue'
let name = ref('Command Center')
function UpdateWidth() {
  document.querySelector('.title-bar-input').style.width =
    `${document.querySelector('.title-bar-text').clientWidth + 30}px`
}
</script>

<template>
  <div class="title-bar flex items-center gap-2 justify-between">
    <div class="title-bar-left flex items-center gap-2 justify-start">
      <label>
        <span class="title-bar-text">{{ name }}</span>
        <input
          class="title-bar-input input input-ghost"
          @input="UpdateWidth()"
          @mouseenter="UpdateWidth()"
          v-model="name"
        />
      </label>
    </div>
    <div class="title-bar-right flex items-center gap-2 justify-end">
      <button class="btn">Save</button>
      <button class="btn">Settings</button>
    </div>
  </div>
</template>

<style scoped>
label {
  display: inline-block;
  position: relative;
  min-width: 2em;
  min-height: 1.4em;
}

.title-bar-text {
  white-space: pre;
  position: absolute;
  opacity: 0;

  /* max-width : could be wised to set a maximum width and overflow:hidden; */
}

.title-bar-input {
  font-family: inherit;
  font-size: inherit;

  width: 100%;
}
</style>
