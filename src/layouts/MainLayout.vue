<template>
  <q-layout view="hHh Lpr lFf">
    <q-header >
      <q-toolbar>
        <q-btn flat dense round icon="mdi-menu" aria-label="Menu" @click="leftDrawerOpen = !leftDrawerOpen" />

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
      <q-list>
       <!--  -->
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>

export default {
  name: 'MainLayout',
  data () {
    return {
      leftDrawerOpen: false
    }
  }
}
</script>
