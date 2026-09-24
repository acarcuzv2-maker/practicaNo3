<script setup lang="ts">
import { ref } from 'vue'

const contador = ref<number>(0)

function sumar(): void {
  contador.value++
}

function restar(): void {
  contador.value--
}
</script>

<template>
  <div class="contador">
    <div class="botones">
      <button @click="restar">−</button>

      <span>{{ contador }}</span>

      <button @click="sumar">+</button>
    </div>
  </div>
</template>

<style scoped lang="scss">
.contador {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.botones {
  display: flex;
  gap: 20px;

  button {
    width: 50px;
    height: 50px;
    background-color: red;
    color: white;
    font-size: 40px;
    border: none;
    border-radius: 10px;
    cursor: pointer;
  }
}
</style>