<template>
  <div id="app">
    Parent counter : {{ count }} <br>
    <button @click="addCounter">+</button>
    <button @click="subCounter">-</button>

    <!-- Child 컴포넌트를 등록하고 counter 데이터 속성을 props 로 전달한다. -->
    <child v-bind:passedCounter="counter"></child>
  </div>
</template>

<script>
  // App.vue
  import Child from './Child.vue'

  export default {
    data () {
      return {
        // data 속성 등록
        counter: 0
      }
    },
    methods: {
      // 이벤트 추가
      addCounter() {
        this.counter++;
      },
      subCounter() {
        this.counter--;
      }
    },
    components: {
      // Child 컴포넌트를 하위 컴포넌트로 등록
      'child': Child
    }
  }
</script>
