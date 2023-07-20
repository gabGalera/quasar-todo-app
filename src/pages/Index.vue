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
      <q-list bordered>
        <q-item>
          <q-item-section side>
            <q-checkbox :value="true" />
          </q-item-section>
          <q-item-section>
            Go Shopping
          </q-item-section>
          <q-item-section side>
            <q-btn
              flat
              round
              size="sm"
              icon="mdi-delete"
            />
          </q-item-section>
        </q-item>
      </q-list>
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

export default defineComponent({
  name: 'PageIndex',
  components: {
    CreateTodoButton
  },
  data () {
    return {
      search: ''
    }
  }
})
</script>
