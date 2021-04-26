<template>
  <div>
    <div>

    <h1 class="mt-4 text-center">TODO LIST</h1>
    <todo-form />
    </div>
  </div>
</template>

<script>
  import TodoForm from '@/components/TodoForm';

  export default {
    name: 'SiteIndex',
    components: {
      TodoForm
    }
  }
</script>

<style lang="scss" scoped>

</style>