<template>
  <div class="hello">
    <!-- 데이터 바인딩 -->
    <div> {{ msg }} </div>
    <!-- 양방향 데이터 바인딩 -->
    <input v-model="input">
    <div> input : {{ input }} </div>
    <!-- v-for 예제 -->
    <div> <span :key="num" v-for="num in list">{{ num }}</span> </div>
    <!-- event 바인딩  -->
    <div @click="clickEvent">이벤트버튼</div>
    <!-- 속성 바인딩 -->
    <a :href="href">링크</a>

    <!-- 자식 컴포넌트 예제 -->
    <child :data="childData"></child>

    <!-- 자식 컴포넌트와 v-for의 결합 -->
    <child :key="index" v-for="(fordata,index) in forData" :data="fordata"></child>

    
  </div>
</template>

<script>
import Child from '@/components/Child'
export default {
  name: 'HelloWorld',
  components: {
    child: Child
  },
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      input: '',
      list : [1,2,3,4,5],
      href : 'http://www.naver.com',
      childData : '자식에게 넘겨줄 데이터',
      forData: ['a','b','c','d','e']
    }
  },
  methods: {
    clickEvent: function () {
      this.msg = 'Hi hycube';
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
