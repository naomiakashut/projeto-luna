<template>
<v-app>
  <AppTopBar/>
    <v-main>
      <v-container>
        <router-view/>
        </v-container>
    </v-main>
  <BottomBar/>
  </v-app>
</template>

<script>
import AppTopBar from './components/shared/AppTopBar.vue'
import BottomBar from './components/shared/BottomBar.vue'

export default {
  name: 'App',
  components: {
    AppTopBar,
    BottomBar
  }
};
</script>
