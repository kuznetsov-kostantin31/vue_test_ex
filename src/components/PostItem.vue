<script>

import MyButton from "@/components/ui/MyButton.vue";

export default {
  components: {MyButton},
  props:{
    post:{
      type: Object,
      required: true
    }
  }
}
</script>

<template>
  <div class="post">
    <div>
      <div> <strong>Название: </strong> {{post.title}} </div>
      <div> <strong>Описание: </strong> {{post.body}} </div>
    </div>
    <div class="post__btns">
      <my-button
          @click="$emit('remove', post)"
      >
        Удалить
      </my-button>
    </div>
  </div>
</template>

<style scoped>
.post{
  padding: 15px;
  border: 1px solid darkred;
  border-radius: 16px;
  margin-top: 20px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}
</style>