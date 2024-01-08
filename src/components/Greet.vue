<script setup lang="ts">
const { name } = defineProps<{ name: string }>()
const fromRust = useObservable(from(invoke('greet', {
  name,
})))
</script>

<template>
  <div center col h-dvh>
    <h2>
      {{ fromRust }}
    </h2>
  </div>
</template>

<style scoped>

</style>
