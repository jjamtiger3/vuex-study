<template>
  <div id="app">
  <hr>
   Child counter : {{ passedCounter }}
   <br>
   <button>+</button>
   <button>-</button>
  </div>
</template>

<script>
  // Child.vue
  export default {
    // Parent 에서 넘겨준 counter 속성을 passedCounter 로 받음
    props: ['passedCounter']
  }
</script>
