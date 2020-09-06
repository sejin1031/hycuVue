<template>
  <div>자식 컴포넌트 예시<span>{{ this.data }}</span></div>
</template>

<script>
export default {
  name: 'Child',
  props: [ 'data' ]
}
</script>
