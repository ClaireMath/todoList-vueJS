<template>
  <div class="hello">
   
    <h3>To do List :</h3>
    <input type="text" placeholder="Write your tasks here">
   
  </div>
</template>

<script>
// import MyInp from './components/myInp.vue'

export default {
  name: 'todoList',
  components: {
    // myInp,
  },
  props: {
    
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}

</style>
