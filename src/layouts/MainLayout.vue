<template>
  <q-layout view="hHh Lpr lFf">
    <q-header>
      <q-toolbar>
        <q-btn
          flat
          dense
          round
          icon="mdi-menu"
          aria-label="Menu"
          @click="leftDrawerOpen = !leftDrawerOpen"
        />
        <q-toolbar-title>
          Quasar App
        </q-toolbar-title>

        <q-btn
          flat
          round
          icon="mdi-logout"
        />
      </q-toolbar>
    </q-header>

    <q-drawer v-model="leftDrawerOpen" show-if-above bordered content-class="bg-grey-1">
      <q-toolbar class="bg-primary"></q-toolbar>
      <q-item class="bg-grey-3">
        <q-item-section>
          Lists
        </q-item-section>
        <q-item-section side>
          <CreateTodoListButton />
        </q-item-section>
      </q-item>
      <TodoListsList />
    </q-drawer>
    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import CreateTodoListButton from '../components/CreateTodoListButton.vue'
import TodoListsList from '../components/TodoListsList.vue'

export default {
  name: 'MainLayout',
  components: {
    CreateTodoListButton,
    TodoListsList
  },
  data () {
    return {
      leftDrawerOpen: false
    }
  }
}
</script>
