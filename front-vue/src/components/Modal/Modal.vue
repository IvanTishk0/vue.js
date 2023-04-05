<script setup>
import {Teleport, Transition} from "vue";
import css from "./Modal.module.css"
defineEmits(["close"]);
defineProps(["show"])
</script>

<template>
  <Teleport to="#modal">
    <Transition>
        <div :class="css.modal" v-if="show">
          <div :class="css.modal__text1"><slot></slot></div>
          <div :class="css.modal__text2">UNDO</div>
          <div :class="css.modal__header">
            <button @click="$emit('close')">&times;</button>
          </div>
        </div>
    </Transition>
  </Teleport>
</template>

<style scoped>

  .v-enter-active,
  .v-leave-active {
    transition: all 200ms ease;
  }

  .v-enter-from,
  .v-leave-to {
    opacity: 0;
    transform: translateY(10px);
  }

</style>