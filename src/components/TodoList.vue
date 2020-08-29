<template>
  <div id="todo-list">
    <div class="new-content">
      제목 : <input v-model="titleText"> <br/>
      내용 : <input v-model="contentText" @keypress.enter="addList"> <br/>
      <button @click="addList">
        추가</button>
    </div>
    <div class="todo-wrap">
      <todo :key="index" v-for="(data,index) in listData" :todo="data"><button @click="removeList(index)">삭제</button></todo>
    </div>
  </div>
</template>

<script>
import Todo from '@/components/Todo'
export default {
  name: 'TodoList',
  components: {
    todo: Todo
  },
  data () {
    return {
      titleText: '',
      contentText: '',
      listData: [],
    }
  },
  methods: {
    addList : function () {
      var todo = {
        title: this.titleText,
        content: this.contentText
      };
      this.listData.push(todo);
      this.titleText = '';
      this.contentText = '';
    },
    removeList : function (index) {
      this.listData.splice(index,1)
    }
  }
}
</script>

<style scoped>
#todolist {
  font-weight: bold;
}
.todo-wrap {
  border: black 3px solid; width: 30vw; left: auto; right: auto;
}
</style>
