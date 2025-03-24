<script setup>
import { ref } from 'vue'
let name = ref('Command Center')
</script>

<template>
  <div class="title-bar flex items-center gap-2 justify-between">
    <div class="title-bar-left flex items-center gap-2 justify-start">
      <!--Set the width of test equal to tpl -->
      <label
        ><span id="tpl">{{ name }}</span
        ><input id="test" v-model="name"
      /></label>
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

#tpl {
  white-space: pre;
  /* max-width : could be wised to set a maximum width and overflow:hidden; */
}

#test {
  font-family: inherit;
  font-size: inherit;
  position: absolute;
  vertical-align: top;
  top: 0;
  left: 0;
  width: 100%;
  background: rgb(0, 0, 0);
}
</style>
