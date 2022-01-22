<template>
  <div class="box" @click="$emit('close')">
    <p>click</p>
  </div>
</template>

<script>
export default {
  emits: ['close'],
};
</script>

<style></style>
