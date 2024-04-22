<template>
  <q-layout view="hHh lpR fFf">
    
    <q-header elevated class="bg-secondary text-white" height-hint="98">
      <q-toolbar>
        <q-btn dense flat round icon="menu" @click="toggleLeftDrawer" />

        <q-toolbar-title>
          <q-avatar>
            <img src="https://cdn.quasar.dev/logo-v2/svg/logo-mono-white.svg">
          </q-avatar>
          Title
        </q-toolbar-title>
      </q-toolbar>

      <q-tabs align="left">
        <q-route-tab to="/page1" label="About us" />
        <q-route-tab to="/page2" label="Projects" />
        <q-route-tab to="/page3" label="Partners" />
      </q-tabs>
    </q-header>

    <q-drawer v-model="leftDrawerOpen" side="left" bordered>
      <!-- drawer content -->
      <p class="text-center q-ma-md">Скоро доработаем...</p>
      <div class="flex flex-center">
        <main-button label="Пример UI компоннента"></main-button>
      </div>
    </q-drawer>

    
    <q-parallax
      src="https://cdn.quasar.dev/img/parallax1.jpg"
      style="height: 100vh;"
    >
      <q-page-container >
        <router-view class="flex items-center"/>
      </q-page-container>
    </q-parallax>

    <q-footer elevated class="bg-secondary text-white">
      <q-toolbar>
        <q-toolbar-title>
          <div class="text-body2 text-weight-thin text-center">We are its you</div>
        </q-toolbar-title>
      </q-toolbar>
    </q-footer>

  </q-layout>
</template>

<script>
import { ref } from 'vue'
import MainButton from 'src/components/UI/MainButton.vue'

export default {
  components: { MainButton },
  setup () {
    const leftDrawerOpen = ref(false)

    return {
      leftDrawerOpen,
      toggleLeftDrawer () {
        leftDrawerOpen.value = !leftDrawerOpen.value
      }
    }
  }
}
</script>