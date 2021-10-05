<template>
  <div>

    <h3>To do List :</h3>
    <input v-model="task" type="text" placeholder="Write your tasks here" />
    <button v-on:click="addItem">Add</button>

    <TodoListItem v-for="task in listItemTab" :key="task"/>
    <TodoListItemDone />
 
  </div>
</template>

<script>
// import MyInp from './components/myInp.vue'
import TodoListItem from "./TodoListItem.vue";
import TodoListItemDone from "./TodoListItemDone.vue";

export default {
  name: "todoList",
  components: {
    TodoListItem,
    TodoListItemDone,
  },
  props: {},

  data() {
    return {
      task: "",
      listItemTab: [],
      listItemDoneTab: [],
    };
  },
  methods: {
    addItem() {
      this.listItemTab.push(this.task);
      console.log(this.listItemTab);
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
</style>
