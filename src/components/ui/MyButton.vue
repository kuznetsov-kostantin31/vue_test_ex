<script>
export default {
  name: 'my-button'
}
</script>

<template>
  <button class="btn">
    <slot></slot>
  </button>
</template>

<style>
.btn{
  padding: 10px 15px;
  background: none;
  color: darkred;
  border: 2px solid darkred;
  border-radius: 16px;
}
</style>