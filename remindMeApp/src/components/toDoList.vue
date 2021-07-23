<template>
  <div>
    <input
      type="text"
      class="todo-input"
      placeholder="Type your to do task here ..."
      v-model="newTodo" @keyup.enter="addTodo">
    <div v-for="todo in todos" :key="todo.id" class="todo-item">
      {{ todo.title }}
    </div>
  </div>
</template>

<script>
export default {
  name: "toDo-List",
  data() {
    return {
      msg: "The App that reminds you to do your to-do list",

      newTodo: "",
      idForTodo: 3,
      todos: [
        {
          id: 1,
          title: "Finish Vue Project",
          completed: "false",
        },
        {
          id: 2,
          title: "Hook in Laravel or Firebase on the back end for DB purposes",
          completed: "false",
        },
      ],
    };
  },
  methods: {
    addTodo() {
      this.todos.push({
        id:this.idForTodo,
        title: this.newTodo,
        completed: false,
      })

      this.newTodo = "",
      this.idForTodo++
    }
  }
};
</script>

<style lang="scss">
.todo-input {
  width: 100%;
  padding: 10px 18px;
  font-size: 18px;
  margin-bottom: 16px;
  &:focus {
    outline: 0;
  }
}
.todo-item::before {
      content: "\2022";
}
.todo-item {
    text-align: left;
    font-size: 15px;
    font-weight: 700;
    padding: 10px 0;
}
</style>
