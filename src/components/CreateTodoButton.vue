<template>
  <q-btn
    fab
    style="margin-bottom: -56px;"
    class="q-ml-md"
    color="secondary"
    icon="mdi-plus"
    @click="handleButtonClicked"
  />
</template>

<script>
export default {
  name: 'CreateTodoButton',
  methods: {
    handleButtonClicked () {
      this.$q.dialog({
        title: 'Create Todo',
        prompt: {
          model: '',
          type: 'text'
        }
      }).onOk(this.createTodo)
    },
    createTodo (data) {
      this.$q.notify({
        message: 'Todo Created!',
        icon: 'mdi-check',
        color: 'positive'
      })
    }
  }
}
</script>
