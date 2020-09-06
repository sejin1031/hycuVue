<template>
  
</template>

<script>
import '@/components/Todo.vue' // @는 src/와 동일한 의미
export default {
  name: 'TodoList',
  data () { // data 속성은 반드시 함수형 (return이 되도록)
    return {
      todolist: [],
      titleText: '',
      contentText: ''
    }
  },
  methods: {
    addTodo: function () {
      
    },
    removeTodo: function () {
      
    }
  }

}
</script>

<style>

</style>