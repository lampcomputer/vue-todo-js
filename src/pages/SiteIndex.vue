<template>
  <div>
    <div>
      <h1 class="mt-4 text-center">TODO LIST</h1>
      <todo-form @handleParentsAddTodo='handleParentsAddTodo'/>
      <todo-list :todos="todos" @handleParentsDelTodo='handleParentsDelTodo' @handleParentsCompliteTodo='handleParentsCompliteTodo' />
    </div>
  </div>
</template>

<script>
  import TodoForm from '@/components/TodoForm';
  import TodoList from '@/components/TodoList';

  export default {
    name: 'SiteIndex',
    components: {
      TodoForm,
      TodoList
    },
    data() {
      return {
        todos: []
      }
    },
    methods: {
      handleParentsAddTodo(value) {
        this.todos.unshift({ text: value, complite: false, doneTitle: '未完了', doneColor: 'light' })
      },
      handleParentsDelTodo(index) {
        this.todos.splice(index, 1)
      },
      handleParentsCompliteTodo(index) {
        this.todos[index].complite = !this.todos[index].complite
        if(this.todos[index].complite) {
          this.todos[index].doneTitle = '完了'
          this.todos[index].doneColor = 'success'
        } else {
          this.todos[index].doneTitle = '未完了'
          this.todos[index].doneColor = 'light'
        }
      }
    }
  }
</script>

<style lang="scss" scoped>

</style>