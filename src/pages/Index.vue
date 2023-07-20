<template>
  <q-page class="row">
    <q-card class="col-xs-9">
      <q-toolbar>
        <q-input
          dense
          placeholder="Search"
          borderless
          class="full-width"
          :value="search"
        >
          <template #append>
            <q-icon name="mdi-magnify"></q-icon>
          </template>
        </q-input>
      </q-toolbar>
      <TodoList />
    </q-card>

    <div class="col-xs-3">
      <q-toolbar class="bg-primary">
        <CreateTodoButton />
      </q-toolbar>
    </div>
  </q-page>
</template>

<script>
import { defineComponent } from 'vue'
import CreateTodoButton from '../components/CreateTodoButton.vue'
import TodoList from '../components/TodoList.vue'

export default defineComponent({
  name: 'PageIndex',
  components: {
    CreateTodoButton,
    TodoList
  },
  data () {
    return {
      search: ''
    }
  }
})
</script>
