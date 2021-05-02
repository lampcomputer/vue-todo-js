<template>
  <div>
    <b-container>
      <b-input-group>
        <b-form-input type="text" v-model="value" />
        <b-input-group-append>
          <b-button @click="handleAddTodo()" variant="dark">送信</b-button>
        </b-input-group-append>
      </b-input-group>
    </b-container>
  </div>
</template>

<script>
  export default {
    name: 'TodoForm',
    handleAddTodo() {
      return {
        value: ''
      }
    },
    methods: {
      handleAddTodo() {
        this.$emit('handleParentsAddTodo', this.value)
      }
    }
  }
</script>

<style lang="scss" scoped>

</style>