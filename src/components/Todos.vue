
<template>
  <div>
      <div v-for="todo in todos"  v-bind:key="todo">
          <TodoItem v-bind:todo="todo" v-on:del-todo="$emit('del-todo', todo.id)"/>
      </div>
  </div>
</template>

<script>

import TodoItem from './Todoitem.vue';

export default {
    components:{
        TodoItem
    },
    name: "Todos",
    props: ["todos"]
};
</script>

<style scoped>
</style>
