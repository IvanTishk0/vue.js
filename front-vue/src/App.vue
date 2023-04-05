<script setup>
  import Header from "./components/Header/Header.vue";
  import Modal from "./components/Modal/Modal.vue";
  import {provide, ref, Transition, Teleport} from "vue";
  const isShow = ref(false);
</script>

<template>
  <Header @click="isShow = true">Open simple snackbar</Header>
  <Modal :show="isShow" @close="isShow = false">Note archived</Modal>
</template>

<style>

</style>


