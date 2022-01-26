<template>
  <div class="box" @click="$emit('close')">
    <p>click</p>
  </div>
</template>

<script>
export default {};
</script>

<style>
.box {
  width: 400px;
  padding: 100px 0;
  background-color: #15daa8;
  border-radius: 10px;
}
</style>
