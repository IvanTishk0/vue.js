<script setup>
  import {ref} from "vue";
  const props = defineProps(["foo", "bar"]);
  const time = ref(Date.now());
</script>

<template>
  <button><slot name="header"></slot></button>
  <slot name="footer"></slot>
</template>
