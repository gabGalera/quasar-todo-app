<template>
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
</template>

<script>
export default {
  name: 'TodoList',
  data () {
    return {}
  }
}
</script>
