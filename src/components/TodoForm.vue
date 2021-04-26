<template>
  <div>
    <b-container>
      <b-input-group>
        <b-form-input type="text" v-model="value" />
        <b-input-group-append>
          <b-button @click="todoValue()">送信</b-button>
        </b-input-group-append>
      </b-input-group>
    </b-container>
  </div>
</template>

<script>
  export default {
    name: 'TodoForm',
    data() {
      return {
        value: ''
      }
    },
    methods: {
      todoValue() {
        console.log(this.value);
      }
    }
  }
</script>

<style lang="scss" scoped>

</style>