<script setup lang="ts">
import { ref, watch } from 'vue'

const a = ref(1)
const b = computed(() => a.value + 1)
</script>

<template>
  <div v-if="toValue(a)" @click="(e)=>console.log(e, shallowRef(2))">
    {{ a }} + {{ b }} = {{ a + b }}
    {{ reactive(useRoute()).path }}
  </div>
</template>
