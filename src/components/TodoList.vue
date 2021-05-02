<template>
  <div>
    <b-container>
      <div v-for="(todo, index) in todos" :key="index" class="my-2">
        <b-row class="align-items-center">
          <b-col cols="8" class="text-left">
            <h3 class="lead mb-0">{{ todo.text }}</h3>
          </b-col>
          <b-col cols="4" class="text-right">
            <b-button @click="handleCompliteTodo(index)" class="mr-2" :variant="todo.doneColor">{{ todo.doneTitle }}</b-button>
            <b-button @click="handleDelTodo(index)" variant="danger">削除</b-button>
          </b-col>
        </b-row>
      </div>
    </b-container>
  </div>
</template>

<script>
  export default {
    name: 'TodoList',
    props: ['todos'],
    methods: {
      handleDelTodo(index) {
        this.$emit('handleParentsDelTodo', index)    
      },
      handleCompliteTodo(index) {
        this.$emit('handleParentsCompliteTodo', index)
      }
    }
  }
</script>

<style lang="scss" scoped>

</style>