<template>
  <div class="app-top-bar">
    <v-app-bar>
      <v-spacer />
      <v-toolbar-title><h3><strong>Coleta Seletiva</strong> ♻️</h3></v-toolbar-title>
      <v-spacer />
    </v-app-bar>
  </div>
</template>


<script>
export default {
  name: "AppTopBar",
  data() {
    return {
      value: 0,
    };
  },
};
</script>

<style scoped>
    .app-top-bar a{
            text-decoration: none;
            display:flex;
            justify-content: center;
            flex-grow: 1;
            text-transform: uppercase;
             
    }
</style>