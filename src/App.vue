<template>
  <div id="app">
    
    <h1>To-Do List</h1>
    <ul>
      <li v-for="item in ToDoItems" :key="item.id">
       <to-do-item :label="item.label" :done="item.done" :id="item.id"></to-do-item>
      </li>
    </ul>
  </div>
</template>

<script>
import ToDoItem from './components/ToDoItem.vue';

export default {
  name: 'App',
  components:{
    ToDoItem
  },
  data(){
    return {
      ToDoItems: [
        { label: 'Create a Vue project with the CLI', done: true },
        { label: 'Have fun', done: true },
        { label: 'Create a to-do list', done: false },
        { label: 'Learn Vue', done: false }
      ]
    };
  }

};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
