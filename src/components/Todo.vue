<template>
  <div class="todo-container">
    <div class="title">제목: {{ this.todo.title }}</div>
    <div class="todo-content">내용: {{ this.todo.content }}</div>
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: 'TodoComp',
  props: [ 'todo' ]
}
</script>

<style>
.todo-container{
  margin-bottom: 30px;
  border: 3px black solid;
}
.title { font-size: 30pt; color: blue; }
.todo-content { font-size: 45pt; color: green; }
</style>